insert_text
finter as tkrom tkinter import messagebox

def show_login_screen():
    # લોગો સ્ક્રીન હટાવીને લોગિન સ્ક્રીન બતાવવી
    logo_label.destroy()
    
    tk.Label(root, text="તમારું નામ લખો:", font=("Arial", 12)).pack(pady=10)
    
    name_entry = tk.Entry(root)
    name_entry.pack(pady=5)
    
    def enter_app():
        user_name = name_entry.get()
        if user_name:
            messagebox.showinfo("સ્વાગત છે", f"નમસ્તે {user_name}, તમે એપમાં પ્રવેશ કર્યો છે!")
            # અહીંથી તમારી મુખ્ય એપ શરૂ થશે
        else:
            messagebox.showwarning("ભૂલ", "મહેરબાની કરીને નામ લખો")

    tk.Button(root, text="લોગિન", command=enter_app, bg="green", fg="white").pack(pady=20)

# મેઈન વિન્ડો સેટઅપ
root = tk.Tk()
root.title("My Python App")
root.geometry("300x400")

# ૧. લોગો સ્ક્રીન (ચોક્કસ સમય માટે દેખાશે)
logo_label = tk.Label(root, text="APP LOGO", font=("Arial", 24, "bold"), fg="blue")
logo_label.pack(expand=True)

# ૩ સેકન્ડ (૩૦૦૦ ms) પછી લોગિન સ્ક્રીન પર જવા માટે
root.after(3000, show_login_screen)

root.mainloop()inter as tk
from tkinter import messagebox

def show_login_screen():
    # લોગો સ્ક્રીન હટાવીને લોગિન સ્ક્રીન બતાવવી
    logo_label.destroy()
    
    tk.Label(root, text="તમારું નામ લખો:", font=("Arial", 12)).pack(pady=10)
    
    name_entry = tk.Entry(root)
    name_entry.pack(pady=5)
    
    def enter_app():
        user_name = name_entry.get()
        if user_name:
            messagebox.showinfo("સ્વાગત છે", f"નમસ્તે {user_name}, તમે એપમાં પ્રવેશ કર્યો છે!")
            # અહીંથી તમારી મુખ્ય એપ શરૂ થશે
        else:
            messagebox.showwarning("ભૂલ", "મહેરબાની કરીને નામ લખો")

    tk.Button(root, text="લોગિન", command=enter_app, bg="green", fg="white").pack(pady=20)

# મેઈન વિન્ડો સેટઅપ
root = tk.Tk()
root.title("My Python App")
root.geometry("300x400")

# ૧. લોગો સ્ક્રીન (ચોક્કસ સમય માટે દેખાશે)
logo_label = tk.Label(root, text="APP LOGO", font=("Arial", 24, "bold"), fg="blue")
logo_label.pack(expand=True)

# ૩ સેકન્ડ (૩૦૦૦ ms) પછી લોગિન સ્ક્રીન પર જવા માટે
root.after(3000, show_login_screen)

root.mainloop()st.sidebar.error("યુઝરનેમ અથવા પાસવર્ડ ખોટો છે!")

# સેક્શન 1: શાળાની વિગતો (બધા જોઈ શકે)
st.subheader("📖 શાળાની વિગતો")
st.write("""
સાખડાસર 1 પ્રાથમિક શાળામાં તમારું હાર્દિક સ્વાગત છે. 
અમારી શાળામાં બાળકોના સર્વાંગી વિકાસ માટે ઉત્તમ શિક્ષણ અને રમતગમતની સુવિધાઓ પૂરી પાડવામાં આવે છે.
""")
st.markdown("---")

