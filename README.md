# SEI TESTNET | KURULUM REHBERİ | INSTALL GUIDE
![first](https://cdn.discordapp.com/attachments/987875932129886231/987875966070161458/seicover.jpg)

# İLK KURULUM | FIRST INSTALLATION

## İşletim Sistemi / Operating System 

Linux Ubuntu 20.04

## Sistem Gereksinimleri / System Requirements

|    Bellek/Ram   |       İşlemci/Cpu      |      Disk      |   Network/Ağ           |
|-------------|----------------|----------------|----------------|
|     4GB     |   Quad-Core    |     250GB      |  1Gbps/100Mbps |

## Sunucu Kurulumu | Server Installation

### [TR]
Sunucunuza bu komutları sırasıyla girip kurulama başlayın.

### [EN]
Enter these commands on your server in order and start the installation.

`sudo su`
 
`cd`
  
`apt install screen -y`
 
`screen -S node`

`wget -q -O sei-install-lalilax.sh https://raw.githubusercontent.com/lalilax/sei-test-net-kurulum/main/sei-install-lalilax.sh && chmod +x sei-install-lalilax.sh && sudo su -c "./sei-install-lalilax.sh"`

![two](https://cdn.discordapp.com/attachments/987875932129886231/988094872080756797/unknown.png)

### [TR]
Otomatik kurulum node adı soracak oraya node adınızı girin. (Not: Node adınızı mutlaka bir yere not ediniz.)

### [EN]
Automatic installation will ask for a node name, enter your node name there. (Note: Be sure to write down your node name.)

![three](https://cdn.discordapp.com/attachments/987875932129886231/988095898074611812/unknown.png)

### [TR]
Kurulum tamamlandıktan sonra sunucunuz blok tarıyor mu diye kontrol etmelisiniz. Alttaki komutu yazarak loglarınızı izleyebilirsiniz.

### [EN]
After the installation is complete, you should check if your server is scanning blocks. You can monitor your logs by typing the command below.

`journalctl -fu seid -o cat `

### [TR]
Eğer üstteki kodu yazdığınızda ekranda hiç bir şey çıkmıyorsa alttaki kodları sırasıyla tek tek yazınız. 

### [EN]
If nothing appears on the screen when you type the code above, write the codes below one by one.

`systemctl restart systemd-journald `  
`journalctl -fu seid -o cat `  

![4](https://cdn.discordapp.com/attachments/987875932129886231/988098955302801531/111111.png)

### [TR]
Eğer bu şekilde blok tarama kısmında hata alıyorsanız bir süre beklemeniz gerekmekte peer listesi eşlemesi biraz zaman alabiliyor 5-15 dakika arası

### [EN]
If you get an error in the block scanning part in this way, you need to wait for a while, peer list matching may take some time, between 5-15 minutes.

![5](https://cdn.discordapp.com/attachments/987875932129886231/988098954975666216/22222.png)

### [TR]
Bir süre sonra loglarınız yukarıdaki resim gibi olacaktır yani bloklarınızı taramaya başlayacaktır. Yukarıda örnek bir fotoğraf ekledim kırmızı alan içine aldığım yer height yazan kısmın yanındaki rakam taradığınız blok sayısını gösterir 153.000 blok sayısına gelene kadar bir süre beklemeniz gerekmektedir.

153 bin blok taradıktan sonra bir hata alacaksınız bu hatayı aldıktan sonra sei networkün yeni sürümünü kurup blok taramaya devam etmeniz gerekiyor.
CTRL tuşuna basılı tutarak C tuşuna bastığınızda konsoldan çıkış yapabilirsiniz

### [EN]
After a while, your logs will be like the picture above, that is, it will start scanning your blocks. I added a sample photo above. The number next to the part that says height, where I put it in the red area, shows the number of blocks you have scanned. You have to wait for a while until the number of blocks is 153,000.

After scanning 153 thousand blocks, you will receive an error. After receiving this error, you need to install the new version of sei network and continue block scanning.
You can exit the console by holding down the CTRL key and pressing the C key.

![6](https://cdn.discordapp.com/attachments/987875932129886231/988240264571269190/unknown.png)

### [TR]
153 bin blok taradığınızda bu exit hatasını almanız gerekiyor burdan sonra klavyenizdeki CTRL tuşuna basılı tutup C harfine basmanız ve log ekranından çıkış yapmanız gerekiyor. Altta bulunan 1.0.3 güncellemesi başlığındaki yönergeleri takip edin ve sei versiyonunuzu güncelleyin
 
### [EN]
When you scan 153 thousand blocks, you need to get this exit error, then you need to hold down the CTRL key on your keyboard and press the letter C and exit the log screen. Follow the instructions in the 1.0.3 update heading below and update your sei version

## SURUM GUNCELLEMESI 1.0.3 | SEI VERSION UPDATE 1.0.3

### [TR]
Alttaki komut güncelleme scriptini başlatır.

### [EN]
The below command starts the update script.

`wget -q -O sei-install-lalilax1.0.3.sh https://raw.githubusercontent.com/lalilax/sei-test-net-kurulum/main/sei-install-lalilax1.0.3.sh && chmod +x sei-install-lalilax1.0.3.sh && sudo su -c "./sei-install-lalilax1.0.3.sh"`

![6](https://cdn.discordapp.com/attachments/987875932129886231/988245245424697354/seee.png)

![7](https://cdn.discordapp.com/attachments/987875932129886231/988241060931199026/unknown.png)

### [TR]
Bu çıktıyı aldığınızda sürüm güncellemesi bitmiş demektir. Logları görmek için altta yazan komutu yazınız.

### [EN]
When you get this printout, the version update is finished. Type the command below to see the logs.

`journalctl -fu seid -o cat `

![4](https://cdn.discordapp.com/attachments/987875932129886231/988098955302801531/111111.png)

### [TR]
Eğer bu şekilde blok tarama kısmında hata alıyorsanız bir süre beklemeniz gerekmekte peer listesi eşlemesi biraz zaman alabiliyor 5-15 dakika arası

### [EN]
If you get an error in the block scanning part in this way, you need to wait for a while, peer list matching may take some time, between 5-15 minutes.

![8](https://cdn.discordapp.com/attachments/987875932129886231/988247189895643146/000.png)

### [TR]
Bir süre sonra loglarınız yukarıdaki resim gibi olacaktır yani bloklarınızı taramaya devam edecektir. 150 binden 681 bin sayısına gelene kadar beklemeniz gerekmektedir. 681 binden sonra 1.0.4 sürümünü yüklemek için altta bulunan başlığı takip ediniz.

### [EN]
After a while, your logs will be like the picture above, so it will continue to scan your blocks. You have to wait until you reach the number from 150 thousand to 681 thousand. Follow the title below to install version 1.0.4 after 681 thousand.

## SURUM GUNCELLEMESI 1.0.4 | SEI VERSION UPDATE 1.0.4

![8](https://cdn.discordapp.com/attachments/988475852310327336/989553007035293736/unknown.png)

### [TR]
Alttaki komut güncelleme scriptini başlatır.

### [EN]
The below command starts the update script.

`wget -q -O lalilax104.sh https://raw.githubusercontent.com/lalilax/sei-1.0.4-update/main/lalilax104.sh && chmod +x lalilax104.sh && sudo /bin/bash lalilax104.sh`

![8](https://cdn.discordapp.com/attachments/985345620220977212/989666408369651822/unknown.png)

### [TR]
Bir süre sonra loglarınız yukarıdaki resim gibi olacaktır yani bloklarınızı taramaya devam edecektir. 681 binden güncel blok sayısına gelene kadar beklemeniz gerekmektedir. Bu işlem biraz zaman alabilir güncel blok sayısına gelip gelmediğini aşşağıdaki komut ile kontrol edebilirsiniz.

### [EN]
After a while, your logs will be like the picture above, so it will continue to scan your blocks. You have to wait until you reach the current block number from 681 thousand. This process may take some time, you can check whether the current block number is reached with the command below.

`seid status 2>&1 | jq .SyncInfo`

![9](https://cdn.discordapp.com/attachments/987875932129886231/988493822377996308/9950xx.png)

### [TR]
Üstteki işaretli alanda mevcut blok sayınızı görebilirsiniz.  
Aktif blok sayısına gelene kadar beklemeniz gerekmektedir.  
Aktif blok sayısını öğrenmek için https://sei.explorers.guru/ adresine girip bakabilirsiniz. (Alttaki fotoğrafta blok sayısının yazdığı yeri işaretledim)
Alttaki işaretli alan "true" olarak gözüküyorsa beklemeniz gerekiyor. Çıktı ne zaman "false" olursa o zaman cüzdan açma işlemine geçebilirsiniz. 

### [EN]
You can see your current block number in the marked area above.  
You have to wait until you reach the number of active blocks.  
To find out the number of active blocks, you can go to https://sei.explorers.guru/ and have a look. (I marked the place where the number of blocks is written in the photo below)  
If the marked field at the bottom shows as "true", you need to wait. Whenever the output is "false" then you can proceed to the wallet opening process.  

![sei](https://cdn.discordapp.com/attachments/987875932129886231/988495931576029235/999.png)  

# Validatör Olma Rehberi | Guide to becoming a validator
## Cüzdan Oluşturma | Creating a Wallet

### [TR]
Cüzdan oluşturmak için alttaki komutu kullanın. walletname yazan kısmı silip kendi cüzdan adınızı yazın. Ardından sizden şifre isteyecek en az 8 haneli olacak şekilde bir şifre giriniz. (Önemli not : Şifre girerken yazıyor gibi gözükmez boşluk görünür ama yazar bu güvenlik amaçlıdır.) ardından şifreyi tekrar girmenizi isteyecek bir daha giriyorsunuz.

### [EN]
Use the command below to create a wallet. Delete the part that says walletname and write your own wallet name. Then enter a password of at least 8 digits that will ask you for a password. (Important note: While entering the password, it does not appear to be typing, a space appears, but the author is for security purposes.) Then you will be asked to re-enter the password.

`seid keys add walletname`

![10](https://cdn.discordapp.com/attachments/987875932129886231/988254875169202186/unknown.png)

### [TR]
Eğer böyle bir çıktı aldıysanız. Cüzdanınızı oluşturdunuz demektir.(Önemli Not: Bilgilerinizi mutlaka bir yere kayıt ediniz.)

### [EN]
If you have an output like this. It means you have created your wallet. (Important Note: Be sure to save your information somewhere.)

## Faucet botunu kullanarak cüzdanımıza token eklemek  | Adding tokens to our wallet using the Faucet bot

![10](https://cdn.discordapp.com/attachments/987875932129886231/988254875169202186/unknown.png)

### [TR]
1- Cüzdan bilgilerimizde address kısmındaki sei adresimizi kopyalıyoruz.  
2- SEI NETWORK resmi discord sunucusuna giriş yapıyoruz. (https://discord.gg/bzJxPskFMz)  
3- Discorda giriş yaptıktan sonra #testnet-faucet kanalına geliyoruz  
4- Kanala şu şekilde mesaj gönderiyoruz !faucet sei-adresimiz  

### [EN]
1- We copy our sei address in the address section of our wallet information.  
2- Login to SEI NETWORK official discord server. (https://discord.gg/bzJxPskFMz)  
3- After logging in to Discord, we come to the #testnet-faucet channel  
4- Sending a message to the channel like this !faucet sei-address  

![11](https://cdn.discordapp.com/attachments/987875932129886231/988258416831127562/unknown.png)  
![12](https://cdn.discordapp.com/attachments/987875932129886231/988258601191755816/unknown.png)  
![13](https://cdn.discordapp.com/attachments/987875932129886231/988258974866485268/unknown.png)  

### [TR]
Komutu gönderdikten sonra bu şekilde bot size bu şekilde cevap verirse cüzdanımıza token almış oluyoruz.

### [EN]
If the bot responds to you in this way after sending the command, we get tokens in our wallet.

## Validatör Olma Komutu | Command to Become a Validator

### [TR]
Validatör olma komutunu kolay olması açısından tek satır tek satır kopyalayarak sunucunuza yapıştırabilirsiniz.
Komut içersinde özelleştirmeniz gereken alanlar alttakilerdir birisi cüzdan adı biri node adıdır.  
- --moniker=nodename  
- --from=walletname
  
Bunları değiştirdikten sonra tüm komutu sunucuya yapıştırıp enterlayın  
Sizden şifre isteyecektir. Cüzdan oluştururken girdiğiniz şifreyi kullanmanız gerekmektedir.  
(Önemli not : Şifre girerken yazıyor gibi gözükmez boşluk görünür ama yazar bu güvenlik amaçlıdır.)

### [EN]
Copy and paste commands line by line
The following are the fields you need to customize in the command, one is the wallet name and the other is the node name.  
- --moniker=nodename  
- --from=walletname  
  
After changing them, paste the whole command into the server and enter  
It will ask you for a password. You must use the password you entered when creating the wallet.  
(Important note: While entering the password, it does not appear to be typing, a space appears, but the author is for security purposes.)

`PUBKEY=$(seid tendermint show-validator)`  
`seid tx staking create-validator \`  
`--amount=980000usei \`  
`--fees=5000usei \`  
`--gas=300000 \`  
`--pubkey=$PUBKEY \`  
`--moniker=nodename \`  
`--chain-id=sei-testnet-2 \`  
`--from=walletname \`  
`--commission-rate="0.10" \`  
`--commission-max-rate="0.20" \`  
`--commission-max-change-rate="0.01" \`  
`--min-self-delegation="1" \`  
`--yes`

### [TR]
Komutu gönderdikten sonra sizden şifre girmenizi isteyecek cüzdan oluştururken girdiğiniz şifreyi kullanmanız gerekiyor.  
(Önemli not : Şifre girerken yazıyor gibi gözükmez boşluk görünür ama yazar bu güvenlik amaçlıdır.)

### [EN]
After sending the command, you need to use the password you entered when creating the wallet that will ask you to enter a password.  
(Important note: While entering the password, it does not appear to be typing, a space appears, but the author is for security purposes.)

![pass](https://cdn.discordapp.com/attachments/987875932129886231/988499825181982770/unknown.png)

### [TR]
Alttaki gibi bir çıktı aldıysanız işlem başarıyla gerçekleştirilmiştir.

### [EN]
If you have an output like the one below, the operation has been successfully completed.

![hash](https://cdn.discordapp.com/attachments/987875932129886231/988501550831906856/asdasd.png)

## Validatör olduğunu kontrol etme | Checking you have a validator


### [TR]
https://sei.explorers.guru/ Sitesine giriş yapınız  
Altda bulunan resimleri takip ederek kendinizi sitede arayabilirsiniz.  
- Önemli Not: Sitede gözüken adınız cüzdan oluşturma komutunda girdiğiniz moniker komutunun yanındaki node adıdır.

### [EN]
Login to https://sei.explorers.guru/  
You can search for yourself on the site by following the pictures below.
- Important Note: Your name that appears on the site is the node name next to the moniker command you entered in the wallet creation command.

![site1](https://cdn.discordapp.com/attachments/987875932129886231/988503942256279622/11.png)
![site2](https://cdn.discordapp.com/attachments/987875932129886231/988503942596014090/22.png)
![site3](https://cdn.discordapp.com/attachments/987875932129886231/988503941983662080/33.png)

### [TR]
Adınızı görüyorsanız validatör olmuşsunuzdur.

### [EN]
If you see your name, you are a validator.

