
```r
words <- readLines(url("http://dtkaplan.github.io/ScientificComputing/Syllabus/Daily/Day-07/word_list_moby_crossword-flat/word_list_moby_crossword.flat.txt"))
# Summary

length(words[grep("^.$", words)])
```

```
## [1] 0
```

```r
length(words[grep("^..$", words)])
```

```
## [1] 85
```

```r
length(words[grep("^...$", words)])
```

```
## [1] 908
```

```r
length(words[grep("^....$", words)])
```

```
## [1] 3686
```

```r
length(words[grep("^.....$", words)])
```

```
## [1] 8258
```

```r
length(words[grep("^......$", words)])
```

```
## [1] 14374
```

```r
length(words[grep("^.......$", words)])
```

```
## [1] 21727
```

```r
length(words[grep("^........$", words)])
```

```
## [1] 26447
```

```r
length(words[grep("^.........$", words)])
```

```
## [1] 16658
```

```r
length(words[grep("^..........$", words)])
```

```
## [1] 9199
```

```r
length(words[grep("^...........$", words)])
```

```
## [1] 5296
```

```r
length(words[grep("^............$", words)])
```

```
## [1] 3166
```

```r
length(words[grep("^.............$", words)])
```

```
## [1] 1960
```

```r
length(words[grep("^..............$", words)])
```

```
## [1] 1023
```

```r
length(words[grep("^...............$", words)])
```

```
## [1] 557
```

```r
length(words[grep("^................$", words)])
```

```
## [1] 261
```

```r
length(words[grep("^.................$", words)])
```

```
## [1] 132
```

```r
length(words[grep("^..................$", words)])
```

```
## [1] 48
```

```r
length(words[grep("^...................$", words)])
```

```
## [1] 16
```

```r
length(words[grep("^....................$", words)])
```

```
## [1] 5
```

```r
tail(words[grep("..................", words)], n = 100L)
```

```
##  [1] "absentmindednesses"    "adventitiousnesses"   
##  [3] "antiadministration"    "anticonservationist"  
##  [5] "antidiscrimination"    "apprehensivenesses"   
##  [7] "biodegradabilities"    "bloodthirstinesses"   
##  [9] "cantankerousnesses"    "characteristically"   
## [11] "chemotherapeutical"    "comprehensivenesses"  
## [13] "counteraccusations"    "counteraggressions"   
## [15] "counterdemonstration"  "counterdemonstrations"
## [17] "counterdemonstrator"   "counterdemonstrators" 
## [19] "counterinflationary"   "counterpropagation"   
## [21] "counterpropagations"   "counterretaliation"   
## [23] "counterretaliations"   "counterrevolutions"   
## [25] "countersuggestions"    "disinterestednesses"  
## [27] "electrocardiograms"    "electrocardiograph"   
## [29] "electrocardiographs"   "extraconstitutional"  
## [31] "feeblemindednesses"    "heterogenousnesses"   
## [33] "hydroelectricities"    "hyperaggressiveness"  
## [35] "hyperaggressivenesses" "hyperconscientious"   
## [37] "hypernationalistic"    "hypersensitiveness"   
## [39] "hypersensitivenesses"  "hypersensitivities"   
## [41] "inappropriatenesses"   "inconsideratenesses"  
## [43] "indispensabilities"    "industrializations"   
## [45] "interdenominational"   "interinstitutional"   
## [47] "internationalizing"    "interrelatednesses"   
## [49] "irreconcilabilities"   "irresponsibilities"   
## [51] "lightheartednesses"    "microminiaturization" 
## [53] "microminiaturizations" "miscellaneousnesses"  
## [55] "misinterpretations"    "misrepresentations"   
## [57] "multidenominational"   "nondiscriminations"   
## [59] "obstreperousnesses"    "perpendicularities"   
## [61] "postfertilizations"    "rehospitalizations"   
## [63] "remunerativenesses"    "representativeness"   
## [65] "representativenesses"  "simultaneousnesses"   
## [67] "straightforwardest"    "subclassifications"   
## [69] "subconsciousnesses"    "superintellectuals"   
## [71] "superintelligences"    "unscrupulousnesses"
```

