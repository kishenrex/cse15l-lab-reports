# Grep

## Option 1: -c
[Source link -c] (https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
This option causes the output to be a count of the lines that match a pattern, instead of the filename and lines containing the string

### Example 1:
```
$ find written_2/ > find-results.txt
$ grep -c "non-fiction" find-results.txt
```

### Output 1:
```
53
```

In example 1, we created a file called find-results.txt, which contains the paths of the files and subdirectories in the written_2 directory. 
The output is 53, suggesting there are 53 paths which contain the string "non-fiction". This would be useful to know how many paths contain a 
certain string in a directory.


### Example 2:
```
$ grep -c "urban" written_2/travel_guides/berlitz1/IntroMalaysia.txt
```

### Output 2:
```
5
```

In example 2, we search for the string "urban" in the IntroMalaysia text file, which results in an output of 5.
This suggests that the word "urban" appears on 5 lines in the IntroMalaysia text file. This could be useful to know on how many lines 
in a text file a certain string appears.


## Option 2: -r:
[source link -r] (https://linuxhandbook.com/grep-search-all-files-directories/)
This option will cause the command to search in all the files and subdirectories of the current directory, recursively.

### Example 3:
```
$ grep -r "Kuala" written_2/travel_guides/berlitz1/
```

### Output 3:
```
written_2/travel_guides/berlitz1/HistoryMalaysia.txt:        The lucrative tin mines of Kuala Lumpur in the State of
written_2/travel_guides/berlitz1/HistoryMalaysia.txt:        Resident-General of the Federation, with Kuala Lumpur as the
written_2/travel_guides/berlitz1/HistoryMalaysia.txt:        Malay Congress in Kuala Lumpur in 1939. In Singapore the following
written_2/travel_guides/berlitz1/HistoryMalaysia.txt:        naval base was left empty. Kuala Lumpur fell on 11 January 1942, and
written_2/travel_guides/berlitz1/HistoryMalaysia.txt:        with Kuala Lumpur over Malay privileges that Singapore, with its
written_2/travel_guides/berlitz1/IntroMalaysia.txt:        and Hindu shrines, and even the Petronas Twin Towers of Kuala Lumpur.
written_2/travel_guides/berlitz1/IntroMalaysia.txt:        capital, Kuala Lumpur, a modern city of broad expressways, skyscrapers,
written_2/travel_guides/berlitz1/IntroMalaysia.txt:        Even in Kuala Lumpur — as modern an urban sprawl as you
written_2/travel_guides/berlitz1/JungleMalaysia.txt:        Your best chance to see it is at the Ampang reserve near Kuala Lumpur
written_2/travel_guides/berlitz1/WhatToMalaysia.txt:        arts and crafts in Kuching, or check out the night markets of Kuala
written_2/travel_guides/berlitz1/WhatToMalaysia.txt:        airports in Kuala Lumpur, Johor Bahru, and Penang.    
written_2/travel_guides/berlitz1/WhatToMalaysia.txt:        traditional products are to be found in the museum shops in Kuala
written_2/travel_guides/berlitz1/WhatToMalaysia.txt:        Sarawak, and Sabah. In Kota Bharu or Kuala Terengganu, take a guided
written_2/travel_guides/berlitz1/WhatToMalaysia.txt:        sports clothes, and jeans in the street markets of Kuala
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        separate neighborhoods. This takes on a metropolitan dimension in Kuala
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        town, and Kuala Kangsar is the leisurely, royal state capital. The vast
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Kuala Lumpur
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        At times Kuala Lumpur — often referred to as KL — appears
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        modern Kuala Lumpur. But the more fascinating splendors of the past are
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        known officially as the Kuala Lumpur City Centre (KLCC), will be
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Menara Kuala Lumpur — or communications tower — which opened in July
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Day Trips from Kuala Lumpur
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        open-cast mining operation. South of Kuala Lumpur along Jalan Sungai
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Kuala Lumpur — The Genting and Fraser’s Hill — while the Cameron
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Nearest of the highland resort areas to Kuala Lumpur at 51
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        the second largest city in Malaysia, while Kuala Kangsar is the royal
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Kuala Kangsar
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Home to the Sultans of Perak for the past 500 years, Kuala
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Kuala Kangsar has long been famous for Malay College, set
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Another 30 minutes’ drive from Kuala Kangsar, this old
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        from Kuala Tembeling. (Buy your film, batteries, mineral water,
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        The headquarters at Kuala Tahan have a good range of 
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        through the rapids to Kuala Trenggan, returning to headquarters on
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        The highway from Kuala Lumpur and Selangor leads through
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        km (23 miles) east of Seremban on the Kuala Pilah Road. The ruler’s
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        than taking a flight from KL), ferries leave from Kuala Perlis and
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Kuala Kedah. There are overnight ferries from Penang and a twice-weekly
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        At the nearby port of Kuala Kedah, also a departure point
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        systems meet. Kuala Perlis, south of the state capital, Kangar, is the
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        their eggs at Cherating near Kuantan or to view the craftsmen at Kuala
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        just 40 minutes by air from Kuala Lumpur and only 30 km (19 miles) from
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        busy traffic of the capital, Kuala Terengganu. So far the economic
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        interstate bus to the Kuala Terengganu, which is generally the starting
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        from both Kuala Terengganu — where most of the resort companies have
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        booking offices — or by way of the fishing village of Kuala Besut, 45
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Pulau Perhentian’s islands. Before departing from Kuala Besut, a visit
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        strongly promoted by resort and travel agents in Kuala Terengganu,
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Kuala Terengganu
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        miles) from Kuala Terengganu, where visitors can witness different
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Around Kuala Terengganu
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Fifty-five kilometers (34 miles) inland from Kuala   
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        west of Kuala Terengganu. After trekking through the rainforest, you
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Marang is a fishing village 15 km (9 miles) south of Kuala
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        (38 miles) south of the Kuala Terengganu, is one of only six places in
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        in the region. Farther south is Kuala Dungun, predominantly Chinese in
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        accommodate between 250 and 300 visitors. These are located at Kuala
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Jasin, Batu Hampar, Upeh Guling, and Kuala Marong. You must employ a
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        It is 90 minutes by air from Kuala Lumpur to Kuching, the
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Kuala Baram along the majestic Baram River, or via Sibu, from Kapit or
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        Kuala Baram, at the mouth of the Batang Baram. From here, you take an
```

In example 3, we search for the word "Kuala" in the files in the berlitz1 subdirectory. The output is each filepath containing a line which has the "Kuala" string,
followed by the line containing the string. This could be useful if you have a word in many different files and you want to see each filename as well as the line
containing the string.

### Example 4:
```
$grep -r "Hello"
```

### Output 4:
```
written_2/non-fiction/OUP/Berk/CH4.txt:Children’s earliest efforts at make-believe also reveal how challenging they ﬁnd the task of detaching thought from reality. Initially, object substitutions are closely tied to the real things they represent. Toddlers between ages 1 1/2 and 2 generally use only realistic-looking objects while pretending—a toy telephone to talk into or a cup to drink from.9 Once, I handed a 21-month-old a small wooden block, put another to my ear, and called her on the phone: “Ring! Ring! Hello, Lynnay!” She responded by throwing down the block and turning to another activity. Yet when given a plastic replica of a push-button phone, Lynnay readily put the receiver to her ear and pretended to converse.
written_2/non-fiction/OUP/Berk/CH4.txt:As children engage in play talk, they not only build their vocabularies but correct one another’s errors, either directly or by demonstrating the acceptable way to speak. In one instance, a kindergartner enacting a telephone conversation said, “Hello, come to my house, please.” Her play partner quickly countered with appropriate telephone greeting behavior: “No, ﬁrst you’ve got to say ‘How are you? What are you doing?’”28
written_2/travel_guides/berlitz1/WhereToFrance.txt:        Saint-Wandrille, Le Bec-Hellouin, and Caen, culminating in their
```

In example 4, perform a search for the string "Hello" in all files and subdirectories from the current directory (docsearch/). This results in each filename outputted alongside the line containing the string. This could be useful if you don't want to specify a specific subdirectory to perform a search for a given string, and want to search in all subdirectories.

## Option 3: -h
[Source link -h] (https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
This command will cause the output to display the matching lines without the filenames.

### Example 5:
```
$ grep -rh "festival" written_2/travel_guides/berlitz1/
```

### Output 5:
```
        one of the world’s most important arts festivals. In addition, the
        task of organizing the first annual arts festival, which aimed to
        however, the main arts festival is only part of a veritable circus of
        And each year at festival time, Edinburgh willingly gives its streets
        festivals in spring, summer, and autumn all over the country. Even
        festivals.
        summer festivals, especially Roman ruins and medieval monasteries. In
        important festival in an expensive traditional costume, perhaps
        religious or patriotic festivals, prayers, traditions, or a summer
        Dublin Theater Festival in October. The festival is a showcase for
        the Calendar of Events for music festivals. The NCH also hosts jazz and
        separate festivals running concurrently. The major festivals discussed
        access websites for all the festivals at
        <www.edinburghfestivals.co.uk> (see tickets, page 127, for
        contact information for the various festivals).
        rapidly became one of the premier festivals of its kind in the world.
        center. Although the first festival was biased toward orchestral music,
        the modern festival has a comprehensive program of dance, music, opera,
        Dietrich brought their own inimitable style to the festival. Details of
        official festival and acts as a sometimes irreverent, loose collection
        official festival program but nevertheless decided to hold performances
        festival itself.
        summer festivals to see performances of the arts. The city is home to
        especially for children aged 8 to 15. During the summer festival
        with the Egyptian Tourist Board (see page tk) for exact festival dates
        Gifts and celebrations on the last three days of the festival, called
        new cultural festivals.
        January: Avoriaz (Savoie), science-fiction film festival;
        festival); Prades Festival Pablo Casals (chamber music; until
        festival; Paris, Festival d’Automne (music and theater; till December);
        Dijon, wine festival; Mont-Saint-Michel, procession and Mass for Saint
        and Chablis), wine festivals; Dijon, gastronomy fair; Cannes, dance
        Only in the country during patron saint day festivals or at a folk
        islands. Cultural festivals are one opportunity, but the better way is
        mostly based on saints’ days and religious festivals.
        February and also in the autumn festival at Pushkar (see page 209).
        festivals. Tuscany, San Gimignano and Lucca stage open-air concerts,
        to look long or hard for music festivals in most towns.
        it in early September at the Piedigrotta festival.
        A great open-air festival of jazz, pop, and rock music, the
        Italy’s most important jazz festival is held in Perugia in July, and
        music festivals (as well as theater and film) refer to the web site
        <www.italiafestival.it>. Click on the British flag for an English
        original versions). International film festivals are held at Venice and
        festivals has dwindled in the 20th century, but many continue for the
        May: Assisi: Calendimaggio Christian and pagan festival;
        festival of patron Santa Rosalia; Venice: Redentore regatta;
        Rimini: Festival of the Sea; Rome: Noantri street-festival in
        early January, when the Maroon people hold a major festival.
        matsuri (festivals) are much more than just fun for the community: for
        festival happening somewhere in Japan on any day of the year.
        Each region has its own festivals or variations on the
        major Buddhist temples. Buddhist festivals are usually fairly
        The real drama is at Shinto festivals. Some are austere
        festivals to galvanize community spirit and the local economy by
        Many festivals, though, are so spectacular that it is worth
        planning your trip. Note that since many festivals follow the lunar
        festivals and ceremonies taking place annually, this entire book
        sampling of large and small festivals. But when planning a visit, some
        January. In Japan, New Year’s Day is the big festival,
        February. The important setsubun festival marks the end of
        festival held at Tagata Jinja in Gifu Prefecture, north of Nagoya. This
        festivals held throughout Japan. The best place to view the spring
        time to catch on. This festival features giant carp streamers flying
        lanterns. Originally, the festival invoked the help of the gods against
        August is O-bon, a colorful and joyous national Buddhist festival
        other major festivals held annually around Japan, check the JNTO
        also hold annual festivals such as the popular Victorian Festival at
        is the centerpiece of the annual music festival, here in June (see
        Madeira celebrates four major festivals, among the best
        Flower Festival. This festival in late April or early May
        festival has earned a worldwide reputation. It jams Funchal’s hotels
        Several religious festivals also take place throughout the
        any of the major festivals (see page 79 and Calendar of Events, below).
        any of the levada paths highlighted in this book. The festivals with
        showcase of festivals of events and festivities throughout the year as
        festivals, as most of them are determined by lunar calendars which vary
        Thaipusam is the Hindu festival for Lord Murugan,
        during the special festivals that stage statewide contests (see page
        resorts. Maó has a charming outdoor cinema festival, Cinema a la
        during the festival season. During the summer, beside the flight of
        cathedral, or palace as a magnificent setting for festivals of music,
        festival’s opera and symphony concerts. From the top of the Colline
        with a festival in May.
        home of one of Europe’s greatest arts festivals, and all year round a
        and today it hosts major productions during the annual festival.
        choral recitals are held there during Aix’s summer music festival; the
        is the venue of the international film festival in May and the recorded
        music festival (MIDEM) in January. If you don’t mind crowds, both these
        festivals offer plenty of opportunities to gawk at the stars, but don’t
        festival is held on Place de la Liberté, the marketplace and a center
        festivals, Assumption Day on 15 August and Annunciation Day on 25
        festival on 29 August every year.
        holds a major festival at its Panagia Vrefokratoussa church on 15
        autumn festivals, when people traditionally seek out the hilltops, the
        Lover’s Rock, is the gathering place for the annual Maiden’s festival.
        monuments is the annual market-festival at Pushkar held each year in
        Mandir on Pichola, used for festivals; the Lakshmi Vilas Palace for
        annual festivals. East of the Bindu Sagar, the tenth-century
        old glory every October during the Dussehra festival, when the heir of
        Madurai festivals in April and May celebrate their marriage as a grand
        carry the deities through the streets during the festivals. Look out
        each spring with a tulip festival in the palace grounds.
        the Noantri (“We Others”) street festival of music, food, and
        fireworks, during the last two weeks of July. Another sort of festival
        the autumn grape-harvest festivals. The pope has his summer palace at
        use for summertime festivals — which seats 2,500 spectators.
        other parts of Japan. And their festivals, in an area without the usual
        Pride Celebration, a lively two-day festival and parade which has grown
        with several arts festivals taking place each year in July and August
        was once the scene of pageants, lively marketplaces, theater festivals,
        During festivals, the square springs to life with excitement and
        most attention during the Thaipusam festival celebrated in the early
        festival held in the early months of the year.
```

In example 5, we combine the `-r` and `-h` options to search for the string "festival" in all the files in the berlitz1 subdirectory. This could be useful
if you want to see the lines that contain a given string, without the filenames.

### Example 6:
```
$ grep -h "Malaysia" written_2/travel_guides/berlitz1/WhatToMalaysia.txt written_2/travel_guides/berlitz1/JungleMalaysia.txt
```

### Output 6:
```
        Malaysia. You will probably want to take time to shop for traditional
        vacation just sampling the local shopping scene. And Malaysia offers a
        A variety of goods are available throughout Malaysia. Large
        Malaysia’s tax havens are Pulau Langkawi and Labuan.
        over the peninsula and East Malaysia. KL’s Central Market gives you a
        pieces of indigenous workmanship in all of Malaysia. Really good ones
        Malaysia’s traditional entertainment is more often than not
        information can also be found at the Malaysian Tourist Information
        Malaysians love celebrating, and with so many different
        Christmas Day: Celebrated throughout Malaysia as a national
        To go to Malaysia without setting foot in the jungle would
        animals of the Malaysian jungle are not very conspicuous. Tigers and
        Malaysia are the smallest of their kind.
        Malaysian deer is the brown antlered sambar. Another shy creature, you
        Tiger. The few Malaysian tigers left roaming the peninsula
```

In example 6, we search for the string "Malaysia" in the WhatToMalaysia.txt and JungleMalaysia.txt files. The lines containing the string are outputted, without the filename. This command is useful if you want to search multiple files for a string, without wanting the filenames to be output as well.


## Option 4: -A n
[Source link -A n] (https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
This command will print the searched line and n lines after the result.

### Example 7:
```
$ grep -A1 "based" written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt
```

### Output 7:
```
Next to the fort is the pretty Legislature building with a classical façade painted bright lime green. Finished in 1874, the building was originally used as a barracks for troops based at the fort. Behind the fort and the Vendors Plaza is Emancipation Park, perhaps the one place in town where you can sit in the shade of the trees and enjoy the cooling sea breeze after your sightseeing and shopping. The park was named to commemorate the freeing of the slaves in 1848. Across Tolbod Gade is the Tourist Information Office, where you can pick up maps and other information. On the northern corner of Tolbod Gade is the main post office. Make your way in that direction, but don’t be tempted to turn right and head for the stores just yet. Take the steps to Kongens Gade, which is the street behind the Lutheran Church. The steps climb onto the steep hill that has many of the oldest and most important buildings of Danish Charlotte Amalie. The family houses of the merchants and civil servants where built high on this rise — named Government Hill — to take advantage of the cooling breeze. Kongens Gade itself has several buildings dating back to the late 18th and early 19th centuries. Hotel 1829, named for the year in which it was built, sits amid other fine homes. Walk past Hotel 1829 and pause at the steps beside it, which climb higher onto Government Hill. These are the 99 Steps, one of a series built by the Danes in the mid 1700s to allow pedestrian access to the town below. The 99 Steps are the longest in town, but whoever named the flight must have become tired toward the end and miscounted — there are in fact 103.
Before climbing the steps, make a small detour farther along Kongens Gade, past the Lutheran Parsonage (1725), to reach Government House, an archetypal colonial mansion. Now the office for the Governor of the USVIs, this 1867 structure was originally used for meetings of the Danish Colonial Council; it was totally renovated in 1974. Nearby is Seven Arches House Museum, once the home of a Danish master craftsman. The house has a “welcoming arms” staircase — fashionable in the 18th century — leading to the entrance. Renovated and filled with period furniture, walking through it is a step back in time.
```

In example 7, we search for the string "based" in the PuertoRico-WhereToGo.txt file. We get the searched line, as well as 1 line additional after that. This could be useful to find a specific word in a file, and have additional lines after that printed as well to give additional context.


### Example 8:
```
$ grep -rA2 "Fabulous"
```

### Output 8:
```
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt:Fabulous beaches, dramatic dunes, fragile salt marshes, and brilliant light have long drawn people, particularly artists to Cape Cod, “the bare and bended arm of Massachusetts.”
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt-In summer, it is incredibly crowded, and so if you can, you should avoid the Friday evening mass exodus, (see page 105) and visit during the week or off-season when it’s only an hour from Boston to Sandwich, the nearest town on the Cape. With so many alluring inns, however, why not plan to stay overnight, but make sure to reserve in advance. Provincetown is right at the end of the Cape and in summer can most easily be reached from Boston via the ferry operated by Bay State Cruise Company (Tel. 748-1428).       
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt-The most alluring section of the Cape is its north shore and “upper arm.” Beaches vary. The sheltered Cape Cod Bay beaches on the north shore are transformed into mud flats when the tide is out. The spectacular East Coast Atlantic beaches can have a strong undertow. On a sunny summer’s day parking lots at the latter fill up fast; at many beaches visitors need a parking permit, which can be obtained from the town hall.
```

In example 8, we combine the `r` and `-A n` commands to search for the string "Fabulous" and print out this line and the following 2 lines, as well as the filename, searching through all files and subdirectories from the current directory. This could be useful to find a given string and getting additional context for that string, across many files, to see how the word usage varies between files. 

