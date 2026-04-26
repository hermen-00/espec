# espec
Especionador inteligente de desempenho escolar. Single-file HTML sem backend. Calcula médias pelo método real do professor, sugere notas para atingir metas e gera relatórios trimestrais. Freemium — versão Pro activa por chave M-Pesa. Sistema moçambicano 0–20.
```markdown
# Espec Pro

Especionador inteligente de desempenho escolar. Single-file HTML — sem backend, sem base de dados, sem API. Funciona 100% no navegador do utilizador.

## Como funciona

O aluno abre o ficheiro no Chrome, adiciona disciplinas, regista notas e o sistema calcula automaticamente:
- Média por disciplina e global
- Média real do professor (conta testes não feitos como zero)
- Sugestão de quanto precisa tirar no próximo teste para atingir uma meta
- Evolução temporal por gráficos
- Planilha e relatório trimestral
- Detecção de disciplinas em risco e tendências

Escala de notas: 0/20 (sistema moçambicano). Três trimestres por ano lectivo.

## Modelo de negócio

- **Grátis:** até 4 disciplinas, funcionalidades básicas
- **Pro (50 MZN):** ilimitado + partilha WhatsApp + exportar CSV + nome nos relatórios
- Activação via chave + validação local (sem servidor)
- Pagamento manual por M-Pesa
- Distribuição via Bluetooth e WhatsApp

## Estrutura do ficheiro

```
espec.html (~1800 linhas)
├── Tailwind CSS + Chart.js + Font Awesome (CDN)
├── Dados → localStorage
├── 5 views: Dashboard, Disciplinas, Sugestões, Trimestres, Configurações
├── 5 modais: Disciplina, Nota, Upgrade, Partilha, Confirmar
└── Onboarding + Review mode
```

## Chaves técnicas

- Dados sanitizados na inicialização (protecção contra corrupção)
- Versão interna para migração automática entre versões
- Gráficos Chart.js com destruição segura (anti memory leak)
- Sistema de chaves PRO embutido no código (20 chaves fixas, validação local)
- Modelo freemium com limite de 4 disciplinas na versão grátis

## Configuração

As definições do utilizador (nome, escola, testes por trimestre) são guardadas em `localStorage`. Não há contas, sem autenticação.

Para desenvolver: abrir `espec.html` directamente no browser — nenhuma build step necessária.

## Status

- [x] Fase 0 — Modelo Free/Pro + sistema de chaves
- [x] Fase 1 — Hospedagem GitHub Pages
- [ ] Fase 2 — Beta fechado (5 pessoas)
- [ ] Fase 3 — Lançamento em grupos WhatsApp
- [ ] Fase 4 — Avaliação e decisão
```

Abre `espec.html` no Chrome para testar localmente.
```
