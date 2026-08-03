# Índice de General Intelligence Requirements (CU-GIRH v7.0)

> **Este archivo no es el CU-GIRH.** Es un índice de códigos y títulos para navegación e
> interoperabilidad, acompañado de notas propias de uso en Dirección de Inteligencia.
> Las definiciones y los **Elementos Esenciales de Información (EEIs)** de cada GIR son
> contenido de Intel 471 y **no se reproducen aquí**: se citan por número de página del
> handbook oficial. Descarga el PDF en
> **<https://www.intel471.com/cyber-underground-handbook>**.

Fuente: *Cyber Underground General Intelligence Requirements Handbook (CU-GIRH)*, versión 7.0,
Intel 471 Inc. Publicado bajo CC BY-NC-ND 4.0.

---

## Cómo se lee un código GIR

La numeración es jerárquica y las subcategorías **heredan** los atributos y EEIs de su categoría padre:

```
1          Familia          MALWARE
1.1        Categoría        Malware variants
1.1.1      Subcategoría     Ransomware malware
```

Un GIR 1.1.1 arrastra, por herencia, los EEIs definidos en 1.1 más los suyos propios. Por eso
un requerimiento formulado sobre una hoja del árbol es más específico y más obtenible que uno
formulado sobre la raíz.

## Las seis familias

| # | Familia | Pregunta que acota | Stakeholders típicos |
|---|---------|--------------------|----------------------|
| 1 | Malware | ¿Qué se ejecuta? | SecOps, IR, Forensics, Hunting |
| 2 | Vulnerabilidades y exploits | ¿Por dónde entra? | SecOps, Vuln/Patch Mgmt, Red Team |
| 3 | Infraestructura maliciosa | ¿Desde dónde opera? | SecOps, Blue Team, IR |
| 4 | Fraude, identidad y acceso | ¿Cómo se monetiza? | Fraude, Legal, Riesgo, IR |
| 5 | Tácticas del adversario | ¿Cómo se comporta? | SecOps, Blue/Red Team, Insider |
| 6 | Industria o región | ¿A quién afecta? | Dirección, Legal, Riesgo |

---

## GIR 1 · MALWARE

Variantes de malware, MaaS, cadena de desarrollo/distribución y plataformas objetivo.

- **Stakeholders típicos:** Security Operations · Blue Team · Red Team · Incident Response · Forensics · Threat Hunting
- **Casos de uso frecuentes:** Protección de red y endpoint · reproducción de ataques y pen testing · investigación y remediación
- **EEIs de esta familia:** CU-GIRH v7.0, desde la página 17.

> **Uso en Dirección.** Úsala cuando el PIR pregunta **qué** se ejecutará dentro de la organización. Se cruza casi siempre con GIR 5 (cómo llega y cómo se mueve) y con GIR 3 (dónde está su C2).


### 1.1 Malware variants

- `1.1.1` Ransomware malware
- `1.1.2` Mobile malware
- `1.1.3` Remote access trojan (RAT) malware
- `1.1.4` Banking trojan malware
- `1.1.5` Information-stealer malware
- `1.1.6` Loader malware
- `1.1.7` Botnet malware
- `1.1.8` Worm malware
- `1.1.9` Point-of-sale (PoS) malware
- `1.1.10` ATM malware
- `1.1.11` Internet of Things (IoT) malware
- `1.1.12` Denial of service (DoS) malware
- `1.1.13` Proxy malware
- `1.1.14` Destructive malware
- `1.1.15` Cryptomining malware
- `1.1.16` Clipper malware
- `1.1.17` Drainer malware
- `1.1.18` Rootkits
- `1.1.19` Web shells

### 1.2 Malware-as-a-service (MaaS)

- `1.2.1` Multifunctional malware-as-a-service (MaaS)
- `1.2.2` Ransomware-as-a-service (RaaS)

### 1.3 Malware development, support and delivery

