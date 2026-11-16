# Massinha 30

[![Massinha 30](guia/assets/banner.jpg)](https://inematds.github.io/massinha-30/guia/)

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

## O que é

Você tem uma ideia de história, mas fazer os personagens, a voz e as cenas combinarem dá trabalho. Massinha 30 é um kit para criar narrativas curtas com aparência de massinha artesanal. Ele organiza o roteiro aprovado, as referências dos personagens, os clipes gerados no Kling, a narração ElevenLabs e as legendas. Serve a criadores que querem repetir o processo em novas histórias. Para produzir, é preciso ter acesso aos serviços de geração; o guia pode ser lido gratuitamente.

## Guia de uso

https://inematds.github.io/massinha-30/guia/

Abra o projeto no Codex e peça: “Use skills/massinha-30/SKILL.md para criar uma nova história de massinha”. Leia [o fluxo completo](skills/massinha-30/references/producao.md).

Python 3.10+, FFmpeg/ffprobe com libass, CLI Kling oficial autenticada e ElevenLabs configurado. As imagens são geradas pelo agente com image_gen pela assinatura. A instalação não gera vídeo nem faz chamada paga.

```bash
git clone https://github.com/inematds/massinha-30.git
cd massinha-30
python3 -m unittest discover -s tests -v
python3 skills/massinha-30/scripts/pipeline.py iniciar exemplos/retalhos.json --out runs/retalhos
```

O exemplo espera aprovação explícita do roteiro. `voz` e `kling` só enviam a provedores com `--enviar`. Credenciais no ambiente ou `--env-file`, nunca no repositório. Nenhum modelo de vídeo roda localmente.

## Estado

v1.0.0: skill validada e testes locais passando; demonstração aguarda aprovação do roteiro. Adaptadores implementados: Kling oficial e ElevenLabs. Fish e Agnes são alternativas sem adaptador neste kit. Confira o estado atualizado no guia.

A montagem exporta limpo.mp4 e final.mp4 (30s, 720×1280, 30fps, H.264/AAC), além de legendas.srt. O áudio original do Kling é descartado; trilha e efeitos entram como arquivos separados. A verificação técnica não substitui assistir com som.

## Licença

MIT. Não inclui licenças de música, fontes, marcas ou condições dos provedores.
