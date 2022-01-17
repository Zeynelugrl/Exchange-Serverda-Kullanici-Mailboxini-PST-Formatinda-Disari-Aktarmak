# Exchange Server’da Kullanıcı Mailbox’ını PST Formatında Dışarı Aktarmak

Exchange Server giriş yaptıktan sonra Exchange Management Shell açıyoruz.

Öncelikle işlem yaptığımız kullanıcıda Import-Export yetkisini kontrol ediyorum.

New-ManagementRoleAssignment -Role "Mailbox Import Export" -User "<DOMAIN\USER>"



Kullanıcıya yetkilerimizi verdikten sonra dışarı aktarma komutunu giriyoruz.

New-MailboxExportRequest -Mailbox "<MAIL ADRESİ>" -FilePath "<DOSYA YOLU>"


Talebimizin sıraya alındığını görüyoruz. Talebimizin durumunu kontrol etmek için aşağıdaki komutu çalıştırıyoruz.

Get-MailboxExportRequest -Mailbox "<MAIL ADRESI>" | Get-MailboxExportRequestStatistics
  
  
  Detaylı bilgi için https://www.mshowto.org/exchange-serverda-kullanici-mailboxini-pst-formatinda-disari-aktarmak.html
  
  Konuyla ilgili sorularınızı iletisim@zeynelugurlu.com adresinden bana ulaştırabilirsiniz.
