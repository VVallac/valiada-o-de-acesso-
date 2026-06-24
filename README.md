# Validador de Acesso
Uma solução de validação de acesso com bloqueio automático de IPs suspeitos.

## Descrição
Este projeto implementa uma lógica de validação de acesso em Python com proteção contra tentativa de acesso não autorizado (Força Bruta). O sistema monitora tentativas de login com falhas e bloqueia automaticamente IPs após um determinado número de erros, simulando o comportamento de ferramentas de mitigação como o Fail2Ban.

## Características
* Contador de erros por IP.
* Bloqueio automático após 5 tentativas falhas.
* Alerta visual de monitoramento.
* Execução direta de bloqueio no firewall do servidor.
* Prevenção ativa contra ataques de força bruta.

## Requisitos
* Python 3.x (Biblioteca padrão `os` incluída).
* Sistema Operacional Linux (para o uso do firewall nativo).
* Permissões de administrador (root/sudo) para execução do comando iptables.

## Instalação
bash
git clone [https://github.com/VVallac/valiada-o-de-acesso-.git](https://github.com/VVallac/valiada-o-de-acesso-.git)
cd valiada-o-de-acesso-

Uso
O script funciona com base no recebimento de IPs suspeitos. Exemplo prático de chamada da função dentro do código:
Python

# Simulação de uso chamando a função com um IP invasor
ip_atacante = "192.168.1.100"
analisar_log(ip_atacante)

# Configuração
Limite de erros (limite_erros): 5 tentativas (pode ser ajustado diretamente nas variáveis globais do código fonte).

# Licença
Distribuído sob a licença MIT.
