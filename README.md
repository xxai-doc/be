<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

Рэкамендуецца спачатку ўсталяваць nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) , а затым `direnv allow` пасля ўваходу ў каталог ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) будзе выкананы аўтаматычна пасля ўваходу ў каталог).

Значэнне: пераклад з кітайскай на японскую, карэйскую, англійскую, пераклад з англійскай на ўсе іншыя мовы. Калі вы хочаце падтрымліваць толькі кітайскую і англійскую мовы, вы можаце проста напісаць `zh: en` .

Значэнне: пераклад з кітайскай на японскую, карэйскую, англійскую, пераклад з англійскай на ўсе іншыя мовы. Калі вы хочаце падтрымліваць толькі кітайскую і англійскую мовы, вы можаце проста напісаць `zh: en` .

* [інтэрфейсны код](https://github.com/xxai-art/web)
* [Моўныя пакеты для сайта ў цэлым](https://github.com/xxai-art/web/tree/main/i18n)
* [Моўныя пакеты для модуляў уваходу](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Шматмоўная дакументацыя вэб-сайта](https://github.com/xxai-doc)

Унутраная мова праграмавання — [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , якая дадае некаторыя магчымасці, заснаваныя на сінтаксісе coffeescript, гл [. ./coffee_plus.md](./coffee_plus.md) .

## Інтэрнацыяналізацыя вэб-сайтаў і дакументаў

Абапірайцеся на наступныя 3 праекты

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  Суфікс - `.mdt` , вы можаце выкарыстоўваць сінтаксіс, аналагічны `<+ ./coffee_plus/import.js>` , каб спасылацца на знешнія файлы, і ствараць уцэнку з суфіксам `.md` .

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Пераклад Markdown не перакладае коды і спасылкі і кэшуе перакладзеныя прапановы. Калі пераклад зменены, але арыгінальны тэкст не зменены, яго паўторнае выкананне не перазапіша змены перакладу.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  Моўныя файлы для перакладу вэб-сайтаў, створаных `yaml` .

### Інструкцыя па аўтаматызацыі перакладу дакументаў

Глядзіце сховішча кодаў [xxai-art/doc](https://github.com/xxai-art/doc)

Рэкамендуецца спачатку ўсталяваць nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) , а затым `direnv allow` пасля ўваходу ў каталог ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) будзе выкананы аўтаматычна пасля ўваходу ў каталог).

Каб пазбегнуць вялікай кодавай базы, перакладзенай на сотні моў, я стварыў асобную кодавую базу для кожнай мовы і стварыў арганізацыю для захоўвання кодавай базы

Усталяванне зменнай асяроддзя `GITHUB_ACCESS_TOKEN` і затым запуск [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) аўтаматычна створаць сховішча кода.

Вядома, вы таксама можаце змясціць яго ў кодавую базу.

Спасылка на сцэнарый перакладу [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Код сцэнарыя інтэрпрэтуецца наступным чынам:

[bunx](https://bun.sh/docs/cli/bunx) - гэта замена npx, які працуе хутчэй. Вядома, калі ў вас не ўсталяваны bun, вы можаце выкарыстоўваць замест яго `npx` .

`bunx mdt zh` адлюстроўвае `.mdt` у каталогу zh як `.md` , глядзіце 2 звязаныя файлы ніжэй

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` - гэта асноўны код для перакладу (калі ў вас усталяваны толькі `nodejs` , але `bun` і `direnv` не ўсталяваны, вы таксама можаце запусціць `npx i18n` для перакладу).

Ён будзе аналізаваць [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , канфігурацыя `i18n.yml` у гэтым дакуменце выглядае наступным чынам:

```
en:
zh: ja ko en
```

Значэнне: пераклад з кітайскай на японскую, карэйскую, англійскую, пераклад з англійскай на ўсе іншыя мовы. Калі вы хочаце падтрымліваць толькі кітайскую і англійскую мовы, вы можаце проста напісаць `zh: en` .

Апошнім з'яўляецца [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , які здабывае змест паміж асноўным загалоўкам і першым субтытрам `README.md` кожнай мовы для стварэння запісу `README.md` . Код вельмі просты, вы можаце паглядзець на яго самі.

Google API выкарыстоўваецца для бясплатнага перакладу. Калі вы не можаце атрымаць доступ да Google, наладзьце і ўсталюйце проксі, напрыклад:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Скрыпт перакладу згенеруе перакладзены кэш у каталогу `.i18n` , праверце яго `git status` і дадайце ў рэпазітар кода, каб пазбегнуць паўторных перакладаў.

Калі ласка, запускайце `bunx i18n` кожны раз, калі вы змяняеце пераклад, каб абнавіць кэш.

Калі арыгінальны тэкст і пераклад змяняюцца адначасова, кэш будзе пераблытаны, таму, калі вы хочаце змяніць, вы можаце змяніць толькі адзін, а затым запусціць `bunx i18n` , каб абнавіць кэш.