# સેક્શન 2: અપલોડ સેક્શન (ફક્ત લોગિન થયેલા સ્ટાફ માટે જ દેખાશે)
if st.session_state['logged_in']:
    st.subheader("📤 ફોટા અને વિડીયો અપલોડ કરો (માત્ર સ્ટાફ માટે)")
    uploaded_file = st.file_uploader("અહીંથી ફાઇલ પસંદ કરો", type=["jpg", "png", "jpeg", "mp4"])
    
    if uploaded_file is not None:
        # વાસ્તવિક એપમાં અહીં ફાઇલને સર્વર પર સેવ કરવાનો કોડ આવે
        st.success(f"તમારી ફાઇલ '{uploaded_file.name}' સફળતાપૂર્વક અપલોડ થઈ ગઈ છે!")
        
    st.markdown("---")

# સેક્શન 3: ગેલેરી (બધા જોઈ શકે)
st.subheader("🖼️ ગેલેરી (ફોટા અને વિડીયો)")
st.info("અપલોડ કરેલા ફોટા અને વિડીયો અહીં દેખાશે.")
# નોંધ: વાસ્તવિક એપમાં અહીં ફોલ્ડરમાંથી સેવ કરેલા ફોટા લાવીને બતાવવાનો કોડ આવે છે.
🚀 આ એપને તમારા કમ્પ્યુટર પર કઈ રીતે ચાલુ કરવી?
Python ઇન્સ્ટોલ કરો: તમારા કમ્પ્યુટરમાં Python ઇન્સ્ટોલ હોવું જરૂરી છે.

Streamlit ઇન્સ્ટોલ કરો: કમાન્ડ પ્રોમ્પ્ટ (CMD) અથવા ટર્મિનલ ખોલીને નીચેનો કમાન્ડ રન કરો:

Bash
pip install streamlit
એપ રન કરો: જ્યાં તમે app.py ફાઇલ સેવ કરી છે, તે ફોલ્ડરમાં જઈને ટર્મિનલમાં લખો:

Bash
streamlit run app.search_entry.insert(0, current + char)

# સર્ચ બટન માટેનું ફંક્શન
def search_action():
    query = search_entry.get()
    std = std_combo.get()
    if query:
        result_label.config(text=f"પરિણામ: તમે '{std}' માં '{query}' શોધી રહ્યા છો.")
    else:
        result_label.config(text="કૃપા કરીને કંઈક લખો!")

# મુખ્ય વિન્ડો બનાવવી
root = tk.Tk()
root.title("ગુજરાતી શૈક્ષણિક એપ")
root.geometry("500x700")
root.configure(bg="#f4f4f4")

# ફોન્ટ સેટિંગ
guj_font = ("Arial", 14, "bold")

# 1. સર્ચ ઓપ્શન (Search Box)
search_label = tk.Label(root, text="અહીં શોધો:", font=guj_font, bg="#f4f4f4")
search_label.pack(pady=(20, 5))

search_entry = tk.Entry(root, font=("Arial", 16), width=25, justify="center")
search_entry.pack(pady=5)

# 2. ધોરણ પસંદ કરવાનો ઓપ્શન (Standard Selection)
std_label = tk.Label(root, text="ધોરણ પસંદ કરો:", font=guj_font, bg="#f4f4f4")
std_label.pack(pady=(15, 5))

# ધોરણ 1 થી 12 ની યાદી
standards = [f"ધોરણ {i}" for i in range(1, 13)]
std_combo = ttk.Combobox(root, values=standards, font=("Arial", 12), state="readonly", width=20)
std_combo.set("ધોરણ 10") # ડિફોલ્ટ ધોરણ 10 રહેશે
std_combo.pack(pady=5)

# સર્ચ બટન
search_btn = tk.Button(root, text="શોધો (Search)", font=guj_font, bg="#4CAF50", fg="white", command=search_action)
search_btn.pack(pady=15)

# રિઝલ્ટ બતાવવા માટે
result_label = tk.Label(root, text="", font=("Arial", 12), fg="blue", bg="#f4f4f4")
result_label.pack(pady=5)

