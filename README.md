# Gerador de vídeo a partir de imagens

Junta todas as imagens de uma pasta e gera um vídeo com elas, em sequência.

## Como funciona

1. O programa percorre a pasta `Imagens/` e separa os arquivos `.jpg`, `.jpeg`,
   `.png` e `.gif`
2. Lê a primeira imagem para descobrir a largura e a altura do vídeo
3. Cria um `VideoWriter` do OpenCV com o codec DIVX, a 0,8 quadro por segundo
4. Escreve cada imagem como um quadro e salva o resultado em `Project.avi`

Como a taxa é de menos de um quadro por segundo, cada imagem fica um pouco mais de um
segundo na tela — o resultado é uma apresentação de slides em vídeo.

## Tecnologias

- Python
- OpenCV
- os (leitura da pasta)

## Como executar

```bash
pip install opencv-python
cd PRO-C117
python CreateVideo.py
```

Coloque suas imagens numa pasta `Imagens/` ao lado do script. As imagens precisam ter
todas o mesmo tamanho, senão o vídeo sai com quadros cortados.
