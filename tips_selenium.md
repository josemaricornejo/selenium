# SELENIUM

### Formas de proceder

1. Selenium

~~~Java
WebElement vegetable = driver.findElement(By.xpath("//span[text()='tomatoes']"));

vegetable.click();
~~~

2. Selenium Actions

~~~Java
WebElement vegetable = driver.findElement(By.xpath("//span[text()='tomatoes']"));

Actions action = new Actions(driver);

action.moveToElement(inputNombre, 0, 30).click().perform();

~~~

3. Javascript

~~~Javascript
js.executeScript("arguments[0].click()", driver.findElement(By.xpath("//span[text()='tomatoes']")));
~~~

4. Robot

> Utilizarlo si hay algún fallo técnico al usar la clase de Actions en ciertos entornos.

~~~Java

Robot robot = new Robot();

robot.keyPress(KeyEvent.VK_T);
robot.keyPress(KeyEvent.VK_NUMPAD0);  
robot.keyPress(KeyEvent.VK_TAB);
robot.keyPress(KeyEvent.VK_SHIFT);       
robot.keyPress(KeyEvent.VK_J);
robot.mouseMove(980, 260);//Botón Sign in
robot.mousePress(InputEvent.BUTTON1_DOWN_MASK);
robot.mouseRelease(InputEvent.BUTTON1_DOWN_MASK);


~~~