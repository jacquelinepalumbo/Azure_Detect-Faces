# Detect faces in Vision Studio
Testing face detection capabilities of the Azure AI Face

As soluções de visão geralmente exigem IA para serem capazes de detectar rostos humanos. Suponha que a empresa de varejo fictícia queira localizar onde os clientes estão em uma loja para melhor ajudá-los. Uma maneira de fazer isso é determinar se há faces nas imagens e, em caso afirmativo, retornar as coordenadas da caixa delimitadora que mostram sua localização.

Para testar os recursos de detecção de rosto do serviço [Azure AI Face](https://portal.vision.cognitive.azure.com/), você usará o Azure Vision Studio. Esta é uma plataforma baseada em interface do usuário que permite explorar os recursos do Azure AI Vision sem precisar escrever nenhum código.

## Criar um recurso de serviços de IA do Azure
Você pode usar o serviço Azure AI Face com um recurso multisserviço dos serviços de IA do Azure. Se você ainda não tiver feito isso, crie um recurso de serviços de IA do Azure em sua assinatura do Azure.

1. Em outra guia do navegador, abra o portal do Azure em [https://portal.azure.com]([https://portal.azure.com]), entrando com a conta da Microsoft associada à sua assinatura do Azure.

2. Clique no botão **+Criar um recurso** e procure serviços de IA do Azure.
Selecione criar um plano de serviços de _IA do Azure_. Você será levado a uma página para **criar** um recurso de serviços de IA do Azure.

Configure-o com as seguintes configurações:

* **Assinatura**: sua assinatura do Azure.
* **Grupo de recursos**: selecione ou crie um grupo de recursos com um nome exclusivo.
* **Região**: Leste dos EUA.
* **Nome**: insira um nome exclusivo.
* **Nível de preços**: Standard S0.
Ao marcar esta caixa, reconheço que li e entendi todos os termos abaixo: _Selecionado_.

3.Selecione Revisar + criar e, em seguida, Criar e aguarde a conclusão da implantação.

## Conectar seu recurso de serviço de IA do Azure ao Vision Studio

Em seguida, conecte o recurso de serviços de IA do Azure provisionado acima ao Vision Studio.

1. Em outra guia do navegador, navegue até **o Vision Studio** em [https://portal.vision.cognitive.azure.com](https://portal.vision.cognitive.azure.com).

2. Entre com sua conta e verifique se você está usando o mesmo diretório em que criou seu recurso de serviços de IA do Azure.

3. Na home page do Vision Studio, selecione **Exibir todos os recursos** no cabeçalho **Introdução ao Vision**.

<img width="626" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/5bb0961c-9003-4e29-872e-b7aae15e4fb5">

4. Na página **Selecione um recurso para trabalhar**, passe o cursor do mouse sobre o recurso criado acima na lista e marque a caixa à esquerda do nome do recurso e selecione **Selecionar como recurso padrão**.

<img width="933" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/e6e8a1e0-ff03-4986-b6e1-a79d09d57481">

5. Feche a página de configurações selecionando o "x" no canto superior direito da tela.

# Detectar rostos no Vision Studio
1. Em um navegador da Web, navegue até **o Vision Studio** em [https://portal.vision.cognitive.azure.com](https://portal.vision.cognitive.azure.com).

2. Na página inicial **Introdução ao Vision**, selecione a guia **Rosto** e selecione o bloco **Detectar faces** em uma imagem.

3. No subtítulo **Experimentar**, reconheça a política de uso de recursos lendo e marcando a caixa.

4. Selecione cada uma das imagens de amostra e observe os dados de detecção de rosto retornados.

5. Agora vamos tentar com algumas de nossas próprias imagens. Selecione https://aka.ms/mslearn-detect-faces para **baixar detect-faces.zip**. Em seguida, abra a pasta no computador.

6. Localize o arquivo chamado **store-camera-1.jpg**; que contém a seguinte imagem:
<img width="451" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/6cbe52f7-f8cb-4b4c-afa9-c40f61740116">

7. Carregue  **store-camera-1.jpg** e revise os detalhes de detecção de rosto que são retornados.

8. Localize o arquivo **chamado store-camera-2.jpg**; que contém a seguinte imagem:
<img width="452" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/e8cef85c-ddab-4366-b53a-d130541975ac">

9. Carregue **store-camera-2.jpg** e revise os detalhes de detecção de rosto retornados.

10. Localize o arquivo chamado **store-camera-3.jpg**; que contém a seguinte imagem:
<img width="445" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/68815143-be26-4437-83a7-2d363d253b71">

11. Carregue **store-camera-3.jpg** e revise os detalhes de detecção de rosto que são retornados. Observe como o Azure AI Face não detectou o rosto que está obscurecido.

# Resultados:

   1.
<img width="503" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/32efd34a-f31e-4cc1-9122-eb68166de21f">


` [
  {
    "recognitionModel": "recognition_01",
    "faceRectangle": {
      "width": 93,
      "height": 144,
      "left": 324,
      "top": 95
    },
    "faceLandmarks": {
      "pupilLeft": {
        "x": 365.5,
        "y": 156.7
      },
      "pupilRight": {
        "x": 404.7,
        "y": 158.1
      },
      "noseTip": {
        "x": 396.8,
        "y": 183.8
      },
      "mouthLeft": {
        "x": 357.5,
        "y": 200.1
      },
      "mouthRight": {
        "x": 398.7,
        "y": 202.3
      },
      "eyebrowLeftOuter": {
        "x": 346.2,
        "y": 146.7
      },
      "eyebrowLeftInner": {
        "x": 381.6,
        "y": 145.9
      },
      "eyeLeftOuter": {
        "x": 358.1,
        "y": 156.6
      },
      "eyeLeftTop": {
        "x": 366,
        "y": 154.6
      },
      "eyeLeftBottom": {
        "x": 365.8,
        "y": 158.6
      },
      "eyeLeftInner": {
        "x": 372,
        "y": 157.1
      },
      "eyebrowRightInner": {
        "x": 400.1,
        "y": 147
      },
      "eyebrowRightOuter": {
        "x": 417,
        "y": 145.8
      },
      "eyeRightInner": {
        "x": 398.6,
        "y": 158.5
      },
      "eyeRightTop": {
        "x": 405,
        "y": 155.7
      },
      "eyeRightBottom": {
        "x": 404.9,
        "y": 159.9
      },
      "eyeRightOuter": {
        "x": 410.3,
        "y": 158.4
      },
      "noseRootLeft": {
        "x": 383,
        "y": 158.7
      },
      "noseRootRight": {
        "x": 395.2,
        "y": 159.2
      },
      "noseLeftAlarTop": {
        "x": 379.9,
        "y": 174.9
      },
      "noseRightAlarTop": {
        "x": 400.2,
        "y": 174.8
      },
      "noseLeftAlarOutTip": {
        "x": 373.8,
        "y": 182.8
      },
      "noseRightAlarOutTip": {
        "x": 402.9,
        "y": 183.2
      },
      "upperLipTop": {
        "x": 388.7,
        "y": 197.5
      },
      "upperLipBottom": {
        "x": 387.4,
        "y": 201.8
      },
      "underLipTop": {
        "x": 385.2,
        "y": 213.5
      },
      "underLipBottom": {
        "x": 384.1,
        "y": 220.1
      }
    },
    "faceAttributes": {
      "mask": {
        "type": "noMask",
        "noseAndMouthCovered": false
      }
    }
  }
]
`  

   
   2.

<img width="508" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/3780d903-f1cf-4deb-b37e-0b08a515430f">


`   [
  {
    "recognitionModel": "recognition_01",
    "faceRectangle": {
      "width": 88,
      "height": 144,
      "left": 441,
      "top": 132
    },
    "faceLandmarks": {
      "pupilLeft": {
        "x": 488.2,
        "y": 190.8
      },
      "pupilRight": {
        "x": 519,
        "y": 196.4
      },
      "noseTip": {
        "x": 516.6,
        "y": 223.3
      },
      "mouthLeft": {
        "x": 481,
        "y": 242
      },
      "mouthRight": {
        "x": 507.6,
        "y": 246.3
      },
      "eyebrowLeftOuter": {
        "x": 472.1,
        "y": 177
      },
      "eyebrowLeftInner": {
        "x": 506,
        "y": 181.6
      },
      "eyeLeftOuter": {
        "x": 482,
        "y": 189.6
      },
      "eyeLeftTop": {
        "x": 489.3,
        "y": 187.9
      },
      "eyeLeftBottom": {
        "x": 487.9,
        "y": 193.5
      },
      "eyeLeftInner": {
        "x": 493.7,
        "y": 192.2
      },
      "eyebrowRightInner": {
        "x": 519.2,
        "y": 184.9
      },
      "eyebrowRightOuter": {
        "x": 530.4,
        "y": 183.8
      },
      "eyeRightInner": {
        "x": 514.3,
        "y": 196.4
      },
      "eyeRightTop": {
        "x": 520,
        "y": 193.3
      },
      "eyeRightBottom": {
        "x": 519,
        "y": 198.7
      },
      "eyeRightOuter": {
        "x": 522.9,
        "y": 197.1
      },
      "noseRootLeft": {
        "x": 503,
        "y": 194.7
      },
      "noseRootRight": {
        "x": 513.3,
        "y": 196.6
      },
      "noseLeftAlarTop": {
        "x": 498.3,
        "y": 213.3
      },
      "noseRightAlarTop": {
        "x": 516.3,
        "y": 214.3
      },
      "noseLeftAlarOutTip": {
        "x": 492.9,
        "y": 222.5
      },
      "noseRightAlarOutTip": {
        "x": 516.6,
        "y": 224.6
      },
      "upperLipTop": {
        "x": 504.5,
        "y": 240.7
      },
      "upperLipBottom": {
        "x": 502.5,
        "y": 244.5
      },
      "underLipTop": {
        "x": 502.4,
        "y": 246.3
      },
      "underLipBottom": {
        "x": 500.9,
        "y": 252.2
      }
    },
    "faceAttributes": {
      "mask": {
        "type": "noMask",
        "noseAndMouthCovered": false
      }
    }
  }
]
`


3. <

img width="511" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/129ea882-d14b-4571-99f8-86cb5029bfcb">



`[
  {
    "recognitionModel": "recognition_01",
    "faceRectangle": {
      "width": 78,
      "height": 109,
      "left": 409,
      "top": 169
    },
    "faceLandmarks": {
      "pupilLeft": {
        "x": 449.2,
        "y": 210
      },
      "pupilRight": {
        "x": 469,
        "y": 204.5
      },
      "noseTip": {
        "x": 481,
        "y": 223.8
      },
      "mouthLeft": {
        "x": 460.6,
        "y": 251.7
      },
      "mouthRight": {
        "x": 479.3,
        "y": 244.8
      },
      "eyebrowLeftOuter": {
        "x": 432.4,
        "y": 204.5
      },
      "eyebrowLeftInner": {
        "x": 455.4,
        "y": 195.7
      },
      "eyeLeftOuter": {
        "x": 444.7,
        "y": 211.1
      },
      "eyeLeftTop": {
        "x": 449.1,
        "y": 207.1
      },
      "eyeLeftBottom": {
        "x": 450.2,
        "y": 212.2
      },
      "eyeLeftInner": {
        "x": 453,
        "y": 209.6
      },
      "eyebrowRightInner": {
        "x": 464.7,
        "y": 194.3
      },
      "eyebrowRightOuter": {
        "x": 469,
        "y": 191.5
      },
      "eyeRightInner": {
        "x": 466.1,
        "y": 206.3
      },
      "eyeRightTop": {
        "x": 468.6,
        "y": 201.5
      },
      "eyeRightBottom": {
        "x": 470.2,
        "y": 206.3
      },
      "eyeRightOuter": {
        "x": 471,
        "y": 203.9
      },
      "noseRootLeft": {
        "x": 458.8,
        "y": 208.9
      },
      "noseRootRight": {
        "x": 465.6,
        "y": 206.7
      },
      "noseLeftAlarTop": {
        "x": 463.1,
        "y": 224.4
      },
      "noseRightAlarTop": {
        "x": 475,
        "y": 218.6
      },
      "noseLeftAlarOutTip": {
        "x": 462.9,
        "y": 232.8
      },
      "noseRightAlarOutTip": {
        "x": 478.6,
        "y": 225.9
      },
      "upperLipTop": {
        "x": 478,
        "y": 240.5
      },
      "upperLipBottom": {
        "x": 478,
        "y": 244.5
      },
      "underLipTop": {
        "x": 479,
        "y": 249.3
      },
      "underLipBottom": {
        "x": 480.5,
        "y": 254.4
      }
    },
    "faceAttributes": {
      "mask": {
        "type": "noMask",
        "noseAndMouthCovered": false
      }
    }
  }
]
`

4.


 <img width="754" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/35fe233f-890c-4746-9b69-4b002515edb9">


`[
  {
    "recognitionModel": "recognition_01",
    "faceRectangle": {
      "width": 68,
      "height": 113,
      "left": 274,
      "top": 111
    },
    "faceLandmarks": {
      "pupilLeft": {
        "x": 316.1,
        "y": 160.2
      },
      "pupilRight": {
        "x": 333.1,
        "y": 157.2
      },
      "noseTip": {
        "x": 342.3,
        "y": 176.6
      },
      "mouthLeft": {
        "x": 314,
        "y": 194.8
      },
      "mouthRight": {
        "x": 332.5,
        "y": 190.3
      },
      "eyebrowLeftOuter": {
        "x": 304.6,
        "y": 155.9
      },
      "eyebrowLeftInner": {
        "x": 325.2,
        "y": 151.4
      },
      "eyeLeftOuter": {
        "x": 312.5,
        "y": 160.9
      },
      "eyeLeftTop": {
        "x": 316.4,
        "y": 158.9
      },
      "eyeLeftBottom": {
        "x": 316.6,
        "y": 161.2
      },
      "eyeLeftInner": {
        "x": 318.7,
        "y": 159.8
      },
      "eyebrowRightInner": {
        "x": 332.4,
        "y": 150.9
      },
      "eyebrowRightOuter": {
        "x": 335.2,
        "y": 148.3
      },
      "eyeRightInner": {
        "x": 330.6,
        "y": 157.9
      },
      "eyeRightTop": {
        "x": 333.6,
        "y": 155.8
      },
      "eyeRightBottom": {
        "x": 333.6,
        "y": 158
      },
      "eyeRightOuter": {
        "x": 334.4,
        "y": 157
      },
      "noseRootLeft": {
        "x": 325.1,
        "y": 159.9
      },
      "noseRootRight": {
        "x": 331.6,
        "y": 159
      },
      "noseLeftAlarTop": {
        "x": 325.1,
        "y": 172.8
      },
      "noseRightAlarTop": {
        "x": 336.4,
        "y": 169.5
      },
      "noseLeftAlarOutTip": {
        "x": 322.7,
        "y": 179.4
      },
      "noseRightAlarOutTip": {
        "x": 337.3,
        "y": 175.3
      },
      "upperLipTop": {
        "x": 333.4,
        "y": 189.7
      },
      "upperLipBottom": {
        "x": 332.4,
        "y": 192.6
      },
      "underLipTop": {
        "x": 331.9,
        "y": 197.7
      },
      "underLipBottom": {
        "x": 332,
        "y": 202
      }
    },
    "faceAttributes": {
      "mask": {
        "type": "noMask",
        "noseAndMouthCovered": false
      }
    }
  },
  {
    "recognitionModel": "recognition_01",
    "faceRectangle": {
      "width": 69,
      "height": 106,
      "left": 624,
      "top": 80
    },
    "faceLandmarks": {
      "pupilLeft": {
        "x": 630.1,
        "y": 125.4
      },
      "pupilRight": {
        "x": 645.1,
        "y": 124.4
      },
      "noseTip": {
        "x": 622.8,
        "y": 146.4
      },
      "mouthLeft": {
        "x": 635.7,
        "y": 160.3
      },
      "mouthRight": {
        "x": 651.9,
        "y": 160.3
      },
      "eyebrowLeftOuter": {
        "x": 624.9,
        "y": 116.8
      },
      "eyebrowLeftInner": {
        "x": 628.1,
        "y": 117.8
      },
      "eyeLeftOuter": {
        "x": 629.1,
        "y": 125.5
      },
      "eyeLeftTop": {
        "x": 629.4,
        "y": 123.7
      },
      "eyeLeftBottom": {
        "x": 630.2,
        "y": 126.8
      },
      "eyeLeftInner": {
        "x": 631.8,
        "y": 125.5
      },
      "eyebrowRightInner": {
        "x": 634.9,
        "y": 117.1
      },
      "eyebrowRightOuter": {
        "x": 655,
        "y": 115.9
      },
      "eyeRightInner": {
        "x": 642.8,
        "y": 125
      },
      "eyeRightTop": {
        "x": 643.9,
        "y": 122.2
      },
      "eyeRightBottom": {
        "x": 645,
        "y": 126
      },
      "eyeRightOuter": {
        "x": 648.6,
        "y": 124.4
      },
      "noseRootLeft": {
        "x": 631.9,
        "y": 126.4
      },
      "noseRootRight": {
        "x": 636.1,
        "y": 126.5
      },
      "noseLeftAlarTop": {
        "x": 628.2,
        "y": 139.5
      },
      "noseRightAlarTop": {
        "x": 638.2,
        "y": 139.8
      },
      "noseLeftAlarOutTip": {
        "x": 628.5,
        "y": 145.9
      },
      "noseRightAlarOutTip": {
        "x": 641.5,
        "y": 146.8
      },
      "upperLipTop": {
        "x": 634.4,
        "y": 158.6
      },
      "upperLipBottom": {
        "x": 635.3,
        "y": 161
      },
      "underLipTop": {
        "x": 636.3,
        "y": 164.1
      },
      "underLipBottom": {
        "x": 637.1,
        "y": 168.2
      }
    },
    "faceAttributes": {
      "mask": {
        "type": "noMask",
        "noseAndMouthCovered": false
      }
    }
  },
  {
    "recognitionModel": "recognition_01",
    "faceRectangle": {
      "width": 52,
      "height": 86,
      "left": 874,
      "top": 273
    },
    "faceLandmarks": {
      "pupilLeft": {
        "x": 885.8,
        "y": 301
      },
      "pupilRight": {
        "x": 896.1,
        "y": 304.2
      },
      "noseTip": {
        "x": 875.4,
        "y": 316.9
      },
      "mouthLeft": {
        "x": 884.5,
        "y": 335.1
      },
      "mouthRight": {
        "x": 894.3,
        "y": 337.9
      },
      "eyebrowLeftOuter": {
        "x": 883.7,
        "y": 291.9
      },
      "eyebrowLeftInner": {
        "x": 885.2,
        "y": 293.5
      },
      "eyeLeftOuter": {
        "x": 885.4,
        "y": 300.7
      },
      "eyeLeftTop": {
        "x": 885.3,
        "y": 299.5
      },
      "eyeLeftBottom": {
        "x": 885.6,
        "y": 302.2
      },
      "eyeLeftInner": {
        "x": 887,
        "y": 301.5
      },
      "eyebrowRightInner": {
        "x": 889.8,
        "y": 294.7
      },
      "eyebrowRightOuter": {
        "x": 904.4,
        "y": 298.9
      },
      "eyeRightInner": {
        "x": 894.5,
        "y": 303.8
      },
      "eyeRightTop": {
        "x": 895.2,
        "y": 302.2
      },
      "eyeRightBottom": {
        "x": 895.7,
        "y": 305.6
      },
      "eyeRightOuter": {
        "x": 899,
        "y": 305.1
      },
      "noseRootLeft": {
        "x": 886.5,
        "y": 302.3
      },
      "noseRootRight": {
        "x": 889.2,
        "y": 303.2
      },
      "noseLeftAlarTop": {
        "x": 881.6,
        "y": 312.6
      },
      "noseRightAlarTop": {
        "x": 888.3,
        "y": 314.8
      },
      "noseLeftAlarOutTip": {
        "x": 881.3,
        "y": 318.2
      },
      "noseRightAlarOutTip": {
        "x": 889.9,
        "y": 321.6
      },
      "upperLipTop": {
        "x": 882.1,
        "y": 330.2
      },
      "upperLipBottom": {
        "x": 882.9,
        "y": 333
      },
      "underLipTop": {
        "x": 884.7,
        "y": 341.2
      },
      "underLipBottom": {
        "x": 885.1,
        "y": 345.1
      }
    },
    "faceAttributes": {
      "mask": {
        "type": "noMask",
        "noseAndMouthCovered": false
      }
    }
  }
]
`
5. sinta-se à vontade para experimentar as imagens de amostra ou algumas de suas próprias imagens:

<img width="619" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/0f5ae6e1-3040-4b63-a8e8-468bb8aae658">