- `1.3.1` Malware installs
- `1.3.2` Malvertising
- `1.3.3` Malware source code
- `1.3.4` Web-injects
  - `1.3.4.1` Automatic transfer systems (ATSs)
- `1.3.5` Malware crypting
- `1.3.6` Counter antivirus (CAV)
- `1.3.7` Rogue certificates
  - `1.3.7.1` Rogue code-signing certificates
  - `1.3.7.2` Rogue web certificates
- `1.3.8` Malware spamming
- `1.3.9` Traffic redistribution system
- `1.3.10` Exploit kits
- `1.3.11` Illicit use of legitimate tools and software
  - `1.3.11.1` Post-exploitation frameworks
  - `1.3.11.2` Network scanners
  - `1.3.11.3` Authentication and credential tools
  - `1.3.11.4` Active Directory tools
  - `1.3.11.5` Remote access tools
  - `1.3.11.6` Search engine optimization (SEO)
  - `1.3.11.7` Anti-detect tools
  - `1.3.11.8` Artificial intelligence (AI)
  - `1.3.11.9` Living-off-the-land binaries

### 1.4 Platforms

- `1.4.1` Windows
- `1.4.2` Linux
- `1.4.3` macOS
- `1.4.4` Android
- `1.4.5` iOS

---

## GIR 2 · VULNERABILIDADES Y EXPLOITS

Vulnerabilidades por capa tecnológica y madurez del exploit asociado.

- **Stakeholders típicos:** Security Operations · Blue Team · Red Team · Incident Response · Forensics · Vulnerability/Patch Management
- **Casos de uso frecuentes:** Identificación y parcheo de vulnerabilidades · exploiting y pen testing
- **EEIs de esta familia:** CU-GIRH v7.0, desde la página 22.

> **Uso en Dirección.** Úsala cuando el PIR pregunta **por dónde entra**. El código por sí solo no prioriza: la señal útil aparece al cruzar la subcategoría tecnológica con 2.2.2 (explotado en el wild) y 2.1.12 (zero-day).


### 2.1 Vulnerabilities

- `2.1.1` Operating system (OS) vulnerabilities
  - `2.1.1.1` Desktop and server OS vulnerabilities
    - `2.1.1.1.1` Linux
    - `2.1.1.1.2` Windows
    - `2.1.1.1.3` macOS
    - `2.1.1.1.4` Unix
  - `2.1.1.2` Mobile OS vulnerabilities
    - `2.1.1.2.1` Android
    - `2.1.1.2.2` iOS
- `2.1.2` Software vulnerabilities
  - `2.1.2.1` Web browser vulnerabilities
  - `2.1.2.2` Office and productivity software vulnerabilities
  - `2.1.2.3` Open source software vulnerabilities
  - `2.1.2.4` Web application vulnerabilities
    - `2.1.2.4.1` Application programming interface (API) vulnerabilities
- `2.1.3` Protocol vulnerabilities
- `2.1.4` Server platform vulnerabilities
  - `2.1.4.1` Database server vulnerabilities
  - `2.1.4.2` Web server vulnerabilities
  - `2.1.4.3` Email server vulnerabilities
  - `2.1.4.4` Content management software vulnerabilities
    - `2.1.4.4.1` WordPress vulnerabilities
  - `2.1.4.5` Application server vulnerabilities
  - `2.1.4.6` Identity management or authentication server vulnerabilities
  - `2.1.4.7` Managed file transfer software vulnerabilities
- `2.1.5` Network appliance or endpoint vulnerabilities
- `2.1.6` Cloud computing or storage vulnerabilities
- `2.1.7` Hardware vulnerabilities
- `2.1.8` Industrial control systems (ICS) or supervisory control and data acquisition (SCADA) vulnerabilities (deprecated)
- `2.1.9` IoT-related vulnerabilities
- `2.1.10` Health care systems-related vulnerabilities (deprecated)
- `2.1.11` Cryptocurrency and exchanges vulnerabilities
- `2.1.12` Zero-day vulnerabilities
- `2.1.13` Initial access vulnerabilities

