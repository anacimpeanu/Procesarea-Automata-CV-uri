# 📄 Procesare Automată a CV-urilor

Această aplicație automatizează procesul de colectare, organizare și analiză a CV-urilor primite prin email, extrăgând informații relevante și generând un raport centralizat.

---

## 🚀 Funcționalități principale

- 📩 **Identificarea emailurilor relevante**
  - Monitorizare automată a unei căsuțe de email dedicate
  - Identificarea emailurilor conform unor criterii predefinite (subiect, atașamente PDF)
  
- 📥 **Descărcarea și organizarea atașamentelor**
  - Descărcarea automată a fișierelor PDF atașate
  - Salvarea CV-urilor într-un folder organizat, cu denumire standardizată (`Nume_Prenume_Data.pdf`)
  
- 📊 **Extracția informațiilor relevante din CV-uri**
  - **Informații personale**: Nume, prenume, email, număr de telefon, adresă
  - **Experiență profesională**: Istoricul locurilor de muncă
  - **Educație**: Studii finalizate și calificări
  
- 📑 **Generarea unui raport centralizat (Excel)**
  - Crearea automată a unui raport Excel cu datele extrase
  - Organizarea informațiilor în coloane relevante (Nume, Prenume, Date de contact, Experiență profesională, Educație, Adresă, Job etc.)
  
- 📤 **Trimiterea raportului către HR**
  - Salvarea raportului într-o locație desemnată
  - Trimiterea automată a raportului Excel către departamentul de HR prin email

---

## 🛠️ Tehnologii utilizate
- **UiPath Studio** – pentru implementarea automatizării
- **Automation GPT** – pentru extragerea datelor din CV-uri
- **Excel Automation** – pentru generarea rapoartelor
- **IMAP/SMTP** – pentru gestionarea emailurilor

---

## 🔄 Workflow-uri utilizate

| Workflow | Descriere |
|----------|------------|
| `Config.xaml` | Creează structura de foldere necesară, încarcă configurația din `config.json` și gestionează logarea erorilor inițiale |
| `GetEmails.xaml` | Se conectează la email folosind IMAP, descarcă atașamente PDF din emailurile necitite și le salvează într-un folder specific |
| `Main.xaml` | Orchestrarea principală a execuției: configurare, preluare emailuri, procesare CV-uri, trimitere rapoarte |
| `ProcessCV.xaml` | Citește conținutul CV-urilor PDF salvate, extrage informații relevante folosind AI și creează un raport Excel |
| `SendEmailReport.xaml` | Trimite rezultatele procesate prin Outlook, atașând raportul Excel generat |
| `config.json` | Stochează setările de conexiune email, regulile de procesare și căile de salvare |

---

## 📂 Structura folderelor

Aplicația conține un folder `data`, care este organizat astfel:

- 📁 `CVs/` - conține toate CV-urile descărcate din emailuri
- 📁 `Reports/` - stochează rapoartele Excel generate în urma procesării CV-urilor

---

## 📥 Instalare și utilizare

1. **Clonează repository-ul**
   ```bash
   git clone https://github.com/utilizator/procesare-cv.git
   cd procesare-cv
   ```
2. **Deschide proiectul în UiPath Studio**
3. **Rulează `Main.xaml` pentru a începe procesarea CV-urilor**

---

## 📜 Licență
Acest proiect este licențiat sub **MIT License**.

## 👩‍💻 Autor
**Cîmpeanu Ana-Maria**  
📍 Universitatea din București  
📅 2024-2025  