```r
length(words[grep("^a", words)])
```

```
## [1] 6557
```

```r
length(words[grep("^b", words)])
```

```
## [1] 6848
```

```r
length(words[grep("^c", words)])
```

```
## [1] 10385
```

```r
words[grep("q[^u]", words)]
```

```
##  [1] "buqsha"  "buqshas" "faqir"   "faqirs"  "qaid"    "qaids"   "qindar" 
##  [8] "qindars" "qintar"  "qintars" "qiviut"  "qiviuts" "qoph"    "qophs"
```

```r

crossword <- function(x) {
    list <- grep(x, words)
    return(words[list])
}

crossword("b..t")
```

```
##    [1] "abaft"            "abattis"          "abattises"       
##    [4] "abattoir"         "abattoirs"        "abbatial"        
##    [7] "abbot"            "abbotcies"        "abbotcy"         
##   [10] "abbots"           "abettal"          "abettals"        
##   [13] "abetted"          "abetter"          "abetters"        
##   [16] "abetting"         "abettor"          "abettors"        
##   [19] "abiotic"          "ablate"           "ablated"         
##   [22] "ablates"          "ablating"         "ablation"        
##   [25] "ablations"        "ablative"         "ablatives"       
##   [28] "abluted"          "ablution"         "ablutions"       
##   [31] "aboiteau"         "aboiteaus"        "aboiteaux"       
##   [34] "abort"            "aborted"          "aborter"         
##   [37] "aborters"         "aborting"         "abortion"        
##   [40] "abortions"        "abortive"         "aborts"          
##   [43] "about"            "absorbent"        "abuttal"         
##   [46] "abuttals"         "abutted"          "abutter"         
##   [49] "abutters"         "abutting"         "abwatt"          
##   [52] "abwatts"          "acerbest"         "airboat"         
##   [55] "airboats"         "alabaster"        "alabasters"      
##   [58] "albeit"           "antiabortion"     "antibacterial"   
##   [61] "antibiotic"       "antibiotics"      "asbestic"        
##   [64] "asbestos"         "asbestoses"       "asbestus"        
##   [67] "asbestuses"       "babbitt"          "babbitted"       
##   [70] "babbitting"       "babbitts"         "backbitten"      
##   [73] "bacteria"         "bacterial"        "bacterin"        
##   [76] "bacterins"        "bacteriologic"    "bacteriological" 
##   [79] "bacteriologies"   "bacteriologist"   "bacteriologists" 
##   [82] "bacteriology"     "bacterium"        "baht"            
##   [85] "bahts"            "bait"             "baited"          
##   [88] "baiter"           "baiters"          "baith"           
##   [91] "baiting"          "baits"            "baltimore"       
##   [94] "bantam"           "bantams"          "banter"          
##   [97] "bantered"         "banterer"         "banterers"       
##  [100] "bantering"        "banters"          "bantling"        
##  [103] "bantlings"        "baptise"          "baptised"        
##  [106] "baptises"         "baptisia"         "baptisias"       
##  [109] "baptising"        "baptism"          "baptismal"       
##  [112] "baptisms"         "baptist"          "baptists"        
##  [115] "baptize"          "baptized"         "baptizer"        
##  [118] "baptizers"        "baptizes"         "baptizing"       
##  [121] "barbette"         "barbettes"        "bartend"         
##  [124] "bartended"        "bartender"        "bartenders"      
##  [127] "bartending"       "bartends"         "barter"          
##  [130] "bartered"         "barterer"         "barterers"       
##  [133] "bartering"        "barters"          "bartholomew"     
##  [136] "bartisan"         "bartisans"        "bartizan"        
##  [139] "bartizans"        "bast"             "bastard"         
##  [142] "bastardies"       "bastardize"       "bastardized"     
##  [145] "bastardizes"      "bastardizing"     "bastards"        
##  [148] "bastardy"         "baste"            "basted"          
##  [151] "baster"           "basters"          "bastes"          
##  [154] "bastile"          "bastiles"         "bastille"        
##  [157] "bastilles"        "basting"          "bastings"        
##  [160] "bastion"          "bastioned"        "bastions"        
##  [163] "basts"            "batt"             "battalia"        
##  [166] "battalias"        "battalion"        "battalions"      
##  [169] "batteau"          "batteaux"         "batted"          
##  [172] "batten"           "battened"         "battener"        
##  [175] "batteners"        "battening"        "battens"         
##  [178] "batter"           "battered"         "batterie"        
##  [181] "batteries"        "battering"        "batters"         
##  [184] "battery"          "battier"          "battiest"        
##  [187] "battik"           "battiks"          "batting"         
##  [190] "battings"         "battle"           "battled"         
##  [193] "battlefield"      "battlefields"     "battlement"      
##  [196] "battlements"      "battler"          "battlers"        
##  [199] "battles"          "battleship"       "battleships"     
##  [202] "battling"         "batts"            "battu"           
##  [205] "battue"           "battues"          "batty"           
##  [208] "bawtie"           "bawties"          "bawty"           
##  [211] "beat"             "beatable"         "beaten"          
##  [214] "beater"           "beaters"          "beatific"        
##  [217] "beatification"    "beatifications"   "beatified"       
##  [220] "beatifies"        "beatify"          "beatifying"      
##  [223] "beating"          "beatings"         "beatless"        
##  [226] "beatnik"          "beatniks"         "beats"           
##  [229] "bedtick"          "bedticks"         "bedtime"         
##  [232] "bedtimes"         "beet"             "beetle"          
##  [235] "beetled"          "beetles"          "beetling"        
##  [238] "beetroot"         "beetroots"        "beets"           
##  [241] "belt"             "belted"           "belting"         
##  [244] "beltings"         "beltless"         "beltline"        
##  [247] "beltlines"        "belts"            "beltway"         
##  [250] "beltways"         "bent"             "benthal"         
##  [253] "benthic"          "benthos"          "benthoses"       
##  [256] "bents"            "bentwood"         "bentwoods"       
##  [259] "berth"            "bertha"           "berthas"         
##  [262] "berthed"          "berthing"         "berths"          
##  [265] "best"             "bestead"          "besteaded"       
##  [268] "besteading"       "besteads"         "bested"          
##  [271] "bestial"          "bestialities"     "bestiality"      
##  [274] "bestiaries"       "bestiary"         "besting"         
##  [277] "bestir"           "bestirred"        "bestirring"      
##  [280] "bestirs"          "bestow"           "bestowal"        
##  [283] "bestowals"        "bestowed"         "bestowing"       
##  [286] "bestows"          "bestrew"          "bestrewed"       
##  [289] "bestrewing"       "bestrewn"         "bestrews"        
##  [292] "bestrid"          "bestridden"       "bestride"        
##  [295] "bestrides"        "bestriding"       "bestrode"        
##  [298] "bestrow"          "bestrowed"        "bestrowing"      
##  [301] "bestrown"         "bestrows"         "bests"           
##  [304] "bestud"           "bestudded"        "bestudding"      
##  [307] "bestuds"          "betta"            "bettas"          
##  [310] "betted"           "better"           "bettered"        
##  [313] "bettering"        "betterment"       "betterments"     
##  [316] "betters"          "betting"          "bettor"          
##  [319] "bettors"          "bhut"             "bhuts"           
##  [322] "biathlon"         "biathlons"        "biltong"         
##  [325] "biltongs"         "bint"             "bints"           
##  [328] "biota"            "biotas"           "biotic"          
##  [331] "biotical"         "biotics"          "biotin"          
##  [334] "biotins"          "biotite"          "biotites"        
##  [337] "biotitic"         "biotope"          "biotopes"        
##  [340] "biotron"          "biotrons"         "biotype"         
##  [343] "biotypes"         "biotypic"         "birth"           
##  [346] "birthdate"        "birthdates"       "birthday"        
##  [349] "birthdays"        "birthed"          "birthing"        
##  [352] "birthplace"       "birthplaces"      "birthrate"       
##  [355] "birthrates"       "births"           "bistate"         
##  [358] "bister"           "bistered"         "bisters"         
##  [361] "bistort"          "bistorts"         "bistouries"      
##  [364] "bistoury"         "bistre"           "bistred"         
##  [367] "bistres"          "bistro"           "bistroic"        
##  [370] "bistros"          "bitt"             "bitted"          
##  [373] "bitten"           "bitter"           "bittered"        
##  [376] "bitterer"         "bitterest"        "bittering"       
##  [379] "bitterly"         "bittern"          "bitterness"      
##  [382] "bitternesses"     "bitterns"         "bitters"         
##  [385] "bittier"          "bittiest"         "bitting"         
##  [388] "bittings"         "bittock"          "bittocks"        
##  [391] "bitts"            "bitty"            "blat"            
##  [394] "blatancies"       "blatancy"         "blatant"         
##  [397] "blate"            "blather"          "blathered"       
##  [400] "blathering"       "blathers"         "blats"           
##  [403] "blatted"          "blatter"          "blattered"       
##  [406] "blattering"       "blatters"         "blatting"        
##  [409] "blet"             "blether"          "blethered"       
##  [412] "blethering"       "blethers"         "blets"           
##  [415] "blite"            "blites"           "blithe"          
##  [418] "blithely"         "blither"          "blithered"       
##  [421] "blithering"       "blithers"         "blithesome"      
##  [424] "blithest"         "blitz"            "blitzed"         
##  [427] "blitzes"          "blitzing"         "blot"            
##  [430] "blotch"           "blotched"         "blotches"        
##  [433] "blotchier"        "blotchiest"       "blotching"       
##  [436] "blotchy"          "blotless"         "blots"           
##  [439] "blotted"          "blotter"          "blotters"        
##  [442] "blottier"         "blottiest"        "blotting"        
##  [445] "blotto"           "blotty"           "boat"            
##  [448] "boatable"         "boatbill"         "boatbills"       
##  [451] "boated"           "boatel"           "boatels"         
##  [454] "boater"           "boaters"          "boating"         
##  [457] "boatings"         "boatload"         "boatloads"       
##  [460] "boatman"          "boatmen"          "boats"           
##  [463] "boatsman"         "boatsmen"         "boatswain"       
##  [466] "boatswains"       "boatyard"         "boatyards"       
##  [469] "bobcat"           "bobcats"          "bobtail"         
##  [472] "bobtailed"        "bobtailing"       "bobtails"        
##  [475] "boite"            "boites"           "bolt"            
##  [478] "bolted"           "bolter"           "bolters"         
##  [481] "bolthead"         "boltheads"        "bolting"         
##  [484] "boltonia"         "boltonias"        "boltrope"        
##  [487] "boltropes"        "bolts"            "bombast"         
##  [490] "bombastic"        "bombasts"         "bontebok"        
##  [493] "bonteboks"        "boot"             "booted"          
##  [496] "bootee"           "bootees"          "booteries"       
##  [499] "bootery"          "booth"            "booths"          
##  [502] "bootie"           "booties"          "booting"         
##  [505] "bootjack"         "bootjacks"        "bootlace"        
##  [508] "bootlaces"        "bootleg"          "bootlegged"      
##  [511] "bootlegger"       "bootleggers"      "bootlegging"     
##  [514] "bootlegs"         "bootless"         "bootlick"        
##  [517] "bootlicked"       "bootlicking"      "bootlicks"       
##  [520] "boots"            "booty"            "bort"            
##  [523] "borts"            "borty"            "bortz"           
##  [526] "bortzes"          "boston"           "bostons"         
##  [529] "bott"             "bottle"           "bottled"         
##  [532] "bottleneck"       "bottlenecks"      "bottler"         
##  [535] "bottlers"         "bottles"          "bottling"        
##  [538] "bottom"           "bottomed"         "bottomer"        
##  [541] "bottomers"        "bottoming"        "bottomless"      
##  [544] "bottomries"       "bottomry"         "bottoms"         
##  [547] "botts"            "bout"             "boutique"        
##  [550] "boutiques"        "bouts"            "boxthorn"        
##  [553] "boxthorns"        "brat"             "brats"           
##  [556] "brattice"         "bratticed"        "brattices"       
##  [559] "bratticing"       "brattier"         "brattiest"       
##  [562] "brattish"         "brattle"          "brattled"        
##  [565] "brattles"         "brattling"        "bratty"          
##  [568] "brethren"         "brit"             "britches"        
##  [571] "brits"            "britska"          "britskas"        
##  [574] "britt"            "brittle"          "brittled"        
##  [577] "brittler"         "brittles"         "brittlest"       
##  [580] "brittling"        "britts"           "britzka"         
##  [583] "britzkas"         "britzska"         "britzskas"       
##  [586] "broth"            "brothel"          "brothels"        
##  [589] "brother"          "brothered"        "brotherhood"     
##  [592] "brotherhoods"     "brothering"       "brotherliness"   
##  [595] "brotherlinesses"  "brotherly"        "brothers"        
##  [598] "broths"           "brothy"           "browbeat"        
##  [601] "browbeaten"       "browbeating"      "browbeats"       
##  [604] "brut"             "brutal"           "brutalities"     
##  [607] "brutality"        "brutalize"        "brutalized"      
##  [610] "brutalizes"       "brutalizing"      "brutally"        
##  [613] "brute"            "bruted"           "brutely"         
##  [616] "brutes"           "brutified"        "brutifies"       
##  [619] "brutify"          "brutifying"       "bruting"         
##  [622] "brutish"          "brutism"          "brutisms"        
##  [625] "bumboat"          "bumboats"         "bunt"            
##  [628] "bunted"           "bunter"           "bunters"         
##  [631] "bunting"          "buntings"         "buntline"        
##  [634] "buntlines"        "bunts"            "burthen"         
##  [637] "burthened"        "burthening"       "burthens"        
##  [640] "burton"           "burtons"          "bust"            
##  [643] "bustard"          "bustards"         "busted"          
##  [646] "buster"           "busters"          "bustic"          
##  [649] "bustics"          "bustier"          "bustiest"        
##  [652] "busting"          "bustle"           "bustled"         
##  [655] "bustles"          "bustling"         "busts"           
##  [658] "busty"            "butt"             "buttals"         
##  [661] "butte"            "butted"           "butter"          
##  [664] "buttercup"        "buttercups"       "buttered"        
##  [667] "butterfat"        "butterfats"       "butterflies"     
##  [670] "butterfly"        "butterier"        "butteries"       
##  [673] "butteriest"       "buttering"        "buttermilk"      
##  [676] "butternut"        "butternuts"       "butters"         
##  [679] "butterscotch"     "butterscotches"   "buttery"         
##  [682] "buttes"           "butties"          "butting"         
##  [685] "buttock"          "buttocks"         "button"          
##  [688] "buttoned"         "buttoner"         "buttoners"       
##  [691] "buttonhole"       "buttonholes"      "buttoning"       
##  [694] "buttons"          "buttony"          "buttress"        
##  [697] "buttressed"       "buttresses"       "buttressing"     
##  [700] "butts"            "butty"            "bystander"       
##  [703] "bystanders"       "bystreet"         "bystreets"       
##  [706] "cabestro"         "cabestros"        "cablet"          
##  [709] "cablets"          "cabretta"         "cabrettas"       
##  [712] "calibrate"        "calibrated"       "calibrates"      
##  [715] "calibrating"      "calibration"      "calibrations"    
##  [718] "calibrator"       "calibrators"      "cambist"         
##  [721] "cambists"         "catboat"          "catboats"        
##  [724] "celebrate"        "celebrated"       "celebrates"      
##  [727] "celebrating"      "celebration"      "celebrations"    
##  [730] "celebrator"       "celebrators"      "celebrities"     
##  [733] "celebrity"        "cerebrate"        "cerebrated"      
##  [736] "cerebrates"       "cerebrating"      "cerebration"     
##  [739] "cerebrations"     "childbirth"       "childbirths"     
##  [742] "cobalt"           "cobaltic"         "cobalts"         
##  [745] "cobnut"           "cobnuts"          "cockboat"        
##  [748] "cockboats"        "combatted"        "combatting"      
##  [751] "combust"          "combusted"        "combustibilities"
##  [754] "combustibility"   "combustible"      "combusting"      
##  [757] "combustion"       "combustions"      "combustive"      
##  [760] "combusts"         "counterrebuttal"  "counterrebuttals"
##  [763] "cubist"           "cubistic"         "cubists"         
##  [766] "deadbeat"         "deadbeats"        "doublet"         
##  [769] "doublets"         "downbeat"         "downbeats"       
##  [772] "drabbest"         "drabbet"          "drabbets"        
##  [775] "dribblet"         "dribblets"        "driblet"         
##  [778] "driblets"         "drumbeat"         "drumbeats"       
##  [781] "dubieties"        "dubiety"          "dumbest"         
##  [784] "ebbet"            "ebbets"           "embattle"        
##  [787] "embattled"        "embattles"        "embattling"      
##  [790] "embitter"         "embittered"       "embittering"     
##  [793] "embitters"        "embrute"          "embruted"        
##  [796] "embrutes"         "embruting"        "eyebolt"         
##  [799] "eyebolts"         "faltboat"         "faltboats"       
##  [802] "ferryboat"        "ferryboats"       "fibrotic"        
##  [805] "filbert"          "filberts"         "filibuster"      
##  [808] "filibustered"     "filibusterer"     "filibusterers"   
##  [811] "filibustering"    "filibusters"      "fireboat"        
##  [814] "fireboats"        "firebrat"         "firebrats"       
##  [817] "fishboat"         "fishboats"        "flatboat"        
##  [820] "flatboats"        "flybelt"          "flybelts"        
##  [823] "flyboat"          "flyboats"         "foldboat"        
##  [826] "foldboats"        "freeboot"         "freebooted"      
##  [829] "freebooter"       "freebooters"      "freebooting"     
##  [832] "freeboots"        "frostbitten"      "gabbart"         
##  [835] "gabbarts"         "gadabout"         "gadabouts"       
##  [838] "gibbet"           "gibbeted"         "gibbeting"       
##  [841] "gibbets"          "gibbetted"        "gibbetting"      
##  [844] "gibbsite"         "gibbsites"        "giblet"          
##  [847] "giblets"          "gilbert"          "gilberts"        
##  [850] "glabrate"         "glibbest"         "gobbet"          
##  [853] "gobbets"          "goblet"           "goblets"         
##  [856] "gunboat"          "gunboats"         "halbert"         
##  [859] "halberts"         "hardboot"         "hardboots"       
##  [862] "heartbeat"        "heartbeats"       "hellbent"        
##  [865] "hereabout"        "hereabouts"       "hoofbeat"        
##  [868] "hoofbeats"        "houseboat"        "houseboats"      
##  [871] "howbeit"          "iceboat"          "iceboats"        
##  [874] "imbitter"         "imbittered"       "imbittering"     
##  [877] "imbitters"        "imbrute"          "imbruted"        
##  [880] "imbrutes"         "imbruting"        "incombustible"   
##  [883] "incumbent"        "incumbents"       "inkblot"         
##  [886] "inkblots"         "invertibrate"     "invertibrates"   
##  [889] "jackboot"         "jackboots"        "jackrabbit"      
##  [892] "jackrabbits"      "jailbait"         "johnboat"        
##  [895] "johnboats"        "keelboat"         "keelboats"       
##  [898] "kibbutz"          "kibbutzim"        "kingbolt"        
##  [901] "kingbolts"        "labiate"          "labiated"        
##  [904] "labiates"         "labret"           "labrets"         
##  [907] "lambast"          "lambaste"         "lambasted"       
##  [910] "lambastes"        "lambasting"       "lambasts"        
##  [913] "lambent"          "lambently"        "lambert"         
##  [916] "lamberts"         "layabout"         "layabouts"       
##  [919] "liberties"        "libertine"        "libertines"      
##  [922] "liberty"          "librate"          "librated"        
##  [925] "librates"         "librating"        "libretti"        
##  [928] "librettist"       "librettists"      "libretto"        
##  [931] "librettos"        "lifeboat"         "lifeboats"       
##  [934] "longboat"         "longboats"        "marabout"        
##  [937] "marabouts"        "motorboat"        "motorboats"      
##  [940] "nonabsorbent"     "noncombustible"   "numbest"         
##  [943] "oblate"           "oblately"         "oblates"         
##  [946] "oblation"         "oblations"        "oblatory"        
##  [949] "obliterate"       "obliterated"      "obliterates"     
##  [952] "obliterating"     "obliteration"     "obliterations"   
##  [955] "offbeat"          "offbeats"         "overbetted"      
##  [958] "overbetting"      "pigboat"          "pigboats"        
##  [961] "postpubertal"     "postpuberty"      "prebattle"       
##  [964] "precombustion"    "prepubertal"      "pubertal"        
##  [967] "puberties"        "puberty"          "rabbet"          
##  [970] "rabbeted"         "rabbeting"        "rabbets"         
##  [973] "rabbit"           "rabbited"         "rabbiter"        
##  [976] "rabbiters"        "rabbiting"        "rabbitries"      
##  [979] "rabbitry"         "rabbits"          "rabietic"        
##  [982] "rebait"           "rebaited"         "rebaiting"       
##  [985] "rebaits"          "rebaptize"        "rebaptized"      
##  [988] "rebaptizes"       "rebaptizing"      "rebirth"         
##  [991] "rebirths"         "rebuttal"         "rebuttals"       
##  [994] "rebutted"         "rebutter"         "rebutters"       
##  [997] "rebutting"        "rebutton"         "rebuttoned"      
## [1000] "rebuttoning"      "rebuttons"        "recumbent"       
## [1003] "redbait"          "redbaited"        "redbaiting"      
## [1006] "redbaits"         "responsiblities"  "responsiblity"   
## [1009] "resubmit"         "resubmits"        "resubmitted"     
## [1012] "resubmitting"     "riblet"           "riblets"         
## [1015] "ringbolt"         "ringbolts"        "riverboat"       
## [1018] "riverboats"       "robust"           "robuster"        
## [1021] "robustest"        "robustly"         "robustness"      
## [1024] "robustnesses"     "roundabout"       "rowboat"         
## [1027] "rowboats"         "runabout"         "runabouts"       
## [1030] "sabbat"           "sabbath"          "sabbaths"        
## [1033] "sabbatic"         "sabbats"          "sailboat"        
## [1036] "sailboats"        "seaboot"          "seaboots"        
## [1039] "sherbert"         "sherberts"        "showboat"        
## [1042] "showboats"        "slyboots"         "sobeit"          
## [1045] "sorbent"          "sorbents"         "speedboat"       
## [1048] "speedboats"       "steamboat"        "steamboats"      
## [1051] "stibnite"         "stibnites"        "stillbirth"      
## [1054] "stillbirths"      "subabbot"         "subabbots"       
## [1057] "subcategories"    "subcategory"      "subcutaneous"    
## [1060] "subcutes"         "subcutis"         "subcutises"      
## [1063] "subentries"       "subentry"         "sublate"         
## [1066] "sublated"         "sublates"         "sublating"       
## [1069] "sublet"           "sublethal"        "sublets"         
## [1072] "subletting"       "subliterate"      "submit"          
## [1075] "submits"          "submitted"        "submitting"      
## [1078] "subnetwork"       "subnetworks"      "suboptic"        
## [1081] "subset"           "subsets"          "subtitle"        
## [1084] "subtitled"        "subtitles"        "subtitling"      
## [1087] "subtotal"         "subtotaled"       "subtotaling"     
## [1090] "subtotalled"      "subtotalling"     "subtotals"       
## [1093] "superbest"        "surfboat"         "surfboats"       
## [1096] "symbiot"          "symbiote"         "symbiotes"       
## [1099] "symbiots"         "tablet"           "tableted"        
## [1102] "tableting"        "tabletop"         "tabletops"       
## [1105] "tablets"          "tabletted"        "tabletting"      
## [1108] "thereabout"       "thereabouts"      "thumbnut"        
## [1111] "thumbnuts"        "thunderbolt"      "thunderbolts"    
## [1114] "tolbooth"         "tolbooths"        "tollbooth"       
## [1117] "tollbooths"       "towboat"          "towboats"        
## [1120] "trabeate"         "tugboat"          "tugboats"        
## [1123] "ubieties"         "ubiety"           "umbrette"        
## [1126] "umbrettes"        "unbeaten"         "unbelt"          
## [1129] "unbelted"         "unbelting"        "unbelts"         
## [1132] "unbent"           "unbitted"         "unbolt"          
## [1135] "unbolted"         "unbolting"        "unbolts"         
## [1138] "unbutton"         "unbuttoned"       "unbuttoning"     
## [1141] "unbuttons"        "upbeat"           "upbeats"         
## [1144] "vertebrate"       "vertebrates"      "vibist"          
## [1147] "vibists"          "vibrate"          "vibrated"        
## [1150] "vibrates"         "vibrating"        "vibration"       
## [1153] "vibrations"       "vibrato"          "vibrator"        
## [1156] "vibrators"        "vibratory"        "vibratos"        
## [1159] "whereabouts"      "whitebait"        "whitebaits"      
## [1162] "workboat"         "workboats"
```

