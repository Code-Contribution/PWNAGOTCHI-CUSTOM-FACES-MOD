# <img src="https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/pwnaflowey_MINI.png?raw=true" height="48"> pwnaflowey

A custom theme featuring my favorite character.

|                                  Without Optional Plugins                                            |                                            Animated Sample                                                     |
| :--------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------: |
|                                                ![Simple version](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/.screenshots/ui.png?raw=true)    |           ![Cool version](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/.screenshots/ui.gif?raw=true)  |


## Requirements
First and foremost, keep in mind that you must meet this requirements:
- Having followed all the steps in [this tutorial](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/tree/main#pwnagotchi-v155---custom-faces-mod-_)

## How To
First, with the pwnagotchi connected to a computer in `MANU` mode, establish an SSH connection.

Place the images from the `faces_pwnaflowey` folder into your custom faces folder path.

Login as root:
```console
pi@pwnagotchi:~ $ sudo su
root@pwnagotchi:/home/pi#
root@pwnagotchi:/home/pi# whoami
root
root@pwnagotchi:/home/pi# cd /
```
Stop pwnagotchi service
```console
root@pwnagotchi:/# systemctl stop pwnagotchi
```

Assuming you have already downloaded this project, upload the images using `FileZilla` or your preferred method to the custom faces folder created during [this tutorial](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/tree/main#pwnagotchi-v155---custom-faces-mod-_).

Open the pwnagotchi's configuration file:
```console
root@pwnagotchi:/# nano /etc/pwnagotchi/config.toml
```

Add or replace the new entries pointing to the folder where the images were placed, set the position (x, y) where the custom Face will be displayed and set the activation flag to `True`.
> **_Note 1:_** Check if your installed plugins modify the 'faces'. If there are any, replace them with the equivalent custom image address. If you don't do this, the pwnagotchi may crash. The code looks like this: `ui.set('face', "(◕‿‿◕)")` or `view.set('face', "(◕‿‿◕)")`


> **_Note 2:_** I recommend that you always use the same path (`/custom-faces/` folder) for your customization. That way, it becomes easier as you only need to replace the files!


```python
...
ui.faces.look_r = "/custom-faces/LOOK-R.png"
ui.faces.look_l = "/custom-faces/LOOK-L.png"
ui.faces.look_r_happy = "/custom-faces/LOOK-R-HAPPY.png"
ui.faces.look_l_happy = "/custom-faces/LOOK-L-HAPPY.png"
ui.faces.sleep = "/custom-faces/SLEEP.png"
ui.faces.sleep2 = "/custom-faces/SLEEP2.png"
ui.faces.awake = "/custom-faces/AWAKE.png"
ui.faces.bored = "/custom-faces/BORED.png"
ui.faces.intense = "/custom-faces/INTENSE.png"
ui.faces.cool = "/custom-faces/COOL.png"
ui.faces.happy = "/custom-faces/HAPPY.png"
ui.faces.excited = "/custom-faces/EXCITED.png"
ui.faces.grateful = "/custom-faces/GRATEFUL.png"
ui.faces.motivated = "/custom-faces/MOTIVATED.png"
ui.faces.demotivated = "/custom-faces/DEMOTIVATED.png"
ui.faces.smart = "/custom-faces/SMART.png"
ui.faces.lonely = "/custom-faces/LONELY.png"
ui.faces.sad = "/custom-faces/SAD.png"
ui.faces.angry = "/custom-faces/ANGRY.png"
ui.faces.friend = "/custom-faces/FRIEND.png"
ui.faces.broken = "/custom-faces/BROKEN.png"
ui.faces.debug = "/custom-faces/DEBUG.png"
ui.faces.upload = "/custom-faces/UPLOAD.png"
ui.faces.upload1 = "/custom-faces/UPLOAD1.png"
ui.faces.upload2 = "/custom-faces/UPLOAD2.png"
ui.faces.png = true
ui.faces.position_x = 0
ui.faces.position_y = 34
...
```
CTRL + O to save, CTRL + X to close file.


Reboot pwnagotchi service
```console
root@pwnagotchi:/# systemctl restart pwnagotchi
```

Reboot pwnagotchi service again
```console
root@pwnagotchi:/# systemctl restart pwnagotchi
```

Enjoy!

# Hint

If the status of your pwnagotchi is misaligned or if you want to change the position of the text, you can edit the screen configuration file. In my case, it is located at: 

```console
root@pwnagotchi:/# nano /usr/local/lib/python3.7/dist-packages/pwnagotchi/ui/hw/waveshare3.py
```

Look for:

```python
        self._layout['status'] = {
            'pos': (125, 20),
            'font': fonts.status_font(fonts.Medium),
            'max': 20
        }

```


And put whatever position you want in `pos` (x, y).

In my case:

```python
        self._layout['status'] = {
            'pos': (125, 34),
            'font': fonts.status_font(fonts.Medium),
            'max': 20
        }

```

CTRL + O to save, CTRL + X to close file.


Reboot pwnagotchi service again
```console
root@pwnagotchi:/# systemctl restart pwnagotchi
```

### Sprite Table

---



|                                               Emotion                                                |                                                     Original                                                     |                                                                            Replacement                                                                             |     |               Emotion (cont'd)                |  Original  |                                                                            Replacement                                                                             |
| :--------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-: | :-------------------------------------------: | :--------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|                                                LOOK_R                                                |                                                     `( ⚆_⚆)`                                                     |                              ![Look_R](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/LOOK-R.png?raw=true)                              |     |                   GRATEFUL                    |  `(^‿‿^)`  | ![Grateful](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/GRATEFUL.png?raw=true) <!-- I refuse to draw her doing aheago. fight me. --> |
|                                                LOOK_L                                                |                                                     `(☉_☉ )`                                                     |                              ![Look_L](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/LOOK-L.png?raw=true)                              |     |      EXCITED <!-- on_unread_messages -->      |  `(ᵔ◡◡ᵔ)`  |                           ![Excited](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/EXCITED.png?raw=true)                               |
|                                             LOOK_R_HAPPY                                             |                                                     `( ◕‿◕)`                                                     |                              ![Look_R_Happy](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/LOOK-R-HAPPY.png?raw=true)                  |     |                   MOTIVATED                   |  `(☼‿‿☼)`  |                           ![Motivated](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/MOTIVATED.png?raw=true)                           |
|                                             LOOK_L_HAPPY                                             |                                                     `(◕‿◕ )`                                                     |                              ![Look_L_Happy](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/LOOK-L-HAPPY.png?raw=true)                  |     |                  DEMOTIVATED                  |  `(≖__≖)`  |                           ![Bored](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/BORED.png?raw=true)                                   |
|                            SLEEP <!-- long sleep --> <br/> *(long sleep)*                            |                                                     `(⇀‿‿↼)`                                                     |                              ![Sleep](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/SLEEP.png?raw=true)                                |     |        SMART <br/> *(on free channel)*        |  `(✜‿‿✜)`  |                           ![Smart](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/SMART.png?raw=true)                                   |
|                          SLEEP2 <!-- short sleep --> <br/> *(short sleep)*                           |                                                     `(≖‿‿≖)`                                                     |                              ![Sleep2](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/SLEEP2.png?raw=true)                              |     |                    LONELY                     |  `(ب__ب)`  |                           ![Lonely](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/LONELY.png?raw=true)                                 |
|                                                AWAKE                                                 |                                                     `(◕‿‿◕)`                                                     |                              ![Awake](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/AWAKE.png?raw=true)                                |     |             SAD <!-- on_miss -->              |  `(╥☁╥ )`  |                           ![Sad](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/SAD.png?raw=true)                                       |
|                                                BORED                                                 |                                                     `(-__-)`                                                     |                              ![Bored](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/BORED.png?raw=true)                                |     |                     ANGRY                     |  `(-_-')`  |                           ![Angry](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/ANGRY.png?raw=true)                                   |
| INTENSE <!-- on_assoc : post auth, data transfer can begin --> <br/> *(successful wifi association)* |                                                     `(°▃▃°)`                                                     | ![INTENSE](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/INTENSE.png?raw=true) <!-- There's also an Anonymous one you could use here --> |     |                    FRIEND                     |  `(♥‿‿♥)`  |                           ![Friend](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/FRIEND.png?raw=true)                                 |
|                                       COOL <!-- on_deauth -->                                        |                                                     `(⌐■_■)`                                                     |                              ![Cool](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/COOL.png?raw=true)                                  |     | BROKEN <!-- on_reboot --> <br/> *(on reboot)* |  `(☓‿‿☓)`  |                           ![Broken](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/BROKEN.png?raw=true)                                 |
|                                    HAPPY <!-- new handshakes -->                                     |                                                     `(•‿‿•)`                                                     |                              ![Happy](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/HAPPY.png?raw=true)                                |     | DEBUG <!-- on_custom --> <br/> *(on custom)*  |  `(#__#)`  |                           ![Debug](https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/DEBUG.png?raw=true)                                   |
|                                            UPLOAD [ /1/2]                                            | <img src="https://github.com/roodriiigooo/PWNAGOTCHI-CUSTOM-FACES-MOD/blob/main/custom-themes/pwnaflowey/faces_pwnaflowey/UPLOAD.png?raw=true" height="64">                          |     |                                               |            |                                                                                                                                                                    |
