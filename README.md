# k8s

Repositorio para administrar la configuracion de aplicaciones, controladores y componentes de plataforma desplegados en clusters de Kubernetes.

## Estructura del proyecto

```text
.
├── README.md
├── apps/
│   ├── app1/
│   │   ├── values.yml
│   │   ├── values-dev.yml
│   │   └── values-prod.yml
│   └── app2/
│       ├── values.yml
│       ├── values-dev.yml
│       └── values-prod.yml
├── controllers/
│   └── amazon-vpc-lattice-gateway-api/
│       ├── values.yml
│       ├── values-dev.yml
│       └── values-prod.yml
└── core/
    ├── alb-ingressclass.yml
    ├── kustomization.yml
    ├── nodeclass-apps.yml
    ├── nodeclass-system.yml
    ├── nodepool-apps.yml
    ├── nodepool-system.yml
    └── overlays/
        ├── dev/
        │   └── kustomization.yml
        └── prod/
            └── kustomization.yml
```

## Descripcion por carpeta

- `apps/`: valores de despliegue por aplicacion y por entorno (`dev` y `prod`).
- `controllers/`: configuracion de controladores instalados en el cluster.
- `core/`: manifiestos base de cluster y overlays por entorno (`dev` y `prod`).
