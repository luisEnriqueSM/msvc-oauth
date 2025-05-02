# msvc-oauth

# Comandos Docker para levantar el contenedor de msvc-oauth


```bash
# Limpiar, generar Jar file y omitir tests
.\mvnw clean package -DskipTests

# Construir imagen
docker build -t msvc-oauth:v1 .

# Correr contenedor
docker run -d -p 9100:9100 --name msvc-oauth --network springcloud msvc-oauth:v1