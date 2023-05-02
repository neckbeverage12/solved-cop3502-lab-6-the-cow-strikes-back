Download Link: https://assignmentchef.com/product/solved-cop3502-lab-6-the-cow-strikes-back
<br>
<h1> Overview</h1>

This lab’s purpose is to provide students with experience in inheritance of classes and working with multiplace classes. It is recommended that students use command line tools and editors for this lab (though it is not strictly speaking required). This lab will require students to build on their previous lab experience, in which a version of the cowsay utility was created.




<h1>Specification</h1>

Students will update the driver program class (Cowsay) and also create two new classes – Dragon and IceDragon. The Dragon class just extend the Cow class, and IceDragon must be derived from Dragon. As before, HeiferGenerator.java is provided for you – but updated to handle the new Dragon class and its subtypes. (Please refer to specification for previous lab for a refresher.) <u>Students may implement protected attributes and</u> <u>methods if they chose to do so.</u> This is not required – it is purely optional. No public attributes / methods should be added to the specification!




<h2>Cowsay Class (Program Driver)</h2>

Your program must accept <u>command line arguments</u> as follows:




java cowsay -l                                Lists the available cows

java cowsay MESSAGE Prints out the MESSAGE using the default COW java cowsay -n COW MESSAGE Prints out the MESSAGE using the specified COW




In addition, this version of the utility handles a special set of Cow-derived Dragon classes (and its subclasses).  Whenever a dragon-type cow is selected, the display of the message must be followed by a line stating whether or not the dragon is fire-breathing:

<table width="707">

 <tbody>

  <tr>

   <td width="414">&gt;java Cowsay -n dragon Fiery RAWR Fiery RAWR\|___/|       /  //|\/0  0  __   /  // |  /     /  /_ /   //  |    \_^_’/   /_   //   |      //_^_/     /_ //    |        ( //) |         //     |          ( / /) _|_ /   )   //     |           _( // /) ‘/,_ _ _/  ( ; -.   |    _ _.-~       .-~~~^-.(( / / )) ,-{        _      `.|.-~-.          .~         `.(( // / ))  ‘/      /                ~-. _.-~      .-~^-.  (( /// ))      `.   {            }                 /        (( / ))     .—-~-.        -‘               .~           `.   __///.—-..&gt;                    _ -~            `.  ^-`                 ///-._ _ _ _ _ _ _}^ – – – – ~                   `—–‘This dragon can breathe fire.</td>

   <td width="18"></td>

   <td width="275">&gt;java Cowsay -n ice-dragon Ice-cold RAWR Ice-cold RAWR\|___/|       /  //|\/0  0  __   /  // |  /     /  /_ /   //  |    \_^_’/   /_   //   |      //_^_/     /_ //    |        ( //) |         //     |          ( / /) _|_ /   )   //     |           _    ( // /) ‘/,_ _ _/  ( ; -.   |    _ _.-~(( / / )) ,-{        _      `.|.-~-.(( // / ))  ‘/      /                ~-. _.-~(( /// ))      `.   {            }(( / ))     .—-~-.        -‘///.—-..&gt;                    _///-._ _ _ _ _ _ _}^ – – – – ~ This dragon cannot breathe fire.</td>

  </tr>

 </tbody>

</table>

<h2>Cow Class</h2>

The Cow class must have all of the same methods as previously required, though students may add protected and private methods.) The methods are repeated here, briefly, for reference.




<table width="704">

 <tbody>

  <tr>

   <td width="309">public Cow(String name)</td>

   <td width="395">// Constructor</td>

  </tr>

  <tr>

   <td width="309">public String getName()</td>

   <td width="395">// Returns name of this cow object</td>

  </tr>

  <tr>

   <td width="309">public String getImage()</td>

   <td width="395">// Return image for this cow object</td>

  </tr>

  <tr>

   <td width="309">public void setImage(String image)</td>

   <td width="395">// Sets the image for this cow object to image</td>

  </tr>

 </tbody>

</table>




<h2>Dragon Class</h2>

The Dragon class must be derived from the Cow class and must make all of its methods available. In addition, Dragon must provide the following methods:

public Dragon(String name, String image)

Constructor; creates a new Dragon object with the given name and image. This should be the only public constructor for the Dragon class!




public boolean canBreatheFire()

This method should exist in every Dragon class. For the default Dragon type, it should always return true.




<h2>IceDragon Class</h2>

The IceDragon class must be derived from the Dragon class and must make all of its methods available:

public Dragon(String name, String image)

Constructor; creates a new IceDragon object with the given name and image. This should be the only public constructor for the IceDragon class!




public boolean canBreatheFire()

For the IceDragon type, this method should always return false.




<h1>Submissions</h1>

NOTE: Your output must match the example output *exactly*. If it does not, you will not receive full credit for your submission!




Files:  Cowsay.java, Cow.java, Dragon.java, IceDragon.java, HeiferGenerator.java Method: Submit on ZyLabs

<h1>Sample Output</h1>




&gt;javac Cowsay.java

&gt;java Cowsay Hello World!




Hello World!







^__^

(oo)_______

(__)       )/

||—-w |

||     ||




&gt;java Cowsay -n kitteh Moew-Moew!

Moew-Moew!







(“`-‘  ‘-/”) .___..–‘ ‘ “`-._

` *_ *  )    `-.   (      ) .`-.__. `)

(_Y_.) ‘ ._   )   `._` ;  “ -. .-‘

_.. `–‘_..-_/   /–‘ _ .’ ,4

( i l ),-”  ( l i),’  ( ( ! .-‘




&gt;java Cowsay -l

Cows available: heifer kitteh dragon ice-dragon




&gt;java Cowsay -n ninja Hello world!

Could not find ninja cow!




&gt;java Cowsay -n dragon Firey RAWR




Fiery RAWR







|___/|       /  //|\

/0  0  __   /  // |  

/     /  /_ /   //  |    

_^_’/   /_   //   |      

//_^_/     /_ //    |        

( //) |         //     |          

( / /) _|_ /   )   //     |           _

( // /) ‘/,_ _ _/  ( ; -.   |    _ _.-~       .-~~~^-.

(( / / )) ,-{        _      `.|.-~-.          .~         `.

(( // / ))  ‘/      /                ~-. _.-~      .-~^-.  

(( /// ))      `.   {            }                 /        

(( / ))     .—-~-.        -‘               .~           `.   __

///.—-..&gt;                    _ -~            `.  ^-`  

///-._ _ _ _ _ _ _}^ – – – – ~                   `—–‘




This dragon can breathe fire.




&gt;java Cowsay -n ice-dragon Ice-cold RAWR




Ice-cold RAWR







|___/|       /  //|\

/0  0  __   /  // |  

/     /  /_ /   //  |    

_^_’/   /_   //   |      

//_^_/     /_ //    |        

( //) |         //     |          

( / /) _|_ /   )   //     |           _

( // /) ‘/,_ _ _/  ( ; -.   |    _ _.-~       .-~~~^-.

(( / / )) ,-{        _      `.|.-~-.          .~         `.

(( // / ))  ‘/      /                ~-. _.-~      .-~^-.  

(( /// ))      `.   {            }                 /        

(( / ))     .—-~-.        -‘               .~           `.   __

///.—-..&gt;                    _ -~            `.  ^-`  

///-._ _ _ _ _ _ _}^ – – – – ~                   `—–‘




This dragon cannot breathe fire.


