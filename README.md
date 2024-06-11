import tkinter as tk

root= tk.Tk()
root.geometry("400x800")
root.resizable(False,False)

# Functions:
def backspace():
   widget.delete(len(widget.get())-1,tk.END)
def clear():
   widget.delete(0,tk.END)
def get(value):
   widget.insert('end', value)      
def sumbit():
   pass
def evaluate_calculation():
   pass

# GUis:
frame1 =tk.Frame(root)
frame1.columnconfigure(0,weight=2)

widget = tk.Entry(frame1, justify="right" , font=("Time New Roman" , 32) )
widget.grid(row=0, column=0 , sticky=tk.W+tk.E)
frame1.pack(fill="x")

frame = tk.Frame(root)
frame.columnconfigure(0, weight=1)
frame.columnconfigure(1,weight=1)
frame.columnconfigure(2, weight=1)
frame.columnconfigure(3,weight=1)


btn1 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 , text="(",command=lambda:get('('))
btn1.grid(row=0, column=0 , sticky=tk.W+tk.E )

btn2 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text=")",command=lambda:get(')'))
btn2.grid(row=0, column=1 , sticky=tk.W+tk.E )

btn3 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4  ,text="B", command=backspace)
btn3.grid(row=0, column=2 , sticky=tk.W+tk.E )

btn4 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="C" , command=clear)
btn4.grid(row=0, column=3 , sticky=tk.W+tk.E )

btn5 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="7",command=lambda:get(7))
btn5.grid(row=1, column=0 , sticky=tk.W+tk.E )

btn6 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="8",command=lambda:get(8))
btn6.grid(row=1, column=1 , sticky=tk.W+tk.E )

btn7 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="9",command=lambda:get(9))
btn7.grid(row=1, column=2 , sticky=tk.W+tk.E )

btn8 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="/",command=lambda:get('/'))
btn8.grid(row=1, column=3 , sticky=tk.W+tk.E )

btn9 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="4",command=lambda:get(4))
btn9.grid(row=2, column=0, sticky=tk.W+tk.E )

btn10 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="5",command=lambda:get(5))
btn10.grid(row=2, column=1 , sticky=tk.W+tk.E )

btn11 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="6",command=lambda:get(6))
btn11.grid(row=2, column=2, sticky=tk.W+tk.E )

btn12= tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="*",command=lambda:get('*'))
btn12.grid(row=2, column=3 , sticky=tk.W+tk.E )

btn13 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="1",command=lambda:get(1))
btn13.grid(row=3, column=0 , sticky=tk.W+tk.E )

btn14 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="2",command=lambda:get(2))
btn14.grid(row=3, column=1 , sticky=tk.W+tk.E )

btn15 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="3",command=lambda:get(3))
btn15.grid(row=3, column=2 , sticky=tk.W+tk.E )

btn16 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="+",command=lambda:get('+'))
btn16.grid(row=3, column=3, sticky=tk.W+tk.E )

btn17 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="0",command=lambda:get(0))
btn17.grid(row=4, column=0 , sticky=tk.W+tk.E )

btn18 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text=".",command=lambda:get('.'))
btn18.grid(row=4, column=1 , sticky=tk.W+tk.E )

btn19 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="=")
btn19.grid(row=4, column=2, sticky=tk.W+tk.E )

btn20 = tk.Button(frame , font= ('Time New Roman ' ,19) , height=4 ,text="-",command=lambda:get('-'))
btn20.grid(row=4, column=3 , sticky=tk.W+tk.E )

frame.pack(fill="x" ,padx=1, pady=1)




root.mainloop()
