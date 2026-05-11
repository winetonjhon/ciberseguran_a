# 🛡️ Laboratório de Cibersegurança — Simulação de Malware com Python

## 📌 Visão Geral

Este repositório foi desenvolvido com finalidade exclusivamente educacional, como parte de estudos práticos em Segurança da Informação e Defesa Cibernética.

O projeto demonstra, em ambiente controlado, o funcionamento básico de técnicas utilizadas por **Ransomwares** e **Keyloggers**, permitindo compreender vetores de ataque, identificar vulnerabilidades e aplicar estratégias de mitigação e resposta a incidentes.

> ⚠️ **Importante:**
> Todos os testes devem ser realizados apenas em ambientes isolados, como máquinas virtuais (VMs) ou sandboxes.
> O uso indevido deste material contra sistemas reais, sem autorização, é ilegal e viola princípios éticos da cibersegurança.

---

# 🎯 Objetivos do Projeto

* Demonstrar conceitos fundamentais de malware em ambientes controlados;
* Compreender técnicas de criptografia utilizadas por ransomwares;
* Simular captura de entradas de teclado para análise defensiva;
* Estudar mecanismos de detecção, mitigação e resposta a ameaças;
* Desenvolver habilidades práticas em Python aplicado à segurança ofensiva e defensiva.

---

# 📂 Estrutura do Projeto

```bash
.
├── ransomware.py
├── decrypter.py
├── keylogger.py
├── secreta.key
├── LEIA_ME_RESGATE.txt
└── meus_documentos/
```

| Arquivo               | Descrição                                                                               |
| --------------------- | --------------------------------------------------------------------------------------- |
| `ransomware.py`       | Script responsável por criptografar arquivos de teste utilizando criptografia simétrica |
| `decrypter.py`        | Script de recuperação dos arquivos utilizando a chave gerada                            |
| `keylogger.py`        | Simulação de monitoramento e captura de eventos do teclado                              |
| `secreta.key`         | Chave criptográfica gerada automaticamente                                              |
| `LEIA_ME_RESGATE.txt` | Nota de resgate criada após a simulação                                                 |
| `meus_documentos/`    | Diretório utilizado para testes de criptografia                                         |

---

# 🔐 Simulação de Ransomware

## Funcionalidades Implementadas

* Criptografia de arquivos utilizando **AES/Fernet**
* Geração automática de chave criptográfica
* Criação de nota de resgate simulada
* Processo de descriptografia para recuperação dos dados

## Fluxo da Simulação

1. O script identifica os arquivos da pasta de teste;
2. Os arquivos são criptografados;
3. Uma chave é gerada localmente;
4. A nota de resgate é criada;
5. O script `decrypter.py` realiza a recuperação dos arquivos.

---

# ⌨️ Simulação de Keylogger

## Funcionalidades Implementadas

* Monitoramento de entradas do teclado
* Registro local das teclas capturadas
* Armazenamento em arquivo de log (`log_teclado.txt`)
* Estudo teórico sobre técnicas de persistência e furtividade

## Objetivo Educacional

A implementação busca demonstrar como ferramentas maliciosas podem capturar credenciais e dados sensíveis, reforçando a importância de mecanismos modernos de proteção de endpoints.

---

# 🛡️ Estratégias de Defesa e Mitigação

## 1. Proteção Contra Ransomware

### ✅ Backups Offline

Aplicação da estratégia **3-2-1**:

* 3 cópias dos dados;
* 2 mídias diferentes;
* 1 cópia offline.

### ✅ EDR (Endpoint Detection and Response)

Ferramentas capazes de detectar:

* Criptografia em massa;
* Alterações suspeitas em arquivos;
* Comportamentos anômalos em endpoints.

### ✅ Segmentação de Rede

Redução da propagação lateral do malware entre dispositivos e setores da infraestrutura.

---

## 2. Proteção Contra Keyloggers

### ✅ Autenticação Multifator (MFA)

Reduz significativamente o impacto do roubo de credenciais.

### ✅ Gerenciadores de Senhas

Minimizam a necessidade de digitação manual de senhas.

### ✅ Ferramentas Anti-Keylogging

Soluções capazes de:

* Bloquear captura de eventos do teclado;
* Detectar processos suspeitos;
* Impedir monitoramento não autorizado.

---

# 🚀 Execução em Ambiente de Teste

## Instalação das Dependências

```bash
pip install cryptography pynput
```

---

## Executando a Simulação de Ransomware

### 1. Criar diretório de teste

```bash
mkdir meus_documentos
```

### 2. Executar o script

```bash
python ransomware.py
```

### 3. Recuperar os arquivos

```bash
python decrypter.py
```

---

## Executando a Simulação de Keylogger

```bash
python keylogger.py
```

Após a execução:

* Digite em outras janelas;
* Verifique o arquivo `log_teclado.txt`.

---

# 📚 Tecnologias Utilizadas

* Python 3
* Biblioteca `cryptography`
* Biblioteca `pynput`

---

# ✅ Resultados de Aprendizagem

* Compreensão prática de técnicas utilizadas por malwares;
* Aplicação de criptografia simétrica em Python;
* Entendimento de vetores de ataque e engenharia social;
* Desenvolvimento de documentação técnica;
* Fortalecimento de conhecimentos em Cybersecurity e análise defensiva.

---

# ⚖️ Considerações Éticas

Este projeto foi desenvolvido exclusivamente para fins acadêmicos e educacionais, com foco em pesquisa, conscientização e fortalecimento de estratégias defensivas em segurança da informação.

O autor não incentiva nem se responsabiliza pelo uso indevido deste conteúdo.

---

# 👨‍💻 Autor

Projeto desenvolvido como parte da jornada de aprendizado em **Cybersecurity**, com foco em:

* Segurança Ofensiva
* Defesa Cibernética
* Análise de Malware
* Automação com Python
