# Классификация видов тканей

Для выполнения задания мной была использована предобученная модель EfficientNet из библиотеки Torchvision. Эта модель предобучалась на датасете Imagenet, я заменила классификатор на подходящий под нашу задачу (изменила количество классов) и дообучила модель несколько эпох на датасете train. Итоговое качество на test: 0.9796 accuracy, на test_tiny: 0.9556

Дополнительно реализовано:
1) LBL1 Вывод значения функции потерь и accuracy во время обучения
2) LBL2 Использование аугментации (RandomRotate, RandomHorizontalFlip - использовала то, что не меняет цвет картинки и не искажает ее, так как данная задача чувствительна к этим параметрам. Поворот и отражение же в данном случае никак не мешают)
3) LBL3 Валидация модели во время обучения на выборке test_small
