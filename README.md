# gerekli kütüphaneler
 cv2 içe aktar
 numpy'yi  np olarak  içe aktar

# haarcascade yüklendi python çıktı dizine
cascade  =  cv2 . CascadeClassifier ( 'haarcascade_eye.xml' )

img  =  cv2 . imread ( ' image.jpg ' ) # resmi okuduk
img  =  cv2 . resize ( img , ( 500 , 750 )) # resmi 500x700 olarak boyutlandırdık
copy  =  img . copy () # resmi kopyaladık
gray  =  cv2 . cvtColor ( kopya , cv2 . COLOR_BGR2GRAY )
gözler  =  kaskad . DetectMultiScale ( gri , 1.3 , 5 ) # gözleri tespit ettik
için ( ex , ey , ew , eh ) içinde  gözlerde : # çizeceğimiz karelerin Boyutları
    cv2 . dikdörtgen ( kopya , ( ex , ey ), ( ex + ew , ey + eh ), ( 0 , 255 , 0 ), 2 )
    
yığın  =  np . hstack ([ img , kopya ])
cv2 . imshow ( 'Çıktı' , yığın )
cv2 . bekleme anahtarı ( 0 )