### 2.2 Exploit development

- `2.2.1` Proof-of-concept (PoC) exploit code
- `2.2.2` Exploited in wild
- `2.2.3` Exploit advertised

---

## GIR 3 · INFRAESTRUCTURA MALICIOSA

IaaS criminal, infraestructura legítima reutilizada e infraestructura dedicada al crimen.

- **Stakeholders típicos:** Security Operations · Blue Team · Red Team · Incident Response · Forensics
- **Casos de uso frecuentes:** Identificación y monitoreo de infraestructura maliciosa para protección perimetral
- **EEIs de esta familia:** CU-GIRH v7.0, desde la página 25.

> **Uso en Dirección.** Familia corta pero de alto rendimiento en obtención: es la que produce IOCs accionables. Suele ser el EEI de soporte de un PIR anclado en GIR 1 o GIR 5, no un PIR por sí misma.


### 3.1 Infrastructure-as-a-service (IaaS)

- `3.1.1` Bulletproof hosting (BPH) services
- `3.1.2` Proxy services
- `3.1.3` Domain registration services
- `3.1.4` Botnet services

### 3.2 Legitimate infrastructure repurposed for malicious activity


### 3.3 Dedicated criminal infrastructure


---

## GIR 4 · FRAUDE, ROBO DE IDENTIDAD Y ACCESO NO AUTORIZADO

Monetización del fraude, datos y accesos comprometidos, ATO, ingeniería social, bypass de controles y fraude con IA.

- **Stakeholders típicos:** Fraud · Forensics · Incident Response · Legal and Privacy · Risk Management
- **Casos de uso frecuentes:** Credenciales y tarjetas robadas · información comprometida (dumps, fullz, PII, PHI, IP) · cadena de fraude · account checking y fuerza bruta · phishing
- **EEIs de esta familia:** CU-GIRH v7.0, desde la página 27.

> **Uso en Dirección.** La familia más grande después de la geográfica, y la de mayor tracción con stakeholders no técnicos. Si tu organización es financiera, aquí vive la mayoría de los PIRs de Fraude y de Dirección.


### 4.1 Fraud supply chain monetization

- `4.1.1` Cashout
- `4.1.2` Money laundering
  - `4.1.2.1` Cryptocurrency exchange fraud
- `4.1.3` Mules and networks
- `4.1.4` Drop accounts and fund transfers
- `4.1.5` Prepaid or gift card fraud
- `4.1.6` Travel fraud
- `4.1.7` Hospitality fraud
- `4.1.8` Tax fraud and scams
- `4.1.9` Business email compromise (BEC)
- `4.1.10` Document fraud
- `4.1.11` Insurance fraud (deprecated)
- `4.1.12` Registration fraud
- `4.1.13` Reshipping fraud
- `4.1.14` Payroll fraud scam
- `4.1.15` Refund fraud
- `4.1.16` Employment fraud

### 4.2 Compromised data or access

- `4.2.1` Payment card fraud
  - `4.2.1.1` Online payment card skimming
- `4.2.2` Compromised credentials
  - `4.2.2.1` Credential combination list(s)
- `4.2.3` Compromised personally identifiable information (PII)
  - `4.2.3.1` Compromised protected health information (PHI)
- `4.2.4` Compromised intellectual property (IP)
- `4.2.5` Compromised network or system access
  - `4.2.5.1` Compromised cloud service provider access
  - `4.2.5.2` Compromised point-of-sale (PoS) access
- `4.2.6` Compromised business intelligence

### 4.3 Account takeover (ATO)

- `4.3.1` Call centers
- `4.3.2` Account checking and credential stuffing
  - `4.3.2.1` Account-checking configuration file(s)
- `4.3.3` Account brute forcing
  - `4.3.3.1` Password spraying
- `4.3.4` Subscriber identity module (SIM) swapping

### 4.4 Social engineering

- `4.4.1` Phishing
  - `4.4.1.1` Phishing-as-a-service (PhaaS)
  - `4.4.1.2` Phishing kits
