# Como Treinar e Implantar Modelos YOLO com Ultralytics (YOLO11, YOLOv8 e YOLOv5)
Tutoriais e exemplos mostrando como treinar e implantar modelos YOLO com Ultralytics.

## Treinar Modelos YOLO

**Opção 1. Com o Google Colab**

Clique abaixo para acessar um notebook do Colab para treinar modelos YOLO. Ele torna o treinamento de um modelo YOLO personalizado tão fácil quanto fazer o upload de um conjunto de dados de imagens e executar alguns blocos de código.

<a href="https://colab.research.google.com/drive/12_tjJdJqi6TaCEkqm9i-DMWZodI6kGVY?usp=sharing" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Abrir no Colab"/></a>

**Opção 2. Em um PC local**

Escrevi um artigo que descreve o processo de treinamento de modelos YOLO em um PC local equipado com uma GPU NVIDIA. Confira no link abaixo.

**Opção 2. Em um PC local**

Escrevi um artigo que descreve o processo de treinamento de modelos YOLO em um PC local equipado com uma GPU NVIDIA. Confira no link abaixo.

**Opção 2. Em um PC local** [Como Treinar Modelos de Detecção de Objetos YOLO 11 Localmente com NVIDIA](https://www.ejtech.io/learn/train-yolo-models)

## Implantar Modelos YOLO
O script `yolo_detect.py` fornece um exemplo básico que mostra como carregar um modelo, executar inferência em uma imagem de origem, analisar os resultados da inferência e exibir caixas ao redor de cada classe detectada na imagem. Este script mostra como trabalhar com modelos YOLO em Python e pode ser usado como ponto de partida para aplicações mais avançadas.

Para baixar o arquivo `yolo_detect.py` deste repositório, execute o seguinte comando:

```
curl --output yolo_detect.py https://raw.githubusercontent.com/EdjeElectronics/Train-and-Deploy-YOLO-Models/refs/heads/main/yolo_detect.py
```

Para executar a inferência com um modelo YOLOv8s em uma câmera USB com resolução de 1280x720, execute o seguinte comando:

```
python yolo_detect.py --model yolov8s.pt --source usb0 --resolution 1280x720
```

Aqui estão todos os argumentos para o yolo_detect.py:

- `--model`: Caminho para um arquivo de modelo (por exemplo, `my_model.pt`). Se o modelo não for encontrado, o padrão será usar `yolov8s.pt`.

- `--source`: Fonte na qual executar a inferência. As opções são:

- Arquivo de imagem (exemplo: `test.jpg`)

- Pasta de imagens (exemplo: `my_images/test`)

- Arquivo de vídeo (exemplo: `testvid.mp4`)

- Índice de uma câmera USB conectada (exemplo: `usb0`)

- Índice de um módulo PiCamera conectado para Raspberry Pi (exemplo: `picamera0`)
- `--thresh` (opcional): Limiar mínimo de confiança para exibir os objetos detectados. O valor padrão é 0,5 (exemplo: `0,4`)
- `--resolution` (opcional): Resolução em largura x altura para exibir os resultados da inferência. Se não for especificada, o programa usará a resolução da fonte. (exemplo: `1280x720`)
- `--record` (opcional): Grava um vídeo dos resultados e o salva como `demo1.avi`. (Se usar esta opção, o argumento `--resolution` também deve ser especificado.)

### Implantação no Raspberry Pi
O Raspberry Pi 4 e 5 são suficientemente potentes para executar modelos YOLO nano e de pequeno porte em tempo real. O artigo abaixo explica como executar modelos YOLO no Raspberry Pi.

[Como executar modelos de detecção YOLO no Raspberry Pi](https://www.ejtech.io/learn/yolo-on-raspberry-pi)