# 3. ગુજરાતી વર્ચ્યુઅલ કીબોર્ડ (Gujarati Keyboard)
kb_label = tk.Label(root, text="ગુજરાતી કીબોર્ડ:", font=guj_font, bg="#f4f4f4")
kb_label.pack(pady=(20, 5))

kb_frame = tk.Frame(root, bg="#f4f4f4")
kb_frame.pack()

# ઉદાહરણ માટે ગુજરાતી મૂળાક્ષરો અને માત્રા
guj_chars = [
    ['અ', 'આ', 'ઇ', 'ઈ', 'ઉ', 'ઊ', 'એ'],
    ['ક', 'ખ', 'ગ', 'ઘ', 'ચ', 'છ', 'જ'],
    ['ઝ', 'ટ', 'ઠ', 'ડ', 'ઢ', 'ણ', 'ત'],
    ['થ', 'દ', 'ધ', 'ન', 'પ', 'ફ', 'બ'],
    ['ભ', 'મ', 'ય', 'ર', 'લ', 'વ', 'શ'],
    ['ષ', 'સ', 'હ', 'ળ', 'ક્ષ', 'જ્ઞ', ' '],
    ['ા', 'િ', 'ી', 'ુ', 'ૂ', 'ે', 'ૈ'] # માત્રાઓ 
]

# કીબોર્ડના બટન લૂપ દ્વારા બનાવવા
for r, row in enumerate(guj_chars):
    for c, char in enumerate(row):
        # સ્પેસ (Space) બટન માટે અલગ ડીઝાઇન
        text_display = "Space" if char == ' ' else char
        btn = tk.Button(kb_frame, text=text_display, font=("Arial", 14), width=4, height=1,
                        command=lambda ch=char: insert_text(ch))
        btn.grid(row=r, column=c, padx=3, pady=3)

# એપ ચાલુ રાખવા માટે
root.mainloop()OOL",
    "rooms": 12,  # તમારા મુજબ આંકડો બદલી શકો છો
    "sound_system": "Advanced Digital System",
    "facilities": ["Library", "Computer Lab", "Playground", "Garden"],
    "location": {
        "latitude": 22.1234,  # લાઈવ લોકેશન માટેના કોર્ડિનેટ્સ
        "longitude": 71.5678,
        "map_link": "https://maps.google.com/?q=Sankhadasar+1+Primary+School"
    },
    "multimedia": {
        "photos": ["photo1.jpg", "photo2.jpg"],
        "videos": ["school_tour.mp4"]
    },
    "results": "https://sps-school.com/online-results"
}

def search_school_info(query):
    query = query.lower()
    
    if "room" in query or "રૂમ" in query:
        return f"શાળામાં કુલ {sps_school_data['rooms']} રૂમ છે."
    
    elif "sound" in query or "સાઉન્ડ" in query:
        return f"સાઉન્ડ સિસ્ટમની વિગત: {sps_school_data['sound_system']}"
    
    elif "location" in query or "લોકેશન" in query:
        return f"લાઈવ લોકેશન લિંક: {sps_school_data['location']['map_link']}"
    
    elif "result" in query or "પરિણામ" in query:
        return f"ઓનલાઈન પરિણામ જોવા માટે અહીં ક્લિક કરો: {sps_school_data['results']}"
    
    elif "photo" in query or "video" in query or "ફોટા" in query:
        return f"મીડિયા ફાઇલ્સ: {sps_school_data['multimedia']['photos']} અને {sps_school_data['multimedia']['videos']}"
    
    else:
        return "ક્ષમા કરશો, આ વિગત ઉપલબ્ધ નથી. કૃપા કરીને રૂમ, સાઉન્ડ, લોકેશન અથવા પરિણામ સર્ચ કરો."

# સર્ચ કરવાનું ઉદાહરણ
print("--- S.P.S App Search ---")
user_input = input("તમે શું જાણવા માંગો છો? ")
print(search_school_info(user_input))import tkinter as tk
from tkinter import ttk, messagebox

