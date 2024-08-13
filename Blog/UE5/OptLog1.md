# OptLog1

### 들어가며...
최근 많은 device의 발전으로 사용자들은 High-quality를 가지는 Game 들을 손쉽게 만날 수 있다. 특히, Apple 의 M1 chip 의 개발은 Macbook, iPad 등 많은 device의 성능을 크게 증가시켰다. 또한, 추가적으로 비교적 최근에 나온 M3 chip은 H/W 가속 Ray tracing을 탑재 했기 때문에 Blender 등 Rendering의 성능이 매우 좋아졌다. 

하지만 이런 부분에서도 한 가지 아쉬운 점이 존재한다. 많은 AAA 게임들을 만들 때 Unreal Engine을 사용하여 정말 실사와 같은 Game을 만드려고 노력한다. 여기에서 NVIDIA RTX GPU를 이용한다면 충분히 좋은 성능을 얻어낸다. 하지만 Apple의 Macbook (M1 pro) 기준 아직 FPS 가 상대적으로 많이 부족한 것을 볼 수 있다. 이 점에서 현재 사이드 프로젝트는 시작된다. 

Unreal Engine 5.4.1을 기준으로 프로젝트를 진행할 예정이다. 현재의 성능은 아래와 같이 나타난다.  
```console
$ stat unit # UE5에서 성능 지표를 Frame에 보여주는 console command 
``` 

---
| Performance | Time (ms) | 
|     ---     |    ---    |
| Frame | 42.64 |
| Game | 5.46 |
| Draw | 0.08 | 
| RHIT | 0.10 | 
| GPU Time | 42.12 |

위의 표를 해석했을 때 아래와 같이 해석할 수 있다. [(참고 링크)](https://devjino.tistory.com/364) 
총 1 Frame을 생성하기 위해 소요된 총 시간이다. 이 현재 내 Macbook에서는 42.64ms가 소요가 된다. 이 부분에서 가장 시간이 많이 소요 되는 부분은 GPU에서 연산을 처리하는 부분이다. GPU Time 이 42.12ms가 걸리는 것을 확인할 수 있다.  

장면에 또 다른 정보는 아래와 같다.   
| Info |  |
| --- | --- | 
| Mem | 780.27 MB |
| DynRes | OFF | 
| Draw | 523 | 
| Prims | 17.8K | 

AAA Game 에서 상대적으로 매우 낮은 Primitive의 개수를 가지고 있는 상황임에도 불구하고 오래 걸리는 것을 확인할 수 있다. 
우리가 최적화를 해야할 부분은 GPU Time 부분이다. 즉, Scene을 위해 Rendering 하는 시간이 매우 오래 걸리는 것을 확인할 수 있다.   
이 부분을 중점적으로 보자.

--- 
[Blog Home](../Blog.md)