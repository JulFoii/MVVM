---
marp: true
theme: gaia
paginate: true
backgroundColor: #F4F4F4
transition: slide
---

# **MVVM - Ein Architekturmuster für moderne Anwendungen**

---

## **Einführung in MVVM**
- MVVM = Model-View-ViewModel  
- Ein Architekturmuster zur besseren Strukturierung von Anwendungen  
- Entwickelt für UI-getriebene Anwendungen  
- Wichtig für skalierbare, wartbare und testbare Software  


---

## **Warum Architekturmuster?**
- Klare Trennung von Verantwortlichkeiten  
- Erleichtert Wartung und Erweiterung  
- Fördert Wiederverwendbarkeit von Code  
- Reduziert Abhängigkeiten zwischen UI & Geschäftslogik

---

## **Die drei Hauptkomponenten von MVVM**
 **Model:** Daten & Geschäftslogik  
 **View:** UI-Darstellung  
 **ViewModel:** Vermittler zwischen Model & View

---

## **Wie funktioniert MVVM?**
- Die View ruft keine Geschäftslogik direkt auf  
- Die ViewModel-Schicht verarbeitet Benutzereingaben  
- Das Model liefert die eigentlichen Daten  
- Änderungen im Model aktualisieren die View via Data-Binding

---

## **Vorteile von MVVM**
 - Bessere Trennung von UI und Logik
 - Erhöhte Testbarkeit durch isolierte Logik
 - Wiederverwendbare & austauschbare UI-Komponenten
 - Skalierbare Anwendungskonzepte

---

## **Vergleich mit anderen Architekturmustern**
### **MVC (Model-View-Controller)**
- Klassisch für Webanwendungen
- Controller agiert als Vermittler
- Stärkere Kopplung zwischen UI & Logik

### **MVP (Model-View-Presenter)**
- Eher für Desktop-Anwendungen
- Presenter übernimmt UI-Logik

### **MVVM (Model-View-ViewModel)**
- Perfekt für moderne UI-Frameworks
- Nutzt Data-Binding für bessere Trennung

---

## **MVVM in der Praxis (Code-Beispiel)**
### **Model:**
```csharp
public class Person
{
    public string Name { get; set; }
    public int Alter { get; set; }
}
```

### **ViewModel:**
```csharp
public class PersonViewModel : INotifyPropertyChanged
{
    public ObservableCollection<Person> PersonenListe { get; set; }
}
```

### **View (XAML):**
```xml
<ListView ItemsSource="{Binding PersonenListe}">
    <ListView.ItemTemplate>
        <DataTemplate>
            <TextBlock Text="{Binding Name}" />
        </DataTemplate>
    </ListView.ItemTemplate>
</ListView>
```

📌 *Nutzen von `INotifyPropertyChanged` für reaktive UI-Updates*

---

## 🌍 **MVVM in modernen Frameworks**
 **WPF (.NET)** → Desktop-Anwendungen  
 **Blazor (WebAssembly)** → Webanwendungen  
 **SwiftUI (Apple)** → Apple-Ökosystem  
 **Angular + RxJS** → Reaktive Webarchitektur

---

## Herausforderungen & Best Practices
**Herausforderungen:**
- Höhere Komplexität durch zusätzliche Abstraktionsschicht  
- Debugging von Data-Binding kann schwierig sein  

**Best Practices:**
- Nutzung von MVVM-Frameworks (Prism, ReactiveUI)  
- Klare Trennung der Zuständigkeiten  
- Dependency Injection zur besseren Testbarkeit

---

## **Fazit**
 - MVVM sorgt für saubere, wartbare und testbare Software**  
 - Optimal für UI-Entwicklung in Desktop-, Mobile- und Webanwendungen**  
 - Erfordert anfangs Einarbeitung, aber bietet langfristige Vorteile**

---

## **Danke für eure Aufmerksamkeit**

**Habt ihr Fragen?**
