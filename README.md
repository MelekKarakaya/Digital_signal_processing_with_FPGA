# FPGA İLE DİJİTAL SİNYAL ÜRETECEİ 
Bu çalışmada amaç, dijital sinyallerin kullandığı osiloskop devrelerinin genelinde kullanılmak üzere değişken frekanslı ve hassasiyeti yüksek olan çeşitli 
formlarda sinyal üreten bir sayısal sinyal üreteci tasarlamaktır. Çalışmada  Nexys DDR4 kartını kullanılarak fpga ile üretilen dijital sinyallerin AD5628 DAC dönüştürücü kartını kullanarak  analog sinyallere dönüştürülerek osiloskopta görüntülenecektir. Bu temel amaç yanında ulaşılmak istenen  hedefler listelenmiştir;  
1. Sistemin frekans çözünürlüğü 1 hz altında olmasını ve değiştirilebilir frekans ayarı oluşturmak.  
2. Her bir örneğin çözünürlüğünü 12 bit olacak şekilde ayarlamak.  
3. Sinüs, kare, üçgen, testere gibi değitirilebilir dalga formları elde etmek.

Sistem Yapısı 
Bu çalışmada, VHDL (VHSIC Hardware Description Language) kullanılarak bir FPGA (Field Programmable Gate Array) tabanlı bir sinüs dalgası üreteci tasarlanmıştır. Aşağıda Şekil 3.7.1 'de sistemin genel şeması verilmiştir.  Sistem ana frekansı clk_in saatinin frekans bölücü yapısı ile daha düşük frekanslı s_clk_out saati oluşturulmuştur. Bu saat sistemin sayici bloğunun referansı olmuştur. Böylece adim ve freq_word sinyallleri ile istenilen frekans ayarlanmaktadır. Daha sonra eklenilen katsayı dosyaları ile sinüs, üçgen, testere ve kare sinyalleri oluşturulup sinyallere atanmaktadır. Seçme biti yapısı ile de istenilen sinyal çıkışa aktarılabilmektedir. Son olarak DAC modülü kullanılarak dijital sinyal, analoga çevrilerel osiloskopta görntülenebilir hale getirilmektedir.


![image](https://github.com/MelekKarakaya/Digital_signal_processing_with_FPGA/assets/78067331/0e9d61c6-68e4-4c0e-af76-49164dd71c5d)


![image](https://github.com/MelekKarakaya/Digital_signal_processing_with_FPGA/assets/78067331/0e06718c-c27f-45be-9bab-5c7e6306072f)


