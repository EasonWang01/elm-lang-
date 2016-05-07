# elm-lang 的中文手冊 

翻譯自  

https://github.com/elm-lang/elm-compiler

#目錄

1.[安裝](#安裝)

2.[elm工具介紹](#elm-工具)

3.[設定你的Editor的syntax](#編譯器的-elm-syntax)

4.[開始學習Elm](#開始學習elm)

5.[語言核心](#語言核心)

# 安裝

1.如果您使用Mac 或 Windows 可以直接點選以下連結進行安裝

http://elm-lang.org/install


2.如果您是使用linux OS 可以使用 npm installer 進行安裝
```
npm install -g elm
```

3.如果以上對您都不適用，您也可以選擇從souce去安裝，可參考以下連結

https://github.com/elm-lang/elm-platform#get-haskell-working



----

#elm 工具

接著會開始引導您使用Elm 與 Elm 之一系列工具.

我們假設您已安裝好Elm

####工具

Elm有一系列的工具可幫助您開發Elm程式，在您安裝好Elm時，他們會跟著安裝在您電腦上:

* [Elm](http://elm-lang.org/get-started#elm)

* [elm-package](http://elm-lang.org/get-started#elm-package)

* [elm-make](http://elm-lang.org/get-started#elm-make)

* [elm-repl](http://elm-lang.org/get-started#elm-repl)
 

以下分別介紹，他們的功能

####elm

elm 為啟動其他工具的方式. 試著打開 terminal 並輸入`elm`試試.

如果沒出現任何訊息，請先將以下路徑，加入環境變數

```
C:\Program Files (x86)\Elm Platform\0.16\bin
```

####elm-package

elm-package 是一個套件管理工具, 讓你可以簡單的發佈即安裝套件到Elm Package Catalog.

當你要開始一個新的Elm程式時, 執行:
```
elm package install
```

這將會安裝` elm-core package` 以即將會創造一個 Elm project的檔案: `elm-package.json`

 `elm-package.json` 用來寫一些關於套件相關的訊息，類似一個描述檔

以下為一些常用的 commands:

```
install: 安裝在 elm-package.json 所描述的套件
publish: 將你的 library 發佈到  Elm Package Catalog
bump: 根據 API changes 改變你的版本號碼
diff: 查看兩個 API 的差異
```


####elm-make

elm-make 是在命令列中執行，用來將elm程式編譯為HTML與Javascript. 一般都以此種方式來編譯elm的程式

當我們在編譯時(例如將: Main.elm)編譯為  HTML 檔案 (index.html), 你將會寫出以下指令:

```
elm make Main.elm --output=index.html
```

可用的附加 flags:
```
--warn: Prints warnings to improve code quality
```

####elm-repl

REPL 意思為 `read-eval-print-loop` 讓你可以執行一些簡單的 Elm 語句.  你可以從你的project引入一些程式碼到elm-repl進行測試 ， elm-repl 最終將會轉為javascript程式碼,所以在這之前你需要安裝好 node.js . 需要注意的是 elm-rep只提供 command line interface, browser 相關的 函式 將無法作用.

常用的 commands:

:help: 將會印出提示訊息
:exit: 離開REPL

####elm-reactor

elm-reactor 為Elm的互動式開發工具. 使用 elm-reactor 你可以不用先編譯程式就可以執行 Elm programs，
elm-reactor 還提供了 hot swapping 與 time travel debugging.(類似於redux開發時的功能)

執行 elm reactor時 將會執行一個 web server 於 `0.0.0.0:8000` 你可以開啟你的 browser 選擇你想要執行的程式去執行，
如果你想使用 elm-reactor 更進階的功能, 點擊左側在檔案名稱旁的 wrench ， 之後將會開啟檔案，並且在右方顯示一些功能欄位.

常用的 flags:

-a=<ADDRESS>: 改變 elm-reactor 執行時的ip位置

由於預設的位置 0.0.0.0 不是所有瀏覽器都支援，但我們建議使用` -a=localhost`


-p=<PORT>: 改變 elm-reactor執行時所監聽的PORT

以下為執行的例子
```
elm reactor -a=localhost
打開瀏覽器，輸入 localhost:8000.
```


以上即為elm tools的相關介紹，可以前往https://github.com/elm-lang查看

----

#編譯器的 elm syntax


[Atom](https://atom.io/packages/language-elm)

[Brackets](https://github.com/lepinay/elm-brackets)

[Emacs](https://github.com/jcollard/elm-mode)

[Light Table](https://github.com/rundis/elm-light)

[Sublime Text](https://github.com/deadfoxygrandpa/Elm.tmLanguage)

[Vim](https://github.com/lambdatoast/elm.vim)

[VS Code](https://github.com/sbrink/vscode-elm)

----

#開始學習Elm

##第一個Elm程式

最簡單學習Elm的方式，可從這個連結進入 [範例](http://elm-lang.org/examples). 或是可以試試Elm的[線上編輯器](http://elm-lang.org/try)
或是先前提到的[elm-reactor](https://github.com/elm-lang/elm-reactor)

##進階學習

在官網的 [documentation](http://elm-lang.org/docs) 頁面, 你可以找到許多學習Elm的資源

####1.如果你是剛開始學習Elm
建議你可以到 [Elm Complete Guide](http://elm-lang.org/guide/core-language)進行學習，
並且使用 elm-repl 及 Online Editor來幫助你學習。

####2.如果你想要觀看一些影片來學習
可以到[Pragmatics Studio's Elm tutorial](https://pragmaticstudio.com/elm)

####3.在你閱讀完 Elm Complete Guide後, 你可以接著閱讀
[Elm's Syntax](http://elm-lang.org/docs/syntax) 以及

[Elm's Style Guide](http://elm-lang.org/docs/style-guide). 

(需要注意的是，elm的語句是對縮排敏感的)(類似python)

####4.為了更了解如何開發一個大型的Elm程式，你可以閱讀
[Elm Architecture Tutorial](https://github.com/evancz/elm-architecture-tutorial/)

####5.你也可以到 
[cs223 Functional Programming course](https://www.classes.cs.uchicago.edu/archive/2015/winter/22300-1/Home.html) 
此為芝加哥大學的課程，裡面講了許多有關 Elm 與 純函式編程, 但該課程使用的是 Elm 0.14.1 或許有點跟最新版本的Elm有些差異，但不用擔心，
你可以隨時回來閱讀Elm的syntax與style-guide.

####6.更多的教學
例如 [Elm for the Frontend Right Now](http://bendyworks.com/elm-frontend-right-now/), 
[Checkboard Grid Tutorial](https://github.com/TheSeamau5/elm-checkerboardgrid-tutorial), 
[Building HTML by Parsing Parameters](http://blog.jessitron.com/2015/08/an-elm-example-reading-url-parameters.html) 
在reddit上的討論 [/r/elm](http://reddit.com/r/elm) 以及 [mailing list](https://groups.google.com/forum/?fromgroups#!forum/elm-discuss)


7.但最重要的是，看完後不要忘記自己寫code! 下面是一些簡單的程式，你可以開始試著練習

* 1.寫出一個會偵測你的滑鼠指標位於螢幕的左半邊或右半邊，並且在螢幕中央顯示(左方或右方)的程式。

* 2.寫出一個會在螢幕上隨機位置顯示小黑點的程式，並且帶有重設、暫停、繼續等按鈕

* 3.寫出一個輸入框，讓Gitgub使用者輸入後，可顯示名稱，avatar圖片，與程式語言清單

* 4.寫出一個貪食蛇遊戲(並且可顯示最高分數)


另外: 如果你在寫elm程式時陷入困境,可將你的問題於[mailing list](https://groups.google.com/forum/?fromgroups#!forum/elm-discuss)發問   或是到irc上的 #elm IRC, freenode.net頻道發問。


#語言核心

  [Values](#values)
  [Functions](#functions)
  [If Expressions](#if-expressions)
  [Lists](#list)
  [Tuples](#tuples)
  [Records](#records)
  
  
#Values

我們先來看一下，下面的例子
```
> "hello"
"hello"

> "hello" ++ "world"
"helloworld"

> "hello" ++ " world"
"hello world"
```
Elm 使用 (++) 來連接字串


Elm的數學部分和其他語言類似

```
> 2 + 3 * 4
14

> (2 + 3) * 4
20

和JavaScript不同， Elm 具有floating point division (/)和 integer division (//)，分別用來計算具有小數或只有整數部分

> 9 / 2
4.5

> 9 // 2
4

```
#Functions
讓我們寫一個 isNegative的函式， 其具有參數可接受數字，並且確認他是否小於零，並返回 True 或 False.
```
> isNegative n = n < 0
<function>

> isNegative 4
False

> isNegative -7
True

> isNegative (-3 * -4)
False

```
和JavaScript、Python、Java的函式寫法不同. 不使用逗點來分隔參數，而是使用空格。

所以 `(add(3,4))` 將為 `(add 3 4)`
此種作法將可避免一個函式的參數區塊具有許多逗點，當你習慣後，你會發現他看起來比較簡潔。 你可以使用 elm-html package 來理解。

#If Expressions
When you want to have conditional behavior in Elm, you use an if-expression.

> if True then "hello" else "world"
"hello"

> if False then "hello" else "world"
"world"
The keywords if then else are used to separate the conditional and the two branches so we do not need any parentheses or curly braces.

It is important to note that Elm does not have a notion of “truthiness” as in many dynamic languages, where numbers and strings and lists all can be used as boolean values. If we try it out, Elm will tell us that we need to work with a real boolean value.

Now let's make a function that tells us if a number is over 9000.

> over9000 powerLevel = \
|   if powerLevel > 9000 then "It's over 9000!!!" else "meh"
<function>

> over9000 42
"meh"

> over9000 100000
"It's over 9000!!!"
Using a backslash in the REPL lets us split things on to multiple lines. We use this in the definition of over9000 above. Furthermore, it is best practice to always bring the body of a function down a line. It makes things a lot more uniform and easy to read, so you want to do this with all the functions and values you define in normal code.
#List

#Tuples

#Records
