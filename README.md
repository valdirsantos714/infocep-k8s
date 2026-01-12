# InfoCep - Manifestos Kubernetes

## 📋 Sobre

Repositório contendo manifestos do Kubernetes para o projeto **InfoCep**. Este projeto oferece uma infraestrutura containerizada e orquestrada para facilitar a implantação e gerenciamento da aplicação em ambientes Kubernetes.

## 🎯 Objetivos

- Facilitar o deploy da aplicação InfoCep em clusters Kubernetes
- Manter a configuração de infraestrutura como código (IaC)
- Automatizar processos de implantação e escalabilidade

## 📁 Estrutura do Projeto

```
infocep-k8s/
├── deployments/          # Manifestos de Deployment
├── services/            # ConfigMaps para configurações
├── secrets/              # Secrets para dados sensíveis
├── ingress/              # Configurações de Ingress
├── namespace.yaml
```

## 🚀 Início Rápido

### Pré-requisitos

- Kubernetes 1.24 ou superior
- `kubectl` instalado e configurado
- Acesso a um cluster Kubernetes

### Instalação

1. **Clone o repositório:**
```bash
git clone https://github.com/valdirsantos714/infocep-k8s.git
cd infocep-k8s
```

2. **Crie o namespace:**
```bash
kubectl create namespace infocep
```

3. **Aplique os manifestos:**
```bash
kubectl apply -f .  -n infocep
```

Ou, se estiver usando **Kustomize**:
```bash
kubectl apply -k . -n infocep
```

## 📦 Componentes

### Deployments
Manifestos para deploys da aplicação InfoCep, com configurações de replicas, recursos e health checks.

### Services
Configurações de serviços (ClusterIP, NodePort, LoadBalancer) para exposição da aplicação.

### Ingress
Configurações de roteamento HTTP/HTTPS para acesso externo.


## 📊 Monitoramento

Para verificar o status dos recursos:

```bash
# Ver todos os recursos no namespace
kubectl get all -n infocep

# Ver logs de um pod
kubectl logs <pod-name> -n infocep

# Descrever um pod
kubectl describe pod <pod-name> -n infocep
```


## 🔄 CI/CD

Este repositório pode ser integrado com pipelines de CI/CD usando: 
- GitHub Actions
- GitLab CI
- Jenkins
- ArgoCD

## 🤝 Contribuindo

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 👤 Autor

- **Valdir Santos** - [@valdirsantos714](https://github.com/valdirsantos714)

## 📞 Suporte

Para reportar problemas ou sugerir melhorias, abra uma issue no repositório.