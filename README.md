#🚂 Тестовое задание для QA-инженера (Unit-тестирование)

### Железная дорога

📋 Контекст задачи
Вы участвуете в тестировании критически важного модуля системы управления железнодорожными перевозками РЖД. Ваша задача — обеспечить надежность расчетов движения поездов и перевозки грузов.

🎯 Цель задания
Написать comprehensive unit-тесты для класса RailwayOperations, покрывающие все возможные сценарии работы.

📂 Структура проекта
Copy
railway-ops-tests/
├── src/
│   ├── main/java/RailwayOperations.java  # Реализация класса
│   └── test/java/RailwayOperationsTest.java  # Ваши тесты
├── pom.xml  # Конфигурация Maven
└── README.md
🛠 Технические требования
Для Java-разработчиков:
JDK 8+

JUnit 5

Maven (рекомендуется)

Для C#-разработчиков:
.NET Core 3.1+

NUnit/xUnit

📝 Задание
1. Тестируемый класс
Протестируйте все методы класса RailwayOperations:

java
Copy
public class RailwayOperations {
    public String calculateArrivalTime(String departureTime, int travelMinutes) { ... }
    public boolean isCargoOverweight(double cargoWeight, double maxWeight) { ... }
    public double calculateShippingCost(double distanceKm, double ratePerKm, double cargoWeight) { ... }
}
2. Требования к тестам
Для каждого метода необходимо реализовать:

Тип теста	Кол-во	Описание
✅ Позитивные	2	Стандартные рабочие сценарии
❌ Негативные	2	Ошибочные входные данные
⚠️ Граничные	1	Пограничные значения
3. Пример теста
java
Copy
@Test
@DisplayName("Расчет времени прибытия: нормальные условия")
void calculateArrivalTime_NormalConditions_ReturnsCorrectTime() {
    RailwayOperations ops = new RailwayOperations();
    String result = ops.calculateArrivalTime("14:30", 90);
    assertEquals("16:00", result, "Время прибытия рассчитано неверно");
}
🧪 Критерии оценки
Полнота покрытия (100% coverage приветствуется)

Качество тест-кейсов

Читаемость кода

Обработка исключений

Стиль именования тестов

💎 Бонусные задания
diff
Copy
+ [Бонус 1] Настройте JaCoCo для измерения покрытия кода
+ [Бонус 2] Реализуйте CI через GitHub Actions
🚀 Как начать
Клонируйте репозиторий

Создайте ветку feature/tests-{yourname}

Реализуйте тесты в файле RailwayOperationsTest.java

Сделайте Pull Request

⁉️ Подсказки
Используйте параметризованные тесты для повторяющихся сценариев

Документируйте предположения в комментариях

Проверяйте не только результат, но и побочные эффекты

График покрытия

"Хорошие тесты — как семафоры на железной дороге: предотвращают катастрофы до того, как они произойдут." © Senior QA Engineer
