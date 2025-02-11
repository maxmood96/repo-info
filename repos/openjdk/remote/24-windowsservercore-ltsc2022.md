## `openjdk:24-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:54904f320a128ef7f81837b58e8d601cd20358685cf00d270a091492f85db9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:24-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

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
