# Agenda Camila 💜

Site de agendamento online para maquiagem, ministração gospel e social media.

## Como funciona
- **Site (`index.html`):** o cliente escolhe o serviço, o dia e o horário e informa só nome e telefone.
- **Calendário inteligente:** bloqueia domingos, datas passadas e horários já reservados. Atendimento de segunda a sábado, das 8h às 19h, um cliente por vez.
- **Painel (`admin.html`):** acesso com e-mail e senha para ver e cancelar agendamentos.

## Arquivos
| Arquivo | Para que serve |
|---|---|
| `index.html` | Site para os clientes |
| `admin.html` | Painel da dona (acesso restrito) |
| `logo.png` | Logo |
| `foto.jpg` | Foto do painel principal |

## Tecnologias
- Hospedagem: GitHub Pages
- Banco de dados e login: Firebase (Firestore + Authentication)

## Como alterar os dados
No começo do script do `index.html`, edite o bloco `CFG`:
- `nome`: nome da profissional
- `whats`: WhatsApp com 55 + DDD (ex.: `5589999999999`)
- `pix` e `pixNome`: chave PIX e nome do titular
- `sinal`: texto da regra de pagamento
- `inicio` e `fim`: horário de funcionamento

Os serviços ficam no bloco `SERV`, logo abaixo.

## Painel de administração
Endereço: `/admin.html`. O acesso é só para o e-mail cadastrado no Firebase Authentication e liberado nas regras do Firestore.

## Segurança
- Nomes e telefones dos clientes só podem ser lidos pelo e-mail autorizado.
- O site público só enxerga quais horários estão ocupados, sem nenhum dado pessoal.
- Nunca publique senhas neste repositório.
