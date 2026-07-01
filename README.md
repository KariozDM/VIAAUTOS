# 🐾 PatasApp — Manejo e Acompanhamento de Cães

Aplicativo web para gerenciar e acompanhar o cuidado com seus cães: cadastro,
vacinas, consultas veterinárias, medicações, controle de peso, passeios e
lembretes.

Feito com **HTML, CSS e JavaScript puro** — sem frameworks, sem build, sem
servidor. Os dados ficam salvos localmente no navegador (`localStorage`).

## ✨ Funcionalidades

- **Cadastro de cães** — nome, raça, sexo, nascimento (com cálculo automático de
  idade), peso, cor, microchip, castração, avatar (emoji) e observações.
- **Vacinas** — histórico com data de aplicação, próxima dose e veterinário.
- **Consultas** — motivo, diagnóstico, data e clínica/veterinário.
- **Medicações** — dose, frequência, início e fim (com destaque para as ativas).
- **Controle de peso** — histórico com **gráfico de evolução** (SVG).
- **Passeios** — duração e distância de cada atividade.
- **Lembretes** — criados manualmente ou gerados automaticamente a partir das
  próximas doses de vacina, com status **Atrasado / Em breve / Agendado**.
- **Dashboard** — visão geral com estatísticas e próximos lembretes.
- **Busca** de cães por nome ou raça.
- Persistência local automática — nenhum dado sai do seu navegador.

## 🚀 Como usar

Basta abrir o arquivo `index.html` no navegador. Ou, para servir localmente:

```bash
# Python
python3 -m http.server 8000
# depois acesse http://localhost:8000

# ou Node
npx serve .
```

Na primeira abertura, um cão de exemplo ("Rex") é criado para você explorar o
app. Você pode editá-lo ou excluí-lo à vontade.

## 📁 Estrutura

```
index.html   → marcação e layout base
styles.css   → estilos (tema claro, responsivo)
app.js       → toda a lógica: roteamento por hash, estado, formulários e views
```

## 💾 Dados e privacidade

Tudo é armazenado em `localStorage`, sob a chave `patasapp.v1`, apenas no seu
navegador. Limpar os dados do site apaga o histórico. Não há backend nem envio
de informações para servidores.

## 🛠️ Tecnologia

- JavaScript puro (ES6+), sem dependências
- Roteamento por hash (`#/dashboard`, `#/dogs`, `#/dog/<id>`, `#/reminders`)
- Gráfico de peso desenhado em SVG
