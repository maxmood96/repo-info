## `openjdk:25-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:8cf29003ddb494746e8801da14e0105112de82c0cd13483b3059357bbd358105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `openjdk:25-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:c8894295841988daa1fb5b186dfe40f7860b590d9953474f4ca64be8be061d2e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2483066957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f58a0dd79ff06d54eeec4fd4c8bf5b1c26f84cb0865d950f3d257783ed250`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 21:02:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:02:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 May 2025 21:02:53 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 14 May 2025 21:02:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 May 2025 21:02:59 GMT
ENV JAVA_VERSION=25-ea+22
# Wed, 14 May 2025 21:02:59 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_windows-x64_bin.zip
# Wed, 14 May 2025 21:03:00 GMT
ENV JAVA_SHA256=8b16ab02467967b98cf7d8743da9c9688d3ff39b4a693b66b6d9fe84cc0bb55a
# Wed, 14 May 2025 21:03:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:03:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162d4dbf96599a9c68463c707bcc8d392c8f5719fddf723bf206419ccc50a9d3`  
		Last Modified: Wed, 14 May 2025 21:03:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14b47e112f6500dc7b8a8d81d3af8c0d42371ac9848121c7c4d16eee0b5d853`  
		Last Modified: Wed, 14 May 2025 21:03:25 GMT  
		Size: 357.6 KB (357608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8049b61789db4123638f4ab57f60496683bde7e72a17774456967bf5c74a6372`  
		Last Modified: Wed, 14 May 2025 21:03:25 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c66710354f9c83f5cf64bb99fe3eae83b89a83b44dedbbbb9486270f77d38a`  
		Last Modified: Wed, 14 May 2025 21:03:25 GMT  
		Size: 345.2 KB (345234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9c89ffd48f468ba0b4b3011cc8141a4dc9638169c246fc0f5e3d2336993d8`  
		Last Modified: Wed, 14 May 2025 21:03:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544373c36dc60dcf577392b8c27a197fe96b353f9bcde659b9c9fdf45050a62`  
		Last Modified: Wed, 14 May 2025 21:03:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc254ea17d6bff5f0993de24c1fb11a4bc7950b544f7015b85b3b620d6da29f8`  
		Last Modified: Wed, 14 May 2025 21:03:23 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a2762c0796b11a2fd8b9e8fe27db19e587155bf47876034d98c3e5d3a17cdd`  
		Last Modified: Wed, 14 May 2025 21:03:34 GMT  
		Size: 208.7 MB (208728254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd807f0200db7b5e19d5504ff036e34f9c9fcc35c2ac3e895fa3e7ac72a1624`  
		Last Modified: Wed, 14 May 2025 21:03:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
