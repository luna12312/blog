## Common Password Patterns in the Wild: An Analysis for Better Cracking Strategies

The effectiveness of password brute-forcing heavily relies on the quality of the wordlist used. To achieve more efficient results in practical scenarios, considerable time has been invested in analyzing password structures, leading to this article. Passwords serve as an authentication mechanism, and security best practices dictate that they should be complex and unique to prevent attackers from successfully guessing them through enumeration within an acceptable timeframe. However, reality often diverges from this ideal. The human element inevitably leads to the creation and use of weak passwords.

Furthermore, in actual password cracking attempts, it's noticeable that the types of commonly used passwords can differ based on the role or type of account being targeted. Regardless, to make them memorable, most passwords are a reflection of certain real-life aspects projected into the virtual world.

### Common Patterns in General User Account Passwords

Taking publicly available password datasets, primarily from Chinese users, as an example, statistical analysis reveals that common weak passwords generally consist of the following elements:

1.  **Keyboard Proximity:** Patterns based on the spatial arrangement of characters on a keyboard.
2.  **Personal Information:** Family members' birthdays, phone numbers, or names.
3.  **Emotional Vocabulary:** Words or phrases expressing feelings or sentiments.
4.  **Auspicious or Catchy Numbers:** Numbers considered lucky or those that are easy to recall.

#### 1. Analysis of User Password Constructions

A review of password datasets shows that a vast majority of passwords exhibit security vulnerabilities. In the common constructions detailed below, the more a password uses popular, generic terms, the easier it is to match with dictionary attacks. Similarly, passwords incorporating personal information are more susceptible to social engineering dictionary attacks. In essence, all these patterns present security risks.

**1.1 Name + (Optional Connector) + Numbers**

This pattern involves variations of personal names combined with numbers such as birthdays, phone numbers, "lucky" numbers, or simple sequences.

* Examples (using "John Doe" as a sample name, with "jd" as initials):
    * `johndoe`
    * `johndoejohndoe`
    * `johndoe20210814` (Name + full date)
    * `johndoe0814` (Name + month/day)
    * `jd20210814` (Initials + full date)
    * `jd0814~~` (Initials + month/day + symbols)
    * `jd15551234567` (Initials + example phone number)
    * `johndoe9876` (Name + sequential numbers)
    * `johndoe@2333` (Name + symbol + common slang number; "2333" often signifies laughter in Chinese internet slang)
    * `johndoe2333`
    * `johndoe666` ("666" can signify "cool" or "smooth" in Chinese internet slang, or simply be repetitive)
    * `jd666888` (Initials + lucky/repetitive numbers; "8" is often considered lucky in Chinese culture)

**1.2 Name + (Optional Connector) + Characters**

This involves variations of names combined with characters, often adjacent keys on the keyboard, short phrases, or simple words.

* Examples:
    * `johndoeqwe123` (Name + common keyboard sequence)
    * `johndoe123` (Name + simple number sequence)

**1.3 Personal Attributes**

These are passwords composed directly of standalone personal information.

* Examples:
    * `15551234567` (An example phone number)
    * `20210814` (A date, like a birthday or anniversary)
    * `iloveyou1314` (A common romantic phrase. In Chinese, `woaini` means "I love you," and `1314` sounds like "forever" – *yīshēngyīshì*.)

**1.4 Keyboard Spatial Layouts**

Passwords are frequently derived from the physical layout of keys, primarily on standard computer keyboards (QWERTY) and mobile phone 9-key (T9-style) numeric keypads.

* Examples:
    * `123456`
    * `qq123456`
    * `111111`
    * `1q2w3e4r` (Top row letters)
    * `qwe123`
    * `zxc123456`
    * `88888888`
    * `1598753` (Numeric keypad pattern)
    * `741258` (Numeric keypad pattern)
    * `a123456789`

**1.5 Short Phrases**

Many passwords consist of highly emotional words or phrases, including terms of endearment, profanity, expressions related to celebrity fandom, and more.

* Examples:
    * `wife520` (In Chinese, `laopo` means "wife," and `520` sounds like "I love you" – *wǒ ài nǐ*.)
    * `love5201314` (Combines "love" with the numeric sound-alikes `520` and `1314`.)
    * `loveyou1314`
    * `mypassword` (Or the Chinese Pinyin `wodemima`)
    * `serialno89757` (Or the Chinese Pinyin `bianhao89757`)

#### 2. Statistical Overview of Common Weak Passwords

