# Workloads en Kubernetes

Este repositorio contiene los manifiestos YAML utilizados en el vídeo  
🎥 **“Workloads en Kubernetes: explicación, despliegue y pruebas”**

🔗 [Ver vídeo en YouTube](https://youtu.be/zq8bU8mnNeM)

Cada fichero representa un tipo de Workload diferente y está diseñado para demostrar su comportamiento básico en un clúster Kubernetes real.

---

## 📂 Contenido

| Fichero | Tipo de Workload | Descripción |
|----------|------------------|--------------|
| `nginx-deployment.yaml` | **Deployment** | Controlador que gestiona ReplicaSets para mantener el número de Pods deseado y permitir actualizaciones automáticas y rollbacks. |
| `nginx-statefulset.yaml` | **StatefulSet** | Controla Pods con identidad estable y persistencia, utilizados en aplicaciones con estado. |
| `fluentd-daemonset.yaml` | **DaemonSet** | Asegura que haya una copia del Pod ejecutándose en cada nodo del clúster. |
| `hello-job.yaml` | **Job** | Ejecuta una tarea puntual que finaliza cuando el proceso se completa correctamente. |
| `hello-cronjob.yaml` | **CronJob** | Programa la ejecución periódica de Jobs según una expresión cron. |

---

## ⚙️ Requisitos

- Kubernetes 1.28 o superior  
- `kubectl` configurado y con acceso al clúster  
- Entorno de pruebas o laboratorio (como el mostrado en el vídeo)

---

## 🚀 Uso

Aplica cualquiera de los manifiestos directamente con:

```bash
kubectl apply -f <fichero>.yaml
```

Y elimina los recursos cuando finalices la prueba:

```bash
kubectl delete -f <fichero>.yaml
```

---

## 🧠 Nota

Estos manifiestos están simplificados con fines educativos y de demostración.  
Puedes adaptarlos para tus propios laboratorios, modificando parámetros como el número de réplicas, la imagen o los volúmenes.
