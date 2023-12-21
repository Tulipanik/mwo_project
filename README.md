***MWO Projekt- laboratorium 5***
---
Zadanie polegało na przygotowaniu odpowiedniego oprogramowania typu CRUD oraz przetestowaniu go przy użyciu Selenium. Dodatkowo należało wykonać pipeline, który będzie zgłaszał błąd na pralformie azuye DevOps.

1. Pierwszym etapem było przygotowanie aplikacji. W moim przypadku wykorzystałam aplikację przygotowaną w ramach zajęć Projektowanie aplikacji mobilnych i webowych. Testy zostały wykonane po stronie serwera aplikacji. Proces testownia oraz zastosowany kod jest przedstawiony na załączonym w repozytorium nagraniu.
2. Następnie należało przygotować odpowiednie środowisko w aplikacji Azure DevOps. W tym celu tworzę najpierw projekt na tej platformie (w moim przypadku w metodyce scrum).
   ![kreacja projektu scrum](/images/Project_creation.png)

   Następnie należało utworzyć token na platformie. W tym celu należało wcisnąć przycisk ustawień przy użytkowniku. W menu rozwija się zakładka "Personal Access tokens"
   ![PAT](/images/PAT_1.png)

   Następnie należy wcisnąć przycisk "+ New Token"
   ![PAT 2](/images/PAT_2.png)

   W zakładce należy uzupełnić dane tokenu. Ważne aby zezwolić na zarządzanie Work Items. Inaczej nie będzie możliwości zgłoszenia błędy z poziomu GitHub Actions
   ![PAT 3](/images/PAT_3.png)

3. Kolenym etapem jest konfiguracja pipeline. W tym celu otwieram zakładę Settings, tam zakładkę branches i dodaję nową regułę. W regule zaznaczam wymaganie wykonania pull requesta oraz brak możliwości pominięcia reguły.
   ![Ustawienia pipeline 1](/images/pipeline_settings.png)
   ![Ustawienia pipeline 2](/images/pipeline_settings_2.png)

Należy również ytworzyć token git hub, można to zrobić w ustawieniach użytkownika
