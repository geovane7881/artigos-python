# 1 - Intalação Tkinter no Python 2.7

`sudo apt-get update` <br/>
`sudo apt-get install python-tk`
<br/>
<br/>
# 2 - Uma aplicação básica com Tkinter.
### Criando um programa simples com Tkinter que contém apenas um botão Quit. 

```
#!/usr/bin/env python                                   #1
import Tkinter as tk                                    #2

class Application(tk.Frame):                            #3
    def __init__(self, master=None):
        tk.Frame.__init__(self, master)                 #4
        self.grid()                                     #5
        self.createWidgets()

    def createWidgets(self):
        self.quitButton = tk.Button(self, text='Quit',
            command=self.quit)                          #6
        self.quitButton.grid()                          #7

app = Application()                                     #8
app.master.title('Sample application')                  #9
app.mainloop()                                          #10		
```

1. Esta linha faz o script se auto-executar, presumindo que o seu sistema tem o Python instalado corretamente.
2. Esta linha importa o módulo *Tkinter* no namespace do seu programa, nós o chamaremos apenas de *tk*.
3. A classe da sua aplicação deve herdar da classe *Frame* contida em *Tkinter*.
4. Chamando o construtor da classe pai.
5. Isso é necessário para fazer a aplicação aparecer na tela, esse método define o layout em forma de *grid* (com linhas e colunas).
6. Cria um botão chamado *“Quit”*.
7. Coloca o botão na aplicação (dentro do grid).
8. O programa principal inicia aqui, instanciando a classe *Application* com o objeto *app*.
9. Esta chamada de método vai definir o titulo da janela como *“Sample application”*.
10. Inicia o loop principal da aplicação, aguardando eventos de mouse ou teclado.

# 3 - Links Úteis

**Fonte:** http://infohost.nmt.edu/tcc/help/pubs/tkinter/web/minimal-app.html<br/>
**Referencia Tkinter:** https://docs.python.org/2/library/tkinter.html<br/>
**Namespaces no Python:** http://www.alan-g.me.uk/tutor/port/tutname_por.htm<br/>
