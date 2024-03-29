Недавно я уже писал про [алгоритм внешней калибровки датчика профилей](/professional-projects?id=12). В том варианте использовалась двухэтапная процедура. Сначала происходило получение профилей калибровочной сферы при фиксированной ориентации сканера для определения его углов поворота, а на втором этапе происходил сбор профилей с различными ориентациями сканера для определения его смещения.

В новой версии алгоритма мне удалось упростить эту процедуру, что позволило выполнять калибровку всего по 10-15 профилям с различными положениями и ориентациями сканера. Процесс численной оптимизации происходит сразу по 6 искомым параметрам.

На анимации ниже показан процесс поиска решения. Видно, как в процессе оптимизации профили постепенно приближаются к поверхности сферы. При этом расчётный радиус сферы приближается к истинному радиусу калибровочной сферы, равному 50 мм. Окончательная среднеквадратичная ошибка отклонения точек от поверхности сферы составляет около 0.06 мм<sup>2</sup>.

Алгоритм был реализован на языке C++ с использованием библиотеки Ceres Solver для численной оптимизации. Для визуализации использовалась библиотека PCL.
