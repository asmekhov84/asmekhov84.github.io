В составе команды из 2 человек работал над системой компьютерного зрения для автоматизированного комплекса лазерной резки. Отвечал, в основном, за разработку алгоритмов обработки облаков точек и полигональных поверхностей: фильтрация, оценка нормалей, кластеризация, совмещение облаков точек, реконструкция поверхности по облаку точек и т.д. Также разработал небольшие приложения для калибровки датчика профилей, закреплённого на 6-осевом манипуляторе, и калибровки неподвижного 3D датчика относительно базы манипулятора.

Ещё одним заметным проектом было приложение для помощи в разметке медицинских видеозаписей, полученных с помощью эндоскопа. Это устройство, оснащённое видеокамерой и оптоволокном, проводящим лазерное излучение, использовалось для дробления камней в почках. Задача состояла в том, чтобы создать инструмент разметки видео и обучить алгоритмы понимать, направлено ли лазерное волокно на камень или нет, и тем самым предотвратить повреждение тканей человека. В этой работе я создавал клиентское приложение, реализованное на C++ и фреймворке Qt. Это приложение позволяет загружать видеофайл и выбирать метку для каждого кадра вручную или автоматически, используя предварительно обученную модель, а затем экспортировать этот набор данных для дальнейшего использования.

**Технологии**: C++, STL, Eigen, PCL, OpenCV, Ceres Solver, LibIGL, CGAL, OpenCASCADE, Qt, Visual Studio, Git, Windows, Jira, Bitbucket