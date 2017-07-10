# golang-JerzySiwecki

Celem postawionego zadania rekrutacyjnego było napisać prosty serwer HTTP przechowujący w pamięci dane typu key-value, udostępniający operacje CRUD na tych danych jako API RESTowe, ale z powodu braku biegłości w zagadnieniu, którego ma dotyczyć przeformułowałem nieco polecenie i wykonałem je trochę po "swojemu". 

Oczywiście rozumiem wagę wykonywania poleceń "precyzyjnie" w przypadku nieścisłości - konieczność "dopytania". Jednak ze względu na ograniczenie czasowe oraz charakter zadania(tzn. fakt, że jest zadaniem rekrutacyjnym) dopuściłem się pewnych odstępstw, traktując je nieco luźniej. 

Starałem się to robić jak najbardziej świadomie i unikac copy-pasty z internetu ale będąc na zupełnie Entry Level i mówiąc uczciwie - wykonując w ogóle pierwsze podejście do GOLANG - który nawiasem mówiąc bardzo mi się podoba!!! - pewien poziom skopiowania i pracy odtwórczej był nie do uniknięcia; jednocześnie nie musi to być zła metodyka - w końcu pozwala zapoznawać się z kodem i mechanizmami co wydaje mi się bardzo dydaktyczne. 

Co postanowiłem zrobić? 
Celem jest stworzenie prostej usługi blogowej, która zapisuje dane JSON jako ciągi znaków do przeglądarki pod różnymi URL. Na przykład wpisanie w pasek adresu localhost wyświetli komunikat powitalny, localhost/post wyświetli wszystkie posty w JSON a localhost/posts/id zwróci post zgodnie z wybranym ID. Mniej więcej właśnie tak zrozumiałem meritum zadania. 
Do tworzenia nowych postów w blogu pmozna wykorzystać cURL:

$ curl -H "Content-Type: application/json" -d '{
        "topic": "some sort of content",
        "text": "...and even more content." 
        }' http://localhost:8080/posts
        
W dalszej części polecenia jest mowa o persystencji przechowywanych danych - 
Do wykonania tej czesci zadania jako narzędzie noSQLowe wykorzystałem REDIS ( https://redis.io/topics/quickstart )z którym to jest również mój pierwszy kontakt. 
Bardzo proszę o wyrozumiałość przy ocenie kodu i napotkanych rozwiązań oraz dla odstępstw od polecenia. 
        
# golang-JerzySiwecki