def open_settings():
    # સેટિંગ્સ માટેની નવી વિન્ડો
    settings_window = tk.Toplevel(root)
    settings_window.title("Account Settings")
    settings_window.geometry("300x200")
    
    tk.Label(settings_window, text="એકાઉન્ટનું નામ બદલો:").pack(pady=5)
    name_entry = tk.Entry(settings_window)
    name_entry.insert(0, account_name.get())
    name_entry.pack(pady=5)
    
    def save_changes():
        account_name.set(name_entry.get())
        label_account_name.config(text=account_name.get())
        messagebox.showinfo("Success", "માહિતી અપડેટ થઈ ગઈ છે!")
        settings_window.destroy()

    tk.Button(settings_window, text="ફોટો અપલોડ કરો", command=lambda: print("Photo selected")).pack(pady=5)
    tk.Button(settings_window, text="સેવ કરો", command=save_changes, bg="green", fg="white").pack(pady=10)

# મેઈન વિન્ડો
root = tk.Tk()
root.title("My App Interface")
root.geometry("500x500")

# ૧. એકાઉન્ટ સેક્શન (નામ અને સેટિંગ બટન)
account_frame = tk.Frame(root)
account_frame.pack(fill="x", padx=20, pady=20)

account_name = tk.StringVar(value="John Doe")
label_account_name = tk.Label(account_frame, text=account_name.get(), font=("Arial", 14, "bold"))
label_account_name.pack(side="left")

# સેટિંગ બટન (બરાબર સામે)
setting_btn = tk.Button(account_frame, text="⚙ Settings", command=open_settings)
setting_btn.pack(side="right")

# ૨. કેલેન્ડર ઓપ્શન (આખા વર્ષનું)
calendar_frame = tk.Frame(root)
calendar_frame.pack(pady=20)

tk.Label(calendar_frame, text="--- વાર્ષિક કેલેન્ડર ---", font=("Arial", 12)).pack()
# અહીં નમૂના માટે લિસ્ટબોક્સ વાપર્યું છે, તમે આખું કેલેન્ડર વિજેટ પણ મૂકી શકો
calendar_list = tk.Listbox(calendar_frame, height=10, width=40)
months = ["જાન્યુઆરી", "ફેબ્રુઆરી", "માર્ચ", "એપ્રિલ", "મે", "જૂન", 
          "જુલાઈ", "ઓગસ્ટ", "સપ્ટેમ્બર", "ઓક્ટોબર", "નવેમ્બર", "ડિસેમ્બર"]
for m in months:
    calendar_list.insert(tk.END, m)
calendar_list.pack(pady=10)

root.mainloop()import tkinter as tk
from tkinter import messagebox
import webbrowser # લાઈવ લોકેશન (Google Maps) ખોલવા માટે

def open_sps_details():
    # S.P.S. માટેની નવી વિન્ડો
    sps_window = tk.Toplevel(root)
    sps_window.title("S.P.S. Details")
    sps_window.geometry("400x450")
    sps_window.configure(bg="#f0f0f0")

    tk.Label(sps_window, text="શાળાની વિગતો (S.P.S.)", font=("Arial", 16, "bold"), bg="#f0f0f0").pack(pady=10)

    # ૧. શાળાના ફોટા (બટન તરીકે)
    tk.Button(sps_window, text="📸 શાળાના ફોટા જુઓ", width=25, command=lambda: messagebox.showinfo("Gallery", "અહીં ગેલેરી ખુલશે")).pack(pady=5)

    # ૨. શાળાના વિડીઓ
    tk.Button(sps_window, text="🎥 શાળાના વિડીઓ", width=25, command=lambda: messagebox.showinfo("Video", "વિડીયો પ્લેયર લોડ થઈ રહ્યું છે...")).pack(pady=5)

    # ૩. લાઈવ લોકેશન (Google Maps લિંક)
    def open_location():
        # અહીં તમારી શાળાનું Google Maps લોકેશન નાખી શકાય
        webbrowser.open("https://www.google.com/maps")
    
    tk.Button(sps_window, text="📍 લાઈવ લોકેશન", width=25, command=open_location, bg="#4CAF50", fg="white").pack(pady=5)

    # ૪. સ્થાપના દિવસ
    tk.Label(sps_window, text="📅 સ્થાપના દિવસ: ૧૫ ઓગસ્ટ, ૧૯૯૫", font=("Arial", 12), fg="blue", bg="#f0f0f0").pack(pady=20)

