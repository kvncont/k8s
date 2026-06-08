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
└── platform/
	├── ingressclass/
	│   ├── base/
	│   │   ├── ingressclass.yml
	│   │   └── kustomization.yml
	│   └── overlays/
	│       └── dev/
	│           └── kustomization.yml
	├── nodeclass/
	│   ├── base/
	│   │   ├── kustomization.yml
	│   │   ├── nodeclass-apps.yml
	│   │   └── nodeclass-system.yml
	│   └── overlays/
	└── nodepools/
		├── base/
		│   ├── kustomization.yml
		│   ├── nodepool-apps.yml
		│   └── nodepool-system.yml
		└── overlays/
			├── dev/
			│   └── kustomization.yml
			└── prod/
				└── kustomization.yml
```

## Descripcion por carpeta

- `apps/`: valores de despliegue por aplicacion y por entorno (`dev` y `prod`).
- `controllers/`: configuracion de controladores instalados en el cluster.
- `platform/`: componentes base de plataforma gestionados con Kustomize (`base` y `overlays`).