- `4.4.2` Spear-phishing
- `4.4.3` Vishing
- `4.4.4` Social media scams
- `4.4.5` Smishing
- `4.4.6` Callback phishing
- `4.4.7` ClickFix technique

### 4.5 Access control bypass

- `4.5.1` Multifactor authentication (MFA) bypass
  - `4.5.1.1` One-time password (OTP) bypass

### 4.6 Artificial intelligence (AI) fraud

- `4.6.1` Deepfake technology
- `4.6.2` Chatbot abuse

### 4.7 Access classification

- `4.7.1` Wholesale access
- `4.7.2` Specified access

---

## GIR 5 · TÁCTICAS Y ACTIVIDADES DEL ADVERSARIO

Tácticas pre y post-ataque (alineadas a MITRE ATT&CK), ataque físico, insider y compromiso de información.

- **Stakeholders típicos:** Security Operations · Blue Team · Red Team · Incident Response · Insider Threats
- **Casos de uso frecuentes:** Reproducción de técnicas y pen testing · acceso a red o sistemas (acceso inicial, escalamiento de privilegios)
- **EEIs de esta familia:** CU-GIRH v7.0, desde la página 33.

> **Uso en Dirección.** Es la capa de comportamiento. Traduce bien a hipótesis de hunting y a coberturas de detección, por lo que es la familia que más directamente alimenta el CMF.


### 5.1 Pre-attack tactics

- `5.1.1` Reconaissance and information gathering tactic
- `5.1.2` Build capabilities tactic

### 5.2 Post-attack tactics

- `5.2.1` Initial access tactic
- `5.2.2` Execution tactic
- `5.2.3` Persistence tactic
- `5.2.4` Privilege escalation tactic
- `5.2.5` Defense evasion tactic
- `5.2.6` Credential access tactic
- `5.2.7` Discovery tactic
- `5.2.8` Lateral movement tactic
- `5.2.9` Collection tactic
- `5.2.10` Command and control tactic
- `5.2.11` Exfiltration tactic
- `5.2.12` Impact tactic

### 5.3 Physical attack techniques against systems

- `5.3.1` Physical ATM attack techniques
- `5.3.2` Physical point-of-sale (PoS) system attack techniques
- `5.3.3` Physical sabotage techniques (deprecated)

### 5.4 Insider threat tactics


### 5.5 Information compromise or disclosure tactics

- `5.5.1` Espionage
- `5.5.2` Outsider trading
- `5.5.3` Information or data breach
- `5.5.4` Blackmail and extortion
- `5.5.5` Supply chain attack tactic
- `5.5.6` Hacktivism
- `5.5.7` Sabotage
- `5.5.8` Intelligence gathering

---

## GIR 6 · AMENAZAS QUE IMPACTAN INDUSTRIA O REGIÓN

Sectores, industrias y regiones geográficas usados como filtro de relevancia.

- **Stakeholders típicos:** Senior Management · Legal and Privacy · Risk Management
- **Casos de uso frecuentes:** Evaluación y gestión de riesgo de terceros · conciencia situacional de amenazas y eventos
- **EEIs de esta familia:** CU-GIRH v7.0, desde la página 37.

> **Uso en Dirección.** No se prioriza sola: **acota** a las demás. Un GIR 6 sin combinar produce un requerimiento inobtenible; combinado (p. ej. 1.1.1 + 6.1.3.1 + 6.2.8) produce una pregunta que un equipo de obtención puede responder.


### 6.1 All sectors and industries

- `6.1.1` Consumer and industrial products sector
  - `6.1.1.1` Consumer business industry
  - `6.1.1.2` Transportation industry
    - `6.1.1.2.1` Aviation industry
  - `6.1.1.3` Consumer products industry
  - `6.1.1.4` Sports and leisure industry
  - `6.1.1.5` Hospitality industry
  - `6.1.1.6` Restaurants and food service industry
  - `6.1.1.7` Retail, wholesale and distribution industry
    - `6.1.1.7.1` Fashion industry
