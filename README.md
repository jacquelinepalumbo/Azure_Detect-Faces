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

Na home page do Vision Studio, selecione **Exibir todos os recursos** no cabeçalho **Introdução ao Vision**.

<img width="626" alt="image" src="https://github.com/jacquelinepalumbo/Azure_Detect-Faces/assets/119548193/5bb0961c-9003-4e29-872e-b7aae15e4fb5">
