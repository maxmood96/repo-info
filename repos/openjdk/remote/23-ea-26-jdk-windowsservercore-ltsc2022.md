## `openjdk:23-ea-26-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:1517609577e3b784adf50a91942ac0a693130df6ca8516789d2d9e35ee2593a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `openjdk:23-ea-26-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull openjdk@sha256:7456cd57db65dd879085292a6bcaac4a70ca4be73e8ae732a4af4b5e81cb7974
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325278451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d06aaee34c79aaf681ec135518021e0994d1713c746f8381cca6d4c8890b0b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:05:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:05:22 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:05:23 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 12 Jun 2024 18:05:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:05:29 GMT
ENV JAVA_VERSION=23-ea+26
# Wed, 12 Jun 2024 18:05:30 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_windows-x64_bin.zip
# Wed, 12 Jun 2024 18:05:31 GMT
ENV JAVA_SHA256=79726b7c310903e3f9fa306110b1316629abf85403efeb1bb660d9fa7cff7a01
# Wed, 12 Jun 2024 18:05:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:05:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea101af398c7c16db5087deff6383f621ccae913f2afdd10d0c5dd8ffba75e0`  
		Last Modified: Wed, 12 Jun 2024 18:06:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f644aac8bbef2d01636c9a583d462d9c99cb06566157f3fff490e98c938a180b`  
		Last Modified: Wed, 12 Jun 2024 18:06:01 GMT  
		Size: 349.3 KB (349304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6278c8c75bbbc9bf0d6bf54762055bb2d4c828ad3e97cac0ab643c3c9994faa8`  
		Last Modified: Wed, 12 Jun 2024 18:06:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2a5b9ec89230bc9d45d17792e7a50b0b9999a9812a4cbee887b6dbd8a39d0a`  
		Last Modified: Wed, 12 Jun 2024 18:06:01 GMT  
		Size: 335.0 KB (335002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7292e28da7d3d23202635a43ad4f6371884fb234c94614811f4f8547fded74`  
		Last Modified: Wed, 12 Jun 2024 18:06:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53bc3f14365b974684d54b455db89dba026be1df1425286b8a342ef9712b72e`  
		Last Modified: Wed, 12 Jun 2024 18:06:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6cd491c7b064ef83e3601be5a978da7b023022e1652368b241537756a1905e`  
		Last Modified: Wed, 12 Jun 2024 18:06:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f62d98c2ea7b60a3235cd3930243d50e225371273bcaf2c29b32a2530e4a887`  
		Last Modified: Wed, 12 Jun 2024 18:06:11 GMT  
		Size: 206.4 MB (206407708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862e0cb52c22e6734d0e46c3299ac69eb475fabe9516c5dba95675e98ddf0eac`  
		Last Modified: Wed, 12 Jun 2024 18:06:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
