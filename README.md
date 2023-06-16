<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

Частка кода вэб-сайта з адкрытым зыходным кодам, запрашаем дапамагчы аптымізаваць пераклад.

## інтэрфейсны код

* [інтэрфейсны код](https://github.com/xxai-art/web)
* [Моўныя пакеты для сайта ў цэлым](https://github.com/xxai-art/web/tree/main/i18n)
* [Моўныя пакеты для модуляў уваходу](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Шматмоўная дакументацыя вэб-сайта](https://github.com/xxai-doc)

Унутраная мова праграмавання — [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , якая дадае некаторыя функцыі на аснове сінтаксісу coffeescript, гл [. ./coffee_plus.md](./coffee_plus.md) .

## Інтэрнацыяналізацыя вэб-сайтаў і дакументаў

Абапірайцеся на наступныя 3 праекты

### [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

Шаблон уцэнкі з суфіксам `.mdt` можа спасылацца на знешнія файлы з сінтаксісам, аналагічным `<+ ./coffee_plus/import.js>` .

[@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

Пераклад Markdown не перакладае коды і спасылкі і кэшуе перакладзеныя прапановы. Калі пераклад зменены, але арыгінальны тэкст не зменены, яго паўторнае выкананне не перазапіша змены перакладу.

[@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

Моўныя файлы для перакладу вэб-сайтаў, створаных `yaml` .
