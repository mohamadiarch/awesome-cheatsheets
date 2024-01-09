WMIC ComputerSystem GET Model

مشاهده نام کامپیوتر و نوع سیستم

wmic computersystem get name,systemtype

مشاهده مک آدرس کارت شبکه های سیستم از طریق ابزار WMIC

wmic nic get macaddress,description

مشاهده نام کارخانه سازنده مادربورد از طریق WMIC

WMIC COMPUTERSYSTEM GET MANUFACTURER

مشاهده اطلاعات مادربورد با ابزار WMIC

wmic baseboard get product,Manufacturer,version,serialnumber

مشاهده ظرفیت حافظه فیزیکی با WMIC

wmic COMPUTERSYSTEM get TotalPhysicalMemory

مشاهده اطلاعات کامل حافظه فیزیکی با WMIC

wmic memorychip

مشاهده اطلاعاتی درباره برنامه های درحال اجرا و میزان رم در حال استفاده برای هر برنامه بوسیله WMIC

wmic process get workingsetsize,commandline

مشاهده اطلاعاتی درباره سایز و نوع پارتیشن های سیستم با WMIC

wmic partition get name,size,type

مشاهده وضعیت سرویس های سیستم با استفاده از WMIC

wmic service list brief

مشاهده پردازش های در حال انجام توسط سی پی یو

wmic process list brief

مشاهده برنامه های موجود در استارت آپ ویندوز با استفاده از WMIC

wmic startup list brief

نمایش سریال هارد دیسک با استفاده از WMIC

wmic path win32_physicalmedia get SerialNumber


نمایش اطلاعات بایوس با استفاده از WMIC

wmic BIOS


نمایش پیکربندی بوت سیستم با استفاده از ابزار WMIC

wmic BOOTCONFIG


نمایش اطلاعات سی دی رام با استفاده از WMIC

wmic CDROM


نمایش اطلاعات پردازنده با استفاده از WMIC

wmic CPU


مدیریت پردازنده با استفاده از ابزار WMIC

wmic CSProduct


مشاهده دیسک های موجود با استفاده از WMIC

wmic DISKDRIVE


مشاهده حجم دیسک های موجود با استفاده از WMIC

wmic DISKQUOTA


نمایش اطلاعات پروتکل شبکه با استفاده از ابزار WMIC

wmic NETPROTOCOL


نمایش نشست های فعال در شبکه با استفاده از WMIC

wmic NETUSE


نمایش اطلاعات سخت افزاری کارت شبکه با استفاده از WMIC

wmic NIC


نمایش اطلاعات قطعات روی مادربورد با استفاده از WMIC

wmic ONBOARDDEVICE


نمایش اطلاعات سیستم عامل با استفاده از ابزار WMIC

wmic OS


نمایش اطلاعات پیج فایل با استفاده از WMIC

wmic PAGEFILE


نمایش اطلاعات پورت ها با استفاده از WMIC

wmic PORT


نمایش اطلاعات پرینتر با استفاده از ابزار WMIC

wmic PRINTER


نمایش اطلاعات منابع به اشتراک گذاشته شده

wmic SHARE


نمایش اطلاعات کارت صوتی

wmic SOUNDDEV

نمایش اطلاعات دمای سیستم

wmic TEMPERATURE


نمایش اطلاعات در مورد برق مصرفی سیستم

wmic VOLTAGE

حذف برنامه ها با استفاده از wmic 
با استفاده از wmic  میتوانید یک یا چند برنامه نصب شده روی ویندوز را حذف کرد. برای اینکار ابتدا دستور زیر را در خط فرمان وارد کنید:

wmic product get name