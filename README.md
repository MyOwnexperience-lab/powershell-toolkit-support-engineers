# PowerShell Toolkit voor IT Support Engineers

Een krachtige verzameling PowerShell-scripts voor supportmedewerkers, systeembeheerders en security engineers die werken met Microsoft 365, Azure AD en Exchange Online.

Doel: taken automatiseren, fouten voorkomen en sneller werken — met security & compliance in het achterhoofd (NIS2 / ISO27001).

---

## Inhoud

### 1. `mfa-analyse.ps1`
- Controleert per gebruiker of MFA is ingeschakeld
- Toont gebruikte MFA-methodes (SMS, Authenticator app, etc.)
- Export naar `MFA_Report.csv`
- Handig voor audits en NIS2-compliance

### 2. `shadow-admin-detector.ps1`
- Detecteert verborgen (indirecte) Global Admins via groepslidmaatschap
- Helpt bij het opschonen van ongewenste of vergeten privileges
- Essentieel voor Zero Trust en rolgebaseerde toegang

### 3. `detect-forwarding-rules.ps1`
- Doorzoekt inboxregels van Exchange Online
- Detecteert verdachte forwarding naar externe adressen
- Export naar `ForwardingRules_Report.csv`
- Nuttig bij phishing- en data exfiltratie-onderzoek

---

## Benodigdheden

Zorg dat je PowerShell-sessie de juiste modules geladen heeft:

```powershell
Install-Module Microsoft.Graph -Scope CurrentUser
Install-Module AzureAD -Scope CurrentUser
Import-Module ExchangeOnlineManagement