- `6.1.2` Energy, resources and agriculture sector
  - `6.1.2.1` Oil, gas and consumable fuels industry
  - `6.1.2.2` Power and utilities industry
  - `6.1.2.3` Shipping and ports industry
  - `6.1.2.4` Water industry
  - `6.1.2.5` Agriculture and food and beverage production industry
  - `6.1.2.6` Mining industry
  - `6.1.2.7` Renewable energy industry
- `6.1.3` Financial services sector
  - `6.1.3.1` Banking and securities industry
  - `6.1.3.2` Insurance industry
    - `6.1.3.2.1` Health insurance providers
    - `6.1.3.2.2` Life insurance providers
    - `6.1.3.2.3` Auto insurance providers
    - `6.1.3.2.4` Property insurance providers
  - `6.1.3.3` Investment management industry
  - `6.1.3.4` Payment processing industry
- `6.1.4` Life sciences and health care sector
  - `6.1.4.1` Health care providers and services industry
  - `6.1.4.2` Health care equipment and technology industry
  - `6.1.4.3` Pharmaceuticals, biotechnology and life sciences industry
- `6.1.5` Manufacturing sector
  - `6.1.5.1` Aerospace and defense industry
  - `6.1.5.2` Automotive industry
  - `6.1.5.3` Industrial products and services industry
  - `6.1.5.4` Chemicals and specialty materials industry
- `6.1.6` Public sector
  - `6.1.6.1` International government
  - `6.1.6.2` National government
  - `6.1.6.3` Regional government
  - `6.1.6.4` Education
  - `6.1.6.5` Public safety
  - `6.1.6.6` Military and defense
    - `6.1.6.6.1` Paramilitary
  - `6.1.6.7` Intelligence agencies
  - `6.1.6.8` Cyber governance organizations
- `6.1.7` Real estate sector
  - `6.1.7.1` Engineering and construction industry
  - `6.1.7.2` Real estate fund and investor industry
  - `6.1.7.3` Real estate investment trust (REIT) and property company industry
  - `6.1.7.4` Real estate management, brokerage and service provider industry
  - `6.1.7.5` Tenants and occupiers industry
- `6.1.8` Technology, media and telecommunications sector
  - `6.1.8.1` Technology industry
  - `6.1.8.2` Media and entertainment industry
    - `6.1.8.2.1` Gaming industry
  - `6.1.8.3` Telecommunications industry
  - `6.1.8.4` Internet of Things (IoT) industry
  - `6.1.8.5` Cloud services industry
- `6.1.9` Professional services and consulting sector
  - `6.1.9.1` Information technology (IT) consulting industry
  - `6.1.9.2` Management and operations consulting industry
  - `6.1.9.3` Financial and investment consulting industry
  - `6.1.9.4` Human resources consulting industry
  - `6.1.9.5` Marketing and sales consulting industry
  - `6.1.9.6` Law services and consulting industry
  - `6.1.9.7` Political consulting industry
  - `6.1.9.8` Physical security consulting industry
- `6.1.10` Nonprofit sector
  - `6.1.10.1` Charitable organizations
  - `6.1.10.2` Civic leagues and social welfare organizations
  - `6.1.10.3` Nongovernmental organizations (NGOs)
    - `6.1.10.3.1` Operational NGOs
    - `6.1.10.3.2` Advocacy NGOs
  - `6.1.10.4` Private charitable foundations
  - `6.1.10.5` Social advocacy groups
- `6.1.11` Research and development sector
  - `6.1.11.1` Scientific research and development organizations
  - `6.1.11.2` Multipurpose research institutes
- `6.1.12` Automation sector
  - `6.1.12.1` Supervisory control and data acquisition (SCADA) and industrial control systems (ICSs)
  - `6.1.12.2` Industrial automation industry
- `6.1.13` Digital currency sector
  - `6.1.13.1` Cryptocurrency industry
- `6.1.14` Diversified business sector
  - `6.1.14.1` Conglomerates

