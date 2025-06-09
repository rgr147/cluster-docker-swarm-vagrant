# Projeto: Cluster Docker com Vagrant e Swarm

## ✅ Objetivo

Provisionar automaticamente um cluster Docker Swarm utilizando **Vagrant** e **VirtualBox**, com 4 máquinas virtuais configuradas para simular um ambiente distribuído.

---

## ⚙️ Estrutura das Máquinas Virtuais

- **master**: Nó principal (manager) do cluster
- **node01**, **node02**, **node03**: Nós secundários (workers)

---

## 📌 Especificações Atendidas

- [x] Criação de um `Vagrantfile` com 4 máquinas virtuais
- [x] Nomes definidos: `master`, `node01`, `node02`, `node03`
- [x] Cada máquina com **IP fixo**
- [x] **Docker** pré-instalado em todas as máquinas
- [x] A máquina `master` inicializa o **Docker Swarm** como **manager**
- [x] As máquinas `node01`, `node02` e `node03` são adicionadas ao cluster como **workers**

---

## 🚀 Como utilizar

1. **Clone este repositório:**
   ```bash
   git clone https://github.com/rgr147/cluster-docker-swarm-vagrant
   cd <nome-da-pasta>

2. **Inicie o ambiente com Vagrant:**
   ```bash
   vagrant up

3. **Verifique o status do cluster. Acesse o nó master:** 
   ```bash
   vagrant ssh master
   docker node ls

## 📌 Tecnologias utilizadas

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?style=for-the-badge&logo=virtualbox&logoColor=white)
![Vagrant](https://img.shields.io/badge/Vagrant-1563FF?style=for-the-badge&logo=vagrant&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Docker Swarm](https://img.shields.io/badge/Docker%20Swarm-0db7ed?style=for-the-badge&logo=docker&logoColor=white)
![Ubuntu Server 24.04](https://img.shields.io/badge/Ubuntu%20Server-0085C7?style=for-the-badge&logo=ubuntu&logoColor=white)