The following is a sample list of the top 200 weak passwords and their frequencies, derived from a publicly available dataset (largely reflecting habits of Chinese users). This illustrates the prevalence of the patterns discussed. Note that some entries include Pinyin (Romanized Chinese) names or phrases.

| Count  | Password         | Notes (if applicable)                                    |
| :----- | :--------------- | :------------------------------------------------------- |
| 224979 | `123456`         |                                                          |
| 62064  | `123456789`      |                                                          |
| 58345  | `111111`         |                                                          |
| 36464  | `123123`         |                                                          |
| 29223  | `000000`         |                                                          |
| 22532  | `5201314`        | Numeric sound-alike for "I love you forever" (Chinese)   |
| 16103  | `aaaaaa`         |                                                          |
| 15617  | `a123456`        |                                                          |
| 10602  | `123321`         |                                                          |
| 8229   | `1314520`        | Numeric sound-alike for "Forever I love you" (Chinese)   |
| 8217   | `7758521`        | Likely a numeric pattern or sound-alike                  |
| 7122   | `123456a`        |                                                          |
| 7076   | `12345678`       |                                                          |
| 6793   | `1234567890`     |                                                          |
| 6663   | `wangyut2`       | Pinyin name (e.g., Wang Yu) + characters               |
| 6377   | `123123123`      |                                                          |
| 6208   | `woaini`         | Pinyin for "I love you"                                  |
| 5798   | `1234567`        |                                                          |
| 5694   | `123`            |                                                          |
| 4761   | `112233`         |                                                          |
| 4729   | `11111111`       |                                                          |
| 4673   | `9958123`        | Likely numeric pattern                                   |
| 4468   | `zxcvbnm`        | Bottom row letters (QWERTY)                              |
| 4459   | `qq123456`       | "qq" is a popular Chinese messenger                      |
| 4421   | `666666`         |                                                          |
| 4355   | `5211314`        | Numeric sound-alike for "I love you forever" (Chinese)   |
| 4340   | `7758258`        | Likely numeric pattern                                   |
| 4158   | `123654`         |                                                          |
| 4136   | `hm9958123`      | Initials/Pinyin + numbers                                |
| 3979   | `a123456789`     |                                                          |
| 3947   | `asdasd`         | Keyboard pattern                                         |
| 3825   | `147258369`      | Numeric keypad pattern                                   |
| 3754   | `520520`         | Numeric sound-alike for "I love you, I love you" (Chinese) |
| 3688   | `110110`         | Common emergency number in China (110) repeated        |
| 3661   | `woaini1314`     | "I love you forever" (Pinyin + numeric)                  |
| 3605   | `100200`         |                                                          |
| 3273   | `1111111`        |                                                          |
| 2880   | `asd123`         |                                                          |
| 2813   | `147258`         | Numeric keypad pattern                                   |
| 2802   | `a123123`        |                                                          |
| 2770   | `123456789a`     |                                                          |
| 2715   | `q123456`        |                                                          |
| 2713   | `159357`         | Numeric keypad pattern                                   |
| 2653   | `159753`         | Numeric keypad pattern                                   |
| 2594   | `00000000`       |                                                          |
| 2531   | `888888`         | "8" is often considered lucky in Chinese culture         |
| 2480   | `654321`         |                                                          |
| 2475   | `121212`         |                                                          |
| 2422   | `qwe123`         |                                                          |
| 2386   | `qwertyuiop`     | Top row letters (QWERTY)                                 |
| 2375   | `asdfghjkl`      | Home row letters (QWERTY)                                |
| 2333   | `123qwe`         |                                                          |
| 2291   | `1314521`        | Numeric sound-alike for "Forever I love you" (Chinese)   |
| 2232   | `789456123`      | Numeric keypad pattern                                   |
| 2222   | `88888888`       |                                                          |
| 2209   | `123000`         |                                                          |
| 2191   | `liuchang`       | Pinyin name (e.g., Liu Chang)                            |
| 2088   | `321321`         |                                                          |
| 2070   | `qazwsx`         | Left-hand keyboard pattern (QWERTY)                      |
| 2012   | `asd123456`      |                                                          |
| 1997   | `qqqqqq`         |                                                          |
| 1947   | `aa123456`       |                                                          |
| 1940   | `z123456`        |                                                          |
| 1913   | `987654321`      |                                                          |
| 1778   | `456852`         | Numeric keypad pattern                                   |
| 1766   | `521521`         | Numeric sound-alike related to "I love you" (Chinese)    |
| 1765   | `woaini123`      | "I love you" (Pinyin) + numbers                          |
| 1717   | `woaini520`      | "I love you" (Pinyin + numeric sound-alike)              |
| 1679   | `741852963`      | Numeric keypad pattern                                   |
| 1654   | `xx123456`       |                                                          |
| 1625   | `qweqwe`         |                                                          |
| 1622   | `qwerty`         |                                                          |
| 1618   | `abc123`         |                                                          |
| 1610   | `222222`         |                                                          |
| 1596   | `1qaz2wsx`       | Keyboard pattern                                         |
| 1571   | `qweasdzxc`      | Keyboard pattern (rows)                                  |
| 1571   | `31415926`       | Digits of Pi                                             |
| 1567   | `123456aa`       |                                                          |
| 1555   | `zxc123`         |                                                          |
| 1544   | `110120`         | Common emergency numbers in China (110, 120)             |
| 1539   | `1q2w3e4r`       | Top row letters (QWERTY)                                 |
| 1535   | `qazwsxedc`      | Left-hand keyboard pattern (QWERTY)                      |
| 1535   | `111222`         |                                                          |
| 1523   | `123456qq`       |                                                          |
| 1502   | `555555`         |                                                          |
| 1446   | `qwe123456`      |                                                          |
| 1418   | `999999`         |                                                          |
| 1416   | `456123`         |                                                          |
| 1408   | `iloveyou`       |                                                          |
| 1401   | `woaini521`      | "I love you" (Pinyin + numeric, 521 also means ILY)      |
| 1382   | `a5201314`       |                                                          |
| 1378   | `12301230`       |                                                          |
| 1373   | `abc123456`      |                                                          |
| 1362   | `w123456`        |                                                          |
| 1359   | `789456`         | Numeric keypad pattern                                   |
| 1357   | `1111111111`     |                                                          |
| 1357   | `0000000`        |                                                          |
| 1347   | `caonima`        | Pinyin for a common profanity                            |
| 1336   | `a111111`        |                                                          |
| 1326   | `zxcvbnm123`     |                                                          |
| 1321   | `1234560`        |                                                          |
| 1312   | `123654789`      |                                                          |
| 1310   | `123456q`        |                                                          |
| 1310   | `1`              |                                                          |
| 1306   | `102030`         |                                                          |
| 1303   | `1230123`        |                                                          |
| 1282   | `asdfgh`         | Home row                                                 |
| 1279   | `753951`         | Numeric keypad pattern                                   |
| 1257   | `asdasdasd`      |                                                          |
| 1226   | `123698745`      | Numeric keypad pattern                                   |
| 1204   | `201314`         | Numeric sound-alike for "Love you forever" (Chinese)     |
| 1199   | `7758520`        | Likely numeric pattern or sound-alike                  |
| 1196   | `333333`         |                                                          |
| 1189   | `zhang123`       | Pinyin name (e.g., Zhang) + numbers                      |
| 1181   | `12345`          |                                                          |
| 1181   | `1234`           |                                                          |
| 1179   | `0123456789`     |                                                          |
| 1175   | `584520`         | Numeric sound-alike (Chinese)                            |
| 1130   | `123123a`        |                                                          |
| 1122   | `aini1314`       | Pinyin for "Love you forever" (shortened `woaini`)       |
| 1108   | `123456abc`      |                                                          |
| 1094   | `25257758`       | Likely numeric pattern                                   |
| 1064   | `a000000`        |                                                          |
| 1044   | `qweasd`         | Keyboard pattern                                         |
| 1020   | `134679`         | Likely numeric pattern                                   |
| 1004   | `111111111`      |                                                          |
| 1003   | `741852`         | Numeric keypad pattern                                   |
| 1000   | `95368452`       | Likely numeric pattern                                   |
| 999    | `147852369`      | Numeric keypad pattern                                   |
| 996    | `wocaonima`      | Pinyin for a common profanity                            |
| 994    | `qaz123`         |                                                          |
| 992    | `5845201314`     | Numeric sound-alike combination (Chinese)                |
| 987    | `963852741`      | Numeric keypad pattern                                   |
| 985    | `1q2w3e`         |                                                          |
| 982    | `7777777`        |                                                          |
| 975    | `1111`           |                                                          |
| 952    | `147852`         | Numeric keypad pattern                                   |
| 951    | `101010`         |                                                          |
| 942    | `woainima`       | Pinyin for "I love your mom" (often offensive)           |
| 936    | `0000000000`     |                                                          |
| 917    | `q123456789`     |                                                          |
| 916    | `zxc123456`      |                                                          |
| 916    | `as123456`       |                                                          |
| 909    | `zzzzzz`         |                                                          |
| 905    | `456456`         |                                                          |
| 899    | `qq123123`       |                                                          |
| 882    | `456789`         |                                                          |
| 879    | `1233211234567`  |                                                          |
| 871    | `123456asd`      |                                                          |
| 856    | `123789`         |                                                          |
| 850    | `xuliang`        | Pinyin name (e.g., Xu Liang)                             |
| 839    | `3344520`        | Numeric sound-alike (Chinese)                            |
| 821    | `woaiwojia`      | Pinyin for "I love my family"                            |
| 816    | `qq5201314`      |                                                          |
| 810    | `111111a`        |                                                          |
| 805    | `123456123`      |                                                          |
| 802    | `1q2w3e4r5t`     | Top row letters (QWERTY)                                 |
| 795    | `963852`         | Numeric keypad pattern                                   |
| 793    | `7895123`        | Numeric keypad pattern                                   |
| 787    | `951753`         | Numeric keypad pattern                                   |
| 786    | `5201314a`       |                                                          |
| 777    | `0123456`        |                                                          |
| 775    | `778899`         |                                                          |
| 775    | `211314`         | Numeric sound-alike (Chinese)                            |
| 773    | `buzhidao`       | Pinyin for "I don't know"                                |
| 763    | `a123456a`       |                                                          |
| 761    | `abcd1234`       |                                                          |
| 761    | `321654`         |                                                          |
| 760    | `asdfasdf`       |                                                          |
| 757    | `zxczxc`         |                                                          |
| 745    | `wang123`        | Pinyin name (e.g., Wang) + numbers                       |
| 739    | `xiaoxiao`       | Common Pinyin given name (reduplicated)                  |
| 738    | `yangyang`       | Common Pinyin given name (reduplicated)                  |
| 732    | `5845211314`     | Numeric sound-alike combination (Chinese)                |
| 731    | `010203`         |                                                          |
| 726    | `windows`        |                                                          |
| 724    | `11223344`       |                                                          |
| 720    | `password`       |                                                          |
| 719    | `020332007051`   | Likely a long number, potentially an ID or phone number  |
| 711    | `789789`         |                                                          |
| 706    | `mm123123`       | "mm" can be Pinyin for "meimei" (younger sister) etc.    |
| 706    | `a1314520`       |                                                          |
| 703    | `11111`          |                                                          |
| 702    | `131421`         | Numeric sound-alike (Chinese)                            |
| 702    | `1234qwer`       |                                                          |
| 702    | `123456789q`     |                                                          |
| 695    | `123abc`         |                                                          |
| 692    | `12345678910`    |                                                          |
| 683    | `aa123123`       |                                                          |
| 680    | `a12345`         |                                                          |
| 676    | `q1w2e3r4`       | Keyboard pattern                                         |
| 664    | `110120119`      | Combination of Chinese emergency numbers (110,120,119)    |
| 653    | `5201314520`     |                                                          |
| 649    | `qaz123456`      |                                                          |
| 648    | `123qweasd`      |                                                          |
| 648    | `0000`           |                                                          |
| 640    | `584521`         | Numeric sound-alike (Chinese)                            |
| 640    | `123321123`      |                                                          |
| 640    | `111222333`      |                                                          |
| 637    | `123456987`      |                                                          |

*Note: Many numeric sequences in the list gain additional meaning in Chinese due to phonetic similarities (e.g., `520` sounds like `wǒ ài nǐ` or "I love you"; `1314` sounds like `yīshēngyīshì` or "forever"). Pinyin entries are Romanized spellings of Chinese words or names.*

### 3. Considerations for Password Cracking

Two primary approaches can be considered:

**3.1 Targeting Individuals (Natural Persons)**

1.  **Initial Attack:** Attempt a dictionary attack using common weak passwords applicable to general users.
2.  **Follow-up:** Employ a social engineering dictionary tailored to the individual.
    * A tool for generating social engineering dictionaries can be found at: [https://github.com/aplyc1a/RainCode](https://grave-blow.com/LbNwO6)

**3.2 Targeting Websites/Systems**

* **Broad Attack:** For each user account on the target system, attempt to crack passwords using a list of common weak passwords.

This analysis highlights the persistent issue of weak passwords and underscores the importance of robust password policies and user education to mitigate these common vulnerabilities.
