## PROJE TANITIMI

## mockapi adresi https://64a7afb1dca581464b84939b.mockapi.io/todos

# API deki veriler asagidaki sekildedir mockapi de
- [
- {"task":"task 1","isDone":false,"id":"1"},
- {"task":"task 2","isDone":false,"id":"2"},
- {"task":"task 3","isDone":false,"id":"3"},
- {"task":"task 4","isDone":false,"id":"4"},
- {"task":"task 5","isDone":false,"id":"5"},
- {"task":"task 6","isDone":false,"id":"6"},
- ]


# yarn create react-app . --template typescript            (https://create-react-app.dev/docs/adding-typescript adresinden aldik) ile actigimiz klasorun terminalinde yapiyi kuracak ve ts ya da tsx uzantisi ile gelecek dosyalar.sitesinde bu code . yerine my-app yazmis ben sildim cunku dosya adimi todo-ts yapmak istedim.ister buraya yaz ister vs de ac dosyayi buraya sadece .koy

# eger halihazirdaki bir projeye TypeScript ekleyeceksek onun create kodu da yine sayfasinda var.

- dosya uzantilari .ts veya .tsx dir.


-- App.tsx  dosyasi js deki ile ayni.
-- index.tsx de root u getirirken as ile type ni belirtmis.bu js den farkli
-- Farkli olarak daha once karsilasmadigimiz src icinde react-app-env.d.ts dosyasi var. burdaki .d.ts uzantisi soyle algilaniyor; burasi global type tanimlama alani.burda tanimlanan type lari istedigin yerde import etmeden kullanabilirsin. react type larini kullanmamiza olanak sagliyor onu referance alarak.

# temizligimizi yapalim.strg ye basili tutarak mausla sec dosyalari ve delete. index.tsx de import reportWebVitals from './reportWebVitals'; ve reportWebVitals(); sil. App.tsx den de divin icini tamamen sil

# bu projede mui ekleyip kullanalim ;  yarn add @mui/material @emotion/react @emotion/styled   icon icin de  yarn add @mui/icons-material  kullaniyoruz. Ama bunlari yan yana da yazip beraber yukleriz.su sekilde;  yarn add @mui/material @emotion/react @emotion/styled  @mui/icons-material

# birde axios kullanacagiz. yarn add axios yazarak terminale onu da yukluyoruz

- simdi src icine components ve pages folderi acip iclerindeki dosyalarla islerimizi yapacagiz.
- components icine ; input alanimiz icin(input ve buton olacak burda), todolari sergilemek icin kapsayici component, ve herbir todo nun yapisi ayni oldugu icin bunlari tek bir componentte cagirmak icin dosyalar aciyoruz

-kurgumuz su; App icinde Main i cagiracagiz.yapiyi burda kurup dagitimi alt comp.lere yapacagiz. Main de AddToDo ve todo lari sergilemek icin ToDolist i cagiracagiz.ToDoList icinde de ToDoListItem i cagiracagiz


## TYPESCRIPT
- Microsoft tarafindan gelistirilmis, JS in söz dizimsel bir süper kümesidir.Yeni bir dil olmak yerine JS uzerine kendi söz dizimini insa eden ve gelistiricilere kodlarinda kullanabilecekleri yeni özellikler sunan bir programlama dili. dunyanin en cok kullanilan 3.prog.dilidir. Js in ustunde dir TS. Js de olmayan ozellikleri JS e kazandiriyor, compile edilmeye ihtiyaci var. 

# Birden fazla Type secenegi sunmus olmasi en önemli özelligi.let isim:string="Abone ol!" seklinde type ni da belirterek yaziyoruz variable i.

## JS zayif ve idnamik bir dildir.Degiskenlerin type larini belirleme yukumlulugu gelistiriciden alinir.Fakat bu durum JS in bazi durumlarda hatayi gormesine engel olur.mesela karekoku alma fonksiyonunda sayi yerine bi string yazarsak, JS bi hata vermeyecektir fakat kodu calistirirken bu kisma gelince sonuctan donut olarak NaN verecektir. TS de ise type i bastan yazilacagi icin fonksiyonu cagirirken hata verir.

## TS ile gelen bir ikinci özellik ise interfaceler dir.variable lara type ekleyebilecegimiz gibi, objelere de type ekleyebilirz.arayuz isminin basina interface yazilir ve herbir özelligin type ni yazariz. sonra olusturdugumuz objeyede bu arayuzun adini9:ile yazariz

- interface IUser{
    isim:string,
    yas:number,
    email:string
}

let user:IUser={
    isim:"ali",
    yas:23,
    email:"jshh@gmail.com"
}


- Js in kullanildigi her alanda kullanilabilir. Daha cok buyuk capli projelerde kullaniliyor. Nesne tabanli dillerin sahip oldugu özellikleri JS e kazandirir. 
- CSS ile SCSS arasindaki iliski gibi. Css de olmayan özellikleri SCSS kazandiriyor.ayni zamanda compile edilip Browserlar tarafindan CSS kodlarinin gozukmesini sagliyor



- JS de kodun runtime zamanina kadar hata alamyiz.calisirken gorulur proje ayaga kalkmis bi dunya maliyet oluyor.mesela string ifadeleri carpmaya kalktik diyelim. TS de ise baslangic degeri atayarak hatalari bastan engellemeye calisiriz. RunTime a gelmeden adim adim göturuyor bizi .



