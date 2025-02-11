## `openjdk:24-rc-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:294d28e98d161044ce1594bb66c494b38715610c7d44a2766163f4ff25710d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-rc-jdk-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:04ebeba240aa22d687e4a2b719f67346d103f87ab2f91acd4f6289ac88fd5142
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709986938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590aea82123aa8e9e2749528909cb9240db53a967c6595bb6d3931fb1c53cff9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Tue, 11 Feb 2025 00:31:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 00:31:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:19 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 11 Feb 2025 00:31:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:25 GMT
ENV JAVA_VERSION=24
# Tue, 11 Feb 2025 00:31:26 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_windows-x64_bin.zip
# Tue, 11 Feb 2025 00:31:27 GMT
ENV JAVA_SHA256=11d1d9f6ac272d5361c8a0bef01894364081c7fb1a6914c2ad2fc312ae83d63b
# Tue, 11 Feb 2025 00:32:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:32:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d7dcf2bcddbdad7557da19e4234025bb6a672cf3b88d03d0878b8727c1bce8`  
		Last Modified: Tue, 11 Feb 2025 00:32:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c89eca89aa9b4ff4cfaa8458d6aee96174fd7c425a419c78542549083b507b`  
		Last Modified: Tue, 11 Feb 2025 00:32:25 GMT  
		Size: 385.6 KB (385592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ec3d96e893ae4cf1140e0c0ae61870b8f8c519be0eb742121d270436321f75`  
		Last Modified: Tue, 11 Feb 2025 00:32:25 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400d617e06805df508fa1d5d31e2d49009c61e98ff9346d6f5d376659579e92d`  
		Last Modified: Tue, 11 Feb 2025 00:32:25 GMT  
		Size: 374.4 KB (374419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7a5cc4ea843ab82cfaf65322b1e954c32866d55945930f43bda5ab255817f2`  
		Last Modified: Tue, 11 Feb 2025 00:32:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca19dc597d5c6c429a93c8942fb9e69e24a066b6fbc0a4d672479547439db5f9`  
		Last Modified: Tue, 11 Feb 2025 00:32:24 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d36d047931df06992b594d27cc88cc0155a495db3dcca47df8e43daab8c01d`  
		Last Modified: Tue, 11 Feb 2025 00:32:24 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc012a3383812a106bee99c2a72766783a951c214f3f919f8bb542dec6b73a`  
		Last Modified: Tue, 11 Feb 2025 00:32:37 GMT  
		Size: 208.9 MB (208941499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081f56f2a7db3acf106d80ad462a353e2ec78a9010bea88735231d862eaf05bb`  
		Last Modified: Tue, 11 Feb 2025 00:32:24 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-rc-jdk-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:b27043dd1a9655108e27179d5dca9d21086160679b0c4e7ecc1ae4488b76b46a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471941970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c94d240abb51ef98f6928f66d54f0023dfaf7506a8bccb9d1282a5ee06330b6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 11 Feb 2025 01:27:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 01:28:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 01:28:32 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 11 Feb 2025 01:28:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 01:28:46 GMT
