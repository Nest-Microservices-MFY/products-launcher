<h1 align="center"> Microservices con NestJS </h1>

Ejemplo de microservice con NestJS

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=nest,typescript,docker,postgres,sqlite,mongo" />
  </a>
</p>

## DEV

1. Clonar el repositorio
2. Crear archivo **.env** basado en el [**.env.template**](./.env.template)
3. Reconstruir los sub-módulos con el comando: `git submodule update --init --recursive`
4. Ejecutar comando: `docker compose up --build`

### Pasos para crear los Git Submodules

1. Crear un nuevo repositorio en GitHub
2. Clonar el repositorio en la máquina local
3. Añadir el submodule, donde `repository_url` es la url del repositorio y `directory_name` es el nombre de la carpeta donde quieres que se guarde el sub-módulo (no debe de existir en el proyecto)

```
git submodule add <repository_url> <directory_name>
```

4. Añadir los cambios al repositorio (git add, git commit, git push)
   Ej:

```
git add .
git commit -m "Add submodule"
git push
```

5. Inicializar y actualizar Sub-módulos, cuando alguien clona el repositorio por primera vez, debe de ejecutar el siguiente comando para inicializar y actualizar los sub-módulos

```
git submodule update --init --recursive
```

6. Para actualizar las referencias de los sub-módulos

```
git submodule update --remote
```

## Importante

Si se trabaja en el repositorio que tiene los sub-módulos, **primero actualizar y hacer push** en el sub-módulo y **después** en el repositorio principal.

Si se hace al revés, se perderán las referencias de los sub-módulos en el repositorio principal y tendremos que resolver conflictos.

## Sub módulos

- [client-gateway](https://github.com/Nest-Microservices-MFY/client-gateway.git)
- [orders-ms](https://github.com/Nest-Microservices-MFY/orders-microservice.git)
- [products-ms](https://github.com/Nest-Microservices-MFY/products-microservice.git)
- [payments-ms](https://github.com/Nest-Microservices-MFY/payments-microservice.git)
- [auth-ms](https://github.com/Nest-Microservices-MFY/auth-microservice.git)

## PROD

1. Clonar repositorio
2. Crear archivo **.env** basado en el [**.env.template**](./.env.template)
3. Ejecutar comando:

```bash
docker compose -f docker-compose.prod.yml build
```
