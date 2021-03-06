
..  Copyright (C)  Peter Wentworth, Jeffrey Elkner, Allen B. Downey and Chris Meyers.
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3
    or any later version published by the Free Software Foundation;
    with Invariant Sections being Foreword, Preface, and Contributor List, no
    Front-Cover Texts, and no Back-Cover Texts.  A copy of the license is
    included in the section entitled "GNU Free Documentation License".

    
|    
    
Programlama Yolu
======================
Bu kitabın amacı size bilgisayar bilimcisi gibi düşünmeyi öğretmektir. Bu
düşünme şekli matematiğin, mühendisliğin ve doğal bilimlerin bazı en iyi
özelliklerini birleştirir. Matematikçiler gibi, bilgisayar bilimcileri
fikirlerini ifade etmek için biçimsel dilleri kullanırlar. Onlar mühendisler
gibi, birşeyler tasarlar, parçaları birleştirip sistem haline getirirler;
avantaj ve dezavantajlarını değerlendirirler. Onlar bilimciler gibi karmaşık
sistemlerin davranışlarını gözlemler, hipotezler oluştururlar ve
varsayımlarını sınarlar. 

       
Bir bilgisayar bilimcisi için tek ve  en önemli yetenek **problem çözmedir**.
Problem çözme, problemleri formüle edebilme, çözümler hakkında yaratıcı
düşünebilme, çözümü kesin ve doğru olarak ifade edebilme yeteniğidir. Görüleceği
üzere, programlamayı öğrenme süreci, problem çözme yeteneklerininin
uygulamasını yapmak için mükemmel bir fırsattır. Bu bölüme bu yüzden
"Programlama Yolu" adı verilmiştir.

Bir yönden yararlı bir yetenek olan proglamayı öğrenirken, diğer bir yönden de
sonuca ulaşmak için bir yol olarak kullanacaksınız. 

.. index:: programlama dilleri, taşınabilir, yüksek seviyeli dil, düşük
   seviyeli dil, derlemek, yorumlamak, PyScripter

Python programla dili
---------------------

Öğreneceğiniz progralama dili Python olacaktır. Python bir **yüksek seviyeli
dil** örneğidir; Daha önce duymuş olabileceğiniz C++, PHP, Pascal, C ve Java
yüksek seviyeli dillere örnektir.

"Yüksek seviyeli dil" ifadesinden anlamı çıkarabileceğiniz gibi,  ayrıca **yüksek
seviyeli diller** vardır, bunlar bazen "makine dili" veya "birleştirici dili
(assemble)" şeklinde isimlendirilir. Kabaca söylersek, bilgisayarlar yalnızca
düşük seviyeli dillerde yazılmış programları çalıştırabilirler. Bu yüzden,
yüksek seviyeli dillerde yazılmış programlar çalıştırılmadan önce bir işlemden
geçmelidir. Bu ek işlem biraz zaman alır, bu da yüksek seviyeli dillerin
dezavantajıdır. 

Hemen hemen bütün programlar avantajlı olmasından dolayı yüksek seviyeli
dillerde yazılır. Bu avantajlar: daha kısa sürede yazılması; daha kısa olması;
okunmasının daha kolay olması; doğru olma olasılıklarnın daha yüksek
olmasıdır. İkincil olarak, yüksek seviyeli diller **taşınabilirlik** özelliği
gösterir. Bunun anlamı, farklı bilgisayarlarda biraz değişikle veya değişiklik
yapmadan çalışabilirler. 

Python'u okuyan ve onu işleten sanal makinaya **Python Yorumlayıcısı** denir. Bunu
kullanmanın kullanmanın iki yolu vardır: *kabuk modu* ve *betik modu.* Kabuk
modunda Python kabuğuna Python cümlelerini yazıp, yorumlayıcının hemen
sonuçları göstermesi sağlanır:

.. image:: illustrations/interpreter_sshot.png
   :alt: Screen shot of interpreter

