# Голоси людей з Reddit (2026-09-09)

Перше в проєкті дослідження, де говорять **реальні люди**, а не продукти. Закриває прогалини №1–3 з [`people-evidence.md`](./people-evidence.md).

**Метод.** Reddit блокує наш веб-краулер, тому пошук ішов через публічний JSON-ендпоїнт (`reddit.com/search.json`, `reddit.com/comments/<id>.json`) у браузері Playwright, без логіну. 9 пошукових запитів → ~17 тредів → топ-коментарі за апвоутами. Цитати наведені мовою оригіналу, апвоути в квадратних дужках.

**Межі вибірки — читати до висновків.**
- Це **англомовний Reddit**. Українських голосів — нуль. Найближче до нашої географії — німецькі, нідерландські, шведські, французькі згадки.
- Сильний перекіс у бік **r/boardgames** (настільники-хобісти) і **Spotify-користувачів**. Це не «довільна незнайома компанія» з CLAUDE.md.
- Багато тредів — **самопіар розробників**. Їхні пости я рахую як сигнал попиту (скільки людей незалежно будують те саме), а не як голос користувача. Голосом користувача вважаю лише коментарі.
- Апвоути на Reddit — не репрезентативність. Коментар з [3] може бути думкою трьох людей.

---

## С1. Ринок, якого немає в research.md: люди самі будують те, що будує БАЗ

Найбільша знахідка. У тредах про Hitster люди **незалежно один від одного** зробили щонайменше 12 інструментів, які роблять рівно одне: **перетворюють твій власний плейліст на гру-вгадайку**.

> guessmyplaylist.com · bopster.app · qrsong.io · forflutna.se (Marimic) · songseeker (open source) · hitdeck.app · blindsongscanner · soundline.app · play-beatly.com · hit-ghost.com · yeartobeat.com · SoundSort
> Джерела: [redd.it/z23sqn](https://redd.it/z23sqn) · [redd.it/1rcew0r](https://redd.it/1rcew0r) · [redd.it/1umud19](https://redd.it/1umud19)

Один із них прямо описує, як з'явився попит:

> [12] «I created a way to print your own QR code cards from a Spotify playlist. **DM me if you want it** :) *Edit: Thanks for all the DMs! Since they kept coming in I've built a website for it.*» — [redd.it/z23sqn](https://redd.it/z23sqn)

**Що це означає для БАЗ.** Гіпотеза «люди хочуть грати зі свого плейліста» — більше не гіпотеза. Але це і попередження: ніша **не порожня**, вона переповнена безкоштовними аматорськими рішеннями. Конкурентна перевага БАЗ не може бути «а ми даємо грати зі свого плейліста» — це вже дають десяток безкоштовних інструментів.

---

## С2. Чому люди йдуть із фіксованого каталогу: він **закінчується**

Це причина №1, названа людьми прямо.

