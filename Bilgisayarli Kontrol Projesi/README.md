<h1 style="border-bottom: 2px solid red; text-align: center;">Çizgi Takip Edebilen Robot</h1>

## Kullanılan Parçalar
1. Arduino Uno R3
2. L298 Motor Sürücüsü
3. Hazır Araç Platformu
4. Pil
5. Motor
6. Çizgi Takip Sensörü
7. Dönüştürücü
8. Jumper Kablo

## Devre Şeması ve Çalışma Düzeni
- Arduino Uno: Projeyin kontrolünü sağlar ve sensörlerden gelen verileri işler.

- L298 Motor Sürücüsü: Motorlara güç sağlar ve yönlendirme işlemlerini gerçekleştirir.

- Sensörler: Zemin üzerindeki çizgiyi algılar ve Arduino'ya bu bilgiyi iletir.

- Motorlar: Arduino ve motor sürücü aracılığıyla kontrol edilir ve çizgiyi takip etmek için hareket eder.
  
<div style="text-align: center;">
  <img src="https://github.com/tahsinemreozturk/LineFollowingRobot/assets/125802474/cef4a494-a9f1-40da-ae56-f2fa0c0ffab0" alt="Devre Şeması" width="70%" />
</div>



## Çizgiyi Takip Etme Olayı
Çizgi takibi için kullanılan sensör sayesinde toplanan verilere göre bir dizi işlem uygulanır. 
Projede 3 tane kontrast farkını algılayan ve farka göre 0 veya 1 değeri dönderen sensör bulunmaktadır. Bu sensörlerden gelen 
0 ve 1 verilerine göre robotun hangi tarafında çizginin olduğunu anlayabiliyoruz. Bu 3 sensör sağ-sol-orta olacak şekilde tanımlanır.
Örneğin sağ sensör eğer bir çizgi tespit ederse 1 değerini dönderir. Gelen bu 1 değeri işlenemden önce diğer sensörlerden gelen değerlerde kontrol edilir.
Eğer diğer sensörlerden de 0 değeri geliyorsa, çizginin sağ tarafta olduğuna emin oluruz. Daha sonra sağ tarafta kalan çizgiyi takip edebilmek için motorlara hareket değişikliği yapmasını söyleriz.
Robotun ilerleyiş yönündeki sağ tarafında çizgi varsa o çizgiyi takip edebilmesi için saü motorun durması/hızının yavaşlaması ve sol motorun harekete devam etmesi/hızlanması gerekir.
Bu şekilde orta sensörden 1 değeri gelinceye yani çizginin tam üzerinde olduğunu anlayıncaya kadar devam eder ve tekrar çizgiden çıkması durumunda bu döngü devam eder. 
<div style="text-align:center">
  <img src="https://github.com/tahsinemreozturk/LineFollowingRobot/assets/125802474/14b95a05-7452-4df1-9090-c4df1ea56362" alt="Çizgiyi Takip Etme Olayı" width="50%" />
</div>


## Projenin Fotoğrafları

<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 10px;">
  <div style="flex: 1; min-width: 200px; max-width: 200px;">
    <img src="https://github.com/tahsinemreozturk/LineFollowingRobot/assets/125802474/c2997760-1551-4c3e-9f39-52226a579408" alt="Fotoğraf 1" width="100%" />
  </div>
  <div style="flex: 1; min-width: 200px; max-width: 200px;">
    <img src="https://github.com/tahsinemreozturk/LineFollowingRobot/assets/125802474/90c41017-bf93-4544-9118-20c5276bee84" alt="Fotoğraf 2" width="100%" />
  </div>
  <div style="flex: 1; min-width: 200px; max-width: 200px;">
    <img src="https://github.com/tahsinemreozturk/LineFollowingRobot/assets/125802474/1872ea6b-af7e-42af-a3d8-730d268f7b55" alt="Fotoğraf 3" width="100%" />
  </div>
  <div style="flex: 1; min-width: 200px; max-width: 200px;">
    <img src="https://github.com/tahsinemreozturk/LineFollowingRobot/assets/125802474/f1afd120-b0d2-40ac-9528-0d9440cd8836" alt="Fotoğraf 4" width="100%" />
  </div>
</div>


