# Словарь терминов рабочего процесса

1. <a href="Dictionary.md#Epic" name="Epic">Epic</a> - это описанная простым языком пожелание, потребность реализации нового функционала, проведения исследования или реализация большой сторонней работы. <a href="Dictionary.md#Epic" name="Epic">Epic</a> может иметь несколько дочерних <a href="Dictionary.md#Feature" name="Feature">Feature</a>.    

1. <a href="Dictionary.md#AnalysisFeature" name="AnalysisFeature">Analysis Feature</a> - это описанная более системным языком, с использования терминов, которые используются на проекте общая доработка, изменение отдельной бизнеслогической ветки функционала(например функционал создания персонажа или регистрация пользователя в продукте). Текст фичи может быть изменён в процессе её жизненного цикла <a href="Dictionary.md#Feature" name="Feature">Feature</a> может иметь только один родительский <a href="Dictionary.md#Epic" name="Epic">Epic</a> и несколько дочерних <a href="Dictionary.md#Task" name="Task">Task</a> и <a href="Dictionary.md#Feature" name="Feature">Development Feature</a>

1. <a href="Dictionary.md#Feature" name="Feature">Development Feature</a> - это описанная более техническим языком набор изменений или исследований, которые должны быть произведи в рамках продукта. <a href="Dictionary.md#Feature" name="Feature">Feature</a> может иметь только один родительский <a href="Dictionary.md#AnalysisFeature" name="AnalysisFeature">Analysis Feature</a> и несколько дочерних <a href="Dictionary.md#Story" name="Story">Story</a>

1. <a href="Dictionary.md#Story" name="Story">Story</a> - это описанная полностью техническим языком общая доработка, изменение отдельного технического сектора проекта (например бекенд или дизайн) <a href="Dictionary.md#Story" name="Story">Story</a> может иметь только один родительский <a href="Dictionary.md#Feature" name="Feature">Feature</a> и несколько дочерних <a href="Dictionary.md#Task" name="Task">Task</a>

1. <a href="Dictionary.md#Bug" name="Bug">Bug</a> - это элемент который содержит в себе описание ошибки работы функционала, который уже вышел в релизную версию продукта. Может иметь несколько дочерних <a href="Dictionary.md#Task" name="Task">Task</a>

1. <a href="Dictionary.md#Issue" name="Issue">Issue</a> - это элемент который содержит в себе описание работ по поддержке продукта, которые появляются из <a href="Dictionary.md#СторонниеИсточники" name="СторонниеИсточники">сторонних источников</a> , который уже вышел в релизную версию продукта. Может иметь несколько дочерних <a href="Dictionary.md#Task" name="Task">Task</a>

1. <a href="Dictionary.md#Task" name="Task">Task</a> - Это элемент, который описывает задачу, которая готова к исполнению, не может быть декомпозирована, имеет критерии приёмки и точно описанный порядок действий для её выполннения. Не имеет дочерних элементов. 

1. <a href="Dictionary.md#СторонниеИсточники" name="СторонниеИсточники">Сторонние источники</a> - это источники появления новых доработок, которые не являются стороной бизнеса, например - <a href="Dictionary.md#ProductOwner" name="ProductOwner">Product Owner</a>

1. <a href="Dictionary.md#ProductOwner" name="ProductOwner">Product Owner</a> - Сотрудник, который берёт на себя роль номинальный владельца продукта. В её обязанности определять бизнес вектор развития продукта. Оставляет за собой право на одобрение или неодобрение разработки нового или изменение текущего функционала. Product Owner является ответственным лицом перед фактическими владельцами продукта. 

1. <a href="Dictionary.md#ScrumMaster" name="ScrumMaster">Scrum master</a> - человек, который создаёт первый родительский элемент в рабочем процесса, Скрам мастер обязан проводить статусные собрания связанные с его работой над его элементом. Скрам мастер является ответственным лицом перед <a href="Dictionary.md#ProductOwner" name="ProductOwner">Product Owner</a> за состояние его элемента. 

1. <a href="Dictionary.md#AnalysisTeam" name="AnalysisTeam">Аналитическая групп</a> - Это лиды отделов внутри команды работающей над продуктом. 

