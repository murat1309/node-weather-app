1.) heroku cli => download win64
2.) setup your pc
3.) restart webstorm and open terminal , sure installed  => heroku -v
4.) run this  => heroku login
5.) and press the space , go to login page and login. Return command line.


-------------crete local GİT repo-----------
1.) Setup git and install => https://git-scm.com/
2.) check git version on cmd => git --version
3.) go to project folder and run => git init
4.) git status ile tracked (git kontrol etsin ,,  izin verildi.) ve untracked(git ellemesin hiçbizaman.)you can see.
5.) .gitignore dosyası oluştururuz ve içerisine gitin karışmaması gereken dosyaları ekleyebiliriz. mesela (node_modules/)
6.) gite takip etmesi için izin verebilmemiz için çalıştır => git add src/
7.) git status yaptığında ise untracked yani gitin izlemediği dosyalar arasında ,, src/ 'nin kalktığını görürsün,,  yani gite bu dosyayı izlemesi için izin verdiğimizi anlamalsıın.' 
8.) git add . => çalıştırarak tüm dosyaları gite açabilirsin. ki böyle yap tek tek uğraşma. sonra gizlemek istediklerini .gitignore'a yazarsın.
9.) git commit -m "init commit" 
        (    doğrulama isterse = > 
             1. git config --global user.name "murat1309"
             2. git config --global user.email "muratcan.gokyokus@hotmail.com")
             
10.) bi değişiklik yaptığında => git status ile kontrol edebilrisin orada çıkar.
11.) git add . => diyerek değişiklikleri stage all files (staging area'ya taşımış) olursun. ve commitlemeye hazır hale gelir.
12.) git commit -m "yorum..." 
             
           -----------GENEL OLARAK-------
           1.) git init
           2.) git status
           3.) git add .
           4.) git status
           5.) git commit -m "comment..."

--------------SSH and git push---------------

1.) OPEN GİT.BASH cmd
2.) ssh-keygen -t rsa -b 4096 -C "muratcan.gokyokus@hotmail.com"
3.) id_rsa (private olan) ve id_rsa.pub (public olan) dosyalarını C:/users/murat/.ssh içerisine oluşturacak ve..
4.) ls -a -l ~/.ssh ile bu dosyaları görebileceğim.
5.) eval $(ssh-agent -s) => bu komut  ile ssh çalıştırdın diyebiliriz.
6.) ssh-add ~/.ssh/id_rsa => id_rsa ile etkileşimi güvenikli sağlayabiliriz. Ve ssh anahtarlarımız devrede.
             Artık github ve herokuya açabiliriz projemizi
7.) github hesabından new repository oluştur.

8.) bizim zaten bi repomuz var localimizde sadece gite göndercez o yüzden karşımıza çıkan sitedeki altta yazan maddedeyi 2 komutu çalıştırmamız yeterli olucak.
8.1.) git remote add origin https://github.com/murat1309/node-weather-app.git  (bu komutla iletişim kanalını kuruyoruz.)
                                    github kullanıcıadı/git repository adı
                                    
8.1.1) Aşağıdaki komutu çalıştıramazsın hata verir. iilk önce ssh konfigurasyonunu githubda yapıcaz.
-> sağ üstten settings -> SSH and GPG keys ->new SSh key ->  title kafana göre ver key kısmı için ise
    -> git bash'de cat ~/.ssh/id_rsa.pub  => komutunu çalıştır ve karşına çıkan keyi ssh-rsa ve sonundaki mailin de dahil olmak üzere kopyala keye yapıştır.
    
8.1.2) git bashden yine test için =>  ssh -T git@github.com => bunu yazarız bağlantıda bi sıkıntı olmadığını görürüz.                                       
8.2.)git push -u origin master      ve kod gider.    


 (bunu git bash'i proje directory'inde yapmalısın. eğer görmezse yine aynı yerde proje directory'inde,
               =>  git remote add origin https://github.com/murat1309/node-weather-app.git
  sonra tekrar =>  git push -u origin master  yapmayı deneyebilrisin.)                         



----------------------------------HEROKU DEPLOY---------------------
webstorm terminalden devam edebiliriz.
1.) Project directory'inde heroku ile ssh keymizi buluşturuyoruz.
 => heroku keys:add => dediğinde ssh keyini heroku hesabına ekleyip isteyip istemediğini sorar. Yes
 
2.) project directoy'inde heroku create murat-weather-application
(heroku sunucularında yeni bi uygulama oluşturuldu ve biz 2 url verdi)

3.) Heroku'ya uygulamamızı nerden başlatıcağını bilmiyor ona bazı şeyleri söylemeliyiz.
3.1.) ona uygulmaayı başlatabilmesi için app.js'i tanıtmalıyız. Bunuda package.json'da start scripti'nde belirtiyoruz. =>  "start": "node src/app.js",
3.2.) sonrasında app.js'de port ayarlaması yapmamız gerek => const port = process.env.PORT || 3000; => sayfanın en sonunda 3000 yazan port yerinede bu port variable'ıı veriyoruz tabi.
3.3.) biz hava durumunu almak için fetch ile local:3000'e istek atıyorduk ama artık heroku'ya atmamız gerekicek mantıken.fetch('/weather?address='  olarak bırakacağız.

4.)yaptığımız değişiklikleri bi pushlayalım.
 4.1) git status ile gördüm değişikliklerimi
 4.2) git add . ile staging area yaptım.
 3.3) git commit -m "Setup for Heroku"
 3.4) git push
 
5.) git remote yaparsak şimdi hem origin hemde heroku konsolda grmüş olucaz. Yani artık origine pushladığımız gibi heroku'yada pushlayabiliriz.
6.) git push heroku master (dependency'leri kurmaya ve uygulamayı ayağa kaldırmaya başladı bile. Ve bize bir url verdi.

        Bu az önce bize verdiği 2 url ile yanı olan url'ler. Artık o url'i açtığımızda uygulamamız çalışır halde karşımıza çıkacaktır.)
 
 -----------------------------------UYGULAMAYA YENI GUNCELLEME ÇIKALIM----------------------
 1.) değişiklikleri yaptın.
 2.) git status ile kontrol ettin.
 3.) git add .
 4.) 
 
 
                                                     
                                                    

