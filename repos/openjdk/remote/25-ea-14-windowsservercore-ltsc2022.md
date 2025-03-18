## `openjdk:25-ea-14-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:ee38d1ff70c06cb071a3069981d53d34461c78ad5dba26f5c4a130497c0f352a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `openjdk:25-ea-14-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:b3d8bc6fcf844f545a3c6c357a163f344c79a0b36752755ca727ee52a386dfac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2478503126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af98dd5bcd65ff6b3df99c313f99f9d11423ee674c5514785fc90aa95b24d9bb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Mon, 17 Mar 2025 21:13:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 17 Mar 2025 21:13:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:14:00 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 17 Mar 2025 21:14:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:14:07 GMT
ENV JAVA_VERSION=25-ea+14
# Mon, 17 Mar 2025 21:14:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_windows-x64_bin.zip
# Mon, 17 Mar 2025 21:14:09 GMT
ENV JAVA_SHA256=4616b55a7c0d6b65d650a08986609158fbffcfed8fc5fa589e9f356898d735d0
# Mon, 17 Mar 2025 21:14:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:14:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229e64bcffaf51716797ae399692049522cb84f67c9645a7c49eb08e9f0690af`  
		Last Modified: Mon, 17 Mar 2025 21:14:37 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd431b4b92ee3bc6fc7b4221d7da302fa1f7c272f6c213509ee7d5f3c3db76c0`  
		Last Modified: Mon, 17 Mar 2025 21:14:37 GMT  
		Size: 361.7 KB (361746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae2267affaa0a919f3d988547257009171c212272945d9a5f106a412c447320`  
		Last Modified: Mon, 17 Mar 2025 21:14:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51313b10bf56c0615e377a6472ec93e3fd29bf5262fbcf3a3c59fbe1ea0ca722`  
		Last Modified: Mon, 17 Mar 2025 21:14:37 GMT  
		Size: 347.1 KB (347117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d2f6e130f0b01b3b489e4118a1992efee59c43bfe4420922a3615f19b64da9`  
		Last Modified: Mon, 17 Mar 2025 21:14:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e69fd1411c9ec5de4e92c6fbfcf888b2a3436bd3b544c328578bbdd837cc60`  
		Last Modified: Mon, 17 Mar 2025 21:14:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e49083d98971cb7f161b9f38908c16f35a77b7e173165c7b9aa0a2002eab015`  
		Last Modified: Mon, 17 Mar 2025 21:14:35 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a35758e85e8afe57bf9cbdd31829275bb06c4e81eb5b9bae6eafea801bfe27`  
		Last Modified: Mon, 17 Mar 2025 21:14:46 GMT  
		Size: 207.8 MB (207845354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c39cc125df696825f83eef46cd919e92a1764344679f62d1054c6895417ad2`  
		Last Modified: Mon, 17 Mar 2025 21:14:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
