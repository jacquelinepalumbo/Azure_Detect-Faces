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

   1. <img width="503" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/32efd34a-f31e-4cc1-9122-eb68166de21f">

   
   2. <img width="508" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/3780d903-f1cf-4deb-b37e-0b08a515430f">

'   [
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
'

