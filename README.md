WorkoutTracker - трекер тренировок. Приложение для учета тренировок: дата тренировки, кол-во подходов, повторений или тайминг тренировки. Статистика выполенных упражнений с поиском. Экран с профилем.

Верстка кодом (без storyboard)

Стек используемых технологий:

- TableView (+ создание customTableViewCell)
- CollectionView (+ создание customCollectionViewCell)
- ScrollView
- AlertController (+ создание custom alert)
- UIKit (label, button, segmentedControll, Switch, Slider, UIView, UIImageView, textField, DatePicker)
- Date (преобразование)
- Notifications
- Основы CoreAnimation
- Переходы между экранами и передача данных между ними
- JSON
- Realm
- TabBarController (+ NavigatonBar)
- Установка шрифтов

Главный экран:
- коллекция с календарем (CollectionView) показывате текущую дату.
- блок с погодой (API), показывает текущую температуру в регионе.
- добавление новой тренировки - Button.
- таблица со списком тренировок (TableView)
- навигация - TabBarController

https://user-images.githubusercontent.com/98170830/205348101-272bacf7-ed13-4d43-96cd-99565a13fcb5.mov

Создание новой тренировки:
- название,
- дата (DatePicker)
- повторять каждые 7 дней - да/нет (switch)
- подходы (slider) - при этом таймер становится не активным.
- повторения или таймер  (slider) - при этом слайдер подходы становится не активным.
- Сохранить - кнопка. При успешном сохранении вылетает стандартный alert об успешном сохранении. При сохранении тренировка появляется на главном экране 
в TableView. Тренировку можно удалить по свайпу влево.


https://user-images.githubusercontent.com/98170830/205349949-76512e89-e0b0-494e-9595-129291690055.mov

Старт тренировки: При нажатии на кнопку старт попадаем на один из экранов с повторениями либо с таймером.
- Экран повторения: при выполнении повторений нажать на ПРОДОЛЖИТЬ количество выполенных подходов увеличивается на 1. 
- Экран с таймером: таймер запускает время отведенное на 1 подход. По истечению времени количество подходов увеличивается на 1. При нажатии на ПРОДОЛЖИТЬ 
также увеличиваются подходы.
- На обоих экранах есть кнопка ИЗМЕНИТЬ - анимация сверху кастомный alert controller в котором можно отредактировать количество подходов, повторений и время упражнения. При нажатии на OK - alert уезжает вниз.
- при достижении нужного кол-ва подходов вылетает alert о том, что тренировка закончена.
- при нажатии на ЗАКОНЧИТЬ треноровка становится ВЫПОЛНЕННОй на главном экране. Тренировка становится не активна.

https://user-images.githubusercontent.com/98170830/205350836-770ee109-31a9-4b61-9a11-da7d9b12c3e5.mov

https://user-images.githubusercontent.com/98170830/205350869-abc7ca80-35f1-46ce-9614-f4a439d116de.mov

Экран статистика: 
- показывает статистику за неделю и за месяц (segmentedControl), т.е. показывается прогресс тренировок по каждому упражнению.
- строка поиска - SearchControlller.

https://user-images.githubusercontent.com/98170830/205351192-63e22f54-c9fe-4e5e-8bc8-a49623aefde4.mov

Экран профиль:
- данные пользователя - imageView и  lable.
- таблица с упражнениями - CollectionView - скролится по горизонтали.
- кнопка ИЗМЕНИТЬ - преход на экран заполнения/редактирования профиля.

Экран заполнения/редактирования профиля:
- загрузка фото пользователя - UIImagePickerController
- поля - textField
- кнопка сохранить.

https://user-images.githubusercontent.com/98170830/205351670-cfce9d88-3e17-4d3b-892f-5fbf5f4487f4.mov


