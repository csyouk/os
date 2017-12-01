# Parallelism in Hardware

#### 무어의 법칙.
- 동일면적에 들어가는 트랜지스터의 갯수가 2년에 2배씩 늘어난다.
- 이 말은 CPU의 속도가 빨라진다는 뜻이다.
- 이 법칙은 2004년에 깨졌다.

#### CPU 개발의 방향
- 코어를 더 붙이고, GPU, Cache를 붙이는 방향으로 발전하고 있다.

#### GPU
- 이미지 처리에 특화된 연산장치.
- ALU가 CPU보다 매우 작다.
- Cache는 없다.
- GPGPU : General Purpose Graphic Processing Unit.
  - CUDA : programming framework
  - OpenCL : apple, 등.

#### 암달의 법칙.
- data dependency가 있는 sequential part부분 때문에, cpu숫자가 늘어난다고 성능이 그에 비례해서 커지지 않는다.

#### Concurrency vs Parallism
- 논리적 병렬성 : Concurrency.
- 물리적 병렬성 : Parallelism.
  - pipelining

- single core라 할지라도 pipe lining때문에, 병렬성을 가지고 있다.


#### SIMD Processing
- Single Instruction Multiple data.
- Data level parallelism 이라고 얘기한다.
- scalar processing.
- vector operation.
  - Array연산을 하는데 최적화한다.
  - ARM의 경우, 이러한 연산을 지원한다.

#### pipe line bubble/stall
- Therad level parallelism.
- Instruction을 fetch 하는 과정에서 stage가 비어있는 경우.
- branch predition을 할 때 발생할 수 있다.
- 아니면, compare시 발생.
- SMT : Simutaneous Multi Thread.
  - Intel : Hyper thread