### 6.2 All geographic regions

- `6.2.1` Africa
  - `6.2.1.1` Algeria
  - `6.2.1.2` Angola
  - `6.2.1.3` Benin
  - `6.2.1.4` Botswana
  - `6.2.1.5` Burkina Faso
  - `6.2.1.6` Burundi
  - `6.2.1.7` Cameroon
  - `6.2.1.8` Cape Verde
  - `6.2.1.9` Central African Republic
  - `6.2.1.10` Chad
  - `6.2.1.11` Comoros
  - `6.2.1.12` Congo (Brazzaville)
  - `6.2.1.13` Congo, Democratic Republic of the
  - `6.2.1.14` Cote d'Ivoire (Ivory Coast)
  - `6.2.1.15` Djibouti
  - `6.2.1.16` Egypt
  - `6.2.1.17` Equatorial Guinea
  - `6.2.1.18` Eritrea
  - `6.2.1.19` Eswatini (ex-Swaziland)
  - `6.2.1.20` Ethiopia
  - `6.2.1.21` Gabon
  - `6.2.1.22` Gambia
  - `6.2.1.23` Ghana
  - `6.2.1.24` Guinea
  - `6.2.1.25` Guinea-Bissau
  - `6.2.1.26` Kenya
  - `6.2.1.27` Lesotho
  - `6.2.1.28` Liberia
  - `6.2.1.29` Libya
  - `6.2.1.30` Madagascar
  - `6.2.1.31` Malawi
  - `6.2.1.32` Mali
  - `6.2.1.33` Mauritania
  - `6.2.1.34` Mauritius
  - `6.2.1.35` Mayotte
  - `6.2.1.36` Morocco
  - `6.2.1.37` Mozambique
  - `6.2.1.38` Namibia
  - `6.2.1.39` Niger
  - `6.2.1.40` Nigeria
  - `6.2.1.41` Réunion
  - `6.2.1.42` Rwanda
  - `6.2.1.43` Saint Helena
  - `6.2.1.44` Sao Tome and Principe
  - `6.2.1.45` Senegal
  - `6.2.1.46` Seychelles
  - `6.2.1.47` Sierra Leone
  - `6.2.1.48` Somalia
  - `6.2.1.49` South Africa
  - `6.2.1.50` South Sudan
  - `6.2.1.51` Sudan
  - `6.2.1.52` Tanzania, United Republic of
  - `6.2.1.53` Togo
  - `6.2.1.54` Tunisia
  - `6.2.1.55` Uganda
  - `6.2.1.56` Western Sahara
  - `6.2.1.57` Zambia
  - `6.2.1.58` Zimbabwe
- `6.2.2` Asia
  - `6.2.2.1` Afghanistan
  - `6.2.2.2` Armenia
  - `6.2.2.3` Azerbaijan
  - `6.2.2.4` Bangladesh
  - `6.2.2.5` Bhutan
  - `6.2.2.6` Brunei Darussalam
  - `6.2.2.7` Cambodia
  - `6.2.2.8` China
  - `6.2.2.9` Georgia
  - `6.2.2.10` Hong Kong
  - `6.2.2.11` India
  - `6.2.2.12` Indonesia
  - `6.2.2.13` Japan
  - `6.2.2.14` Kazakhstan
  - `6.2.2.15` Korea, North
  - `6.2.2.16` Korea, South
  - `6.2.2.17` Kyrgyzstan
  - `6.2.2.18` Laos
  - `6.2.2.19` Macao
  - `6.2.2.20` Malaysia
  - `6.2.2.21` Maldives
  - `6.2.2.22` Mongolia
  - `6.2.2.23` Myanmar (ex-Burma)
  - `6.2.2.24` Nepal
  - `6.2.2.25` Pakistan
  - `6.2.2.26` Philippines
  - `6.2.2.27` Singapore
  - `6.2.2.28` Sri Lanka (ex-Ceylon)
  - `6.2.2.29` Taiwan
  - `6.2.2.30` Tajikistan
  - `6.2.2.31` Thailand
  - `6.2.2.32` Timor Leste (West)
  - `6.2.2.33` Turkmenistan
  - `6.2.2.34` Uzbekistan
  - `6.2.2.35` Vietnam