def open_settings():
    settings_window = tk.Toplevel(root)
    settings_window.title("Settings")
    settings_window.geometry("300x300")
    
    # નામ બદલવાનું ઓપ્શન
    tk.Label(settings_window, text="એકાઉન્ટ સેટિંગ્સ", font=("Arial", 12, "bold")).pack(pady=10)
    tk.Button(settings_window, text="પ્રોફાઈલ એડિટ કરો", width=20).pack(pady=5)

    # --- S.P.S. ઓપ્શન (તમારા કહેવા મુજબ સેટિંગની નીચે) ---
    tk.Frame(settings_window, height=2, bd=1, relief="sunken").pack(fill="x", padx=10, pady=10) # Divider line
    
    sps_btn = tk.Button(settings_window, text="🏫 S.P.S.", font=("Arial", 11, "bold"), 
                        bg="#2196F3", fg="white", width=20, command=open_sps_details)
    sps_btn.pack(pady=10)

# મેઈન વિન્ડો સેટઅપ
root = tk.Tk()
root.title("Main App")
root.geometry("400x300")

# એકાઉન્ટ સેક્શન
main_frame = tk.Frame(root)
main_frame.pack(pady=50, padx=20, fill="x")

tk.Label(main_frame, text="Username: Admin", font=("Arial", 12)).pack(side="left")
tk.Button(main_frame, text="⚙ Settings", command=open_settings).pack(side="right")

root.mainloop()# શાળાની સુવિધાઓ અને વિગતો
school_facilities = {
    "infrastructure": {
        "cool_rooms": 10,
        "office": 2,
        "smart_tv": 5,
        "gyankunj_projects": 3
    },
    "audio_system": [
        "mic_sound_system"
    ],
    "musical_instruments": [
        "tabla",
        "manjira",
        "khanjari",
        "dholki"
    ],
    "amenities": {
        "drinking_water": "pure_water",
        "seating_arrangement": {
            "class_1_to_5": "patli",
            "class_6_to_8": "benches"
        }
    },
    "quality": "best_education"
}

# વિગતો પ્રિન્ટ કરવા માટે
print(f"કૂલ રૂમની સંખ્યા: {school_facilities['infrastructure']['cool_rooms']}")
print(f"સંગીતના સાધનો: {', '.join(school_facilities['musical_instruments'])}")class SchoolCampus:
    def __init__(self):
        # જમીન અને વિસ્તાર
        self.area = "3 Bigha"
        
        # ઇમારતો અને મેદાન
        self.infrastructure = {
            "buildings": 2,
            "sheds": 2,
            "playgrounds": 3
        }
        
        # વનસ્પતિ અને વૃક્ષો
        self.nature = {
            "total_trees": "40-35",
            "tree_types": ["Ashopalav", "Limdo (Neem)", "Karen"]
        }

    def display_info(self):
        print(f"શાળાનો વિસ્તાર: {self.area}")
        print(f"ઇમારતોની સંખ્યા: {self.infrastructure['buildings']}")
        print(f"વૃક્ષોના પ્રકાર: {', '.join(self.nature['tree_types'])}")

