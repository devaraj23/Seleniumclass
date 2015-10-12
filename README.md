# Seleniumclass
package seleniumScript;

import java.util.List;

import org.openqa.selenium.Alert;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.ui.Select;

public class GoogleSearch {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		WebDriver driver = new FirefoxDriver();
		driver.manage().window().maximize();
		driver.get("https://in.edit.yahoo.com/registration");
		WebElement Lan = driver.findElement(By.xpath(".//*[@id='country-lang']"));
		Select Lan1 = new Select(Lan);
		Lan1.selectByIndex(9);
		driver.findElement(By.xpath(".//*[@id='first-name']")).sendKeys("Deva");
		driver.findElement(By.xpath(".//*[@id='last-name']")).sendKeys("N");
		driver.findElement(By.xpath(".//*[@id='user-name']")).sendKeys("ndeva355");
		driver.findElement(By.xpath(".//*[@id='password']")).sendKeys("Ramya143Raj");
		driver.findElement(By.xpath(".//*[@id='mobile']")).sendKeys("9677166645");
		WebElement e = driver.findElement(By.xpath(".//*[@id='month']"));
		Select s = new Select(e);
		s.selectByIndex(3);
		WebElement e1 = driver.findElement(By.xpath(".//*[@id='day']"));
		Select s1 = new Select(e1);
		s1.selectByValue("13");
		WebElement e2 = driver.findElement(By.xpath(".//*[@id='year']"));
		Select s2 = new Select(e2);
		s2.selectByValue("1990");
		driver.findElement(By.xpath(".//*[@id='gender-wrapper']/fieldset/div/label[1]")).click();
		driver.findElement(By.xpath(".//*[@id='mobile-rec']")).sendKeys("7358230034");
		driver.findElement(By.xpath(".//*[@id='relationship']")).sendKeys("Another No");
		driver.findElement(By.xpath(".//*[@id='info-form']/div/div[9]/input")).submit();
