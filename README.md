# Commander
## Store your commands and find it easy

I write this tool to you store your command and find it always that you need.

## Features

- Store your commands used in Pentest or in CTF;
- Easy to add commands;
- Find your command writing 2 letters;
- Click on the line and the command is copied to clipboard;

## How to Use

First you need to open index.html in a web browser.

You can search your commands in the input file.

## How to add a new command

First of all you need to copy a block of code like this:

```sh
1: <tr onclick="copyCommand('nc1')">
2:   <td></td>
3:   <td>nc</td>
4:   <td id="nc1">nc -lnvp 4120</td>
5:   <td>open the 4120 port to listen for connections</td>
6: </tr>
```

After you need to change **nc1** in first and fourth line to another unique identification. This **id** is used to copy the command to clipboard. In my example I changed **nc1** to **nmap1**.

```sh
1: <tr onclick="copyCommand('nmap1')">
...
4:   <td id="nmap1">nc -lnvp 4120</td>
...
```

And than you need to change the slug in the third line. It will be used when you find commands in the search input.

```sh
...
3:  <td>nmap</td>
...
```

After you need to change the command line and the description from command.


```sh
...
4:   <td id="nmap1">nmap -sT -p22 X.X.X.X</td>
5:   <td>do a fast TCP scan in the SSH service</td>
...
```

Save and relaunch your browser.