# TI Radars Basic Information

FMCW(Frequency Modulated Continuous Wave)


* Introduction to mmwave Sensing: FMCW Radars (Youtube)
(Sandeep Rao, Texas Instruments)                
-[Introduction to mmwave Sensing: FMCW Radars1](https://www.youtube.com/watch?v=8cHACNNDWD8)       
-[Introduction to mmwave Sensing: FMCW Radars2](https://www.youtube.com/watch?v=bB-SGw9uRgQ)        

* FMCW Radar Detection and Tracking (Youtube)                  
-[FMCW Radar Detection and Tracking](https://www.youtube.com/watch?v=R3IKBRMi4dc)

관련 TI 자료 
현재 TI사이트에서 자료가 없어져서, 상위 파일에 넣음
이 문서에서 질문을 하는데, 질문이 너무 좋으며, 그 답을 각각에 모듈에서 쉽게 찾을 수 있다.     
-  mmwaveSensing-FMCW-offlineviewing_4.pdf    
  -[Introduction to mmWave radar sensing: FMCW radars](https://training.ti.com/mmwave-training-series)    

<br/>

* RADAR 관련 Blog        
  -[Radar Blogs](https://adasauto.blogspot.com/)      
  -[RADAR, Why need](https://adasauto.blogspot.com/2018/04/requirements-for-radar-system-for.html)    
  -[RADAR, Type](https://adasauto.blogspot.com/2018/02/qualities-that-radar-system-should.html)    

<br/>
<br/>

RADAR의 기본이해는 생각보다 어렵지 않으나 완벽한 이해는 좀 힘들 것 같다. (기본 DSP지식이 있다면 어느정도 기본이해는 되어진다)    
문서를 가끔 다시 한번 보는데, 각 Chapter마다 질문이 있는 Why를 생각하기 위해서 여러번 생각하게 한다.   

<br/>

FMCW의 기본이해는 일단 Ramp FM의 1 Chirp으로 Rx Chirp 에 포함된 Analog 성분을 분석하는 것이다. 
더불어, 이런 Chirp들을 비교 분석하고, 더 나아가 Channel을 구성하여 4D까지 알아내는 것이다. 

<br/>

* RF Calibration 
TI에서는 Self-Calibration 기능제공해주고 있으며, 글을 읽어보면,  주기적으로 Calibration을 해야 하는 것으로 보인다.  
주로 RF기반으로 발생하는 오차들 주로 보정을 하는 것으로 보이며, 동작구조를 보면, Loopback 형식으로 되어 구동되어지는 것 같다.  
List of Calibrations 확인 
(PLL/ Synthesizer VCO/ ADC DC offset / HPF/LPW Cutoff Calibration 기타등등)
AC 와 DC에서 발생되어지는 오차와 Clock 보정을 비롯하여 각 Gain /Phase 오차 보정 등    
정밀한 측정을 위해서 많은 보정을 걸치는 것으로 보인다.  
RF이므로 오차와 Noise 처리 와 매번 새로운 상황마다 테스트해야 하는 것이 반복되리라고 생각된다.
  https://www.ti.com/lit/an/spracf4c/spracf4c.pdf?ts=1675925584167&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FAWR6843AOP


  


<br/>

RF TEST 방법을 소개하고 있으며, 각 부분을 보정하는 부분역시 설명해주고 있다.    
Chamber 구조 및 동작원리 쉽게 설명하면, Loopback으로 TX후 RX가 제대로 오는지 SNR로 보는 방식이며, 각 부분을 보정(Range Bias/Channel Gain/Offset)한다.     
나도 Chamber가 너무 크고 양산할때 문제라고 생각하는데, 아래를 보면, Cubic으로 된 Chamber를 소개한다 (역시 TI ) 
어차피 Chamber 역할은 단순하며, 작아도 상관을 없을 것 같다 (현재 내생각으로)           
흐음 거리가 작으면, 오차를 좀 더 정확하게 잡아햐 할 것으로 생각되어진다.  
  https://www.ti.com/lit/an/spracx7/spracx7.pdf?ts=1675994243978&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FIWR6843AOP

<br/>

# TI  Wellness 관련자료

<br/>
<br/>

**TI Wellness 관련설명자료**    
TI에서 제공하는 Wellness 기술이며, 이미 노인대상으로 많이 나온것으로 알고 있다.    
[IWR6843AOP](https://www.ti.com/product/IWR6843AOP)      
[TI Industrial](https://www.ti.com/sensors/mmwave-radar/industrial/overview.html)     
https://e2e.ti.com/blogs_/b/process/posts/how-mmwave-sensors-create-technology-advantages-for-independent-assisted-living?HQS=epd-rap-null-contactlessmonitoring-rebs-ta-nextrollnet_160x600-kr&DCM=yes&dclid=CL2zjprkz_gCFafBTAIdoSsGcQ

<br/>

**TI Tool**   
mmWave-Studio라고 CCS처럼 GUI Tool을 제공을 해주고 있으며, 현재 버전도 계속 Upddate 되었다.
이제는 Zoom 처럼 Cloud 기반에서 동작되는 것도 있는 것 같은데, 많이 궁금하기는 하다.   
https://www.ti.com/tool/MMWAVE-3P-SEARCH                
https://www.ti.com/tool/MMWAVE-STUDIO#tech-docs                    
https://www.ti.com/lit/ug/swru529c/swru529c.pdf?ts=1677202685363&ref_url=https%253A%252F%252Fwww.ti.com%252Ftool%252FMMWAVE-STUDIO

<br/>

**Contactless patient and elderly care using mmWave sensors | TI.com Video**            
  https://training.ti.com/contactless-patient-and-elderly-care-using-mmwave-sensors

<br/>



<br/>

**3D Occupancy Sensing**    
  https://training.ti.com/3d-occupancy-sensing-home-and-office?context=1128486-1139156-1148009

**mmWave Vital Signs Lab**   
  https://training.ti.com/mmwave-vital-signs-lab?keyMatch=MMWAVE%20VITAL%20SIGN  

**IWR6843AOPEVM Technical Docs**             
  https://www.ti.com/tool/IWR6843AOPEVM#tech-docs

**60GHz mmWave Sensor EVMs (Rev. E)**     
12 Channel Virtual Antenna Array (MIMO), 안테나 설계 및 기본사항을 알려면 아래 부분참조         
Lamda(Wavelength)이며, 삼각함수를 알면 이해가됨 (상위 TI 교육자료 확인)      
Azimuth/Elevation 부분의 이해와 Lamda를 기본으로 이해하면 기본 3D 부분 안테나는 이해가 되어짐 (Phase 기반으로 삼각함수이용)  
아래자료를 보면, 각 PCB의 안테나 선로가 다 같아야 할 것이며, 이부분은 RAM처럼 Leveling(선로길이보정)이 필요할듯 하다     
  * 3.6 xWR6843ISK Antenna  
  * 3.7 IWR6843ISK-ODS Antenna   
  * 4.5 xWR6843AOPEVM Antenna    
  * 5.5 xWR6843AOPEVM Antenna      
  
https://www.ti.com/lit/ug/swru546e/swru546e.pdf?ts=1658041409154&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FIWR6843AOP          

일단 너무 보기 좋은 사이트 ㅋㅋㅋ                         
https://dev.ti.com/tirex/explore/node?node=A__AMKSv8im74YjT7cmO9jVHg__com.ti.mmwave_industrial_toolbox__VLyFKFf__4.9.0    
https://dev.ti.com/tirex/explore/node?node=AJuqjWdTuol3jtoyFrofqw

  

**TI AOP Type**  
IWR6843AOP 
- Radio 3(TX)x4(RX)  : RX 4Channel이 되어지니, 3차원까지 좌표분석이 가능 (각 Phase이용하면됨)        
- C674xDSP/ARM-R4F200MHz 다만 아쉬운것은 RF가 RADAR만 지원 이외 미지원이며, EDMA 대신 DMA로 되어있다          
- 아마 복잡한 DMA까지 필요 없어서 뺀것 같다 다만, Channel이 늘어나면, 추후 EDMA도 필요할꺼 같은데, 다른 모델을 찾아보면 알겠지.                                           
  https://www.ti.com/product/IWR6843AOP

<br/>

**Healthcare 자료**           
TI Traning 자료 
  * Virtal Sign : Amp 와 Frequecny는 거의 Range 영역이 정해져 있으며, Band Pass Filter을 이용하면 쉽게 될꺼 같다.     
    * Breathing Rate: 세부호흡 Data도 DSP를 이용하여 분석가능하며, Noise 경우, 추후 Convolution이나, 다른 필터를 고려??
    * Heart Rate: TI-DSP가 성능이 될꺼라고 생각되어, 이것도 세부분석가능할 걸로 예측    
  * 3D 좌표기반의 분석 
    * 사람의 위치 및 Tracking 가능하며 사람 수도 측정이 가능     
    * Fall Detection의 경우, 3D좌표( 기반으로 Velocity Motion으로 감지할 걸로 예측)     

<br/>

TI에서는 별도로 현재 mmWave Tool을 제공하여, 이부분을 추후에 이용해도록하겠다. 
3D 분석할 경우, TI문서 볼경우, PCB의 Anthena 거리 및 위치를 참조하도록 하자       
  https://training.ti.com/non-contact-patient-and-elderly-monitoring-mmwave-radar-webinar

<br/>
  
**MIMO RADAR**  
이 부분을 보면 쉽게 Phase 기반으로 삼각함수이용하여 이해가능하며, arch(inverse) tangent 도 충분히 이용가능할 것 같다.   
  * single-input-multiple-output (SIMO): 1개 TX기반으로 여러개의 RX에서 이를 분석한다.    
  * Multiple-input-multiple-output (MIMO): 여러개 TX 기반으로 RX에서 이를 구분하여 Virtual Channel을 만들어 사용한다.   
      * 세부내용은 아래 Principle of the MIMO Radar
      * Time Division Multiplexing (TDM-MIMO)  
      * BPM-MIMO 
만약 Lamda/theta/omega 기호의 의미를 파악하지 못했다면, 상위 introdution을 다시 보자.   
수학도출과정이 이해가 안되어진다면, 그냥 그러려니하고 넘어가자   
중요한 것은 안테나의 RX의 Lamda/2 이다. (현재 이해한 바로는 TX의 주파수 분리하는 최소 Phase의 180 필요)    
그 이유를 간단히 보면, OFDM과 유사한 것 같다.                                

<br/>

https://www.ti.com/lit/an/swra554a/swra554a.pdf?ts=1658203955728&ref_url=https%253A%252F%252Flink.zhihu.com%252F%253Ftarget%253Dhttps%253A%252F%252Fwww.ti.com%252Flit%252Fpdf%252Fswra554


<br/>
<br/>

**TI mmWave**     
  https://www.ti.com/ko-kr/design-resources/embedded-development/industrial-mmwave-radar-sensors.html

<br/>

**mmWave Reference**      
  https://www.ti.com/reference-designs/index.html#search?keyword=mmwave&applid=120

<br/>
<br/>

# 일반 Radar

<br/>
<br/>

  https://en.wikipedia.org/wiki/Radar

<br/>
<br/>


## RF 기본용어          

나는 개인적으로 옛날의 일본책들을 좋아하며, 특히 HW쪽으로는 더 쉽게 설명을 해놓았다.          
전자회로부터, 각 소자 HW 책 역시 일본책들이 더 좋다      
  http://www.rfdh.com/rfdb.php3

<br/>
<br/>

## Programming Chirp Parameters 

<br/>
<br/>

 

2.3.1 Angular Resolution  ( MIMO 와 Virtual Anthena , 즉 Phsed Array Anthena )
   - 여기 왜 2 Lamda 와 Lamda/2 (180) 인가에 대해서 많이 생각해봤다. 
   - RX의 경우는 Frequency 중복허용과 이를 분리하기 위해서 최소 Lamda/2로 한걸로 생각했다 (OFDM, 부분 보시길)    
   - TX의 경우는 왜 2 Lamda 일까? 일단 TX의 Fov 와 관련이 있을 꺼 같다.    
3. Chirp Configurations for Common Applications           
   - 중요한 자료이며, 각 FFT Size 및 관련설정부분을 전체 쉽게 알 수 있다. 
   - 내가 가장 찾던 자료이며, 이 부분에서 많은 것을 얻었다.    
https://www.ti.com/lit/an/swra553a/swra553a.pdf?ts=1686732119535&ref_url=https%253A%252F%252Fwww.google.com%252F

<br/>
<br/>

## 시스템 잡음지수 계산 (Cascade Noise Figure)

시스템 잡음지수 계산 (Cascade Noise Figure)
 http://www.rfdh.com/rfdb/nf.htm

이외 RF관련부분 내용을 좀 더 알고 싶다면, 아래의 사이트에서 확인하자. 
  http://www.rfdh.com/invite/ilab/k1.htm

<br/>
<br/>

# FMCW 측정관련내용 

<br/>

- [Analysis of FMCW radar signals in automotive applications](https://www.youtube.com/watch?v=8qaCSQ83ZyU)

<br/>
<br/>

# Radar 와 Communication 관련자료 

<br/>
<br/>

Radar의 HW구조를 보면, synthesizer를 제어를 하여 통신부분으로 편입될 가능성이 있을 것 같아 관련자료 찾음    
Syntesizer를 빼면, 일반 Radio 즉, RF 통신과 큰차이가 없다    
예를들면, WIFI or 5G에 적용가능할 것 같으며, 다만 Time을 분할해서 Syntesizer를 사용해야 하므로 관련부분은 복잡해질 둣하다.   

<br/>

둘 사이에서 가장 큰 차이라고 하면, RADAR는 거리를 2D로 해야 하고 Commmuncation은 D를 사용한다. 
  - 일반 RF Communcation의 거리는 센서사이와 거리. 
  - RADAR  Round Trip, 즉 왕복거리이다 

여기서 문제가 되는 것은 Amp(LNA)와 Noise 를 비롯하여 각종 문제가 있을 것이다. 
더불어 거리에 대한 제약이 항상 민감하게 있다.    
실제 RADAR 이론에서와 거리와 갭이 좀 많이 클거라고 생각되어진다.           

<br/>
<br/>

 https://www5.cadence.com/newsletter-subscription-msa-ebook-rfmw-lp.html?utm_source=google&utm_medium=cpc&utm_term=fmcw&utm_campaign=RF_2021&utm_source=adwords&utm_medium=ppc&hsa_acc=1270110830&hsa_cam=12316095010&hsa_grp=118067585256&hsa_ad=497957189478&hsa_src=g&hsa_tgt=kwd-874051436855&hsa_kw=fmcw&hsa_mt=e&hsa_net=adwords&hsa_ver=3&gclid=CjwKCAjw_b6WBhAQEiwAp4HyIMJ1D7q-PRaTvqNXVGevb5l4NTslvmg8av64Gykcn06Z1Pp_CqX67xoCSagQAvD_BwE
  
<br/>
<br/>