ENV JAVA_VERSION=24
# Tue, 11 Feb 2025 01:28:46 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_windows-x64_bin.zip
# Tue, 11 Feb 2025 01:28:47 GMT
ENV JAVA_SHA256=11d1d9f6ac272d5361c8a0bef01894364081c7fb1a6914c2ad2fc312ae83d63b
# Tue, 11 Feb 2025 01:29:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 01:29:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe06f560d712540b4b82eabb0daea4ecfd3aef32633c2f204c30aec9b789722`  
		Last Modified: Tue, 11 Feb 2025 01:29:20 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa18dee71a9d380f5e11c03fc6a797d36e5ff8c8f33364666fe7e533290ad12`  
		Last Modified: Tue, 11 Feb 2025 01:29:20 GMT  
		Size: 364.9 KB (364896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2e74daea344c3fd9485fe88d247f114cc14457f6bae49270334aa3d4e0d8c7`  
		Last Modified: Tue, 11 Feb 2025 01:29:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91479af73678e24337881dcf2eb31175da6e232e4cda681f8cfdaaee50c3bc7`  
		Last Modified: Tue, 11 Feb 2025 01:29:20 GMT  
		Size: 312.5 KB (312506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5e6a61aca9f77b83abcbce210adedc92772f3c4990c628d47df5613f8948ab`  
		Last Modified: Tue, 11 Feb 2025 01:29:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9508aa9c0ea8f91ca1b713a264aa11fd2697256a24d672f9bba9808878110d8`  
		Last Modified: Tue, 11 Feb 2025 01:29:19 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7231573a5ba928630de6d81838300e0f60e2bd6b57ee0b744c3bd901a375bb`  
		Last Modified: Tue, 11 Feb 2025 01:29:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e7bd99f166c66bb0e0df82043f35721a5dc637f14393c59ac5a5f52d9019d8`  
		Last Modified: Tue, 11 Feb 2025 01:29:30 GMT  
		Size: 208.9 MB (208871616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70628fad79daae0a5ea402c0c41832985a1de694a1414e709f94821d9db57f9a`  
		Last Modified: Tue, 11 Feb 2025 01:29:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-rc-jdk-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:2cb2f938d9f6136ac2e76baa4346b576c9ba326cd68d66e9c34848d57b8a68e6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331793980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48505aa8ce416eeafc0d920a46473bdf6d750fbb1cfd7f0420f56a19e6c7c78`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 11 Feb 2025 01:27:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 01:28:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 01:28:44 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 11 Feb 2025 01:28:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 01:28:53 GMT
ENV JAVA_VERSION=24
# Tue, 11 Feb 2025 01:28:53 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_windows-x64_bin.zip
# Tue, 11 Feb 2025 01:28:54 GMT
ENV JAVA_SHA256=11d1d9f6ac272d5361c8a0bef01894364081c7fb1a6914c2ad2fc312ae83d63b
# Tue, 11 Feb 2025 01:29:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 01:29:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e234e6069560f159ad18cc39139f458f581239319eea40597f2911373a9eaf`  
		Last Modified: Tue, 11 Feb 2025 01:29:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2140653f9fb175a607f063c88779f5242b16471cf76cb60e6f513820a5221186`  
		Last Modified: Tue, 11 Feb 2025 01:29:35 GMT  
		Size: 341.8 KB (341843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc622ca2797c3c6aad46ee02bb7ce468475c098d9d6942ef9e6e59ba67b8b3a9`  
		Last Modified: Tue, 11 Feb 2025 01:29:35 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5268ec88d568b0d8a6f11b42b70c591c6183262e30239679ea83d9d7a625409`  
		Last Modified: Tue, 11 Feb 2025 01:29:35 GMT  
		Size: 332.9 KB (332860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e658a8d2f5b66fc17c6e6f7e9847ce162633273aeb13bc6cca8bda0e47ae6a56`  
		Last Modified: Tue, 11 Feb 2025 01:29:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09f8ac2bd7c4e3cc62e6975cbef316afdba7a2056c2713ced314cc7ec8660e5`  
		Last Modified: Tue, 11 Feb 2025 01:29:33 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a995f2596a6a384dbbb1b6db39e9bcb5923d8bbd446fabc52f4d49aca6ac9b`  
		Last Modified: Tue, 11 Feb 2025 01:29:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da33fcb981601d6961850ed0130205428b31024e16ab45698808d4f39436ab6`  
		Last Modified: Tue, 11 Feb 2025 01:29:47 GMT  
		Size: 208.9 MB (208899320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6ce2a4d253adf4b3b018a4e70b5d7facdc4e4af8bdcadef2d962b293499111`  
		Last Modified: Tue, 11 Feb 2025 01:29:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
