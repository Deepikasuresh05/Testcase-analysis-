# Testcase-analysis-

## Name : Deepika S
## Reg: No: 212223230039

### Code
```
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

driver = webdriver.Chrome()
driver.maximize_window()

wait = WebDriverWait(driver, 10)

# ------------------------------------------------
# TC01 - Open Amazon
# ------------------------------------------------

driver.get("https://www.amazon.in/")

print("TC01: Amazon opened successfully")


# ------------------------------------------------
# TC08 - Search Product and Explicit Wait
# ------------------------------------------------

search_box = wait.until(
    EC.visibility_of_element_located(
        (By.ID, "twotabsearchtextbox")
    )
)

search_box.send_keys("laptop")

driver.find_element(
    By.ID, "nav-search-submit-button"
).click()

product = wait.until(
    EC.visibility_of_element_located(
        (By.CSS_SELECTOR, "div[data-component-type='s-search-result']")
    )
)

print("TC08: Product search results loaded successfully")


# ------------------------------------------------
# Keep Browser Open
# ------------------------------------------------

input("Press Enter to close the browser...")

driver.quit()

```

### Output

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/31442424-992d-417f-a602-7f613b410947" />
