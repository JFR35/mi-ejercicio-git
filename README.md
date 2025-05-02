# Practicando Gitflow

Este repositorio se creó con el único propósito de practicar el flujo de trabajo de Gitflow. Aquí encontrarás una serie de commits y ramas que simulan un ciclo de desarrollo típico utilizando este modelo.

## ¿Qué es Gitflow?

Gitflow es un modelo de flujo de trabajo de Git que define un proceso estricto para la gestión de ramas durante el desarrollo de software. Utiliza varias ramas de larga duración y ramas de soporte para organizar las funcionalidades, correcciones y lanzamientos.

## Ramas Principales

* **`main` (o `master`):** Esta rama representa el código de producción estable y listo para ser desplegado. Todas las versiones liberadas se etiquetan en esta rama.
* **`develop`:** Esta rama es donde se integra todo el trabajo de desarrollo para la próxima versión. Las ramas de funcionalidades (`feature`) se fusionan en `develop`.

## Ramas de Soporte

* **`feature/nombre-de-la-funcionalidad`:** Estas ramas se utilizan para desarrollar nuevas funcionalidades. Se ramifican desde `develop` y se fusionan de nuevo en `develop` al finalizar.
* **`release/version`:** Estas ramas se preparan para un nuevo lanzamiento. Se ramifican desde `develop`, permiten correcciones de errores y ajustes finales, y luego se fusionan tanto en `main` (con una etiqueta de versión) como en `develop`.
* **`hotfix/version`:** Estas ramas se utilizan para corregir errores críticos en la versión de producción. Se ramifican directamente desde `main` (desde una etiqueta de versión), se realizan las correcciones y luego se fusionan tanto en `main` (etiquetándose con una nueva versión) como en `develop`.

## Cómo se usó este repo para practicar:

En este repositorio, podrás observar (si revisas el historial de ramas y commits):

1.  **Creación de la rama `develop`** a partir de `main`.
2.  **Creación de varias ramas de funcionalidades** (por ejemplo, `feature/login`, `feature/user-profile`) a partir de `develop`.
3.  **Desarrollo y commits** dentro de las ramas de funcionalidades.
4.  **Fusión de las ramas de funcionalidades** de vuelta a `develop`.
5.  **Creación de una rama de `release`** (por ejemplo, `release/1.0`) desde `develop` para preparar un lanzamiento.
6.  **Posibles commits de corrección** dentro de la rama de `release`.
7.  **Fusión de la rama de `release`** tanto en `main` (con una etiqueta como `v1.0`) como en `develop`.
8.  **Simulación de un `hotfix`** creando una
