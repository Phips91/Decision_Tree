# Decision Tree
Repository für die Angleichsleistung im Studiengang DBE

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Phips91/Decision_Tree.git/HEAD)


Hier ist eine kurze Dokumentation zum gegebenen Code:

Die vorliegende Code-Dokumentation beschreibt ein Projekt zur Erstellung von Entscheidungsbäumen und Random Forests für die Vorhersage, ob ein Kreditnehmer bei LendingClub.com ein Darlehen vollständig zurückzahlen wird oder nicht. Das Projekt verwendet öffentlich verfügbare Daten von LendingClub.com von 2007 bis 2010. Ziel ist es, ein Modell zu erstellen, das Kreditgeber dabei unterstützt, Kreditnehmer auszuwählen, die mit hoher Wahrscheinlichkeit ihr Darlehen zurückzahlen werden.
Schritt 1: Importieren von Bibliotheken und Laden der Daten

In diesem Schritt werden die erforderlichen Python-Bibliotheken importiert, darunter Pandas, NumPy, Matplotlib und Seaborn. Anschließend werden die Daten aus der Datei "Loan_Data.csv" in ein Pandas DataFrame namens "loans" geladen. Die Methode info(), head(), und describe() werden verwendet, um einen Überblick über die Daten zu erhalten.
Schritt 2: Explorative Datenanalyse (EDA)

In diesem Schritt werden verschiedene Visualisierungen durchgeführt, um die Daten besser zu verstehen. Folgende Visualisierungen werden erstellt:

    Ein Histogramm der FICO-Scores, aufgeteilt nach der "credit.policy"-Spalte.
    Ein Histogramm der FICO-Scores, aufgeteilt nach der "not.fully.paid"-Spalte.
    Ein Countplot, das die Anzahl der Darlehen nach dem Zweck ("purpose") zeigt, wobei die Farben die Rückzahlung oder Nicht-Rückzahlung ("not.fully.paid") anzeigen.
    Ein Jointplot, das den Zusammenhang zwischen FICO-Score und Zinssatz ("int.rate") darstellt.
    Ein paar lmplots, um den Unterschied im Trend zwischen "not.fully.paid" und "credit.policy" zu untersuchen.

Schritt 3: Daten vorbereiten

In diesem Schritt werden die Daten für die Verwendung in einem Klassifikationsmodell vorbereitet. Die kategorische Spalte "purpose" wird in Dummy-Variablen umgewandelt, damit sie von Machine-Learning-Algorithmen verarbeitet werden kann. Die Methode pd.get_dummies() wird verwendet, um diese Transformation durchzuführen.
Schritt 4: Train-Test-Split

Die Daten werden in Trainings- und Testsets aufgeteilt, wobei 70% der Daten für das Training und 30% für Tests verwendet werden. Dies wird mit Hilfe von train_test_split aus scikit-learn durchgeführt.
Schritt 5: Training eines Entscheidungsbaum-Modells

Ein einfaches Entscheidungsbaum-Klassifikationsmodell wird trainiert, indem die DecisionTreeClassifier-Klasse aus scikit-learn verwendet wird. Das Modell wird auf den Trainingsdaten mit der Methode fit angepasst.
Schritt 6: Vorhersage und Auswertung des Entscheidungsbaum-Modells

Mit dem trainierten Modell werden Vorhersagen für die Testdaten erstellt. Dann wird ein Klassifikationsreport und eine Confusion Matrix erstellt, um die Leistung des Modells zu bewerten.
Schritt 7: Training eines Random Forest-Modells

Ein Random Forest-Klassifikationsmodell wird trainiert, indem die RandomForestClassifier-Klasse aus scikit-learn verwendet wird. Das Modell wird auf den Trainingsdaten mit der Methode fit angepasst.
Schritt 8: Vorhersage und Auswertung des Random Forest-Modells

Mit dem trainierten Modell werden Vorhersagen für die Testdaten erstellt. Ein Klassifikationsreport und eine Confusion Matrix werden erstellt, um die Leistung des Modells zu bewerten.
Schritt 9: Bewertung der Modelle

Am Ende des Codes wird die Leistung der beiden Modelle bewertet, wobei auf den Recall für beide Modelle hingewiesen wird. Es wird darauf hingewiesen, dass keines der Modelle besonders gut ist und eine bessere Anpassung der Modellparameter erforderlich sein könnte.

Das Projekt endet mit einer Aufforderung zur Bewertung der Leistung der Modelle und der Anpassung der Eigenschaften, um die Vorhersagegenauigkeit zu verbessern.
