# DLUB2018 - Graphitics
## Багийн ажлын танилцуулга

Deep Learning UB 2018 зуны сургалтаар үзсэн хичээлийн хүрээнд төгсөлтийн ажил болгон хийсэн төслийн үр дүнгээ [Б.Гэрэлтуяа](https://github.com/qerelt) [Б.Янжинлхам](https://github.com/yanjinlkham) бид хоёр танилцуулж байна. Манай багийн гол зорилго нь Recurrent Neural Network-ийг кирилл үсэгт Монгол текстээр сургах байв. Бид нэг суурь кодыг[1] таван ялгаатай сургалтын датан дээр сургаснаас хоёр нь үр дүн муутай байсан, харин бусад гурав нь тодорхой үр дүнг үзүүлсэн.

## Яагаад энэ төсөлт ажлыг хийхээр сонгосон бэ?
Зуны сургалтаар Deep Learning судалж байхад, ялангуяа RNN сэдвийг үзэхэд олон төрлийн асуулт бидэнд төрсөн. Төсөлт ажлаа тэдгээрийн хариуг эрэн эхлүүлсэн ба бидэнд Deep Learning чиглэлээр дадлага бага тул энэ ажлаар өөрсдөдөө туршлага үлдээхийг зорьсон.

### Асуултууд:
1. RNN Монгол оньсого ойлгож, зохиож, тааж чадах уу? Ер нь RNN ямар ч хэлээр оньсого ойлгож, зохиож, тааж чадах уу?
2. Монгол хэл дээр Deep Learning ашиглаж хийгдсэн туршилт, төсөл, шийдэл юу байна вэ? Тэдгээр ажлууд нийтэд нээлттэй юу?
3. Бид төсөлт ажлаараа Deep Learning чиглэлээр цааш туршилт, судалгаа хийх, шийдэл хайх хүмүүст тустай үр дүн гаргаж болох уу?
4. Хүмүүс бид зүүнээс баруун руу уншиж сурдаг хэлүүдийг машинаар баруунаас зүүн рүү уншуулж сургаж болох уу? Тухайн хэлийг зүүнээс баруун, дээрээс доош уншиж, бичих бүтэц, дараалалтайгаар зохиосон ч гэсэн эсрэг чиглэлд нь бичиж уншуулахад ямар нэгэн зүй тогтол олдох уу?

## Төсөлт ажлыг гүйцэтгэсэн аргачлал
### Ямар сургалтын дата сонгосон бэ?
1. Монгол Улсын хуулиуд - 22.5 MB
2. Монголын Нууц Товчоо - 449.6 kB
3. Тунгалаг Тамир роман - 2.0 MB
4. Оньсого - 85.7 kB
5. Tweets about Mongolia - 5.2 MB

### Сургалтын датагаа яаж урьдчилан боловсруулсан бэ?
1. Монгол Улсын хуулиуд - Эрх зүйн мэдээллийн нэгдсэн системээс[4] хүчинтэй байгаа 314 хуулийг сонгож .txt өргөтгөлтэйгөөр хадгалсан. Хуулиуд бүгд эрх зүйн акт бичигддэг албан хэлбэрээр бичигдсэн тул нэмж боловсруулалт хийгээгүй.
2. Монголын Нууц Товчоо - Монголын Нууц Товчоог нээлттэй эхээс[5] цахим хэлбэрээр олсныг .txt өргөтгөлтэйгөөр хадгалсан ба өөр боловсруулалт хийгээгүй.
3. Тунгалаг Тамир роман - Ч.Лодойдамбын зохиол Тунгалаг Тамир романыг нээлттэй эхээс[5] цахим хэлбэрээр олсныг .txt өргөтгөлтэйгөөр хадгалсан ба өөр боловсруулалт хийгээгүй.
4. Оньсого - Ё.Далайжамцын эмхтгэн гаргасан Оньсого 2-ыг[6] нээлттэй эхээс зураг хэлбэрээр олсныг текст болгож .txt өргөтгөлтэйгөөр хадгалсан.
5. Tweets about Mongolia - https://twitter.com/ сайтад 2017 оны 11-р сараас одоог /2018 оны 7-р сар/ хүртэл нийтлэгдсэн #Mongolia түлхүүр үг бүхий жиргээнүүдийг .txt өргөтгөлтэйгөөр хадгалсан. Олон хэлтэй текст учраас хэлний ялгалт хийсэн ба 95% нь англи, 2% нь монгол, үлдсэн 3% нь бусад хэлний тэмдэгт гэдгийг тодорхойлсон.

### Ямар DL модель сонгосон бэ?
Бид Martin Gorner-ийн энд[7] танилцуулсан "Language model in Tensorflow"-ийг энэ[1] repository-гоос шууд авч ашигласан. Энэ моделийг кодчилохдоо Tensorflow болон numpy сангуудыг ашигласан байсан.
Дээрх модель зөвхөн англи хэл дээрх текст уншиж цагаан толгойгоо бүрдүүлдэг байсныг өөрсдийн сургалтын датанд тохируулж зөвхөн монголоор уншдаг, монгол англиар уншдаг болгон өөрчилж ашигласан.

### Яаж үр дүнг хэмжсэн бэ?
Бидэнд төсөлт ажлаа эхлэхэд үр дүнгийн талаар урьдчилсан хүлээлт байгаагүй учир эхний туршилтуудаас ажиглалт хийв. Хэдэн оролдлогын дараа зарим сургалтын датаг шинээр нэмэх зэрэг өөрчлөлт хийсэн учраас үр дүнг цуваа байдлаар хэмжсэн гэж болно. Тиймээс, сүүлд хийсэн туршилтуудыг эхэнд хийснийх нь туршлагад үндэслэн сайжруулахыг хичээсэн тул сүүл хэсэгт нь ажиглалт, тэмдэглэлт арьцангуйгаар олон байгаа.

## Төсөлт ажлын үр дүн

### 1. Монгол Улсын хуулиуд - бүтэн сургалт

ALPHASIZE = 117, бүх хуулиар сургасан, validation хийгээгүй, ~26 цаг сургасан, хамгийн өндөр нарийвчлал 0.8083 92.40M дэх алхамд гарсан, 10 epoch сургасан, batch-ийн алдаа сүүлийн epoch дээр ихэссэн

Хуулийг эхлүүлж сурсан нь:
```
МОНГОЛ УЛСЫН ХУУЛЬ
2016 оны 7 дугаар сарын 01-ний өдөр
Улаанбаатар хот
ТӨЛБӨРИЙН ХУХАЙ ХЭРЭГСЛИЙН ҮНЭЛГЭЭ
21 дүгээр зүйл. Хууль зөрчигчид хүлээлгэх хариуцлага
```
Хуулийг дуусгаж сурсан нь:
```
10.4.Энэ хуулийг 2015 оны 12 дугаар сарын 01-ний өдрөөс эхлэн дагаж мөрдөнө.
МОНГОЛ УЛСЫН ИХ ХУРЛЫН ДАРГА
Д.ДЭМБЭРЭЛ
```
Хуулийн зүйл, заалтуудыг дугаарлаж сурсан нь:
```
11.1.Төрийн байгууллага нь энэ хуулийн 11.2.1-т заасан эрх, үүргийг хэрэгжүүлэхэд шаардагдах мэдээллийг тусгай зөвшөөрөл олгоход 10 000–100 000 төгрөг;
11.1.10.хуульд заасны дагуу төсвийн төв, төрийн бодлого, хууль, энэ хууль болон эдгээртэй нь хөлбогдох хууль тогтоомжийг хэрэгжүүлэх байгууллагын дүгнэлтийг үндэслэл үйлдэх талаархи тайланг хууль тогтоомжийн бусад актаас бүрдэнэ.
```
Улсын Их Хурлын гишүүн байж сурсан нь:
```
Тун удахгүй…
```
### 2. Монгол Улсын хуулиуд - хагас сургалт
ALPHASIZE = 117, бүх хуулиар сургасан, validation хийгээгүй, ~9 цаг сургасан, хамгийн өндөр нарийвчлал 0.7817 52.50M дэх алхамд гарсан, 5 epoch сургасан

### 3. Монголын Нууц Товчоо - бүтэн сургалт
ALPHASIZE = 117, бүхлээр сургасан, validation хийгээгүй, ~20 минут сургасан, хамгийн өндөр нарийвчлал 0.4677 2.10M дэх алхамд гарсан, 9 epoch сургасан

### 4. Тунгалаг Тамир роман - бүтэн сургалт
ALPHASIZE = 117, бүхлээр сургасан, validation хийгээгүй, ~1 цаг 30 минут сургасан, хамгийн өндөр нарийвчлал 0.5936 10.50M дэх алхамд гарсан, 10 epoch сургасан

Дүрүүдийг болон харилцан яриа зохиож сурсан нь:
```
- Бид хоёр болохоор барахгүй гээд Дулмаагийн хэрэгтэй хамт явахад нь болохоор барах билээ. Та харах гэсэн бол морь харахгүй болохоор хэлэхэд Долгорын хэрэгт хэлээд байсан билүү. Гэтэл та хоёр хүн хэлжээ.
- Би ч манай барьж байна гээд Дулмаа хэлээд байсан хүн байх гэж бодоогүй. Харин Төмөрийн дэргэд нэгэн хүн байсан юм бол хоорондоо баригдаж, харин хүн байна гэж Долгор хэлэв.
- Та хамар байна. Би таны амьтан юм байх билээ дээ гээд Итгэлт хэлэв.
```
### 5. Оньсого - бүтэн сургалт
ALPHASIZE = 117, бүхлээр сургасан, validation хийгээгүй, data хэтэрхий бага учир үр дүн муу гарсан

### 6. Tweets about Mongolia - бүтэн сургалт
ALPHASIZE = 169, бүхлээр сургасан, validation хийгээгүй, ~14 цаг 30 минут сургасан, хамгийн өндөр нарийвчлал 0.6207 49.20M дэх алхамд гаргасан, 10 epoch сургасан, t.co холбоосын дараа алдаад байгаа юм шиг санагдсан

Twitter хаягийн хэлбэрийг болон Twitter-ээс автоматаар үүсгэдэг t.co холбоос үүсгэж сурсан нь:
```
@UN_Naomi | @tnamenia | @UNFPA | @Atateshe | @UNFNaomi | @ttemplongal https://t.co/ataataatta"
```
Retweet болон hashtag сурсан нь:
 ```
"RT @Mongolia966: Mongolia beaatifal nattre…#mongolia #mongol #natare #amaaing https://t.co/aaatta
```
### 7. Tweets about Mongolia - хагас сургалт
ALPHASIZE = 169, бүхлээр сургасан, validation хийгээгүй, ~4 цаг сургасан, хамгийн өндөр нарийвчлал 0.6010 18.30M дэх алхамд гарсан, 5 epoch сурсан

## Төсөлт ажлын ерөнхий дүгнэлт

### Асуултуудын маань хариултууд:

1. Бидний бэлтгэсэн оньсогын сургалтын дата хэмжээний хувьд бага байсан тул оньсого зохиох, таах түвшинд хүртэл нь сургаж чадаагүй. Иймээс эх сурвалж болгосон номын нэгдүгээр ботийг нэгтгэн датаг өргөжүүлэх, эсвэл өөр бусад ардын аман зохиолууд болох ертөнцийн гурав, туульс зэргийг нэгтгэн дараагийн туршилтыг хийх шаардлагатай болсон. Туршилтыг цааш үргэлжлүүлснээр бид Монголчуудын аман зохиолын урьд нь анзаарагдаагүй байсан зүй тогтлыг олж магадгүй гэж таамаглаж байна. Цаашид Англи хэл дээрх оньсого тааврууд дээр ижил туршилтыг гүйцэтгэх боломжтой.
2. Бид Монгол хэлтэй холбоотой Deep Learning ашигласан шийдэл, нийтэд нээлттэй үр дүн хайж эдгээрийг олов: 
 - http://www.eduge.mn/ нь тодорхой хэдэн Монгол вебсайтаас мэдээнээс урсгал үүсгээд мэдээнүүдийг эерэг болон сөргөөр нь ялгадаг ба уг мэдээнд хандах нийгмийн хандлагыг мөн тодорхойлдог. /Sentiment Analysis/;
 - http://172.104.34.197/nlp-web-demo/ нь Монгол үгийг бүтцээр задлан ангилдаг ба бичгийг яриа болгон хувиргадаг;
 - http://trans.mglip.com/CyrillicC2T.aspx нь кирилл болон уламжлалт бичиг хооронд хөрвүүлэг хийдэг.
Төсөлт ажлын сэдвийг ярилцахад олон шинэ санаа гарч байсан бөгөөд тэдгээрийг цаашид оролдох, хэрэгжүүлэхэд олон зүйлс; тухайлбал: нээлттэй дата, хэрэгтэй болохыг ойлголоо. Бидний уриалах зүйлс бол: хэрэв та Deap Learning ашигласан шийдэл, бүтээл хийсэн бол үүнийхээ талаар олонд дэлгэж, боломжтой бол сургалтын дата, аргачлал, код зэргээ нээлттэй эх хэлбэрээр байршуулаарай.
3. Монгол хэл дээрх Deep Learning туршилт, оролдлого, судалгаанд бага ч атугай нэмэр болох үүднээс бид бас өөрсдийн бэлдсэн Оньсого, Монгол улсын хуулиуд, хойноос нь бичсэн Шекспирийн жүжгийн зохиолуудыг .txt өргөтгөлтэйгөөр нийтэд ил тавьж байгаа. Мөн өөрсдийн төсөлт ажлын дэлгэрэнгүй тайлбарыг нийтлэл болгон түгээж буй.
4. Бид машинд хойноос нь уншуулах туршилтаа Монгол болон Англи датан дээр хийхээр шийдсэн. Аль аль хэлний дүрэм, бүтцийг маш сайн баримталсан байх шаардлагатай учраас Англиар Шекспирийн зохиолууд, Монголоор хуулиудын датаг сонгосон ба эдгээр нь урдаас хойшоо уншуулж сургахад амжилттай байсан учраас энэ туршилтын хувьд оновчтой сонголт болох юм. Хэдий санаагаа олсон ч, энэ төсөлт ажлыг танилцуулах хугацаанд үр дүнгээ үзэж амжихгүй болсон тул бид энэ туршилтыг төсөлт ажлын дараа бие даан хийх зорилттой байгаа. Хойноос нь урагш уншуулсан дата болон хувиргагчийн кодыг мөн хуваалцах болно.

### Бусад дүгнэлт
Төсөлт ажлын маань хөшүүрэг болсон анхны эргэлзээнүүд (одоохондоо ч гэсэн) хариулттай болж бид анхдагч төсөөлөлтэй болсон нь бидний хувьд чухал үр дүн байв. Гэхдээ ажлын маань үр дүн бидний анхны хүлээлтээс зарим талаараа зөрсөн. Энэ зөрүү нь датаны бэлтгэл, дата болон үр дүнтэй холбоотой буруу таамаглал болон сургалтад шаардагдах хугацаа зэрэг хүчин зүйлүүдээс шалтгаалдгийг ойлгож авлаа. Туршилт, оролдлого болгонд шинээр шийдэх ёстой асуудлууд гарсан ч нийт таван төрлийн датан дээр тодорхой амжилттайгаар Deep Learning, RNN модель сурган ажиллуулж сонирхолтой үр дүнгүүдтэй танилцлаа. Энэ нь цаашид энэ чиглэлээр тууштай оролдох, төрөл бүрийн туршилтуудыг сониучирхан хийх урам өгч буй.

---

Бас багийн гишүүдийн өмнөөс төсөлт ажлын туслах [Энхжаргал]()даа баярлалаа!
Сургалтын дата, ашигласан кодыг энэ repository-д байрлуулсан: https://github.com/Graphitics/dlub2018
Харин үр дүнгүүдийг (checkpoint files, log, accuracy, loss screenshots)-ыг энд байрлуулсан: https://drive.google.com/drive/folders/14O8Oj4SYQypaEMb3lhirFi_X5F6DLfcA?usp=sharing

---

Ашигласан материалууд:
[1] https://github.com/martin-gorner/tensorflow-rnn-shakespeare
[2] https://karpathy.github.io/2015/05/21/rnn-effectiveness/
[3] Fei-Fei Li & Justin Johnson & Serena Yeung's Lecture 10 slides on Recurrent Neural Networks
[4] http://legalinfo.mn/
[5] https://kindlemn.blogspot.com/
[6] Оньсого 2, Ардын аман зохиолын цуврал - Ё.Далайжамц
[7] https://www.youtube.com/watch?v=vq2nnJ4g6N0&t=107m25s

## Сургах код ажиллуулахдаа:

```
> python3 rnn_train.py
```
## Сургалтын явцыг хянахдаа:

```
> tensorboard --logdir=log
```
## Сурсан байдлаас текст зохиолгохдоо:
```
> python3 rnn_play.py
``` 
   
Сурсан байдлаас текст зохиолгохдоо checkpoint файлуудыг татсан байх хэрэгтэйг анхаарна уу.
