# TI Radars Basic Information

FMCW(Frequency Modulated Continuous Wave)

Introduction to mmwave Sensing: FMCW Radars (Sandeep Rao, Texas Instruments)               

-[Introduction to mmwave Sensing: FMCW Radars1](https://www.youtube.com/watch?v=8cHACNNDWD8)       
-[Introduction to mmwave Sensing: FMCW Radars2](https://www.youtube.com/watch?v=bB-SGw9uRgQ)        

관련 TI 자료 
현재 TI사이트에서 자료가 없어져서, 상위 파일에 넣음
-  mmwaveSensing-FMCW-offlineviewing_4.pdf    
  -[Introduction to mmWave radar sensing: FMCW radars](https://training.ti.com/mmwave-training-series)    

<br/>


-[Radar Blogs](https://adasauto.blogspot.com/)      
  -[RADAR, Why need](https://adasauto.blogspot.com/2018/04/requirements-for-radar-system-for.html)    
  -[RADAR, Type](https://adasauto.blogspot.com/2018/02/qualities-that-radar-system-should.html)    

<br/>
<br/>

RADAR의 기본이해는 생각보다 어렵지 않으며, 기본 DSP지식이 있다면 쉽게 이해하리라고 본다.    
다만. RF이므로 Noise 처리 와 매번 새로운 상황마다 테스트해야 하는 것이 반복되리라고 생각된다.   

<br/>

RF Calibration 방법, 역시 TI에서 제공해주고 있으며, 이 부분도 추후 보도록 하겠다.  

# TI  Wellness 관련자료

<br/>
<br/>

**TI Wellness 관련설명자료**       
https://e2e.ti.com/blogs_/b/process/posts/how-mmwave-sensors-create-technology-advantages-for-independent-assisted-living?HQS=epd-rap-null-contactlessmonitoring-rebs-ta-nextrollnet_160x600-kr&DCM=yes&dclid=CL2zjprkz_gCFafBTAIdoSsGcQ

<br/>

**TI 3rd Party Tool**   
https://www.ti.com/tool/MMWAVE-3P-SEARCH
      
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
  * 3.6 xWR6843ISK Antenna  
  * 3.7 IWR6843ISK-ODS Antenna   
  * 4.5 xWR6843AOPEVM Antenna    
  * 5.5 xWR6843AOPEVM Antenna      
  https://www.ti.com/lit/ug/swru546e/swru546e.pdf?ts=1658041409154&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FIWR6843AOP


**TI AOP Type**  
IWR6843AOP 
- Radio 3(TX)x4(RX)  : RX 4Channel이 되어지니, 3차원까지 좌표분석이 가능 (각 Phase이용하면됨)        
- C674xDSP/ARM-R4F200MHz 다만 아쉬운것은 RF가 RADAR만 지원 이외 미지원  
  https://www.ti.com/product/IWR6843AOP


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


  
**MIMO RADAR**  
이 부분을 보면 쉽게 Phase 기반으로 삼각함수이용하여 이해가능하며, arch(inverse) tangent 도 충분히 이용가능할 것 같다.     
  https://www.ti.com/lit/an/swra554a/swra554a.pdf?ts=1658203955728&ref_url=https%253A%252F%252Flink.zhihu.com%252F%253Ftarget%253Dhttps%253A%252F%252Fwww.ti.com%252Flit%252Fpdf%252Fswra554


<br/>
<br/>

**TI mmWave**     
  https://www.ti.com/ko-kr/design-resources/embedded-development/industrial-mmwave-radar-sensors.html

<br/>

**mmWave Reference**      
  https://www.ti.com/reference-designs/index.html#search?keyword=mmwave&applid=120



# 일반 Radar

  https://en.wikipedia.org/wiki/Radar


<br/>
<br/>

# FMCW 측정관련내용 

- [Analysis of FMCW radar signals in automotive applications](https://www.youtube.com/watch?v=8qaCSQ83ZyU)

<br/>
<br/>

# Radar 와 Communication 관련자료 

<br/>
<br/>

Radar의 HW구조를 보면, synthesizer를 제어를 하여 통신부분으로 편입될 가능성이 있을 것 같아 관련자료 찾음
예를들면, WIFI or 5G에 적용가능할 것 같으며, 다만 Time을 분할해서 Syntesizer를 사용해야 하므로 관련부분은 복잡해질 둣하다.   

<br/>

 https://www5.cadence.com/newsletter-subscription-msa-ebook-rfmw-lp.html?utm_source=google&utm_medium=cpc&utm_term=fmcw&utm_campaign=RF_2021&utm_source=adwords&utm_medium=ppc&hsa_acc=1270110830&hsa_cam=12316095010&hsa_grp=118067585256&hsa_ad=497957189478&hsa_src=g&hsa_tgt=kwd-874051436855&hsa_kw=fmcw&hsa_mt=e&hsa_net=adwords&hsa_ver=3&gclid=CjwKCAjw_b6WBhAQEiwAp4HyIMJ1D7q-PRaTvqNXVGevb5l4NTslvmg8av64Gykcn06Z1Pp_CqX67xoCSagQAvD_BwE
  
<br/>
<br/>