# શાળાનો ઓબ્જેક્ટ બનાવવો
my_school = SchoolCampus()
my_school.display_info()૧૦ શિક્ષકો હરપાલ સિહ , પંડ્યા સમીર ભાઈ , બારૈય૧૦ શિક્ષકો હરપાલ સિહ , પંડ્યા સમીર ભાઈ , બારૈયા હરેશભાઈ , બારૈયા ભરતભાઈ ,ભટ્ટ નીલેશભાઈ ,ચોપડા રાજુભાઈ,,વઘાસીયા પીયુષ ભાઈ ,સોલંકી ગણેશભાઈ ,જોશી માયાબેન ,પટેલ પાયલબેન ,આચાર્ય શ્રી બારૈયા  ભરતભાઈ અને પાયથોન ભાષામાં કોન્વેર્ત કરોschool_features = {
    "શાળાનો સમય": "૧૦:૩૦ થી ૫:૦૦",
    "પ્રવૃત્તિઓ": ["દરરોજ પ્રાર્થના", "ઇન્ટરનેશનલ રમતોમાં ભાગ"],
    "સુવિધાઓ": ["રમત ગમતના સાધનો", "કોમ્પ્યુટર લેબ", "શુદ્ધ વાતાવરણ"],
    "સ્પર્ધાત્મક પરીક્ષાઓ": ["CET", "NMMS", "PSE"]
}

# વિગતો પ્રિન્ટ કરવા માટે
print("--- શાળાની વિશેષતાઓ ---")
for key, value in school_features.items():
    if isinstance(value, list):
        print(f"{key}: {', '.join(value)}")
    else:
        print(f"{key}: {value}")schedule = {
    "સોમવાર": "ધોરણ ૬",
    "મંગળવાર": "ધોરણ ૭",
    "બુધવાર": "ધોરણ ૮",
    "ગુરુવાર": "ધોરણ ૪",
    "શુક્રવાર": "ધોરણ ૫",
    "શનિવાર": "બાળ સભા",
    "રવિવાર": "રજા"
}

# યુઝર પાસેથી વારનું નામ લેવા માટે
day = input("વારનું નામ લખો (દા.ત. સોમવાર): ")

# શિડ્યુલ ચેક કરવા માટે
if day in schedule:
    print(f"{day} ના દિવસે '{schedule[day]}' નો વારો છે.")
else:
    print("કૃપા કરીને સાચો વાર લખો.")class School:
    def __init__(self):
        self.name = "અમારી આદર્શ શાળા"
        self.established_date = "07/05/1957"
        self.student_count = "320 થી વધારે"
        self.standards = "1 થી 8"
        self.features = [
            "તદ્દન મફત શિક્ષણ (ફી... ફી... ફી...)",
            "લાઇવ લોકેશન સુવિધા",
            "પરિણામ ઓનલાઇન ચેક કરવાની સુવિધા",
            "એપ્સ લોગો અને ડિજિટલ હાજરી",
            "ફોટા અને વિડિયો ગેલેરી"
        ]
        self.nutrition = {
            "ભોજન": "સ્વચ્છ અને પૌષ્ટિક મધ્યાહન ભોજન",
            "ખાસિયત": "શાળામાં જ ઓર્ગેનિક શાકભાજીનું વાવેતર"
        }

    def display_info(self):
        print(f"--- {self.name} ---")
        print(f"સ્થાપના દિવસ: {self.established_date}")
        print(f"ધોરણ: {self.standards} (તદ્દન ફી મફત!)")
        print(f"બાળકોની સંખ્યા: {self.student_count}")
        print("\n--- મુખ્ય સુવિધાઓ ---")
        for feature in self.features:
            print(f"• {feature}")
        
        print("\n--- આરોગ્ય અને ભોજન ---")
        print(f"મેનુ: {self.nutrition['ભોજન']}")
        print(f"ખાસ નોંધ: {self.nutrition['ખાસિયત']}")

# પ્રોગ્રામ શરૂ કરવા માટે
my_school = School()
my_school.display_info()
git init
git add
git commit-m
git branch-m main
git remot add origin
