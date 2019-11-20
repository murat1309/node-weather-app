1.) heroku cli => download win64
2.) setup your pc
3.) restart webstorm and open terminal , sure installed  => heroku -v
4.) run this  => heroku login
5.) and press the space , go to login page and login. Return command line.


-------------GİT-----------
1.) Setup git and install => https://git-scm.com/
2.) check git version on cmd => git --version
3.) go to project folder and run => git init
4.) git status ile tracked (git kontrol etsin ,,  izin verildi.) ve untracked(git ellemesin hiçbizaman.)you can see.
5.) .gitignore dosyası oluştururuz ve içerisine gitin karışmaması gereken dosyaları ekleyebiliriz.
6.) gite takip etmesi için izin verebilmemiz için çalıştır => git add src/
7.) git status yaptığında ise untracked yani gitin izlemediği dosyalar arasında ,, src/ 'nin kalktığını görürsün,,  yani gite bu dosyayı izlemesi için izin verdiğimizi anlamalsıın.' 
8.) git add . => çalıştırarak tüm dosyaları gite açabilirsin. ki böyle yap tek tek uğraşma. sonra gizlemek istediklerini .gitignore'a yazarsın.
9.) git commit -m "init commit" 
        (    doğrulama isterse = > 
             1. git config --global user.name "murat1309"
             2. git config --global user.email "muratcan.gokyokus@hotmail.com")
             
10.) bi değişiklik yaptığında => git status ile kontrol edebilrisin orada çıkar.
11.) git add . => diyerek değişiklikleri stage all filesyapmış olursun. ve commitlemeye hazır hale gelir.
12.) git commit -m "yorum..." 
             
