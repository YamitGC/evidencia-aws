# AWS Ejercicios — Portafolio de Evidencias

Repositorio en crecimiento con las prácticas, laboratorios y evidencias de aprendizaje sobre **Amazon Web Services (AWS)** realizadas mediante AWS CLI e IAM.

> **Nota de seguridad:** Ninguna evidencia de este repositorio incluye claves secretas (`SecretAccessKey`), tokens temporales ni credenciales privadas. Todos los recursos temporales creados en cada actividad (usuarios de prueba, llaves de acceso, buckets, etc.) son eliminados al finalizar la práctica.

---

## Índice de prácticas y evidencias

| # | Carpeta | Actividad | Servicios AWS | Evidencia | Estado |
|---|---|---|---|---|---|
| 1 | [`semana02/`](./semana02/) | Ciclo de vida de un usuario IAM y principio de menor privilegio | IAM, EC2 | [Ver evidencia](./semana02/evidencia.md) | Completada |
| 2 | [`practica-s3/`](./practica-s3/) | Gestión de buckets S3, enlaces temporales (*presigned URLs*) y política de solo lectura | S3, IAM | [Ver evidencia](./practica-s3/evidencia.md) | Completada |

<!-- Agrega nuevas prácticas como filas adicionales en esta tabla conforme avancen las semanas -->

---

## Resumen de prácticas realizadas

### 1. Ciclo de vida de un usuario IAM ([`semana02/`](./semana02/))
- Creación, renombrado y etiquetado de un usuario IAM (`dev-yamit` -> `lector-yamit`).
- Asignación y revocación de la política administrada `AmazonEC2ReadOnlyAccess`.
- Verificación de acción permitida (`ec2 describe-instances`) y acción denegada (`iam list-users`).
- Eliminación ordenada de llaves de acceso, políticas y usuario final.
- **Documento:** [`semana02/evidencia.md`](./semana02/evidencia.md)

### 2. Práctica de Amazon S3 e IAM ([`practica-s3/`](./practica-s3/))
- Creación de bucket en `us-east-2`, carga de archivos e inspección de metadatos (`head-object`).
- Uso y expiración de enlaces temporales prefirmados (*presigned URLs*).
- Creación de usuario IAM con política personalizada de menor privilegio ([`solo-lectura.json`](./practica-s3/solo-lectura.json)) limitada únicamente a `s3:GetObject`.
- Validación de una acción permitida y dos denegadas (`s3:ListAllMyBuckets` y `s3:DeleteObject`), error `BucketNotEmpty` y limpieza total de recursos.
- **Documento:** [`practica-s3/evidencia.md`](./practica-s3/evidencia.md)

---

## Estructura del repositorio

Cada nueva semana o laboratorio se organiza en su propia carpeta independiente para mantener el historial ordenado y fácil de navegar:

```text
aws-ejercicios/
├── README.md
├── semana02/
│   ├── capturas/
│   └── evidencia.md
├── practica-s3/
│   ├── capturas/
│   ├── solo-lectura.json
│   └── evidencia.md
└── <proxima-practica>/
    ├── capturas/
    └── evidencia.md
```

---