Ekranda ``>>>`` ile başlayan satırlar **Python İstemcisi**\ dir. Yorumlayıcı,
bilgi istemini komutlar için hazır olduğunu belirtmek için kullanmaktadır. Biz
``2+2`` yazdık ve yorumlayıcı yanıt olarak ``4`` dönürdü. Sonraki satırda yeni
bir istemci, bize yeni bir giriş için hazır olduğunu belirtmektedir. 

Alternatif olarak, programı bir dosya içine yazıp, yorumlayıcının dosya
içeriğini çalıştırmasını sağlıyabiliriz. Bu tip dosyaya **betik** adı
verilmektedir. Betik dosyasının diske yazdırma, yazıcıdan çıktısının
alınabilmesi gibi avantajları vardır. 

Bu kitapda **PyScripter** adlı program geliştirme ortamını kullanacağız (Bu
programı http://code.google.com/p/pyscripter adresinde bulabilirsiniz.) Daha
farklı geliştirme ortamları da vardır. Eğer siz başka birisini
kullanıyorsanız (örneğin **idle** ya da **spyderlib** , burda gösterilen
örnekleri kendi ortamınıza uyarlamak zor olmayacaktır. 

Örnek olarak, PyScripter kullanarak ``firstprogram.py`` adlı dosyayı
yaratalım. Kural olarak, Python programlarını içeren dosyalar ``.py``
uzantısıyla biter. 

Programı çalıştırmak, için PyScripter içindeki **Run** düğmesine basalım:

.. image:: illustrations/my_first_program.png
   :alt: first program screenshot
 
Çoğu program verilen bu örnekten daha ilginçtir. 

Kabuk modunda çalışmak küçük kod parçalarını sınamak için uygundur, çünkü
anında sonucu alırsınız. Bunu sanki bir problemi çözmeden önce bir kağıt
parçası üzerinde karalama yapmaya benzetebilirsiniz. Birkaç satırdan daha uzun
herşey betik içine koyulmalıdır.

.. index:: program, algoritma

Program nedir?
--------------

Program, hesaplamayı gerçekleştirmek için birbirini izleyen komutlardan
(yönergelerden) oluşan yapıdır. Hesaplama matematiksel olabilir, örneğin bir
denklem sisteminin çözülmesi veya bir polinomun köklerini bulmak gibi. Fakat
bu bir belgenin içindeki metni arama ve değiştirme veya programı derleme
(yeterince ilginç) gibi sembolik hesaplama da olabilir. 

Ayrıntılar farklı programlama dillerinde farklı gözükebilir, fakat bazı basit
komutlar her dilde gözükür:

girdi
    Klavyeden, dosyadan veya başka bir aygıttan veri alma.

çıktı
    Ekranda veriyi görüntüleme veya veriyi dosyaya veya başka bir aygıta
    gönderme.

matematik
    Toplama, çarpma gibi bazı temel matematiksel işlemleri gerçekleştirme.

koşullu yürütme
    Belirli durumları sınamak ve komutları uygun bir sıraya göre çalıştırmak.

tekrarlama
    Bazı eylemleri genellikle ufak tefek değişikliklerle tekrar tekrar
    yürütme.

İnanın veya inanmayın, var olanların hepsi bu kadardır. Şu ana kadar
kullandığınız bütün programlar, ne kadar karmaşık olursa olsun, az yada çok
yukarıda verilen benzeyen komutlardan yapılmıştır. Bu yüzden programlamayı,
büyük ve karmaşık bir görevi yukarıdaki temel komutlarla gerçekleştirebilecek
kadar basit olan küçük alt görevlere parçalama süreci olarak tanımlıyabiliriz. 

Bu size  biraz belirsiz gelebilir, ancak bu konuya **algoritmalar** hakkında
konuşurken tekrar geleceğiz. 

.. index:: Hata ayıklama, hata

Hata ayıklama (Debugging ) nedir?
---------------------------------

Programlama karmaşık bir süreçtir ve insanlar tarafından yapıldığı için
sıklıkla hatalara yol açar. Programlama hataları **bugs** (böcek,hata) adı
verilir. Bu hataları bulma ve düzeltme işlemine ise **debugging** (böcekten
arındırma) adı verilmektedir. *Bug* terimi, Thomas Edison tarafından gramafon
makinasından oluşan hata sonucu, mühendislikte küçük mühendislik
zorluklaklarını tanımlamak için kullanılmıştır. Kullanım tarihi 1889 yılına
kadar uzanmaktadır. [#bocek]_ 

Bir programda üç tür hata oluşabilir: `sözdizimsel hatalar
<http://en.wikipedia.org/wiki/Syntax_error>`__, `çalışma zamanı hataları
<http://en.wikipedia.org/wiki/Runtime_error>`__, and `anlambilimsel hatalar
<http://en.wikipedia.org/wiki/Logic_error>`__. Bu hataları daha hızlı
belirliyebilmek için aralarındaki farkları bilmek faydalıdır. 

.. [#bocek]

   Çeviren Notu (Çn): *Bug*, İngilizce'de halk arasında böcek anlamına gelmektedir. Bilgisayar
   bilimlerinde hata anlamında kullanılmaktadır. Biz türkçedeki karşılığı
   olarak *hatadan arındırma* olarak kullanacağız.  Niçin *böcekten arındırma*  anlamında
   kullanıldığını anlamak için  http://tr.wikipedia.org/wiki/Yazılım_hatas
   sayfasına bakınız. 


.. index:: sözdizimi, sözdizimsel hatalar

Sözdizimsel hatalar
-------------------

Python bir programı yalnızca sözdizimsel olarak doğru ise çalıştırabilir; aksi
halde, bu işlem başarısız olur ve bir hata mesajı verir. **Sözdizimi**
programın yapısını ve bu yapı hakkındaki kuralları kasteder. Örneğin,
Türkçe'de bir cümle büyük bir harfle başlamalı ve nokta işaretiyle sona
ermelidir. bu cümle **sözdizimi** hatası içermektedir. Bu cümle de öyle

Birçok okuyucu için, bazı sözdizimi hataları önemli değildir. Bu yüzden E.E.
Cumings'in şiirlerini bir sorun olmadan okuyabiliriz. Python ise bu kadar
affedici değildir. Programınızın herhangi bir yerinde tek bir sözdizimi hatası
olduğunda bile, Python bir hata mesajı verip çıkacaktır ve programı
çalıştırmanız mümkün olmayacaktır. Programlama kariyenizin ilk birkaç
haftasını sözdizilim hatalarınızın izini sürmekle geçireceksiniz. Deneyim
kazandıkça, daha az hata yapmaya ve bu hataları daha hızlı bulmaya
başlayacaksınız. 

.. index:: çalışma zamanı hataları, istisna, güvenli dil

Çalışma zaman hataları
----------------------

İkinci tür hata çalışma zamanı hatalarıdır; böyle bir ismin verilmesinin
nedeni program çalıştırılana kadar bu hataların ortaya çıkmamasıdır. Bu
hatalara ayrıca **istisna** adı da verilmektedir, çünkü istisnai (ve kötü) bir
kötü durumun ortaya çıktığını belirtirler. 

İlk bölümlerdeki basit programlarda çalışma zamanı hatalarıyla karşılaşmanız
düşük bir ihtimaldir. Bu yüzden bu hatalarla karşılaşılana kadar biraz zaman
geçebilir. 

.. index:: anlambilim, anlambilimsel hata

Anlambilimsel hatalar
---------------------

Üçüncü tür hata **anlambilimsel hata**\lardır. Programınızda anlambilimsel
hata var ise, programınız başarıyla çalışacaktır. Bundan kastedilen,
bilgisayar herhangi bir hata mesajı üretmiyecek, ancak doğru şeyi
yapmayacaktır. Beklenilenden farkıl bir şey yapacaktır. Siz ona ne yapmasını
söylemişseniz, o da onu yapacaktır. 

Sorun, yazdığınız program yazmak istediğiniz program değildir. Programın
anlamı (anlambilimi) hatalıdır. Anlambilim hatalarını belirlemek ustalık
ister, çünkü programın çıktısına bakarak geriye doğru yönelik çalışmanızı ve
ne yaptığını anlamaya çalışmanızı gerektirir.

.. index:: 
   single: Holmes, Sherlock
   single: Doyle, Arthur Conan
   single: Linux

Deneysel hata ayıklama
----------------------

Kazanabileceğiniz en önemli yeteneklerden biri hata ayıklamadır. Sinir bozucu
olmasına rağmen, hata ayıklama programlamının zihinsel zenginlik gerektiren,
zorlayıcı ve ilginç bir parçasıdır. 

Birkaç yönden, hata ayıklama sanki bir dedektif çalımasıdır. Bazı ipuçlarıyla
karşılaşırsınız; gördüğünüz sonuçlara size götürmüş olan süreçleri ve
olaylardan anlam çıkarmanız gerekir. 

Hata ayıklama deneysel bilim dalı gibidir. Neyin hatalı gittiğine dair bir
fikriniz oluştuğunda, programınızı değiştir ve tekrar denersiniz. Eğer sizin
hipoteziniz doğru ise, değişikliğin sonucunu tahmin edebilir ve çalışan bir
programa bir adım daha yaklaşmış olursunuz. Eğer hipoteziniz yanlış ise, yeni
bir tane hipotez üretmeniz gerekir. Sherlock Holmes'un işaret ettiği gibi "
imkansızı elediğinizde elinizde kalan şey, ne kadar olasılık dışı olsa bile
gerçek olmak zorundadır." (A. Conan Doyle, *The Sign of Four*)

Bazı kişiler için, programlama ve hata ayıklama aynı şeyleydir. Yani
Programlama, programın istediğiniz şeyi yapana kadar aşamalı olarak hata
ayıklama sürecidir. Bu fikir, *bir şey* yapan bir program ile başlamınızı,
ilerledikçe programda küçük değişikler yaparak hataları ayıklamanızı tavsiye
eder. Böylece her zaman çalışan bir programa sahip olursunuz.

Örneğin, Linux bir işletim sistemi çekirdeğidir  ve binlerce kaynak kod
içerir, fakat Linus Torvalds tarafından Intel 80386 yongasını keşfetmek için
basit bir program olarak başlatılmıştır. Larry Greenfield'a göre, Linus'un
başlangıç projelerinden biri AAAA ve BBBB arasında seçim yaparak bunu ekranda
gösteren programdı. Bu program daha sonra Linux'a evrilmiştir ( *The Linux
Users's Guide Version 1*.)

Kitabın  sonraki bölümleri hata ayıklama ve diğer programlama
pratikleri hakkında daha fazla önerilerde bulunacaktır.

.. index:: biçimsel diller, doğal diller, andaç

Biçimsel ve doğal diller
------------------------

**Doğal diller** konuştuğumuz dillerdir; Türkçe, İngilizce, İspanyolca ve
Fransızca gibi. Doğal diller insanlar tarafından tasarlanmamıştır (insanlar
bunlar için kurallar koymaya çalışsa bile), doğal olarak evrilmişlerdir. 

**Biçimsel diller** insanlar tarafından özel uygulamalar için geliştirilmiş
dillerdir. Örneğin, matematikçilerin kullandığı gösterim (notasyon), sayılar
ve semboller arasındaki ilişkiyi göstermek için iyi bir biçimsel dildir.
Kimyacılar,  moleküllerün kimyasal yapısını göstermek için biçimsel dili
kullanırlar. Ve en önemlisi: 

    *Programlama dilleri hesaplamaları ifade etmek için tasarlanmış biçimsel
    dillerdir.*

Biçimsel diller sözdizimi açısından katı kurallara sahip olma eğilimindedir.
Örneğin ``3+3=6`` ifadesi matematiksel sözdizimsel ifadedir, ancak ``3=+6$``
değildir. H\ :sub:`2`\ 0 sözdizimi kimya için doğrudur, fakat :sub:`2`\ Zz
geçerli değildir, çünkü ``Zz`` kısaltmasına sahip bir element yoktur. 

Sözdizimsel kurallar **token**\lere ve yapıya ait olmak üzere iki türdedir.
Token'lar dilin temel öğeleridir; kelimeler, sayılar, parantezler, virgül,
gibi. Python'da, ``print ("Hoşgeldin Yeni Yıl", 2013)`` gibi bir ifade 6 tane
token vardır. Bunlar: fonksiyon ismi, açılış parentezi, cümle, virgül, sayı ve
kapanış parentezi dir. 

Tokenlar dizilirknhata yapılabilir. ``3=+6$`` ifadesiyle ilgili bir sorun, ``$`` sembolü
matematikte geçerli bir token değildir (bildiğim kadarıyla.) Benzer olarak,
:sub:`2`\ Zz ifadesi de geçerli değildir çünkü Zz  kısaltmasına sahip bir
element yoktur. 

İkinci tür sözdizimi kuralı cümlelerin yapısıyla ---tokenların nasıl
dizildiği---
ile ilgilidir. ``3=+6$`` yapısal olarak geçersizdir cünkü eşittir işaretinden
hemen sonra artı işareti gelemez. Benzer olarak, molekül formüllerinde de alt
işaretler element sonra gelmelidir; önce gelemezler. Bizim Python örneğimizde,
eğer virgülü ihmal etseydik; veya sol ve sağ parantezlerin yerlerini
değiştirseydik, ``print)" Hoşgelding Yeni Yıl", 2013(`` elde ederdik. Bu komut
altı tane geçerli tokenlara sahip olmasına rağmen, bu yapı geçerli değildir. 

Biçimsel bir dildeki veya Türkçe'deki bir cümleyi okuduğunuzda, cümlenin
yapısını çözmek gerekir (doğal dillerde bunu bilinçiz bir şekilde yaparız.) Bu
sürece **ayrıştırma** ( parsing) denir. 

Örneğin, "Ayaklarıma kara sular indi" cümlesini dudyuğunuzda, "ayaklarıma"nın
özne, "indi"'nin de yüklem olduğunu anlarsınız. Cümleyi ayrıştırdığınızda,
cümlenin ne anlama geldiğini ( cümlenin anlambilimini) çözersiniz. "Ayak"ın en
olduğunu ve "indi" eyleminin anlamını bildiğinizi varsayarsak, bu cümleyle
kastedilen anlamı ortaya çıkarabilirsiniz. 

Her ne kadar biçimsel ve doğal diller birçok ortak özelliğe ---tokenlar, yapı,
sözdizimi, anlambilim--- sahip olsa da, birçok farklılıkları da vardır:

.. glossary:: 

   belirsizlik:
        Doğal diller belirsizlikle doludur, kişiler bağlamsal ipuçları ve
        diğer bilgilerden yararlanarak bu belirsizliği aşarlar. Biçimsel
        diller neredeyse veya tamamen belirli olmak üzere tasarlanmıştır.
        Bunun anlamı cümlenin sadece bir anlamı vardır, bağlam ne olursa
        olsun. 

   fazlalık:
        Belirsizliği önlemek ve yanlış anlamaları azaltmak için, doğal diller
        birçok gereksiz içeriğe sahiptir. Bu yüzden birçok fazlalık
        barındırır. Biçimsel diller daha az belirsiz ve özdür.

   gerçekçilik:
        Biçimsel diller ne söylüyorsa onu kasteder. Diğer bir yandan, doğal
        diller deyim ve mecazlarla doludur. Eğer bir kişi, " Ayaklarıma kara
        sular indi." diyorsa, bu ayaklarına kara sular indi ( sanki çamurlu
        bir suda yürüyormuşta, ayakkabılarına kara sular doldu.) anlamına
        gelmez. Bunun gizli bir anlamı vardır ve kişinin yorgun olduğunu
        belirtir. Biçimsel dillerde cümlenin gerçeği aynen yansıtması gerekir,
        anlamı yazılanla aynı olmalıdır. 
    

Doğal dilleri konuşarak büyüyen kişiler ---herkes--- biçimsel dillere
alışmaktar zorlanabilirler. Bu bazı yönlerden, biçimsel dil ile doğal dil
arasındaki fark, düzyazı ile şiir arasındaki fark gibidir. Ancak:

.. glossary::

   şiir:
        Kelimeler anlamları olduğu kadar sesleri için de kullanılır ve tüm
        şiir bir etki veya duygusal bir tepki yaratır. Belirsizlik yaygın
        olmasının yanında, sıklıkla bir gerekliliktir. 

   düzyazı:
        Kelimelerin gerçek anlamı daha önemlidir ve yapı anlama daha fazla
        katkı sağlar. Düzyazının çözümlenmesi şiire göre daha kolaydır ancak
        yine de belirsizlik içerebilir.

   program:
        Bilgisayar programının anlamı belirli (tek anlamlı) ve gerçek
        olmalıdır; token ve yapının çözümlenmesi ile tamamen anlaşılmalıdır.

Programları (ve diğer biçimsel dilleri) bazı öneriler şu şekildedir: İlk
olarak, biçimsel dillerin doğal dillerden daha youn olduğunu hatırlamak
gerekir. Bu yuzden bunları okumak daha uzun zaman alır. Ayrıca yapı oldukça
önemlidir, bu yüzden yukarıdan aşağıya soldan sağa okumak iyi bir fikir
değildir. Bunun yerine, programı kafanızda ayrıştırmayı, tokenları belirlemeyi
ve yapıyı yorumlamayı öğrenmemiz gerekir. Son olarak, ayrıntılar önemlidir.
Yazım yanlışları ve noktalama hataları gibi küçük şeyler, doğal dillerde
yakanızı kurturabilir, fakat  biçimsel dillerde büyük farklılıklar
yaratabilir. 
.. index:: İlk Program

İlk program
-----------
Geleneksel olarak, yeni bir dilde yazılan ilk program *Merhaba, Dünya!* adı
verilen programdır, çünkü ekranda "Merhaba, Dünya!" kelimelerini gösterir.
Python'da aşağıdaki şekilde yazılmaktadır ( Betikler için, python komutlarının
sol tarafında satır numaralarını göstereceğiz.)

    .. sourcecode:: python3
        :linenos:

        print ("Merhaba, Dünya!")

Bu print fonksiyonunun bir örneğidir; bu fonksiyon kağıt üzerine birşey
yazmaz, ekranda bir değer gösterir. Yukarıdaki örnekte, sonuç aşağıdaki gibi
olur: 

    .. sourcecode:: python3
        :linenos:

        Merhaba, Dünya!

Programdaki tırnak işaretleri değerin başlangıç ve bitiş değerini gösterir;
ekranda tırnak işaretleri gözükmez. 

Bazı kişiler programlama dilinin kalitesini "Merhaba, Dünya!" programının
basitliğiyle değerlendirirler. Bu standarta göre, Python oldukça iyi sonuç
üretir. 

.. index:: Açıklamalar

Yorumlamalar
------------

Programlar, büyüdükçe ve daha karmaşık hal aldıkça okunmaları zorlaşır.
Biçimsel diller oldukça yoğundur. Koda bakarak, kodun ne yaptığını ve niçin
yazıldığını kavramak genellikle zordur. 

Bu yüzden, programınıza doğal dillerde notlar ekleyerek, programınızın ne
yaptığını açıklıyabilirsiniz. 

Programda yazılan *açıklamalar* yalnızca onu okuyan kişi için amaçlanmıştır.
Python yorumcusu tarafından dikkate alınmaz. 

Python'da açıklama `#` tokenı ile başlar. Geri kalan satır ihmal edilir. Şimdi
*Merhaba, Dünya!* programının açıklamalı haline bakalım:

    .. sourcecode:: python3
        :linenos:

        #-------------------------------------------------------------
        #Bu program Python'un ne kadar güzel bir dil olduğunu gösterir!
        #Joe Soap tarafından Aralık 2010 tarihinde yazılmıştır. 
        #Herhangi biri bu programı kopyalayabilir veya değiştirebilir.
        #-------------------------------------------------------------

        print ("Merhaba, Dünya!") # Kolay değil mi?

Ayrıca programda bir satırı boş bıraktığımızı dikkat edin. Boş satırlar,Python
Yorumlayıcısı tarafından dikkate alınmaz. Fakat açıklamalar ve boş satırlar,
insanların programı okumasını kolaylaştırır. Bunları cömert şeklinde
kullanmaktan kaçınmayınız. 

Glossary
--------

.. glossary:: 

   algoritma
        Bir problem kategorisini çözmek için tanımlanmış adımlar

   bug
        Programdaki bir hata

   açıklama
        Programdaki açıklama programcılar (veya onu okuyan herhangi birisi)
        için yazılmıştır ve programın çalışmasında herhangi bir etkisi yoktur.

   hata ayıklama
        Herhangi üç hatadan birini bulma ve onu ortadan kaldırma sürecidir.

   istisna
        Çalışma zamanı hatasının diğer bir adı

   biçimsel dil
        Bazı özel amaçlar için, matematiksel fikirlerin temsili ve bilgisayar
        programları gibi, insanlar tarafından tasarlanmış herhangi bir dildir.
        Bütün programlama dilleri biçimsel dillerdir. 

   yüksek seviyeli dil
        İnsanlar tarafından rahat okunabilmesi, yazılması ve anlaşılması için
        geliştirilmiş Python benzeri programlama dili

   dolaysız kip (mod) 
        Python komut istemcisine yazılan ifadele sonuçlarının hemen
        gösterilmesini sağlayan Python tarzı. 

   yorumlayıcı
        Python betiklerini ve ifadelerini çalıştıran bilgisayar programı

   düşük seviyeli dil
        Bilgisayarın programları hızlı ve kolay şekilde çalıştırabilmesi için
        tasarlanmış program. "Makina dili" veya "birleştirici dil" adı da
        verilmektedir.

   doğal dil
        İnsanların konuştuğu doğal olarak gelişmiş herhangi bir dil.

   nesne kodu
        Programı bilgisayarın anlayacağı şekilde çevirme yapan derleyici
        sonucundaki çıktı. 

   ayrıştırma
        Bir programı inceleme ve sözdizimsel yapısını çözümleme işlemi

   taşınabilirlik
        Bir programın birden fazla bilgisayar türünde çalıştırılabilmesi
        özelliği

   print fonksiyonu
        Python yorumlayıcısının bir değeri ekranda göstermesini sağlayan
        fonksiyon

   problem çözme
        Problemi formüle etme, buna çözüm bulma ve çözümü ifade etme süreci

   program
        Bilgisayar tarafından gerçekleştirilecek eylemleri ve hesaplamaları
        belirten art arda gelen komutlar

   Python kabuğu
        Python yorumlayıcısının etkileşimli kullanıcı arayüzü. Python kabuğu
        kullancısı bilgi istemcisine ( >>>) komutları yazar ve ENTER tuşuna
        başarak bu komutları  Python yorumlayıcısına gönderir. Kabuk kelimesi
        Unix'ten gelmektedir. Kitabın bu versiyonunda kullanılan Pyscripter'in
        penceresinde yazacağınız komutlar ile "hemen cevap kipinde"
        çalışabiliriz. 

   çalışma zamanı hatası
        Program çalıştırılana kadar ortaya çıkmayan, çalıştırıldıktan sonra
        oluşan ve programın çalışmasına devam etmesini engelleyen hata. 

   betik
        Bir dosyada saklanmış program ( genellikle yorumlayıcıya gönderilecek
        olan)

   anlambilimsel hata
        Programcının yapmak istediğinden farklı birşey yapmasına neden olan
        hata

   anlambilim
        Programın anlamı

   kaynak kod
        Yüksek seviyeli bir dildeki  programın derlenmeden önceki hali

   sözdizimi
        Programın yapısı

   sözdizimi hatası
        Programın ayrıştırılmasını imkansız hale getiren hata (dolayısıyla
        yorumlanmanın imkansız olduğu hal) 

   token
        Programın sözdizimsel yapısının temel öğelerinden biri, doğal
        dillerdeki kelimeye benzetilebilir. 

Alıştırmalar
------------

#. Anlaşılabilir anlama sahip ama sözdizimsel olarak yanlış olan Türkçe bir
   cümle yazınız. Sözdizimsel olarak doğru ancak anlambilimsel hatalara sahip
   bir başka cümle yazınız.
#. Python kabuğunu başlatın ve ``1 + 2`` yazıp, ENTER tuşuna basın. Python bu
   ifadeyi *hesaplar*, sonucu ekranda gösterir ve başka bir bilgi istemi
   yazar. ``*`` işareti *çarpma işlecidir; ``**`` ise *üs alma işlecidir.*
   Farklı ifadeler girerek denemeler yapın. Sonuçları kaydedin. 
#. ``1 2`` yazıp, ENTER tuşuna basın. Python bu ifadeyi hesaplamaya çalışır
   ancak yapamaz çünkü bu ifade sözdizimsel olarak geçerli değildir. Bunun
   yerine, aşağıdaki hata mesajını gösterir:

        .. sourcecode:: python3

            File "<interactive input>", line 1
                1 2
                  ^
            SyntaxError: invalid syntax

   Birçok durumda, Python sözdizimsel hatanın nerde oluştuğunu belirtir, fakat
   bu her zaman için doğru değildir; Ve genelde neyin yanlış olduğu hakkında
   fazla bilgi vermez. 

   Bu yüzden, genellikle, sözdizim kurallarını öğrenmek size düşen bir yüktür. 

   Bu örnekte, sayılar arasında bir işleç olmadığı için Python şikayet
   etmektedir. 

   Python bilgi istemcisine birkaç örnek girip, ENTER tuşuna basınız. Hata
   mesajları üretmeye çalışınız. Girdiğiniz ifadeyi ve Python'un size geri
   verdiği son satırdaki hata mesajını defterinize yazınız.
#. ``print("Merhaba")`` yazınız. Python bunu çalıştırır ve sonuçta m-e-r-h-a-b-a
   harflerini ekranda gösterir. Cümlede kullandığınız tırnak işaretlerinin
   çıktıda olmadığına dikkat edin. Şimdi ise ``"Merhaba"`` yazın ve sonucu
   tanımlayınız. Tırnak işareti kullandığızda ve kullanmadığınızda oluşan
   etkiyi not ediniz.

#. Şimdi ``peynir`` kelimesini tırnak işareti olmadan yazınız. Çıktı aşağıdaki
   gibi birşey olacaktır::

        Traceback (most recent call last):
          File "<interactive input>", line 1, in ?
        NameError: name 'peynir' is not defined

   Bu bir çalışma zamanı hatasıdır; daha doğrusu *NameError ( Değişken İsim
   Hatası)* dır. Burda peynir kelimesi tanımlanmadığından dolayı bir hata
   vermiştir. Eğer bunun ne anlama geldiğini bilmiyorsanız, yakında
   öğreneceksiniz. 

#. Python istemcisine ``6 + 4 * 9`` yazıp, ENTER tuşuna basınız. Çıkan sonucu
   kaydediniz.

   test1.py adlı dosya (betik)  oluşturun ve bu dosyanın içine aşağıdaki
   içeriği yazın:

        .. sourcecode:: python3
            :linenos:

            6+4*9 

   Bu betiği çalıştırdığınızda ne oluyor? Şimdi içeriği aşağıdaki şekilde
   değiştirin:

        .. sourcecode:: python3
            :linenos:

            print(6+4*9)

   ve yeniden çalıştırın. Bu sefer ne oldu?

   Ne zaman bir ifade Python bilgi istemcisine yazılırsa, bu hesaplanır ve
   sonuç *otomatik* olarak bir satır aşağıya yazılır. ( Sanki hesap makinanız
   gibi; eğer bu ifadeyi (deyimi)  yazarsanız,42 sonucunu bulursunuz.) 

   Betik ise farklıdır. Hesaplanan ifadeler *otomatik* olarak ekrana yazılmaz,
   bu yüzden cevabın ekranda gözükmesini istiyorsanız, **print** fonksiyonunu
   kullanmanız gerekir.

   Python kabuğunda  print fonksiyonunu kullanma ihtiyacınız hemen hemen yok
   gibidir.



 


 
           

            

    

  



    
            
    
       













