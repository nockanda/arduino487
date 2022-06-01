# arduino487
https://youtu.be/DxoVpS_I_-E

ESP8266 딥슬립(deep sleep)하는 방법과 소모전류 측정해보기!(deep sleep + mqtt 구현하기)
이번편은 ESP보드의 딥슬립에 대해서 알아보도록 하자!
사물인터넷(IoT)을 위해서는 보드를 인터넷에 연결해야하고 언제 어디서든지 제어가 되도록 해야한다!

언제 어디서든지가 포인트인데 외부에서 보드를 제어하기 위해서는 별다른 전원이 없으므로 베터리를 사용하는게 일반적이다!

베터리를 사용하게되면 사용시간의 개념이 갑자기 생기므로 최대한 소모전류를 줄여야할 필요성이 있다!

일단 ESP8266보드를 냅다 활용하게되면 생각보다 전류소모가 많다고 한다!(얼마 정도인지 측정해보아야 한다)

이때 딥슬립을 걸게되면 보드의 소모전류가 아주 극적으로 줄어든다고 한다!(이것도 해보아야한다)

어떻게 딥슬립을 걸 수 있고, 어떻게 깨울 수 있는지 알아보도록 하자!

녹칸다가 지금껏 사용하던 ESP8266보드인 wemos d1r1보드는 딥슬립이 가능하기는 하지만 wakeup이 안되는 보드라 사용이 안된다!

그래서 실험을 위한 보드 3종을 아래와 같이 준비했다!<BR>
1.wemos D1 mini CH340<BR>
2.wemos D1 mini V3.0.0<BR>
3.wemos D1 Pro 4M<BR>

위에서 아래 순서로 가격이 비싸다!
그리고 보드마다 소모전류가 다르고 딥슬립이 제대로 되는것도 있고 아닌것도 있다고 한다!(테스트 해보아야한다)

아래와 같은 기본 코드를 구현하고 딥슬립일때와 아닐때의 소모전류를 보드마다 측정해보자!<BR>
1.단순프린트<BR>
2.웹서버로 작동중일때<BR>
3.ESPNOW를 사용할때<BR>
4.MQTT를 사용할때<BR>

다음으로 유저에 명령에 의해 딥슬립이 걸리고 풀리는 예제를 몇가지 구현해보도록 하자!

1.wemos d1 mini보드에 deepsleep을 설정하는 기본 예시를 보이시오!<BR>
2.보드 5종을 이용해서 기본예제 7개의 소모전류를 각각 측정하시오!<BR>
3.버튼 1개를 연결해서 내가 원하는 타이밍에 딥슬립을 걸 수 있도록 하시오!<BR>
4.보드에 온습도센서가 달려있고 10초에한번마다 측정한다고 할때 시리얼모니터에 출력하고 나머지 시간은 딥슬립을 거시오!<BR>
5.온도와 습도값을 MQTT로 10초한번 전송하고 딥슬립하기!<BR>
  
(Machine translation)<BR>
ESP8266 How to do deep sleep and measure current consumption! (implementing deep sleep + mqtt)
In this episode, let's learn about the deep sleep of the ESP board!
For the Internet of Things (IoT), you need to connect the board to the Internet and have it be controlled anytime, anywhere!

The point is anytime, anywhere, but to control the board from the outside, there is no special power source, so it is common to use batteries!

When the battery is used, the concept of usage time suddenly arises, so there is a need to reduce the current consumption as much as possible!

Once the ESP8266 board is used, it is said that it consumes more current than expected! (You have to measure how much)

It is said that if deep sleep is applied at this time, the current consumption of the board will be reduced very dramatically! (You should try this too)

Let's learn how to put deep sleep and wake up!

The wemos d1r1 board, the ESP8266 board used by Nokanda so far, is capable of deep sleep, but cannot be used because it cannot wakeup!

So, I prepared three boards for the experiment as follows!<BR>
1.wemos D1 mini CH340<BR>
2.wemos D1 mini V3.0.0<BR>
3.wemos D1 Pro 4M<BR>

From top to bottom, the prices are expensive!
And it is said that the current consumption is different for each board, and some have good deep sleep and some don't! (You have to test it)

Let's implement the basic code below and measure the current consumption during deep sleep and not for each board!<BR>
1. Simple print<BR>
2. When operating as a web server<BR>
3. When using ESPNOW<BR>
4. When using MQTT<BR>

Next, let's implement some examples in which deep sleep is applied and released by the user's command!

1. Show a basic example of setting up deepsleep on wemos d1 mini board!<BR>
2. Measure the current consumption of each of the 7 basic examples using 5 types of boards!<BR>
3. Connect 1 button so that I can put a deep sleep at the timing I want!<BR>
4. When the board has a temperature and humidity sensor and it measures every 10 seconds, print it out on the serial monitor and do deep sleep for the rest of the time!<BR>
5. Send the temperature and humidity values ​​to MQTT once for 10 seconds and go deep sleep!<BR>
