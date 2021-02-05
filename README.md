# BasicLanguage


Kaynak Kod – Lexer – Parser

Yorumlayıcı sizin yazdığınız kaynak kodu alır ve Lexer kısmında (yani söz dizilimi) kısmında işleme sokar, lexer kuralları oluşturur ve sizin oluşturduğunuz kurallara göre kodu parçalara böler, eğer kurallar aşılırsa hata verdirilir. Lexer'de işlem bittikten sonra oluşturulan token'ler parser kısmında yeniden işleme sokulur ve parser ile kodlar ağaç yapısı şeklinde gruplara bölünür.

Shell dosyası çalıştırılarak çalıştırılabilir.


expr    : term ((PLUS|MINUS) term)*

term    : factor ((MUL|DIV) factor)*

factor	: (PLUS|MINUS) factor
				: power

power		: atom (POW factor)*

atom 		: INT|FLOAT
				: LPAREN expr RPAREN
				
				
				