- `6.2.3` Central America
  - `6.2.3.1` Belize
  - `6.2.3.2` Costa Rica
  - `6.2.3.3` El Salvador
  - `6.2.3.4` Guatemala
  - `6.2.3.5` Honduras
  - `6.2.3.6` Mexico
  - `6.2.3.7` Nicaragua
  - `6.2.3.8` Panama
- `6.2.4` Europe
  - `6.2.4.1` Albania
  - `6.2.4.2` Andorra
  - `6.2.4.3` Austria
  - `6.2.4.4` Belarus
  - `6.2.4.5` Belgium
  - `6.2.4.6` Bosnia
  - `6.2.4.7` Bulgaria
  - `6.2.4.8` Croatia
  - `6.2.4.9` Cyprus
  - `6.2.4.10` Czech Republic
  - `6.2.4.11` Denmark
  - `6.2.4.12` Estonia
  - `6.2.4.13` Faroe Islands
  - `6.2.4.14` Finland
  - `6.2.4.15` France
  - `6.2.4.16` Germany
  - `6.2.4.17` Gibraltar
  - `6.2.4.18` Greece
  - `6.2.4.19` Guernsey and Alderney
  - `6.2.4.20` Hungary
  - `6.2.4.21` Iceland
  - `6.2.4.22` Ireland
  - `6.2.4.23` Italy
  - `6.2.4.24` Jersey
  - `6.2.4.25` Kosovo
  - `6.2.4.26` Latvia
  - `6.2.4.27` Liechtenstein
  - `6.2.4.28` Lithuania
  - `6.2.4.29` Luxembourg
  - `6.2.4.30` Malta
  - `6.2.4.31` Man, Isle of
  - `6.2.4.32` Moldova
  - `6.2.4.33` Monaco
  - `6.2.4.34` Montenegro
  - `6.2.4.35` Netherlands
  - `6.2.4.36` North Macedonia
  - `6.2.4.37` Norway
  - `6.2.4.38` Poland
  - `6.2.4.39` Portugal
  - `6.2.4.40` Romania
  - `6.2.4.41` Russia
  - `6.2.4.42` San Marino
  - `6.2.4.43` Serbia
  - `6.2.4.44` Slovakia
  - `6.2.4.45` Slovenia
  - `6.2.4.46` Spain
  - `6.2.4.47` Svalbard and Jan Mayen Islands
  - `6.2.4.48` Sweden
  - `6.2.4.49` Switzerland
  - `6.2.4.50` Turkey
  - `6.2.4.51` Ukraine
  - `6.2.4.52` United Kingdom
  - `6.2.4.53` Vatican City State (Holy See)
- `6.2.5` Middle East
  - `6.2.5.1` Bahrain
  - `6.2.5.2` Iran
  - `6.2.5.3` Iraq
  - `6.2.5.4` Israel
  - `6.2.5.5` Jordan
  - `6.2.5.6` Kuwait
  - `6.2.5.7` Lebanon
  - `6.2.5.8` Oman
  - `6.2.5.9` Palestinian territories
  - `6.2.5.10` Qatar
  - `6.2.5.11` Saudi Arabia
  - `6.2.5.12` Syria
  - `6.2.5.13` United Arab Emirates
  - `6.2.5.14` Yemen
- `6.2.6` North America
  - `6.2.6.1` Bermuda
  - `6.2.6.2` Canada
  - `6.2.6.3` Greenland
  - `6.2.6.4` Saint Pierre and Miquelon
  - `6.2.6.5` United States
