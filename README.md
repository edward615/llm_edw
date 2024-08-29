# llm_edw
este es un proyecto de prueba sobre el uso de llm
# 1. . instalacion
como primer paso descargamos[ollama]
https://ollama.com/download/linux de su pagina web y ejecutamos el siguiente comando :

````bash
$ curl -fsSL https://ollama.com/install.sh | sh 
````

# 2 . Ejecutar el servidor 
ejecutar el servidor de la API REST de ollama con el siguiente comando :
````bash
$ ollama server
````

# 3. descargar un modelo 

En la pagina de ollama descarga un [modelo](https://ollama.com/library)
utilizando el siguiente comando :

````bash
$ ollama pull tinyllama
````
# 4 . Realizar un request a la API REST

para realizar una consulra utilizamos el comando curl como se muestra en el siguiente ejemplo:
````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?"

````
# 5 . realizar un reques sin stream

para realizar uan consulta a la API REST sin stream de hace de la siguiente forma:

````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?",
  "stream":false
}'
````