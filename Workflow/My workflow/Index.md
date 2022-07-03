# Safurion workflow

## Введение 
В этот рабочий процесс будет входить сбор требований, аналитика и прототипирование, чтобы перед началом непосредственной разработки у нас не было вопросов без ответа. Данный рабочий процесс может претерпеть изменения, но он должен покрывать следущие качества:
1. Он должен поддерживать линейную инверсию. То есть каждая конечная точка в процессе имеет только одно начало. 
1. Каждая новая ветка процесса должна завершаться не ожидая другие ветки
1. Каждая ветка процесса может ожидать на каждом из статусных состояний неограниченное кол-во времени и это ожидание не должно оказывать никакого эффекта на другие ветки рабочего процесса 

# Рабочие процессы для каждого элемента 

В нашем текущем процесса существуют следующие рабочие элементы(описание доступно в словаре): <a href="Dictionary.md#Epic" name="Epic">Epic</a>, <a href="Dictionary.md#Feature" name="Feature">Feature</a>, <a href="Dictionary.md#Story" name="Story">Story</a>, <a href="Dictionary.md#Bug" name="Bug">Bug</a>, <a href="Dictionary.md#Issue" name="Issue">Issue</a>,  <a href="Dictionary.md#Task" name="Task">Task</a>. 

<a href="Dictionary.md#Epic" name="Epic">Epic</a> имеет следующий жизненный цикл: 

1. <a href="Index.md#EpicNew" name="EpicNew">Новый</a> - New - Новый созданные элемент этого типа его может создать любой сотрудник. На этом этапе Epic может не иметь конечного описания. Автор эпика становиться Скрам Мастеров в контексте этого эпика
1. <a href="Index.md#EpicInProcess" name="EpicInProcess">В работе</a> - In Process - Человек создавший эпик, корректирует описание, чтобы придать ему конечную форму. Этот статус может поставить только автор элемента
1. <a href="Index.md#EpicToApprove" name="EpicToApprove">На одобрении</a> - To Approve - Эпик ждёт одобрения со стороны <a href="Dictionary.md#ProductOwner" name="ProductOwner">Product Owner</a>. Этот статус может поставить только автор элемента.
1. <a href="Index.md#EpicApproved" name="EpicApproved">Одобрен</a> - Approved - Эпик одобрен со стороны <a href="Dictionary.md#ProductOwner" name="ProductOwner">Product Owner</a> и готов к <a href="Index.md#EpicAnalysis" name="EpicAnalysis">аналитике</a>, то есть у него появилась первая <a href="Dictionary.md#AnalysisFeature" name="AnalysisFeature">Analysis Feature</a>. Этот статус может поставить только  <a href="Dictionary.md#ProductOwner" name="ProductOwner">Product Owner</a>. После получения этого статуса, текст Эпика идёт в Wiki документа как в виде начала нового раздела. 
1. <a href="Index.md#EpicAnalysis" name="EpicAnalysis">Анализируется</a> - Analysis - Эпик проходит стадию системного анализа и прототипирования, к нему начинают создаваться дочерние <a href="Dictionary.md#AnalysisFeature" name="AnalysisFeature">Analysis Feature</a>. Этот статус может поставить любой член <a href="Dictionary.md#AnalysisTeam" name="AnalysisTeam">аналитической группы</a>, который начинает аналитику.
1. <a href="Index.md#EpicToDevelopment" name="EpicToDevelopment">Готов к разработке</a> - To Development - Эпик готов к разработке, то есть хотя бы одна его <a href="Dictionary.md#AnalysisFeature" name="AnalysisFeature">Analysis Feature</a> прошла стадию прототипирования и <a href="Index.md#AnalysisFeatureApproved" name="AnalysisFeatureApproved">одобрена</a>. Этот статус может поставить только автор элемента.
1. <a href="Index.md#EpicInDevelopment" name="EpicInDevelopment">В разработке</a> -  In Development - Эпик готов к разработке, то есть хотя бы одна его фича вошла в стадию <a href="Index.md#AnalysisFeatureInDevelopment" name="AnalysisFeatureInDevelopment">В разработке</a>. Этот статус может поставить только автор элемента.
1.  <a href="Index.md#EpicReleased" name="EpicReleased">Реализована</a> - Released - Все дочерние <a href="Dictionary.md#AnalysisFeature" name="AnalysisFeature">Analysis Feature</a> получили статус <a href="Index.md#AnalysisFeatureReleased" name="AnalysisFeatureReleased">Реализована</a>.