- `6.2.7` Oceania
  - `6.2.7.1` Australia
  - `6.2.7.2` Fiji
  - `6.2.7.3` French Polynesia
  - `6.2.7.4` Guam
  - `6.2.7.5` Kiribati
  - `6.2.7.6` Marshall Islands
  - `6.2.7.7` Micronesia
  - `6.2.7.8` New Caledonia
  - `6.2.7.9` New Zealand
  - `6.2.7.10` Palau
  - `6.2.7.11` Papua New Guinea
  - `6.2.7.12` Samoa
  - `6.2.7.13` Samoa, American
  - `6.2.7.14` Solomon Islands
  - `6.2.7.15` Tonga
  - `6.2.7.16` Tuvalu
  - `6.2.7.17` Vanuatu
- `6.2.8` South America
  - `6.2.8.1` Argentina
  - `6.2.8.2` Bolivia
  - `6.2.8.3` Brazil
  - `6.2.8.4` Chile
  - `6.2.8.5` Colombia
  - `6.2.8.6` Ecuador
  - `6.2.8.7` Falkland Islands (Malvinas)
  - `6.2.8.8` French Guiana
  - `6.2.8.9` Guyana
  - `6.2.8.10` Paraguay
  - `6.2.8.11` Peru
  - `6.2.8.12` Suriname
  - `6.2.8.13` Uruguay
  - `6.2.8.14` Venezuela
- `6.2.9` The Caribbean
  - `6.2.9.1` Anguilla
  - `6.2.9.2` Antigua and Barbuda
  - `6.2.9.3` Aruba
  - `6.2.9.4` Bahamas
  - `6.2.9.5` Barbados
  - `6.2.9.6` Bonaire, Sint Eustatius and Saba
  - `6.2.9.7` British Virgin Islands
  - `6.2.9.8` Cuba
  - `6.2.9.9` Curacao
  - `6.2.9.10` Dominica
  - `6.2.9.11` Dominican Republic
  - `6.2.9.12` Grenada
  - `6.2.9.13` Guadeloupe
  - `6.2.9.14` Haiti
  - `6.2.9.15` Jamaica
  - `6.2.9.16` Martinique
  - `6.2.9.17` Montserrat
  - `6.2.9.18` Puerto Rico
  - `6.2.9.19` Saint Barthélemy
  - `6.2.9.20` Saint Kitts and Nevis
  - `6.2.9.21` Saint Lucia
  - `6.2.9.22` Saint Martin
  - `6.2.9.23` Saint Vincent and the Grenadines
  - `6.2.9.24` Sint Maarten
  - `6.2.9.25` Trinidad and Tobago
  - `6.2.9.26` Turks and Caicos Islands
  - `6.2.9.27` Virgin Islands (U.S.)

---

## Notas de uso

- **Los códigos son el contrato.** Etiquetar cada reporte con su GIR permite medir después qué
  requerimientos se están respondiendo y cuáles llevan meses sin producción. Sin etiquetado no
  hay métrica de satisfacción de PIRs.
- **Un GIR no es un PIR.** El GIR es un tema permanente; el PIR es una pregunta priorizada con
  plazo. La conversión exige formato de pregunta y un plazo (NLT / LTIOV).
- **Hasta 10 por stakeholder.** El handbook recomienda que cada stakeholder seleccione y rankee
  como máximo 10 GIRs. Esa lista ordenada es su conjunto de PIRs; la consolidación de todos
  produce la Collection Guidance del equipo.
- **Revisión trimestral.** Las selecciones de GIRs envejecen: conviene revisarlas con cada
  stakeholder al menos cada tres meses.

## Entradas obsoletas en v7.0

Intel 471 marca algunos códigos como *deprecated*; se mantienen en el índice para no romper
etiquetados históricos, pero no deberían usarse en requerimientos nuevos:

- `2.1.8` ICS/SCADA vulnerabilities
- `2.1.10` Health care systems-related vulnerabilities
- `4.1.11` Insurance fraud
- `5.3.3` Physical sabotage techniques

---

<p align="center"><sub>Índice de referencia · Oneiros Academy · Taxonomía © Intel 471, Inc.</sub></p>