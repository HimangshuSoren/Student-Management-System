# Student-Management-System
This is a computer project for class 12 students. In this project the students has to make an application using python module ( tkinter ),this is the only GUI part of the application, later on I will be adding the back end part of the program....


from tkinter import *
from tkinter import ttk

class Student :
    def __init__(self,root):
        self.root = root
        self.root.title("Student Management System \U0001f130 \U0001f131 \U0001f137")
        ws = root.winfo_screenwidth()
        hs = root.winfo_screenheight()
        w =1350
        h = 700
        x = int(ws/2-w/2-60)
        y = int(hs/2-h/2-30)
        data = str(w)+"x"+str(h)+"+"+str(x)+"+"+str(y)
        self.root.geometry(data)
        self.root.configure(bg ="#ffffff")
        self.root.resizable(0,0)
        #********************** Frame 1 *****

        frame1 = LabelFrame()
        frame1.pack(fill ="x")

        title = Label(frame1,text  ="Student Management System",font=("Comic Sans MS",25,"bold"),bg  ="#00e6a1",fg = "#ffffff",anchor ="center",bd =4)
        title.pack(expand =True,fil="x")

        #*********************** Frame 2 *****

        f2 = Label(self.root, text=" Pffvkbfk ", font=("Comic Sans MS", 15, "bold", "italic"),bg="#cacaca", bd=1)
        f2.place(x=0, y=55, relwidth=50)

        # ********************** Frame 3 *****

        Manage_Frame =Frame(self.root,bd  = 1,bg = "#fff000",relief =GROOVE,)
        Manage_Frame.place(x =13,y = 95,width =457,height =545)

        Manage_Frame3 = LabelFrame(Manage_Frame, text=" Put the Details", font=("Comic Sans MS", 23, "bold", "italic"),
                                  fg="#ffffff", bd=0, bg="#fff000", relief=SUNKEN, )
        Manage_Frame3.place(y =0,x =0,width =457,height =545)

        # **********************  Labels and Entries_____________

        rol_lbl = Label(Manage_Frame,text = "Roll No.",bg ="#fff000",fg ="#ffffff",font =("Comic Sans MS",19,"bold"))
        rol_lbl.grid(row =1 ,column = 0,pady =(65,0),padx =20,sticky ="w")
        rol_txt = Entry(Manage_Frame,width = 18,font= ("Comic Sans MS",15),fg ="#000000",bd =1,relief =GROOVE,)
        rol_txt.grid(row =1,column =2,sticky="w",pady=(65,0))

        name_lbl = Label(Manage_Frame, text="Name", bg="#fff000", fg="#ffffff", font=("Comic Sans MS", 19, "bold"))
        name_lbl.grid(row=2, column=0, pady=10, padx=20, sticky="w")
        name_txt = Entry(Manage_Frame, width=18, fg ="#000000",font=("Comic Sans MS",15), bd=1, relief=GROOVE, )
        name_txt.grid(row=2, column=2,sticky="w")

        email_lbl = Label(Manage_Frame, text="E-mail", bg="#fff000", fg="#ffffff", font=("Comic Sans MS", 19, "bold"))
        email_lbl.grid(row=3, column=0, pady=10, padx=20, sticky="w")
        email_txt = Entry(Manage_Frame, width=18,fg ="#000000", font=("Comic Sans MS",15), bd=1, relief=GROOVE, )
        email_txt.grid(row=3, column=2,sticky="w")

        gender_lbl = Label(Manage_Frame, text="Gender", bg="#fff000", fg="#ffffff", font=("Comic Sans MS", 19, "bold"))
        gender_lbl.grid(row=4, column=0, pady=10, padx=20, sticky="w")
        combo_gender= ttk.Combobox(Manage_Frame,font=("Comic Sans MS",15),width =16,state ="readonly")
        combo_gender["values"]=("Male","Female","Other")
        combo_gender.grid(row =4,column =2,sticky="w")

        contact_lbl = Label(Manage_Frame, text="Phone.No", bg="#fff000", fg="#ffffff", font=("Comic Sans MS", 19, "bold"))
        contact_lbl.grid(row=5, column=0, pady=10, padx=20, sticky="w")
        contact_txt = Entry(Manage_Frame, width=18, fg ="#000000",font=("Comic Sans MS",15), bd=1, relief=GROOVE, )
        contact_txt.grid(row=5, column=2,sticky="w")

        dob_lbl = Label(Manage_Frame, text="D.O.B.", bg="#fff000", fg="#ffffff", font=("Comic Sans MS", 19, "bold"))
        dob_lbl.grid(row=6, column=0, pady=10, padx=20, sticky="w")
        dob_txt = Entry(Manage_Frame, width=18,fg ="#000000", font=("Comic Sans MS",15), bd=1, relief=GROOVE, )
        dob_txt.grid(row=6, column=2,sticky="w")

        add_lbl = Label(Manage_Frame, text="Address", bg="#fff000", fg="#ffffff", font=("Comic Sans MS", 19, "bold"))
        add_lbl.grid(row=7, column=0, pady=10, padx=20, sticky="w")
        add_txt = Text(Manage_Frame, width=27,height = 2,fg ="#000000",  bd=1/2, relief=GROOVE, )
        add_txt.grid(row=7, column=2,sticky="w")



        # ***************************** Frame 3 *****

        btn_frm =Frame(Manage_Frame,bd = 2,relief =RIDGE,bg ="#fff000")
        btn_frm.place(x = 0,y =475,width =455,height =54,)


        # ***************************** Buttons _______________

        add_btn = Button(btn_frm,width =10,text ="Add",font =("Comic Sans MS",12,"bold"),bd =1/2,bg ="#ffffff",fg ="#000000",relief =SUNKEN).grid(row =0,column =0,padx =4,pady =7)

        update_btn = Button(btn_frm, width=10, text="Update", font=("Comic Sans MS", 12, "bold"),bd =1/2,bg ="#ffffff",fg ="#000000",relief =SUNKEN).grid(row=0, column=1,padx=1,pady =7)

        delete_btn = Button(btn_frm, width=10, text="Delete", font=("Comic Sans MS", 12, "bold"),bd =1/2,bg ="#ffffff",fg ="#000000",relief =SUNKEN).grid(row=0, column=2,padx=2,pady =7)

        clear_btn = Button(btn_frm, width=10, text="Clear", font=("Comic Sans MS", 12, "bold"),bd =1/2,bg ="#ffffff",fg ="#000000",relief =SUNKEN).grid(row=0, column=3,padx=2,pady =7)

        # ************************* frm 2 *************

        Manage_Detail = Frame(self.root, bd=1, relief=RIDGE,bg ="#ffffff")
        Manage_Detail.place(x=480, y=95, width=856, height=544)

        Manage_lst = Frame(self.root, bd=1 , relief=RIDGE, )
        Manage_lst.place(x=480, y=95, width=856, height=54)

        srch_lbl = Label(Manage_lst, text="Search By",fg="#676767", font=("Comic Sans MS", 17, "bold"))
        srch_lbl.grid(row=0, column=0, pady=10, padx=20, sticky="w")
        combo_srch = ttk.Combobox(Manage_lst, font=("Comic Sans MS", 14), width=10, state="readonly")
        combo_srch["values"] = ( "Roll.No","Name","E-mail", "Phone.No","Gender","D.O.B",'Address')
        combo_srch.grid(row=0, column=1)

        all_search_btn = Button(Manage_lst, width=10, text="Search", font=("Comic Sans MS", 12, "bold"), bd=1 / 2, bg="#ffffff",
                           fg="#000000", relief=SUNKEN).grid(row=0, column=3, padx=(10,0), pady=7,sticky ="e")

        search_btn = Button(Manage_lst, width=10, text="Search All", font=("Comic Sans MS", 12, "bold"), bd=1 / 2, bg="#ffffff",
                           fg="#000000", relief=SUNKEN).grid(row=0, column=4, padx=20, pady=7,sticky ="e")

        dob_txt = Entry(Manage_lst, width=18, fg="#000000", font=("Comic Sans MS", 15), bd=1, relief=GROOVE, )
        dob_txt.grid(row=0, column=2, sticky="w", padx=27)

        Manage_Detail2 = Frame(self.root, bd=1, relief=RIDGE, bg="#ffffff")
        Manage_Detail2.place(x=480, y=148, width=856, height=490)

        lab1 = Scrollbar(Manage_Detail2, orient=HORIZONTAL)
        lab2 = Scrollbar(Manage_Detail2, orient=VERTICAL)
        tab = ttk.Treeview(Manage_Detail2, columns = ("Roll.No","Name","E-mail","Gender","Phone.No","D.O.B","Address",),yscrollcommand=lab2.set,xscrollcommand =lab1.set )
        lab1.pack(side=BOTTOM, fill=X)
        lab2.pack(side=RIGHT, fill=Y)
        lab1.config(command=tab.xview,)
        lab2.config(command=tab.yview,)
        tab.heading("Roll.No",text = "Roll.No")
        tab.heading("Name", text="Name")
        tab.heading("E-mail", text="E-mail")
        tab.heading("Gender", text="Gender")
        tab.heading("Phone.No", text="Phone.No")
        tab.heading("D.O.B", text="D.O.B.")
        tab.heading("Address", text="Address")
        tab['show']="headings"

        tab.column("Name", width=200)
        tab.column("E-mail", width=300)
        tab.column("Address", width=500)
        tab.column("Roll.No",width = 100)

        tab.pack(expand =True,fill =BOTH)





        # ******************** credit  ****************



        credit =Frame(self.root,bg = "#ff0000",bd =0)
        credit.place(x =0,y =643,relwidth = 1,relheight =0.08,)

        c1 =Label(credit,text = "Developed By : Himangshu and team ,,,",font =("times new roman",20,"bold"),fg = "#ffffff",bg ="#ff0000")
        c1.grid(row = 0, column =0,padx =870,pady =10,sticky ="w")





root= Tk()
ob = Student(root)




root.mainloop()























