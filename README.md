# STELLAR_BUKKIT_DOC
Documentazione, non corso, di Bukkit | by StellarSquad

![637538649057112996](https://github.com/Tyranzx/STELLAR_BUKKIT_DOC/assets/70720366/4b01f9bc-80ab-46cf-a7f6-4db1813e9cd0)

# BUKKIT
## Cos'é?
### Non solo é un motore per creare un nostro server di minecraft ma é pure un mezzo per creare complementi da aggiungere nel nostro server. Evidentemente "Bukkit" non é piú usato peró si parte sempre da lí e la struttura generale é identica al resto di API.

## Cosa si imparerá a fare?
### Sicuramente non modalitá intere, ma il sufficiente perché da soli possiate farlo con sforzo e concentrazione.
### Un esempio bruto di modalitá che non potremo insegnare sono KitPVP e Bedwars, perché entrambi usano tecnologie non solo **Spigot** e **Java** ma pure altre tecnologie e possibilmente altri linguaggi di programmazione.
### 
### In conclusione, servirá per aprire la mente e togliere alcuni dubbi a alcune persone che stanno imparando.
### Utilizzeremo Eclipse per gli esempi e/o esempi scritti per MD (Gli stessi avuti nella doc precendente di java)
### Piccolo spoiler: Per il KitPVP o Bedwars non servono API esterne da acquistare, ecc. Nel senso che tutto lo si puó fare se si ha pazienza e conoscenze sufficienti.
###
## [👋] Il nostro primo "Hello world" in Bukkit
### Per la creazione della classe principale, ovvero la classe la quale il contenuto sará eseguito per primo, dobbiamo estendere "JavaPlugin".
### É importante ricordarsi che si puó solo estendere una volta sola "JavaPlugin", questo perché la classe (JavaPlugin) ha metodi specifici per far diventare una classe quella "principale".
```java
public class Loader extends JavaPlugin {
	
	public void onEnable() {
		Bukkit.broadcastMessage("Hello world!");
	}
	
	public void onDisable() {
		Bukkit.broadcastMessage("Bye world!");
	}
```
![Screenshot 2024-03-23 113937](https://github.com/Tyranzx/STELLAR_BUKKIT_DOC/assets/70720366/ab9977c8-c4a0-4885-a677-8aa4f839b240)
### Ricordiamoci che son solo due metodi da mettere, rispettando le maiuscole, perché il nostro plugin funzioni come noi vogliamo.
### Unicamente "onEnable" é importante per registrare comandi, mandare messaggi, registrare classi o eseguire azioni e/o istruzioni preparate con certe scopi.
### Nel metodo "onDisable" metteremo le cose che ci serviranno eseguire per quando il server, per esempio, si stia chiudendo.
## [🤖] COMANDI
### Passiamo subito alla creazione di un comando, poiché non ha senso spiegare, secondo noi, il resto di cose che si potrebbero scoprire piú in avanti.
```java
public boolean onCommand(CommandSender sender, Command command, String label, String[] args) {
		
	return false;
}
```
### Partiamo con sto pezzo di codice, per spiegare alcune cose e capire la struttura di questo metodo di tipo boolean chiamato "onCommand" (Importante che sia messo come vedete, tranne i parametri (quelli dentro le parentesi), altrimenti il plugin non lo riconosce come la struttura di un comando).
### "CommandSender sender", é un parametro che potete cambiare il nome se volete, tipo "CommandSender oa", ma dovreste usare "oa" da quel momento in poi.
### Cos'é? "send" = "mandare" giusto? "command" = "comando", con questo capiamo che "CommandSender" é colui che manda il comando.
## ATTENZIONE:
### Non si sta specificando il tipo di sender, si sá solo che é un qualcosa che manda il comando, che lo esegue, ma non specifica se é la console o un giocatore.
### Per verificare se é un giocatore o no:
```java
public boolean onCommand(CommandSender sender, Command command, String label, String[] args) {
	if (sender instanceof ConsoleCommandSender) {
//	☝ In java, "instanceof", fa riferimento a "é di tipo", in questo caso:
//  	 Verifica che sia un commandSender di tipo "Console"
// 	->   ConsoleCommandSender
	}
	return false;
}
```
```java
public boolean onCommand(CommandSender sender, Command command, String label, String[] args) {
	if (sender instanceof Player) {
//  	 Verifica che sia un commandSender di tipo "Player" (Giocatore)
	}
	return false;
}
```