<a href="Dictionary.md#AnalysisFeature" name="AnalysisFeature">Analysis Feature</a> имеет следующий жизненный цикл: 

1. <a href="Index.md#AnalysisFeatureNew" name="AnalysisFeatureNew">Новый</a> - New - Новый созданные элемент этого типа его может создать только член <a href="Dictionary.md#AnalysisTeam" name="AnalysisTeam">аналитической группы</a>. На этом этапе Analysis Feature может не иметь конечного описания. 
1. <a href="Index.md#EpicInProcess" name="EpicInProcess">В работе</a> - In Process - <a href="Dictionary.md#AnalysisTeam" name="AnalysisTeam">Аналитическая группа</a>, корректирует описание фичи, чтобы придать ей конечную форму. Этот статус может поставить только член <a href="Dictionary.md#AnalysisTeam" name="AnalysisTeam">Аналитической группы</a>. Так создаются дочерние 
1. <a href="Index.md#EpicToApprove" name="EpicToApprove">На одобрении</a> - To Approve - Эпик ждёт одобрения со стороны <a href="Dictionary.md#ProductOwner" name="ProductOwner">Product Owner</a>. Этот статус может поставить только автор элемента.
1. <a href="Index.md#EpicApproved" name="EpicApproved">Одобрен</a> - Approved - Эпик одобрен со стороны <a href="Dictionary.md#ProductOwner" name="ProductOwner">Product Owner</a> и готов к <a href="Index.md#EpicAnalysis" name="EpicAnalysis">аналитике</a>, то есть у него появилась первая <a href="Dictionary.md#AnalysisFeature" name="AnalysisFeature">Analysis Feature</a>. Этот статус может поставить только  <a href="Dictionary.md#ProductOwner" name="ProductOwner">Product Owner</a>. После получения этого статуса, текст Эпика идёт в <a href="https://github.com/k-kalashnikov/azgame/blob/master/Wiki/Index.md">Wiki</a> документа как в виде начала нового раздела. 
1. <a href="Index.md#EpicAnalysis" name="EpicAnalysis">Анализируется</a> - Analysis - Эпик проходит стадию системного анализа и прототипирования, к нему начинают создаваться дочерние <a href="Dictionary.md#AnalysisFeature" name="AnalysisFeature">Analysis Feature</a>. Этот статус может поставить любой член <a href="Dictionary.md#AnalysisTeam" name="AnalysisTeam">аналитической группы</a>, который начинает аналитику.
1. <a href="Index.md#EpicToDevelopment" name="EpicToDevelopment">Готов к разработке</a> - To Development - Эпик готов к разработке, то есть хотя бы одна его <a href="Dictionary.md#AnalysisFeature" name="AnalysisFeature">Analysis Feature</a> прошла стадию прототипирования и <a href="Index.md#AnalysisFeatureApproved" name="AnalysisFeatureApproved">одобрена</a>. Этот статус может поставить только автор элемента.
1. <a href="Index.md#EpicInDevelopment" name="EpicInDevelopment">В разработке</a> -  In Development - Эпик готов к разработке, то есть хотя бы одна его фича вошла в стадию <a href="Index.md#AnalysisFeatureInDevelopment" name="AnalysisFeatureInDevelopment">В разработке</a>. Этот статус может поставить только автор элемента.
1.  <a href="Index.md#EpicReleased" name="EpicReleased">Реализована</a> - Released - Все дочерние <a href="Dictionary.md#AnalysisFeature" name="AnalysisFeature">Analysis Feature</a> получили статус <a href="Index.md#AnalysisFeatureReleased" name="AnalysisFeatureReleased">Реализована</a>.

