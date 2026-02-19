# Rofi

## 🔸What is rofi?
At its simplest, Rofi is a window switcher, application launcher, and dmenu replacement. But for power users like you, it is a command-line driven portal to your entire operating system.

## 🔸Key Roles of Rofi:

- **Application Launcher:** It scans your `.desktop` files (like the ones we just built!) and presents them in a searchable list.

- **Window Switcher:** If you have 20 windows open, you can type the name of one, and Rofi will jump you straight to it.

- **Highly Scriptable:** This is where the "Super Engineer" part comes in. You can feed Rofi any list of text, and it will let you pick one to trigger a script.

## 🔸Why we should use Rofi over Krunner (KDE netive)?

### 1. Speed and Minimalist Design
KRunner is powerful, but it’s a "heavyweight." It tries to do everything: calculate math, find files, search emails, and check the weather.

**KRunner** often has a slight "fade-in" animation and relies on the heavy Plasma framework.

**Rofi** is built for pure speed. It is a "dmenu" replacement, meaning it is designed to pop up instantly, take a few keystrokes, and disappear before your brain even registers the delay.

### 2. Ultimate Customization (The "Super Engineer" Factor)
KRunner’s look is tied to your KDE Plasma theme. If you want to change how it looks, you usually have to change your whole desktop theme.

**Rofi** uses .rasi files. You can customize every single pixel: the border radius, the transparency, the padding, and even how it behaves when you hover over an item.

> Rofi has priority sorting that makes frequently use apps appear on top.

### 3. Modality (The "Secret Sauce")
This is where Rofi wins for engineers. Rofi is modal. You can use the same tool for different things by passing different flags:

- `rofi -show drun`: Just your apps.

- `rofi -show window `: Just your open windows.

- `rofi -show ssh`: A list of your remote servers to log into.

    Custom Scripts: You can pipe any text into Rofi. For example, you could write a script that fetches your 10 most recent git branches and use Rofi to let you pick one to switch to.

## ✅ My Rofi config:

<mark style="background: #FFF3A3A6;">The color palate is choose according to current theme: Sweet KDE (purple). It should be change according to environment.</mark>

```rasi
/*****----- Configuration -----*****/
configuration {
    modi:                       "drun,run,window";
    show-icons:                 true;
    drun-display-format:        "{name}";
    display-drun:               "Apps";
    display-run:                "Commands";
    display-window:             "Windows";
}
/*****----- Main Window -----*****/
window {
    /* properties for window widget */
    transparency:                "real";
    location:                    center;
    anchor:                      center;
    fullscreen:                  false;
    width:                       800px;
    x-offset:                    0px;
    y-offset:                    0px;

    /* properties for all widgets */
    enabled:                     true;
    margin:                      0px;
    padding:                     0px;
    border:                      2px solid;
    border-radius:               15px;
    border-color:                #948B97;
    cursor:                      "default";
    background-color:            #161925;
}
/*****----- Main Box -----*****/
mainbox {
    enabled:                     true;
    spacing:                     10px;
    margin:                      0px;
    padding:                     30px;
    background-color:            transparent;
    children:                    [ "inputbar", "message", "listview", "mode-switcher" ];
}
/*****----- Inputbar -----*****/
inputbar {
    enabled:                     true;
    spacing:                     10px;
    margin:                      0px 0px 30px 0px;
    padding:                     10px;
    border:                      2px 2px 2px 2px;
    border-radius:               10px;
    border-color:                #999;
    background-color:            #1F2333;
    text-color:                  #eeeeee;
    children:                    [ "prompt", "textbox-prompt-colon" , "entry" ];
}
prompt {
    enabled:                     true;
    background-color:            inherit;
    text-color:                  inherit;
}
textbox-prompt-colon {
    enabled:                     true;
    padding:                     0px;
    expand:                      false;
    str:                         ":";
    background-color:            inherit;
    text-color:                  inherit;
}
entry {
    enabled:                     true;
    padding:                     0px;
    background-color:            inherit;
    text-color:                  inherit;
    cursor:                      text;
    placeholder:                 "";
    placeholder-color:           inherit;
}
/*****----- Listview -----*****/
listview {
    enabled:                     true;
    columns:                     2;
    lines:                       10;
    cycle:                       true;
    dynamic:                     true;
    scrollbar:                   false;
    layout:                      vertical;
    reverse:                     false;
    fixed-height:                true;
    fixed-columns:               true;
    spacing:                     10px;
    background-color:            transparent;
    text-color:                  #eee;
    cursor:                      "default";
    border:                      0;
}
scrollbar {
    handle-width:                5px ;
    handle-color:                transparent;
    border-radius:               10px;
    background-color:            transparent;
}
/*****----- Elements -----*****/
element {
    enabled:                     true;
    spacing:                     10px;
    margin:                      0px;
    padding:                     6px;
    border-radius:               0px;
    background-color:            transparent;
    text-color:                  #eee;
    cursor:                      pointer;
}
element normal.normal,
element alternate.normal {
    background-color:            transparent;
    text-color:                  #eee;
}
element normal.urgent,
element alternate.urgent,
element selected.active {
    //background-color:            var(urgent);
    //text-color:                  var(background);
    background-color:            transparent;
    text-color:                  #eee;
    border:                      2px 2px 2px 2px;
    border-radius:               10px;
    border-color:                #7D138B;
}
element normal.active,
element alternate.active,
element selected.urgent {
    background-color:            transparent;
    text-color:                  #eee;
    border:                      2px;
    border-color:                #7D138B;
}
element selected.normal {
    background-color:            #4E155C;
    text-color:                  #eee;
    border:                      2px 2px 2px 2px;
    border-radius:               10px;
    border-color:                #7D138B;
}
element-icon {
    background-color:            transparent;
    text-color:                  inherit;
    size:                        24px;
    cursor:                      inherit;
}
element-text {
    background-color:            transparent;
    text-color:                  inherit;
    highlight:                   inherit;
    cursor:                      inherit;
    vertical-align:              0.5;
    horizontal-align:            0.0;
}

/*****----- Mode Switcher -----*****/
mode-switcher{
    enabled:                     false;
}
/*****----- Message -----*****/
message {
    enabled:                     true;
    margin:                      0px;
    padding:                     10px;
    border-radius:               0px;
    background-color:            transparent;
    text-color:                  #aaa;
}
textbox {
    background-color:            transparent;
    text-color:                  #eee;
    vertical-align:              0.5;
    horizontal-align:            0.0;
    highlight:                   none;
    placeholder-color:           #aaa;
    blink:                       true;
    markup:                      true;
}
error-message {
    padding:                     30px;
    background-color:            transparent;
    text-color:                  #ff0000;
}

```

## ⌨️ Key Bindings

1. `rofi -show drun -matching glob` : `META` 
	
	This is the primary command that launches the applications.
	`-matching glob` : re-enforce strict search.

2. `rofi -show run -matching fuzzy` : `META + ENTER`
	
	Helps to find specific executable binaries.
	`-matching fuzzy` : Helps to find in broader spectrum.

<mark style="background: #FF5582A6; color : white;"><b>We can't use window mode, because Rofi primarily design for X11 and on wayland specifically KDE wayland the window handler is designed differently. So, it can't be used.</b></mark>
