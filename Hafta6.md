

# Spiderfoot

─(ceren㉿ceren)-[~]

└─$ spiderfoot -l 192.168.189.128:80 


# Nmap

1.soru – Nmap toolu kullanarak 192.168.1.1 ip adresli hedefe TCP Syn Scan paketi göndermeyi sağlayan komut blogunu yazınmız.

Cevap:
nmap -sS -v 192.168.1.1

(-v : vergos(daha acıklayıcı yaz demek))



2.soru – nmap toolu kullanarak www.google.com.tr adresinde bulunan UDP portlarından en sık kullanılan 10 portunu ‘udplistesi.xml’ dökümanına kaydetmeyi sağlayan komut blogunu yazın.

Cevap :
┌──(ceren㉿ceren)-[~]

  └─$ nmap -sU -top-ports 10 -oX  udplistesi.xml www.google.com.tr



3.soru – Nmap toolu kullanarak 192.168.1.1 ip adresindeki açık portlarda çalışan hizmetlerin sürüm bilgilerini sağlayan komut bloğunu yazın. 

Cevap :
┌──(ceren㉿ceren)-[~]

└─$ nmap -sV -v 192.168.1.1    



4.soru – Nmap toolu kullanarak 192.168.1.1 ip adresindeki http hizmetiyle ilgili bilgi toplamak için kullanılan komut blogunu yazınız. 

Cevap:
┌──(ceren㉿ceren)-[~]

└─$ nmap --script=http-title 192.168.1.1



5.soru- Nmap toolu kullanarak www.gelisim.edu.tr adresinin iletişim sistemini tespit etmeyi ve bulunan sonuçları ‘gelisim.txt’dökümanına kaydetmeyi sağlayan komut blogunu yazın.

Cevap:
┌──(ceren㉿ceren)-[~]

└─$ nmap -O www.gelisim.edu.tr -oN gelisim.txt



6.soru - Nmap toolu kullanarak 192.168.1.1 ip adresine TCK ACK ping paketi göndermeyi ve güvenlik duvarının durumunu görüntülemeyi sağlayan kod blogunu yazın. 

Cevap:
┌──(ceren㉿ceren)-[~]

└─$ nmap -PA -sA 192.168.1.1    



7.soru- Nmap toolu kullanarak scanme.nmap.org adresinde http-title ve http-headers scriptlerini çalıştırmayı sağlayan komut blogunu yazınız. 

Cevap:
┌──(ceren㉿ceren)-[~]

└─$ nmap --script=http-title,http-headers scanme.nmap.org



8.soru- Nmap toolu kullanarak scanme.nmap.org sistemindeki bilinen güvenlik açıklarını tarayan komut blogunu yazınız. 

Cevap:
┌──(ceren㉿ceren)-[~]

└─$ nmap --script=vuln 192.168.1.1

 (vuln:tümünü tarar)

 

9.soru- Nmap toolu kullanarak 192.168.1.1 ip adresindeki bilinen güvenlik açıklarını tespit etmek için kullanılan komut blogunu yazınız. 

Cevap:
┌──(ceren㉿ceren)-[~]

└─$ nmap -oN output.txt 192.168.1.1



10.soru- Nmap toolu kullanarak 192.168.1.1 ip adresine yapılan tarama sonuçlarını ‘output.txt’dosyasına kaydetmek için kullanılan komut blogunu yazınız. 

Cevap:
┌──(ceren㉿ceren)-[~]

└─$ nmap --script=ftp-anon 192.168.1.1



11.soru - Nmap toolu kullanarak 192.168.1.1 ip adresindeki FTP hizmetiyle ilgili bilgi toplamak için kullanılan komut blogunu yazınız. 

Cevap:
┌──(ceren㉿ceren)-[~]

└─$ nmap -sN traceroute 192.168.1.1   


(80 ve 443 portları açık kalmalı)


![image](https://github.com/user-attachments/assets/b0f897ad-3e3c-49be-bbf6-5e5cd0bd3417)