<a href="Dictionary.md#Feature" name="Feature">Development Feature</a> имеет следующий жизненный цикл:
1. <a href="Index.md#FeatureNew" name="FeatureNew">Новый</a> - New - Новый созданные элемент этого типа его может создать только ТимЛид разработки, на этом моменте элемент должен иметь полное описание
1. <a href="Index.md#FeatureDecomposition" name="FeatureDecomposition">На декомпозиции </a> - Decomposition - Этот статус может поставить только ТимЛид разработки. Элемент делиться на дочерние задачи
1. <a href="Index.md#FeatureInProgress" name="FeatureInProgress">В работе</a> - In Process - Статус ставиться автоматически, когда первая задача ушла в работу
1. <a href="Index.md#FeatureTesting" name="FeatureTesting">На Тестировании</a> - Testing - Статус ставиться вручную, когда последняя задача прошла тестирование и нужно протестировать весь функционал Feature целиком. Этот статус может поставить только ТимЛид разработки
1. <a href="Index.md#FeatureTested" name="FeatureTested">Протестирована</a> - Tested - Статус ставиться вручную, когда задача feature прошла тестирование. Статус может поставить только QA
1. <a href="Index.md#FeatureToRelease" name="FeatureToRelease">Готова к релизу</a> - To Release - Статус ставиться вручную, может поставить только ТимЛид разработки. Ставиться, когда feature готова к публикации в продакшн или предпродакшн 
1. <a href="Index.md#FeatureReleased" name="FeatureReleased">Готова</a> - Released  - Ставиться вручную, когда feature была опубликована в продакшн или предпродакшн

 <a href="Dictionary.md#Bug" name="Bug">Bug</a> имеет следующий жизненный цикл:
 1. Новый - Новый созданные элемент этого типа его может создать только: разработчики, служба технической поддержки, QA. При этом в описании должен быть описан позитивный сценарий при котором ошибки нет.
 1. На проверке - Элемент отправился на проверку к QA, которые должны удостовериться, что баг существует. Этот статус могут поставить только QA
 1. Подтвержденный - Элемент прошёл проверку QA и была найдена описанная ошибка, на этом моменте в элемент должна быть добавлена информация откуда и почему возникла ошибка. 
 1. НеПодтвержденный - Элемент не прошёл проверку QA, после этого статуса баг считается закрытым
 1. Готов к разработке - Элемент декомпозирован на задачи для нужных отделов разработки. Этот статус может поставить только QA 
 1. В разработке - Элемент взят в работу Этот статус ставиться автоматически, когда первая задача взята в работу
 1. <a href="Index.md#BugTesting" name="BugTesting">На Тестировании</a> - Testing - Статус ставиться вручную, когда последняя задача прошла тестирование и нужно протестировать весь функционал Feature целиком. Этот статус может поставить только ТимЛид разработки
1. <a href="Index.md#BugTested" name="BugTested">Протестирована</a> - Tested - Статус ставиться вручную, когда задача feature прошла тестирование. Статус может поставить только QA
 1. Исправлен - Этот статус ставиться, когда баг исправлен. Статус может поставить только QA и Баг публикуется со следующим релизом

 <a href="Dictionary.md#Task" name="Task">Task</a> имеет следующий жизненный цикл:
 1. Новая 
 1. В работе
 1. На тестировании
 1. Протестирована
 1. На ревью
 1. Готова

 <a href="Dictionary.md#Issue" name="Issue">Issue</a> имеет следующий жизненный цикл:
 1. Новая
 1. На Аналитке
 1. В работе
 1. На тестировании
 1. Протестирована
 1. Готова
 1. Не будет выполнена