> [8] «After getting **overly familiar with the songs from our two boxes**, we started making our own PNP using the Bopster.app webpage.» — [redd.it/1nx62dz](https://redd.it/1nx62dz)

> [2] «Love the base game, but **went through all the cards**. Any recommendations for another expansion (preferably with less German pop songs)?» — [redd.it/1nx62dz](https://redd.it/1nx62dz)

> «We are a couple of friends at work who all really enjoy playing Hitster together after work once a week. But we've **played the available versions many times**...» — автор поста [redd.it/1sz3qlt](https://redd.it/1sz3qlt)

> [3] «This is so cool! Exactly the kind of thing I've wanted for a while, **everything uses generic playlists to pull from** so it's cool I can use my own.» — [redd.it/1oh2dyj](https://redd.it/1oh2dyj)

**Для БАЗ:** це підтверджує біль Б3 з research.md («фіксований каталог не про нас»), але **з іншої причини, ніж припускав бриф**. Бриф пояснював це смаком поза мейнстрімом. Люди пояснюють це **вичерпанням**: каталог не «не про мене», а «я його вже весь знаю». Це ширший і менш нішевий мотив, ніж закладено в CLAUDE.md.

---

## С3. Пряме заперечення проти ідеї БАЗ

Єдиний знайдений голос проти — записую без пом'якшення:

> [3] «I'm sorry but **using your own playlist is so dumb. It completely defeats the concept of the game.**» — [redd.it/1umud19](https://redd.it/1umud19)

Контекст: тред про Hitster, де механіка — вгадати **рік** випуску. Там спільний каталог справді потрібен для чесності змагання. Для БАЗ (вгадати виконавця/назву) заперечення слабше, але сама позиція існує і в компанії може прозвучати.

---

## С4. Стрімінговий замок — біль, який БАЗ уже обійшов, сам того не знаючи

Найчастіше повторюваний біль у всій вибірці. Люди **не можуть грати**, бо не мають потрібної підписки.

> [10] *(топ-коментар треду)* «I would be way better if you allowed it to be **for free users as well** because I wanna try but I'm using free (wahhh, I'm poor)» — [redd.it/1adhtbd](https://redd.it/1adhtbd)

> [3] «Is it still Spotify only? I love it and **would probably have as many as you**, but I don't have premium Spotify (only Apple Music) unfortunately…» — [redd.it/1r5fgxt](https://redd.it/1r5fgxt)
> ↑ Це людина, яка **готова була купити колекцію коробок**, і не купує через стрімінг.

І найпряміший можливий сигнал під стек БАЗ:

> [1] «**Would you make one with YouTube music??** This is like exactly what I was looking to play but I don't have Spotify 😭» — [redd.it/1adhtbd](https://redd.it/1adhtbd)

**Для БАЗ:** вибір YouTube у CLAUDE.md обґрунтовувався ліцензіями й квотами. Reddit показує **другу, продуктову причину**, якої в research.md немає: Spotify-рішення відрізають частину компанії від гри. На вечірці 3–8 людей достатньо одного без Premium, щоб гра не склалась.

---

## С5. Spotify забороняє музичні вікторини в ToS — і люди це знають

Не юридична абстракція: користувачі попереджають розробників у коментарях, а ігри реально ламаються.

> [68] *(топ-коментар)* «Looks great but if you're not already aware, **using Spotify's API to create games is against their policy** so best not to share this publicly» — [redd.it/1oh2dyj](https://redd.it/1oh2dyj)

> [6] «you cannot create games using spotify api. **your app will be deleted soon**» — там же

> [5] «...when I recently submitted an extension request for my own app **I had to check a box to say it isn't anything quiz related** as that's supposed [to be disallowed]» — [redd.it/1adhtbd](https://redd.it/1adhtbd)

> [3] «I was wondering aswell how jumbo were able to publish the hitster game, regarding the fact that the following usecases are **specifically not allowed** to build with the spotify-api: *"Games or trivia quizzes: Incorporating Spotify into any gaming or quiz functionality. For example, a 'name that tune' q..."*» — [redd.it/187pf0w](https://redd.it/187pf0w)

І наслідок у реальному часі — гравці бачать, як гра вмирає:

> [2] «All of the playlists I'm trying to use are invalid. **I guess Spotify got rid of it already**» — [redd.it/1oh2dyj](https://redd.it/1oh2dyj)
> [2] «won't let me create a room (with a public playlist) idk if i'm doing something wrong or **if spotify nerfed it**» — там же

**Для БАЗ:** це найсильніше зовнішнє підтвердження рішення не йти в Spotify — сильніше, ніж уся ліцензійна аргументація в research.md, бо це не історія Heardle, а те, що ламається **зараз**.

---

## С6. Застереження проти YouTube — від тих, хто пробував обидва

Єдиний голос проти нашого стеку, і його варто прийняти серйозно:

> [8] «note the **Youtube version is really hit and miss as far as song quality. Spotify codes is a much better experience** if you happen to have a p[remium]...» — [redd.it/1nx62dz](https://redd.it/1nx62dz)

Тобто YouTube дає доступ усім, але платить за це якістю/консистентністю треків (кавери, лайви, зміщений старт, реміксовані заливки). Для БАЗ це не блокер, а конкретне завдання: **фрагмент має починатися там, де трек упізнаваний**, а не з нульової секунди — див. С7.

Ризик обриву посилань теж названо людьми:

> [7] «Keep in mind **whenever those songs leave spotify, those links won't work anymore.** Seems like a pretty short sighted decision by the designers.» — [redd.it/187pf0w](https://redd.it/187pf0w)

---

## С7. Що ламає темп гри — найкорисніший коментар усієї вибірки

> [98] *(топ-коментар треду на 327 апвоутів)* «Idk if youre taking feedback but, instead of **starting the song at the very start, maybe should start near the more iconic hooks**. Generally **a lot of time waste between rounds which made me close the tab**. Which is a shame because i love the concept but **UX needs work**.» — [redd.it/1swfugu](https://redd.it/1swfugu)

Дві конкретні речі, і обидві прямо стосуються MVP БАЗ:
1. **Звідки грати фрагмент.** CLAUDE.md каже «15–20 сек з випадкового треку», але не каже, з якої секунди. Це не деталь — з інтро трек не впізнається.
2. **Пауза між раундами вбиває гру швидше, ніж погана механіка.** Людина закрила вкладку, хоч концепт їй подобався.

Другий біль темпу — вже соціальний:

> [2] «I had the exact same problem playing Hitster with friends. **Half the time someone didn't know the song and the round kinda fell flat.**» — [redd.it/1rcew0r](https://redd.it/1rcew0r)

**Для БАЗ це прямий ризик:** плейліст поза мейнстрімом = більше треків, яких не знає ніхто = більше «провалених» раундів. Напруга §6 з research.md («немейнстрім vs для всіх») тут отримує механічний, а не лише маркетинговий вимір.

---

## С8. «Усі втикають у свої телефони» — заперечення проти самої топології БАЗ

> [1] «Most music trivia apps **turn the room into a bunch of people staring at their own phones**. I wanted the opposite: one host with a Siri Remote runs the show, everyone else just listens and shouts.» — [redd.it/1rcew0r](https://redd.it/1rcew0r)

Це слабкий за апвоутами, але концептуально гострий сигнал: телефон у кожного може працювати **проти** відчуття спільної кімнати. БАЗ частково захищений тим, що на баззері немає нічого, крім кнопки — але варто мати це на увазі як явну проєктну ціль, а не побічний ефект.

Протилежний запит теж є — люди хочуть **великий спільний екран**:

> [2] «Was looking for something I could play with a group today. **If this was an app I could cast to my TV would have been perfect.** I may try to cast my phone screen to it.» — [redd.it/1adhtbd](https://redd.it/1adhtbd)

---

## С9. Чому люди кидають продукт: SongPop зблизька

Прогалину «чому третина відгуків однозіркові» частково закрито — не текстами відгуків, а сабредітом гри.

**Продуктивність і збої.**
> [11] «Playing a party round this morning was **agonizing — took about 6-7 minutes to claim rewards**» · [10] «Games don't even load sometimes and **I got a loss from a game I already won**» · [7] «Game performance has been terrible the last few days. **Game is no fun at this rate**» — [redd.it/1gdmprv](https://redd.it/1gdmprv)

**Реклама як замок на контенті — і вона ламається.**
> [5] «Same issue, looks like it's permanent so **that'll free up some time for me**. Looks like it **only affects non plus people**. Now I can read books more 😂» — [redd.it/1vlnhxo](https://redd.it/1vlnhxo)
> Контекст поста: «I can't switch playlists using the watch ad option because it says "No available rewarded video now"». Тобто плейлисти замкнені за переглядом реклами, реклама не вантажиться — гра непридатна.

**Ненависть до примусової міграції на наступну версію.**
> [37] «If they end this **I'm done playing. Song pop 3 sucks and I hate it**» · [13] «If SongPop Classic is meeting the end of its 12 year run then absolutely I am done playing because **I detest SP3**» — [redd.it/1rczv85](https://redd.it/1rczv85)

**Для БАЗ:** прямий висновок для розділу «Явно поза скоупом» — реклама, що блокує контент, і збої завантаження вбивають саме **вечірковий** формат, де немає другої спроби: компанія просто перемикається на щось інше.

---

## С10. За що люди реально платять

**Платять — і платять багато разів.** Тред «Hitster Collection Update» — це фото десятків куплених коробок.
> «I think there are **146 Hitster sets** from different country's» [3] · «Nice! **Brazil just got its first Hitster** this week, in case you are considering collecting them all» [2] · «I have the urban hip hop and **want** the movie sound track» [2] — [redd.it/1r5fgxt](https://redd.it/1r5fgxt)

**Платять за привід, а не за доступ.** Один із найтепліших відгуків у вибірці:
> [2] «I love Hitster. **If you know music even just a little, you love this game.** It falls flat with either the really old or really young, but other than that everyone I've played it with loves it. I'm a fairly hardcore gamer, but next year **this game is going to break in my top 10**.» — [redd.it/1nx62dz](https://redd.it/1nx62dz)

**Але платять неохоче, коли є безкоштовна альтернатива.** Щойно каталог вичерпано, люди не докуповують — вони **друкують свій**. Це стеля готовності платити: гроші йдуть за коробку-привід, не за розширення контенту.

**Пейволи названі як причина будувати своє.**
> «...because the existing music quiz apps kept **annoying me with aggressive paywalls** and constant [ads]» — автор поста [redd.it/1tsttrl](https://redd.it/1tsttrl)
> Інший розробник: «made it **completely free with a tip jar**» — [redd.it/1s63htn](https://redd.it/1s63htn)

---

## С11. Привід і склад компанії — уривками

Мало, але вперше не з голови:

- **Регулярно, після роботи:** «friends at work who all really enjoy playing Hitster together **after work once a week**» — [redd.it/1sz3qlt](https://redd.it/1sz3qlt)
- **Родина, різні покоління:** «It's fun! **I have to play team with my kid though**, it's a wild mix of old and new songs» — [redd.it/mizb4x](https://redd.it/mizb4x) · «This is wonderful **for me and my family** to be able to play» — [redd.it/1adhtbd](https://redd.it/1adhtbd)
- **Подарунок:** «Never mind all that, is that game good? ... Think this could be a **Christmas pickup**» — [redd.it/187pf0w](https://redd.it/187pf0w)
- **Вікова межа названа гравцем:** «It **falls flat with either the really old or really young**» — [redd.it/1nx62dz](https://redd.it/1nx62dz), і окремо: «I'm 30 ... most songs used were made **before I was born**» — [redd.it/1swfugu](https://redd.it/1swfugu)

**Для §6 research.md:** маркетингове «20–99» від Hitster люди на практиці звужують самі. Аудиторія — не «всі», а «ті, хто знає музику хоча б трохи», і межа проходить по **збігу каталогу з віком**, а не по віку як такому. Для БАЗ це аргумент на користь власного плейліста: він автоматично влучає у вік компанії.

---

## Що ця сесія закрила і що ні

**Закрито або суттєво просунуто:**
- ~~№1–2 (нуль первинних даних / жодної живої людини)~~ — тепер є ~60 цитат реальних людей.
- ~~№3 (чому однозіркові SongPop)~~ — частково: продуктивність, реклама-замок, примусова міграція (С9).
- ~~№11 (чи потрібен свій плейліст)~~ — так, і мотив інший, ніж думали: вичерпання каталогу, а не нішевість смаку (С2).
- ~~№10 (чим слухають)~~ — частково: Spotify домінує, але Apple Music і «без Premium» — постійна причина випадати з гри (С4).

**Лишається [?] і не закривається Reddit'ом:**
- **Український контекст — повністю.** Жодного українського голосу; вся вибірка англомовна.
- **№9: чи є в аудиторії плейлисти саме на YouTube Music.** Знайдено одну людину, яка цього хоче. Це не дані про поширеність.
- **№11-емоційне: чи ризиковано показувати свій смак** (біль Б2). Reddit говорить про *вичерпання каталогу*, а не про *вразливість*. Головна емоційна гіпотеза БАЗ так і не підтверджена **ніким**.
- **№4–8: контекст вечірки** (як часто, скільки людей, що роблять зараз) — окремі уривки в С11, системних даних немає.
- **№18–19: ціни в Україні й чи платив би приватний хост** — не досліджувалось.
- **№21: жест «трясни телефоном»** — жодної згадки ніде.

---

## Три речі, які варто винести в рішення продукту

1. **Ніша зайнята безкоштовними аматорами (С1).** «Грай зі свого плейліста» більше не є диференціатором. Диференціатором лишається те, чого немає в жодного з 12 знайдених інструментів: **ротація ведучого як ритуал** і **мережевий баззер у вечірковому форматі**.
2. **Темп важливіший за механіку (С7).** Людина закрила вкладку через паузи між раундами, а не через правила. Це ставить «звідки починається фрагмент» і «скільки триває міжраундова пауза» в MVP-рішення, а не в поліш.
3. **Головна емоційна гіпотеза продукту (Б2, «свій смак під ударом») не має жодного підтвердження від людей.** Reddit хоче свій плейліст із прагматичної причини — щоб не набридло. Це не спростування Б2, але це означає, що весь копірайтинг і онбординг БАЗ зараз стоять на неперевіреному припущенні.
