# ✅ AI Engineering Output: SQL Server + REST API + RShiny Integration

## 1. Architecture Design

```mermaid
graph TD
  A[SQL Server Database]
  B[REST API Layer (.NET or Flask)]
  C[RShiny App (Frontend)]
  D[API Testing Tools (Postman, Swagger)]

  A --> B
  B --> C
  B --> D

```

---

## 2. Recommended Free Tools

* **Database**: SQL Server Express
* **API Framework**: Flask (Python) or .NET Core Web API
* **Frontend**: R + Shiny
* **Version Control**: Git + GitHub
* **Testing**: Postman, Swagger

---

## 3. R Packages & API Frameworks

* `httr`, `jsonlite`, `shiny`, `shinydashboard`, `plotly`
* Flask for Python or .NET Core for C#

---

## 4. Sample SQL Schema & Data

```sql
CREATE TABLE SensorReadings (
    id INT PRIMARY KEY,
    timestamp DATETIME,
    temperature FLOAT,
    status VARCHAR(10)
);

INSERT INTO SensorReadings VALUES
(1, '2025-08-04 12:00', 78.6, 'OK'),
(2, '2025-08-04 13:00', 82.3, 'HIGH');
```

---

## 5. Boilerplate REST API (Flask)

```python
from flask import Flask, jsonify
import pyodbc

app = Flask(__name__)

@app.route('/get-data')
def get_data():
    conn = pyodbc.connect('DRIVER={SQL Server};SERVER=localhost;DATABASE=test;Trusted_Connection=yes;')
    cursor = conn.cursor()
    cursor.execute("SELECT * FROM SensorReadings")
    rows = cursor.fetchall()
    return jsonify([dict(zip([column[0] for column in cursor.description], row)) for row in rows])

@app.route('/healthcheck')
def healthcheck():
    return "API is running!"

if __name__ == '__main__':
    app.run(debug=True)
```

---

## 6. RShiny Starter Code

```r
library(shiny)
library(httr)
library(jsonlite)
library(plotly)

ui <- fluidPage(
  plotlyOutput("plot")
)

server <- function(input, output, session) {
  data <- reactive({
    res <- GET("http://127.0.0.1:5000/get-data")
    fromJSON(content(res, "text"), flatten = TRUE)
  })

  output$plot <- renderPlotly({
    df <- data()
    plot_ly(df, x = ~timestamp, y = ~temperature, type = 'scatter', mode = 'lines+markers')
  })
}

shinyApp(ui, server)
```

---

## 7. Code Storage & Structure

Use GitHub with this clean layout:

* `/sql` → schema scripts
* `/api` → Flask or .NET API code
* `/shiny` → R Shiny app code

Include:

* `README.md`
* `.gitignore`
* `LICENSE`

---

## 8. Tips for Success

* Use `.env` for secure DB credentials
* Test endpoints in Postman before RShiny integration
* Document setup and endpoints in `README.md`

---

## 9. Why This Project Matters

This workflow proves you're capable of building and managing an end-to-end data application. You’ll demonstrate full-stack awareness from database → API → frontend — and build technical confidence with resume-worthy results.

---

Let me know if you’d like this exported as `.md` files for a GitHub repo.
