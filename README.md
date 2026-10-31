# Cotas Vendidas 2R · Consórcio Honda (Grupo Cometa)

Painel online das cotas vendidas do Consórcio Honda 2R. Lê as 14 planilhas do IHS no navegador, aplica as regras da conferência e atualiza metas, gráficos e evolução mensal.

## Arquivos
- `index.html`: o painel inteiro (página única, sem build).
- `dados-iniciais.json` (opcional, **não incluído neste repositório público**): dados internos de metas e vendas. Sem ele o painel abre vazio.
- `.nojekyll`: faz o GitHub Pages servir os arquivos como estão.

## Como publicar (GitHub Pages)
1. No GitHub, crie um repositório novo (ex.: `painel-cotas-honda-2r`).
2. Envie os três arquivos para a raiz (Add file → Upload files).
3. Settings → Pages → Source: *Deploy from a branch* → Branch: `main` / `(root)` → Save.
4. Em alguns minutos o painel fica em `https://SEU-USUARIO.github.io/painel-cotas-honda-2r/`.

### Público ou privado?
- Páginas do GitHub Pages ficam **públicas na internet**. Repositório privado só publica Pages em planos pagos (Pro, Team ou Enterprise), e mesmo assim o site pode ficar aberto a qualquer pessoa com o link.
- Se o painel for público, **não envie `dados-iniciais.json`**. Sem ele o painel abre vazio e cada pessoa importa as planilhas do IHS e digita as metas na aba Metas, no próprio navegador.

## Como usar
- **Importar IHS:** solte as 14 planilhas (AF, AN, BL, CA, CG, CO, JP, MA, OP, PB, PL, SG, TB, TF). A leitura é automática.
- **Regras:** cada linha é uma cota; ficam de fora Origem do Contrato = E-COMMERCE e Plano = Motores e Máquinas; data de referência = "Dt Venda" do IHS; corte padrão em D-1 (botão "Todas as vendas" inclui o dia da extração).
- **Metas:** edite meta e meta ideal por concessionária e por mês.

## Onde os dados ficam
Os dados importados ficam salvos **no navegador de quem importou** (localStorage). Para todos verem a mesma posição:
1. Importe as planilhas do dia.
2. Clique em **Exportar dados** (topo da página).
3. Substitua `dados-iniciais.json` no repositório pelo arquivo baixado.

Ao abrir, o painel usa, para cada mês, o registro mais recente entre o do navegador e o do arquivo.

## Privacidade
As planilhas são lidas apenas no navegador. Só totais por concessionária e por dia são guardados; nomes de clientes e vendedores nunca são gravados.
