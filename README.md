# Прогнозирование оттока клиентов в сети отелей «Как в гостях»
Заказчик этого исследования — сеть отелей «Как в гостях».
Чтобы привлечь клиентов, эта сеть отелей добавила на свой сайт возможность забронировать номер без предоплаты. Однако если клиент отменял бронирование, то компания терпела убытки. Сотрудники отеля могли, например, закупить продукты к приезду гостя или просто не успеть найти другого клиента.
Чтобы решить эту проблему, нужно разработать систему, которая предсказывает отказ от брони. Если модель покажет, что бронь будет отменена, то клиенту предлагается внести депозит. Размер депозита — 80% от стоимости номера за одни сутки и затрат на разовую уборку. Деньги будут списаны со счёта клиента, если он всё же отменит бронь.

## Выводы
* наилучший показатель F1-меры показала модель решающего дерева (0.66 в среднем при кросс-валидации, 0.55 на тестовой выборке), метрика ROC-AUC для на нее составила 0.74;
* внедрение модели окупится и принесет компании более 6,2 млн. руб. за год (по данным из тестовой выборки);
* модель относит к ненадежным клиентам португальцев с типом заказчика 'Transient', а также клиентов, с большим количеством дней между датой бронирования и датой прибытия;
* признаки ненадежного клиента выделенные в ходе анализа:
  - тип питания 'BB' (19 тыс. из 24 тыс.);
  - гражданство 'PRT' (16.6 тыс.);
  - номер категории 'A' (19.7 тыс.);
  - канал сбыта 'TA/TO' (22 тыс.);
  - тип заказчика 'Transient' (18 тыс.);
  - большой срок между датой бронирования и датой прибытия;
  - большое количество отмененных заказов у клиента;
  - большое количество дней подтверждения брони.
