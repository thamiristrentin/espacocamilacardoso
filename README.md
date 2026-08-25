# Espaço Camila Cardoso — Site

Landing page do estúdio de estética facial e corporal, em Cangaíba, São Paulo.

## Arquivos

| Arquivo | Função |
|---|---|
| `index.html` | Página principal |
| `styles.css` | Estilos base (cores, tipografia, layout) |
| `responsive.css` | Media queries — comportamento em tablet e mobile |
| `favicon.svg` | Ícone da aba do navegador (folha da marca) |
| `manifest.json` | Metadados do site como app (ícone, cor de tema) |
| `robots.txt` | Diz aos buscadores o que podem indexar |
| `sitemap.xml` | Lista de páginas do site pro Google |
| `.htaccess` | Configuração para hospedagem Apache (HTTPS, cache, compressão) |
| `foto-studio.webp` | Foto real do estúdio (parede com a logo) |

## Antes de publicar — o que trocar

1. **Domínio**: `https://espacocamilacardoso.com.br/` está como placeholder em `index.html` (canonical, Open Graph, dados estruturados), `robots.txt` e `sitemap.xml`. Depois de comprar o domínio de verdade, atualize essas 3 URLs.
2. **Imagem de compartilhamento**: por enquanto o Open Graph usa `foto-studio.webp` (a foto da parede) pro preview de link no WhatsApp/Instagram. Funciona, mas o ideal é uma imagem horizontal (1200x630px) — pode trocar depois se quiser um preview mais "wide".
3. **Foto da seção Sobre**: já está usando `foto-studio.webp`. Se tiver uma foto melhor (da Camila atendendo, ou do ambiente mais aberto), é só trocar o `src` no `index.html`, dentro da `.photo-frame`.
4. **Mapa**: já embutido via `iframe` do Google Maps na seção Localização, com o endereço real do estúdio.
5. **Horário de funcionamento**: só confirmei que fecha às 20h. Não incluí dias da semana no schema (`BeautySalon`) porque não tenho essa informação — se quiser, me diga os dias e eu completo o `openingHoursSpecification` no JSON-LD.

## Deploy

Suba os arquivos (mantendo todos na mesma pasta) em qualquer hospedagem estática:
- **Vercel** ou **Netlify**: arraste a pasta ou conecte um repositório Git — o `.htaccess` é ignorado (não é necessário, essas plataformas já servem via HTTPS e cache automaticamente).
- **Hospedagem compartilhada (cPanel etc.)**: suba tudo via FTP para a pasta `public_html`. O `.htaccess` funciona nesse caso.
- **GitHub Pages**: funciona, mas o `.htaccess` não tem efeito (GitHub Pages não usa Apache).
