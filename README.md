```python
import time

from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

driver = webdriver.Edge()
driver.maximize_window()

driver.get("https://www.amazon.in/")

wait = WebDriverWait(driver, 30)

search = wait.until(
    EC.element_to_be_clickable(
        (By.ID, "twotabsearchtextbox")
    )
)

search.send_keys("wireless mouse")
search.send_keys(Keys.ENTER)

print("Product searched.")

time.sleep(5)

print("Click any product manually.")

add_to_cart = wait.until(
    EC.element_to_be_clickable(
        (By.ID, "add-to-cart-button")
    )
)

print("Product page opened.")

add_to_cart.click()

print("Added to cart.")

time.sleep(3)

cart = wait.until(
    EC.element_to_be_clickable(
        (By.ID, "nav-cart")
    )
)

cart.click()

print("Cart opened.")

time.sleep(3)

checkout = wait.until(
    EC.element_to_be_clickable(
        (By.NAME, "proceedToRetailCheckout")
    )
)

checkout.click()

print("Checkout clicked.")

time.sleep(5)

print("URL:", driver.current_url)
print("Title:", driver.title)

try:
    phone_box = WebDriverWait(driver, 10).until(
        EC.visibility_of_element_located(
            (By.ID, "ap_email_login")
        )
    )

    phone_box.clear()
    phone_box.send_keys("7339102544")

    print("Sign-in page found.")
    print("Phone number entered.")

except:
    print("Sign-in page not found.")

print("Done.")

time.sleep(10)

driver.quit()
```

For GitHub, you can describe it simply like this:

### Amazon E-Commerce Automation Testing

* Automated Amazon website testing using **Selenium WebDriver with Python**.
* Searched for a product using the Amazon search bar.
* Manually selected a product to continue the test flow.
* Automatically detected the product page and clicked **Add to Cart**.
* Navigated to the shopping cart automatically.
* Clicked **Proceed to Checkout**.
* Detected whether the Amazon sign-in page appeared.
* Automatically entered the registered mobile number when the sign-in page was displayed.
* Used **WebDriverWait** and Selenium locators to handle dynamic web elements.
* Tested an end-to-end e-commerce workflow from **product search to checkout**.

**Technologies:** Python, Selenium WebDriver, Microsoft Edge, Web Automation, Explicit Waits, HTML Element Locators.








<img width="1535" height="863" alt="image" src="https://github.com/user-attachments/assets/1ff53516-5d92-41ea-9b31-df58e465868e" />
<img width="1535" height="863" alt="image" src="https://github.com/user-attachments/assets/9441f1e5-0f7d-410d-998a-03cf4628b5cc" />
<img width="1534" height="863" alt="image" src="https://github.com/user-attachments/assets/2a8dccc0-978a-45ea-900b-276bae9a0116" />
<img width="1535" height="863" alt="image" src="https://github.com/user-attachments/assets/a5293a73-af12-4957-81e4-9adabf178d16" />
<img width="1533" height="863" alt="image" src="https://github.com/user-attachments/assets/061ab777-2f51-4b74-8293-86f8751f2d7f" />
<img width="1535" height="863" alt="image" src="https://github.com/user-attachments/assets/136bfd4a-e8c6-466a-b4a4-8b6efba3ec05" />
<img width="1535" height="860" alt="image" src="https://github.com/user-attachments/assets/9e8c63f6-762c-4050-837d-7437a431ed8c" />


