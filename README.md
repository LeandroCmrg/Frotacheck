# 🚛 FrotaCheck

**Leitor de CRLV-e para identificação do tipo de veículo e conferência do prazo de licenciamento.**

O FrotaCheck é um protótipo de ferramenta web desenvolvido para simplificar a análise documental de veículos em operações de transporte. Sua interface é adaptada para computador e celular, com cores inspiradas no universo logístico da DHL.

## Principais funções

- **Tipo do veículo:** sugere uma classificação operacional, como passeio, van, VUC, médio, toco, truck ou carreta, conforme as informações encontradas no documento.
- **Prazo de licenciamento:** utiliza a UF, o final da placa e o exercício do CRLV para consultar as regras estaduais cadastradas.
- **Sinalização visual:** prazo **verde** quando a data calculada ainda não passou, **vermelho** quando já passou e **neutro** quando não foi possível determinar a data.
- **Leitura de CRLV-e:** aceita arquivos PDF e imagens, além de fotografia pelo celular, com extração de dados por texto e OCR.
- **Leitor de QR Code:** permite reconhecer o QR pela câmera, mas **não decodifica nem autentica o QR Seguro VIO** sem integração autorizada.
- **Correção manual:** permite conferir e ajustar informações extraídas incorretamente.

## Como usar

1. Abra o FrotaCheck no navegador.
2. Envie o CRLV-e em PDF ou imagem, ou fotografe o documento completo no celular.
3. Confira os dois resultados em destaque: **tipo do veículo** e **prazo de licenciamento**.
4. Caso algum campo não seja identificado corretamente, utilize a opção de conferência e correção.

> A leitura por câmera exige permissão do navegador e, em geral, publicação via **HTTPS**. Os recursos de PDF e OCR podem depender de bibliotecas carregadas pela internet.

## Publicação no GitHub Pages

Para que o site abra corretamente, o repositório deve conter o arquivo **`index.html`**, exatamente com esse nome, na pasta utilizada para publicar o site.

```text
Frotacheck/
├── index.html   ← página principal do site
└── README.md    ← apresentação do projeto no GitHub
```

**Atenção:** `README.md` não substitui `index.html`. Se o arquivo da página estiver como `index 2.html`, renomeie-o para **`index.html`**. Depois, no repositório, confira **Settings → Pages** e selecione a branch e a pasta que contêm esse arquivo (por exemplo, `main` e `/root`).

## Limitações importantes

- O prazo exibido é calculado a partir dos calendários estaduais cadastrados, que podem ser atualizados. **Não representa confirmação oficial de regularidade do veículo.**
- A versão atual contém regras de **2026 para 15 UFs**; outras UFs e exercícios podem exigir consulta ao Detran correspondente.
- O sistema **não consulta automaticamente débitos, restrições ou autenticidade** do CRLV-e.
- A classificação entre VUC, médio, toco, truck e carreta é uma **sugestão operacional** e pode exigir verificação de eixos, capacidade e dimensões.
- **Não envie documentos pessoais ou corporativos sensíveis a ambientes de teste públicos sem autorização.**

## Situação do projeto

**Em desenvolvimento — protótipo não homologado para decisões operacionais sem conferência humana.**

Projeto independente, com identidade visual inspirada nas cores da DHL. **Não é um produto oficial ou endossado pela DHL.**
