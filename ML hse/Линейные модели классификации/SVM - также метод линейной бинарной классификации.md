
![[Pasted image 20250205104559.png]]

![[Pasted image 20250205104417.png]]
![[Pasted image 20250205104434.png]]
![[Pasted image 20250205104457.png]]![[Pasted image 20250205104627.png]]
# #ЗадачаSVMдляЛинейноРазделимогоСлучая
![[Pasted image 20250205104640.png]]
# #ЗадачаSVMдляОбщегоСлучая - то есть здесь мы сделали 1 - $\xi$, т.е разрешили быть ближе чем на 1 объектам. Ну, и, соответственно, мы должны сделать это разрешение как можно меньше (минимизируем это вместе с $\frac{1}{2}||w||^2$).  
![[Pasted image 20250205105544.png]]

# #ПроОтступSVM
# Красная прямая построена на требовании $y_i(<w,x_i> + w_0) >= 1$, т.е на требовании, чтобы расстояние до ближайшего объекта было не менее 1. То есть в таком случае мы "забили" на $\xi$ и делаем больше ошибок(2 условие выше)
# (такая прямая используются в объяснении линейно разделимого случая) 

![[Pasted image 20250205111318.png]]

# #SVMразделимыйИнеРазделимыйСлуч

# Мы рассматриваем во 2 условии $\xi_i$ для каждого объекта, то есть мы можем где то его сделать отрицательным(тогда этот объект будет классифицироваться неправильно), но из первого условия мы минимизируем  СУММАРНОЕ $\xi$, т.е минимизируем суммарную ошибку классификации. А вот если мы не будем учитывать это $\xi$ в минимизации (С=0), мы забьём на то, что среди объектов "крестики" есть пара объектов "нолики" и проведём разделяющую гиперплоскость как зелёную сверху, которой максимизирует расстояние до ЛЮБОГО! объекта, а не какого то конкретного класса(в таком случае похуй какие $\xi_i$, минимизации происходит только для этого расстояния $||w||$).

![[Pasted image 20250205111251.png]]

# Здесь просто упрощаем нашу задачу(систему из 3 условий). Сначала объединяя 2 и 3 условия и полученное подставляем в 1. Получили следующее выражение, где $\frac{1}{2}||w||^2$ можно считать регуляризатором, а второе слагаемое функционалом ошибки где 
# L = max(0, $1-M$), M - margin. #HingeLoss

![[Pasted image 20250205115449.png]]

# #ОтличиеSVMиLogReg
![[Pasted image 20250205120401.png]]
![[Pasted image 20250205120411.png]]
