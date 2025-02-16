# RED HOUSE RATES

СУ - ФМИ - Зимен семестър 2024/2025
- Изготвил: Стоян Стоянов Иванов
- Специалност: Информатика, 3 курс, I група
- Факултетен номер: 9MI0400132

### 1. ЦЕЛ НА ПРОЕКТА:
- Целта на този проект е да се извърши анализ на данни за жилища в Бостън с фокус 
върху предсказването на цената на имотите - променлива MEDV. Чрез едномерни и 
многомерни статистически методи се установят зависимостите между различни 
характеристики на жилищата и тяхната цена. 

### 2. ЕДНОМЕРЕН АНАЛИЗ (X1, X2 и X3):
- Статистическа сума за X1 = 'CRIM' (Криминални престъпления);
- Статистическа сума за X2 = 'ZN' (% на земя за жилищно строителство);
- Статистическа сума за X3 = 'INDUS' (% на индустриални площи).

### 3. МНОГОМЕРЕН АНАЛИЗ (Y = 'MEDV'):
- Линейна регресия на MEDV спрямо CRIM, ZN и INDUS т.е. Y ~ X1, X2 и X3.

### 4. ПОСТРОЯВАНЕ НА ЛИНЕЕН МОДЕЛ:
- Изграждане на линеен модел, който предсказва log(MEDV) (цената на жилищата) въз основа на долните променливи.
```yaml
model_full <- lm(log(MEDV) ~ CRIM + ZN + INDUS + CHAS + NOX + RM + AGE + DIS + RAD + TAX + PTRATIO + B + LSTAT, data = housing.df)
```

### 5. ЗАКЛЮЧЕНИЕ:
- Проектът включва анализ на данни за жилища с цел предсказване на цената на 
имотите. Извършени са едномерен и многомерен анализ, които помогат да се
идентифицират важни фактори, влияещи на цената на имотите. В рамките на 
едномерния анализ се разглеждат разпределенията на променливите X1 = CRIM,
X2 = ZN, и X3 = INDUS, като се установява, че всяка от тях има специфичен 
ефект върху цената на имотите. Многомерният анализ позволява да изследва
връзките между Y = MEDV и независимите променливи, като използваме линейни 
модели. Посторен е многомерен линеен модел, който предсказва цената на имотите 
въз основа на различни фактори. Резултатите показват значителни зависимости 
между някои от тези променливи и цената на имотите.

### 6. ИЗПОЛЗВАНА ЛИТЕРАТУРА:
- Проектът е базиран на [линк](https://github.com/anushkaparadkar/R-Projects/blob/master/House%20Rate%20Prediction/housing.names).
- Използваният набор от данни е "Boston House Pricing", който се поддържа от 
Университета Карнеги Мелън и е свободно достъпен за изтегляне. Основно се обработват два файла: данни за жилища (housing.data) и съответните имена на колоните (housing.names).

*Линк: [https://lib.stat.cmu.edu/datasets/boston](https://lib.stat.cmu.edu/datasets/boston)*
