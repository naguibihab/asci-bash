Asci emoji generator to make the terminal a bit less boring. It also changes based on the day of the week.

Copy this into your .bash_profile or any other file your shell uses to load up

Add `export PROMPT_COMMAND=asci` if you want it to come up after every command

```
asci() {
	DOW=$(date +%u)

	mon[0]='(ノಠ益ಠ)ノ彡┻━┻ wheres my coffee!!'
	mon[1]='(╯°o°）╯︵ ┻━┻ I QUIT'
	mon[2]=' IM TIED OF THESE MODDAFOKIN SNAKES ON DIS MODDAFOKIN PLANE  ̿̿’̿’\̵͇̿̿\=(•̪●)=/̵͇̿̿/’̿̿ ̿ ̿ ̿ '
	mon[3]=' I hate you all t(-_-t)'
	mon[4]="NOOOOOOO  '(ᗒᗣᗕ)՞"
	mon[5]="Take this monday O=('-'Q)"
	mon[6]='u takin to me? U TAKIN TO ME? (ง'̀-'́)ง'
	mon[7]='shadap (¬_¬)'

	arr[0]='(つ◉益◉)つ eh dah kolo eh dah kolo'
	arr[1]='ᕙ(⇀‸↼‶)ᕗ wa7sh!!'
	arr[2]='mah man (☞ﾟ∀ﾟ)☞'
	arr[3]=' ヽ(゜～゜o)ノ '
	arr[4]='pew pew pew  ̿̿’̿’\̵͇̿̿\=(•̪●)=/̵͇̿̿/’̿̿ ̿ ̿ ̿ bang bang'
	arr[5]='eeyyy 乁( ⁰͡ Ĺ̯ ⁰͡ ) ㄏ fogetboutit'
	arr[6]='(•̪●)=/̵/’̿̿ ̿ ̿ ̿ ̿ bang bang'
	arr[7]='( ━☞´◔‿ゝ◔`)━☞ eyyyy'
	arr[8]='ur awesome (• ε •)'
	arr[9]='Hello there (◟ᅇ)◜'
	arr[10]='EXCITE! (｡☉౪ ⊙｡)'

	fri[0]='ITS FRIDAY ♪~ ᕕ(ᐛ)ᕗ'
	fri[1]='yis (•̀ᴗ•́)و ̑̑'
	fri[2]='TFIF \ (•◡•) /'
	fri[3]='٩(*❛⊰❛)～❤'
	fri[4]="psst it's friday ᶘ ◕ᴥ◕ᶅ"
	fri[5]='Do you know what today is ( ͡° ͜ʖ ͡°)'

	if [ $DOW -eq 5 ]; then
		rand=$[ $RANDOM % ${#fri[@]} ]
		echo ${fri[$rand]}
	elif [ $DOW -eq 1 ]; then
		rand=$[ $RANDOM % ${#mon[@]} ]
		echo ${mon{$rand}}
	else
		rand=$[ $RANDOM % ${#arr[@]} ]
		echo ${arr[$rand]}
	fi
}
```
