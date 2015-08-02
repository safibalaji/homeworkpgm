# homeworkpgm
package program1;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.ui.Select;



public class Firstprogram {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
WebDriver driver=new FirefoxDriver();
driver.manage().window().maximize();
driver.get("https://book.spicejet.com/Register.aspx");
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_MemberInputRegisterView_TextBoxAgentUserName']")).sendKeys("safibalaji");
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_MemberInputRegisterView_PasswordFieldAgentPassword']")).sendKeys("Safibalaji1@");
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_MemberInputRegisterView_PasswordFieldPasswordConfirm']")).sendKeys("Safibalaji1@");
WebElement title = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListTitle']"));
Select tit = new Select(title);
tit.selectByValue("MR");
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxFirstName']")).sendKeys("Balaji");
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxLastName']")).sendKeys("V V");
WebElement day = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListDOBDay']"));
WebElement month = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListDOBMonth']"));
WebElement year = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListDOBYear']"));
Select date = new Select(day);
date.selectByValue("20");
Select mon = new Select(month);
mon.selectByValue("6");
Select yr = new Select(year);
yr.selectByValue("1989");
WebElement nationality = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListNationality']"));
Select nationality1 = new Select(nationality);
nationality1.selectByValue("IN");
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxStreetAddress1']")).sendKeys("Annai Athulya Apartment");
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxStreetAddress2']")).sendKeys("Keelkattalai");
WebElement country = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListCountry']"));
Select country1 = new Select(country);
country1.selectByValue("IN");
WebElement state = driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_DropDownListState']"));
Select states = new Select(state);
states.selectByValue("IN|TN");
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxTownCity']")).sendKeys("Chennai");
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxPostalCode']")).sendKeys("600117");
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxFirstPhone']")).sendKeys("8526508759");
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_TextBoxEmail']")).sendKeys("safibalaji1@gmail.com");
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_PersonInputRegisterView_CheckBoxPromoOpt']")).click();
driver.findElement(By.xpath("//*[@id='CONTROLGROUPREGISTERVIEW_ButtonSubmit']")).click();
	}

}