```r

crosswordPattern <- function(a, length) {
    ""
    grep(, words)
}
crosswordPattern("a", length = 4)
```

```
## Error: argument "pattern" is missing, with no default
```

```r

Scrabble <- function(b, a, n, k, e, r, s) {
    sam2 <- words[grep(b, words)]
    sam3 <- grep(a, sam2, value = TRUE)
    sam4 <- grep(n, sam3, value = TRUE)
    sam5 <- grep(k, sam4, value = TRUE)
    sam6 <- grep(e, sam5, value = TRUE)
    sam7 <- grep(r, sam6, value = TRUE)
    sam8 <- grep(s, sam7, value = TRUE)
    sam8
}
Scrabble("b", "a", "n", "k", "e", "r", "s")
```

```
##  [1] "backwardness"     "backwardnesses"   "bankers"         
##  [4] "bankruptcies"     "bearskin"         "bearskins"       
##  [7] "bedarkens"        "brackens"         "breakdowns"      
## [10] "breakfasting"     "breakings"        "cabinetmakers"   
## [13] "cabinetworks"     "counterblockades" "debarkations"    
## [16] "disembarkation"   "disembarkations"  "disembarking"    
## [19] "embarkations"     "ninebarks"        "pawnbrokers"     
## [22] "remarkableness"   "remarkablenesses" "riverbanks"      
## [25] "shrinkable"       "windbreaks"       "workableness"    
## [28] "workablenesses"
```



