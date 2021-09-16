# CNN 구현
파이토치와 텐서플로우를 이용하여 간단한 리뷰와 함께 CNN 구조를 바닥부터 구현해 보았습니다.


주로 파이토치와 텐서플로우의 내부 구현 소스를 참고하였고 train, validate, fit, test 및 커스텀 데이터 처리는 직접 구현했습니다.  그 외에 핵심적으로 필요하지만 pytorch에서 지원하지 않는 loss클래스 또한 직접 정의하였습니다.

> 깃허브 링크보다, 코랩으로 보면 목차까지 표현되어 더욱 깔끔하게 볼 수 있어서 링크를 걸어놨습니다.


* Inception v2, v3 [PyTorch](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/inception_v2%2C_v3(torch).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/1L7kUpWaaj4glZZ75MJdudunqD61KCvMk?usp=sharing)

> 위 링크는 Inception v3에 대한 간단한 리뷰 및 모델 구현인데, 직접 공부하며 구현했던 모델 중 가장 뿌듯했던 모델입니다.
> 
> 논문에서 제시한 loss가 pytorch(label smoothing)에서 구현되어 있지 않아서 정말 밑바닥 부터 구현하였고, 구조도 그간의 모델들에 비해 복잡했습니다. 



## CNN
TF([colab](https://colab.research.google.com/drive/18jRNx3mYSbOEfgGhj-_0V-8X5dTIYsMJ?usp=sharing))
* AlexNet [TensorFlow](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/AlexNet(TF).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/18jRNx3mYSbOEfgGhj-_0V-8X5dTIYsMJ?usp=sharing)
* VGGNet [TensorFlow](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/VGGNet(TF).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/1PCfNuOx3_8BS_HpzLrbl-ZSOPl0lnw5M?usp=sharing)
* VGGNet [PyTorch](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/VGG(torch).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/1pH3p9JsS0SBrt4EiPRzcsSAPr_Y5766_?usp=sharing)
* GoogLeNet(Inception v1) [TensorFlow](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/inception_v1(TF).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/1rGN2qHRjpWXLHh2MnDhCR-P3SEClf_mA?usp=sharing)
* GoogLeNet(Inception v1) [PyTorch](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/inception_v1(torch).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/1i_WuE9jFUSo0FqFvy3mO4n3qrTYipZAg?usp=sharing)
* ResNet [TensorFlow](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/ResNet50(TF).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/1cvgAuPdfnjS1xJ-eE2YdTdbbAJzJ5vuW?usp=sharing)
* ResNet [PyTorch](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/ResNet(torch).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/1WmztA5ClRDHbtJynmRCVRaqrUolXU6YU?usp=sharing)
* Inception v2, v3 [PyTorch](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/inception_v2%2C_v3(torch).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/1L7kUpWaaj4glZZ75MJdudunqD61KCvMk?usp=sharing)
* SqueezeNet [PyTorch](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/SqueezeNet_(torch).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/17IkS6NlAj3ivpAjkwq8AbJafcRnCVp3u?usp=sharing)
* Xception [PyTorch](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/Xception(torch).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/1JPDZwr8YFl3v_pexekV8zbOObQNjMNvy?usp=sharing)
* DenseNet [PyTorch](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/DenseNet(torch).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/1h0vN8reXhdIBPjMpSJ9XxqGSnko7mveD?usp=sharing)
* MobileNet [PyTorch](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/MobileNet(torch).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/1STNsmGWM_Wof6AqOvXInEjvQZhK_m1TO?usp=sharing)
* SENet(SE-ResNet) [PyTorch](https://github.com/yonghyuk0120/CNN_Study/blob/master/model/SE_ResNet50(torch).ipynb), [Colab에서 보기](https://colab.research.google.com/drive/1Gijdsdn4aIoJBzu_Fxpw-3ic1-g3bMDE?usp=sharing)

