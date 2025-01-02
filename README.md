# MLT
Multi-Language Translation
```diff 
- Under Development 👨‍💻🤖
```
-------------------------------------------------------------------------------------------------------------------------------------
I am planning to build a Multi Language Translator chat bot.
-------------------------------------------------------------------------------------------------------------------------------------
Characteristics
- Take in voice, chat or url as input
- Convert from one language to your required language
- specifying the langauage to be converted is only to be mentioned, automatic identification of the language and translation.
-------------------------------------------------------------------------------------------------------------------------------------
Use case
- Factories
- public place (tourist QA)
- A chatbot the language need not be mentioned everytime, and the bot can identify the language and convert to the needed language.
- this can also used for various applications, where the different language commands are been converted to english and the command is passed as command to the systen to achieve a task.

--------------------------------------------------------------------------------------------------------------
```
pip install tkinter
```
Importing the required libraries and modules:
```
from tkinter import *
from tkinter import ttk, messagebox
import googletrans
import textblob
```
Initializing GUI window-
We will initiate the GUI window for the application.
```
root=Tk()
root.geometry("700x400")
root.title("Language Translator")
root.config(bg='#D3D3D3')
```
Creating Labels and Frames-
We will create labels and frames.
```
Label(root,text="Language Translator-PythonFlood",font=('Arial,bold',20), bg='#8B8B7A',fg='White', width=50, pady=5).pack(pady=10)


f1 = Frame(root, width=320, height=200, bg='white', bd=5)
f1.place(x=15, y=70)
f2 = Frame(root, width=320, height=200, bg='white', bd=5)
f2.place(x=360, y=70)

```
Creating Text widget, Combobox and Buttons-
Now we will create text widget, combobox and buttons widget for the application.
```
txt1=Text(f1,font=('Arial,bold'), width=28, height=8)
txt1.place(x=0,y=0)
txt2=Text(f2,font=('Arial,bold'), width=28, height=8)
txt2.place(x=0,y=0)


c1=ttk.Combobox(root,values=language_list,font=('Arial,bold',12),width=20)
c1.place(x=60,y=290)
c2=ttk.Combobox(root,values=language_list,font=('Arial,bold',12),width=20)
c2.place(x=420,y=290)


btn=Button(root,text="Translate",font=('Arial,bold',15),bd=5, bg='#8B8B7A',fg='White',command=trans_late)
btn.place(x=290,y=320)


root.mainloop()
```
Code for language translation-
We will create main function which will translate the text.


```
def trans_late():
   txt2.delete(1.0, END)
   try:
       for key, value in languages.items():
           if(value == c1.get()):
               from_language_key = key
       for key, value in languages.items():
           if(value == c2.get()):
               to_language_key = key


       words = textblob.TextBlob(txt1.get(1.0, END))
       words = words.translate(from_lang=from_language_key, to=to_language_key)
       txt2.insert(1.0, words)



  except Exception as e:
       messagebox.showerror(("Translater", e))
```
```
```
```
```
```
```
