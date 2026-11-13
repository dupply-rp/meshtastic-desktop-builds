# Meshtastic Desktop: compilações não oficiais

Este repositório contém **apenas** o processo de compilação (GitHub Actions) do
[Meshtastic Desktop](https://github.com/meshtastic/Meshtastic-Android/tree/main/desktopApp).
Nenhuma linha do código do aplicativo é alterada: o workflow baixa o código oficial
na tag de produção escolhida e compila os instaladores nos runners do GitHub.

- Código-fonte original: <https://github.com/meshtastic/Meshtastic-Android>
- Licença do aplicativo: [GPL-3.0](https://github.com/meshtastic/Meshtastic-Android/blob/main/LICENSE).
  O código-fonte correspondente a cada instalador é a tag indicada nas notas da release.
- Estas compilações **não são oficiais**, não têm assinatura digital e não têm
  vínculo com o projeto Meshtastic. "Meshtastic" é marca do Meshtastic LLC.

## Instaladores gerados

| Sistema | Arquivos |
| --- | --- |
| Windows x64 | `.msi`, `.exe` |
| macOS Apple Silicon (arm64), macOS 12+ | `.dmg` |
| Linux x86_64 | `.deb`, `.rpm`, `.AppImage` |

Cada release traz também `SHA256SUMS.txt` para conferência dos arquivos.

## Como gerar uma versão

1. Ver a última release de produção em <https://github.com/meshtastic/Meshtastic-Android/releases>
   (ignorar `snapshot` e tags `-internal.N`).
2. Em **Actions → Compilar Meshtastic Desktop → Run workflow (botão do GitHub)**, informar:
   - `tag_name`: por exemplo `v2.8.4`
   - `version_name`: por exemplo `2.8.4`
3. Aguardar as 3 compilações (macOS, Windows, Linux). A release `desktop-<tag>` é criada com os instaladores.

Pela linha de comando:

```bash
gh workflow run build-desktop.yml -f tag_name=v2.8.4 -f version_name=2.8.4
```

## Se o build falhar

Comparar `.github/workflows/build-desktop.yml` com o job `release-desktop` do
[release.yml oficial](https://github.com/meshtastic/Meshtastic-Android/blob/main/.github/workflows/release.yml)
**na mesma tag**. Corrigir apenas o workflow, nunca o código do app.

## Controle de atualizações

Ver [docs/ATUALIZACOES.md](docs/ATUALIZACOES.md).
