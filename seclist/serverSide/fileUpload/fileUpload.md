# File Upload Vulnerability
shell.jpg.php (satisfies as check for jpg only)
shell.jpg.PhP (obfuscation)
shell.php;.jpg (sometimes can ignore whats after “;”)
shell.php%0delete0.jpg (the infamous NULL byte which comments out trailing text, remove the word delete so the zeros join together, blogspot strips this string!)

shell.php.test (defaults to first recognised extension ignoring “test”)
shell.php.xxxjpg (still ends in .jpg, but not recognised extension so will default to php!)
.phtml (a commonly used php parsed extension often forgotten about!)
.php3/.php4/.php5 (valid PHP extensions possibly left out of extension blacklists)