```r
words <- readLines(url("http://dtkaplan.github.io/ScientificComputing/Syllabus/Daily/Day-07/word_list_moby_crossword-flat/word_list_moby_crossword.flat.txt"))
```


crosswordPattern<- function(x){
 a<-c("a","b","c","d","e","f","g","h","i")
  if(x[1]=="1"){
    return(grep(x[1],words)
  }
   if(x[1]=="2"){
     grep(.x[1],words)
   } 
    if(x[1]=="3"){
      grep(..x[1],words)
    }
    if(x[1]=="4"){
      grep(...x[1],words)
    }
    if(x[1]=="5"){
      grep(....x[1],words)
    }
    if(x[1]=="6"){
      grep(.....x[1],words)
    }
    if(x[1]=="7"){
      grep(......x[1],words)
    }
    if(x[1]=="8"){
      grep(.......x[1],words)
    }
    if(x[1]=="9"){
      grep(........x[1],words)
    }
  if(x[2]=="1"){
    
  }
   if(x[2]=="2"){
     
   } 
    if(x[2]=="3"){
      
    }
    if(x[2]=="4"){
      
    }
    if(x[2]=="5"){
      
    }
    if(x[2]=="6"){
      
    }
    if(x[2]=="7"){
      
    }
    if(x[2]=="8"){
      
    }
    if(x[2]=="9"){
      
    }
  if(x[3]=="1"){
    
  }
   if(x[3]=="2"){
     
   } 
    if(x[3]=="3"){
      
    }
    if(x[3]=="4"){
      
    }
    if(x[3]=="5"){
      
    }
    if(x[3]=="6"){
      
    }
    if(x[3]=="7"){
      
    }
    if(x[3]=="8"){
      
    }
    if(x[3]=="9"){
      
    }
  
  if(length(words[1])==x[3])
  return(words[grep(a,words)],fixed=TRUE)
}
crosswordPattern(a=1,b=5,length=5)
