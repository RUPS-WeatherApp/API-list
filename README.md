# API-list
Seznam API storitev in API ključev

## Koristne informacije
Za razne registracije lahko uporabite ta Microsoft Email Account (če ne želite izbrati svojega):
> www: https://outlook.live.com/mail/0/inbox?nlp=1
> 
> email: feri@lxbq.onmicrosoft.com
> 
> geslo: `Ucenec22`

### Api list
- [OpenWeatherMap](#openweathermap)
- [AccuWeather](#accuweather)
- [WeatherStack](#weatherstack)
- [Meteorologisk Institutt](#meteorologisk-institutt)
- [Oikolab](#oikolab)
- [Open-Meteo](#open-meteo)
- [Tomorrow.io](#tomorrowio)
- [VisualCrossing](#visualcrossing)
- [weather-api](#weather-api)
- [WeatherAPI](#weatherapi)
- [WeatherBit](#weatherbit)

# APIs

## Geonames: 

username: `feri`

password: `Ucenec22`

Primer url: http://api.geonames.org/findNearbyJSON?lat=15.6467&lng=46.5547&username=feri (_lahko traja, da račun aktivirajo_)

---

## [OpenWeatherMap](https://openweathermap.org/)

API key: `61f536c7ec3e62f7c4d43412de9977c8`

### Primer uporabe:
>**URL** : https://api.openweathermap.org
>
>**URL**/data/2.5/weather?q=**Mesto**&appid=**APIKEY**&units=metric
>
>**ALI**
>
>**URL**/data/2.5/weather?lat=**Lat**&lon=**Lon**&appid=**APIKEY**&units=metric
>
> Url vreme: https://api.openweathermap.org/data/2.5/weather?q=maribor&appid=61f536c7ec3e62f7c4d43412de9977c8&units=metric

Zgornji klic vrne trenutne podatke o vremenu v Mariboru. Dokumentacija je na voljo [tukaj](https://openweathermap.org/current).

[*back to list*](#api-list)

---

## [AccuWeather](https://developer.accuweather.com/apis)

API key: `evJqjQoI3glUTIMos9DlAuiPfszayhZy`

> **Login**
>
> username: feri@lxbq.onmicrosoft.com
>
> password: `Ucenec22`

### Primer uporabe:
>**URL** : http://dataservice.accuweather.com
>
>**URL**/currentconditions/v1/**Location code**?apikey=**APIKEY**
>
>Url vreme: http://dataservice.accuweather.com/currentconditions/v1/299438?apikey=evJqjQoI3glUTIMos9DlAuiPfszayhZy&details=true

Zgornji klic vrne trenutno vreme na podani lokaciji. Dokumentacija je na voljo [tukaj](https://developer.accuweather.com/accuweather-current-conditions-api/apis/get/currentconditions/v1/%7BlocationKey%7D).

Da pridobimo location code lahko uporabimo njihov location api.
>**Lokacijska koda glede na ime mesta**
>
>**URL** : http://dataservice.accuweather.com
>
>**URL**/locations/v1/cities/search?apikey=**APIKEY**&q=**Ime mesta**&details=false
>
>Url lokacija: http://dataservice.accuweather.com/locations/v1/cities/search?apikey=evJqjQoI3glUTIMos9DlAuiPfszayhZy&q=Maribor&details=false

**ALI**

>**Lokacijska koda glede na geolokacijo**
>
>**URL** : http://dataservice.accuweather.com
>
>**URL**/locations/v1/cities/geoposition/search?apikey=**APIKEY**&q=**Lat%Lon**&details=true
>
>Url lokacija: http://dataservice.accuweather.com/locations/v1/cities/geoposition/search?apikey=evJqjQoI3glUTIMos9DlAuiPfszayhZy&q=46.5535399%2C15.6445498&details=true

[*back to list*](#api-list)

---

## [Weatherstack](https://weatherstack.com/)

API key: `ad82060852a1b359f14848cd67837805`

>**Login**
>
>username: feri@lxbq.onmicrosoft.com
>
>password: `Ucenec22`

Api ima omejitev na 1000 klicev na mesec.

### Primer uporabe:

>**URL** : http://api.weatherstack.com
>
>**URL**/current?access_key=**APIKEY**&query=**Ime mesta ALI Lat,Lon**
>
>Url vreme: http://api.weatherstack.com/current?access_key=ad82060852a1b359f14848cd67837805&query=Maribor

Dokumentacija za zgornji klic je na voljo [tukaj](https://weatherstack.com/documentation).

[*back to list*](#api-list)

---

## [Meteorologisk Institutt](https://api.met.no)

Za api ne potrebujemo kljuca.

### Primer uporabe:

>**URL** : https://api.met.no
>
>**URL**/weatherapi/locationforecast/2.0/compact?lat=**Lat**&lon=**Lon**
>
>Url vreme: https://api.met.no/weatherapi/locationforecast/2.0/compact?lat=46.55&lon=15.63

Zgornji klic vrne podatke o vremenu za naslednjih nekaj ur, [opis formata](https://api.met.no/doc/ForecastJSON) (Podatki so v json arrayu **timeseries**). Dokumentacija je na voljo [tukaj](https://api.met.no/weatherapi/locationforecast/2.0/documentation).

[*back to list*](#api-list)

---

## [Oikolab](https://oikolab.com/)

API key primary: `91465f4d6c104ad7945a5ace78246ca2`

API key secondary: `c646103112a1453299ac0dad227c64f9`

>**Login**
>
>username: feri@lxbq.onmicrosoft.com
>
>password: `Ucenec22`

### Primer uporabe:

>**URL** : https://api.oikolab.com
> 
>**URL**/weather?param=**Podatki ki jih zelimo**&start=**YYYY-MM-DD**&end=**YYYY-MM-DD**&freq=D&lat=**Lat**&lon=**Lon**
> 
> **ALI**
>
>**URL**/weather?param=**Podatki ki jih zelimo**&start=**YYYY-MM-DD**&end=**YYYY-MM-DD**&freq=D&location=**Mesto**
>
> *(Potrebno je nastavit api-key parameter v headerju requesta)*
>
>Url vreme: https://api.oikolab.com/weather?param=temperature&param=dewpoint_temperature&param=wind_speed&param=mean_sea_level_pressure&param=total_cloud_cover&freq=D&lat=46.55&lon=15.63&start=2023-11-11&end=2023-11-11

Zgorni klic vrne podatke za Maribor dolocene v **param** v formatu gfs za doloceno obdobje nastavljeno z parametroma **start/end**. Dokumentacija je na voljo [tukaj](https://docs.oikolab.com/references/).

[*back to list*](#api-list)

---

## [Open-Meteo](https://open-meteo.com/)

Za api ne potrebujemo kjuca. Zastonj uporaba pod pogojem da ostanemo pod 10.000 klicev na dan.

### Primer uporabe
>**URL** : https://api.open-meteo.com
>
>**URL**/v1/forecast?**Parametri ki jih zelimo**
>
>Url vreme: https://api.open-meteo.com/v1/forecast?latitude=46.5547&longitude=15.6467&daily=weather_code,temperature_2m_max,temperature_2m_min,apparent_temperature_max,apparent_temperature_min,sunrise,sunset,uv_index_max,precipitation_sum,rain_sum,showers_sum,snowfall_sum,precipitation_probability_max,wind_speed_10m_max,wind_gusts_10m_max,wind_direction_10m_dominant&timezone=Europe%2FBerlin&forecast_days=1

Zgornji klic vrne podatke dolocene z parametri za dnevno napoved v Mariboru. Mogoce je pridobiti tudi trenutno vreme vendar ima manj podatkov. Dokumentacija je na voljo [tukaj](https://open-meteo.com/en/docs).

[*back to list*](#api-list)

--- 

## [Tomorrow.io](https://www.tomorrow.io/weather-api/)

API key: `XLLe2XW6eFdCNP8brMq2v9TrmfzXoNlG`

>**Login**
>
>username: feri@lxbq.onmicrosoft.com
>
>password: `Ucenec22!`

### Primer uporabe:

>**URL** : https://api.tomorrow.io
>
>**URL**/v4/weather/realtime?location=**Mesto**&apikey=**APIKEY**
>
>**ALI**
>
>**URL**/v4/weather/realtime?location=**Lat,Lon**&apikey=**APIKEY**
>
>Url vreme: https://api.tomorrow.io/v4/weather/realtime?location=maribor&apikey=XLLe2XW6eFdCNP8brMq2v9TrmfzXoNlG

Zgornji klic vrne trenutno vreme v Mariboru. Dokumentacija je na voljo [tukaj](https://docs.tomorrow.io/reference/welcome).

[*back to list*](#api-list)

---

## [VisualCrossing](https://www.visualcrossing.com/)

API key: `6XCP3LPX3SVQJZY2V5KPGR6JX`

>**Login**
>
>username: feri@lxbq.onmicrosoft.com
>
>password: `Ucenec22`

### Primer uporabe: 
>**URL** : https://weather.visualcrossing.com
>
>**URL**/VisualCrossingWebServices/rest/services/timeline/**Mesto**/today?unitGroup=metric&include=current&key=**APIKEY**&contentType=json
>
>**ALI**
>
>**URL**/VisualCrossingWebServices/rest/services/timeline/**Lat,Lon**/today?unitGroup=metric&include=current&key=**APIKEY**&contentType=json
>
>Url vreme: https://weather.visualcrossing.com/VisualCrossingWebServices/rest/services/timeline/maribor/today?unitGroup=metric&include=current&key=6XCP3LPX3SVQJZY2V5KPGR6JX&contentType=json

Zgornji klic vrne trenutno vreme v Mariboru. Dokumentacija je na voljo [tukaj](https://www.visualcrossing.com/resources/documentation/weather-api/timeline-weather-api/). Na voljo je tudi [query builder](https://www.visualcrossing.com/weather/weather-data-services).

[*back to list*](#api-list)

---

## [weather-api](https://github.com/robertoduessmann/weather-api)

Za api ne potrebujemo kljuca.

### Primer uporabe
>**URL** : https://goweather.herokuapp.com
>
>**URL**/weather/**Mesto**
>
> Url vreme: https://goweather.herokuapp.com/weather/maribor

Zgornji klic vrne trenutno vreme v Mariboru. Api nudi le podatke o temperaturi, hitrosti vetra ter opis zato mogoce ni najbolj primeren. 

[*back to list*](#api-list)

---

## [WeatherAPI](https://www.weatherapi.com/)

API key: `69940ab6788749eb989205344231111`

>**Login**
>
>username: feri@lxbq.onmicrosoft.com
>
>password: `Ucenec22`

### Primer uporabe
>**URL** : http://api.weatherapi.com
>
>**URL**/v1/current.json?key=**APIKEY**&q=**Mesto**&aqi=yes
>
>**ALI**
>
>**URL**/v1/current.json?key=**APIKEY**&q=**Lat,Lon**&aqi=yes
>
> Url vreme: http://api.weatherapi.com/v1/current.json?key=69940ab6788749eb989205344231111&q=maribor&aqi=yes

Zgornji klic vrne trenutno vreme v mariboru. Dokumentacija je na voljo [tukaj](https://www.weatherapi.com/docs/).

[*back to list*](#api-list)

---

## [WeatherBit](https://www.weatherbit.io/)

API key: `4f13fd1604474efbbc0f844bfc299096`
*( Zastonj na voljo le 50 klicev na dan )*

>**Login**
>
>username: feri@lxbq.onmicrosoft.com
>
>password: `Ucenec22`

### Primer uporabe:
>**URL** :  https://api.weatherbit.io
>
>**URL**/v2.0/current?lat=**Lat**&lon=**Lon**&key=**APIKEY**
>
>**ALI**
>
>**URL**/v2.0/current?city=**Mesto**&key=**APIKEY**
>
> Url vreme: https://api.weatherbit.io/v2.0/current?city=maribor&key=4f13fd1604474efbbc0f844bfc299096

Zgornji klic vrne trenutno vreme v mariboru. Dokumentacija je na voljo [tukaj](https://www.weatherbit.io/api).

[*back to list*](#api-list)
