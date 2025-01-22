## `openjdk:25-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:e6f1b4c63e64a930b2db16c039386ea90519e41f69caeeae2f40eb9ea63222f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:25-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:b502d2953496029bd5efcd66e1b0b6a0825e9f57f8313632067258813c76ffe9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470833661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4a17510df344ff6f004df2bf16a655f8bda880e521c90d0b676dffa40e36f3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 02:36:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 02:36:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 22 Jan 2025 02:36:12 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 22 Jan 2025 02:36:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 22 Jan 2025 02:36:18 GMT
ENV JAVA_VERSION=25-ea+6
# Wed, 22 Jan 2025 02:36:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_windows-x64_bin.zip
# Wed, 22 Jan 2025 02:36:19 GMT
ENV JAVA_SHA256=291c57a76ce4ef742a0402b2af6ae2b2eab2614738b9bc0e335ab9d06f105d33
# Wed, 22 Jan 2025 02:36:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 02:36:39 GMT
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
	-	`sha256:640ff1399902962e8a846cd8892cf944881c7be573d616c207c0b43351f80726`  
		Last Modified: Wed, 22 Jan 2025 02:36:45 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54608438a7d0232b333ace8c85c3527a6b174b139d65ecc95bd6542e87f3471`  
		Last Modified: Wed, 22 Jan 2025 02:36:46 GMT  
		Size: 355.1 KB (355118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1c1ec9ab207486d8e62cd9701aea1904f3025e48c6a7aa04db641276f1bfad`  
		Last Modified: Wed, 22 Jan 2025 02:36:45 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc23a8f9a2c33752d0bb0a9fa7f469da01925a79ca85b9108dc11ce94b2d12d`  
		Last Modified: Wed, 22 Jan 2025 02:36:46 GMT  
		Size: 338.8 KB (338774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed8e586951c686ea16bb7dc29c169327c46af96b05f71f9c28bf13d062e45f6`  
		Last Modified: Wed, 22 Jan 2025 02:36:43 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4d8acf31d2e44af6591e3e6a085d5d2c20b8425665e448a5ddbd656fffe70f`  
		Last Modified: Wed, 22 Jan 2025 02:36:43 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e1e04a391617d1215bfc087c0a753affe1439d217065da95b871153ee23d27`  
		Last Modified: Wed, 22 Jan 2025 02:36:43 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efe9c0d0713d683c5f092c80870db4148be0099d0355ebebb048a225fb2c7fc`  
		Last Modified: Wed, 22 Jan 2025 02:36:54 GMT  
		Size: 207.7 MB (207746809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d3b2f834b0b2b7d0a4b7370d8d0a7ce7b0f8f86c205418c123d8cd6f51c093`  
		Last Modified: Wed, 22 Jan 2025 02:36:43 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
