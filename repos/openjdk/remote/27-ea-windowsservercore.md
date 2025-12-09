## `openjdk:27-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:1ffabf20942d7081c95b7696376ef2c897754fab03be3fd1b737e40ad50114b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `openjdk:27-ea-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:78080d34af3859a8bd22dadb96efc45918e6b35e9997f54a80d48960e0c6d7b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3479450848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff9cdc653a7670a5cb7417258cac4b88287a7535189aef96e57d8b9c8ce4323`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:35:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:48:10 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:48:11 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 09 Dec 2025 20:48:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:48:17 GMT
ENV JAVA_VERSION=27-ea+1
# Tue, 09 Dec 2025 20:48:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_windows-x64_bin.zip
# Tue, 09 Dec 2025 20:48:18 GMT
ENV JAVA_SHA256=77d566459162b6597396e779186334a870aeee1837fe453aac80662b023659c1
# Tue, 09 Dec 2025 20:48:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:48:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23e8e2e5cb8541164882e4145834d06a55e4db5f8d5da5b51096f333d0bd1a1`  
		Last Modified: Tue, 09 Dec 2025 20:45:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0884d4e08f60fed344d867d354b68fedf7deb530edb0b05a1a3aa822e0d9aa`  
		Last Modified: Tue, 09 Dec 2025 20:49:05 GMT  
		Size: 360.7 KB (360717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931ad10247d1e4fd0b207c757327ad12832073d2a4b36567cd30117dc2066b9a`  
		Last Modified: Tue, 09 Dec 2025 20:49:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7207cb9acf7b56ff4bb25f39c648ff383e067e8db49bad9782d94c8880c81ec3`  
		Last Modified: Tue, 09 Dec 2025 20:49:05 GMT  
		Size: 346.3 KB (346263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55de431ee7005581e79f5febe58b5df59b1ec8b598771c1512b031378b1267d6`  
		Last Modified: Tue, 09 Dec 2025 20:49:05 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53f97e90a43956575ae45f2617f39cd70c5850b38b3ca91d96885949ea21994`  
		Last Modified: Tue, 09 Dec 2025 20:49:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7274f12cd9ae28db9f128a823bb9b4c570bf3dd3b65c923d7c1a0d3efd043679`  
		Last Modified: Tue, 09 Dec 2025 20:49:05 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f65f607752cbd578f1e50941efdb0f945d91ea6196f96e55a30637a3a8d5eb`  
		Last Modified: Tue, 09 Dec 2025 20:49:46 GMT  
		Size: 225.6 MB (225615628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7abbe3b0585d68560a137ea5b4d5857265babca9e2900a530a9082f32b8a59`  
		Last Modified: Tue, 09 Dec 2025 20:49:05 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:4c7c1047999b86628d817a1d0a72acc4a887e378581d20f8703b16615daeafd9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2006334704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152a656b4e6a7f13e76e6649f7664bb8528130d51e0640cc1541d7768b887055`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:29:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:45:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:45:17 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 09 Dec 2025 20:45:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:45:23 GMT
ENV JAVA_VERSION=27-ea+1
# Tue, 09 Dec 2025 20:45:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_windows-x64_bin.zip
# Tue, 09 Dec 2025 20:45:25 GMT
ENV JAVA_SHA256=77d566459162b6597396e779186334a870aeee1837fe453aac80662b023659c1
# Tue, 09 Dec 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:46:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac22ca67391bc67ae059bdc6b4fe7cfa91d0dd9f198a7a4a48d1208814e923`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2f008183168bde68b91f19059fb5a2932ffca93f573665a863038e54852e67`  
		Last Modified: Tue, 09 Dec 2025 20:46:34 GMT  
		Size: 491.1 KB (491114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678e16c0488e2e52183c36eea1b736af3f24966b5a4804461c92f1f18f0a94a5`  
		Last Modified: Tue, 09 Dec 2025 20:46:34 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a6fabcf69c668a047b14dc04852d4490787bd762850c1f1ddf578c4b08d6f1`  
		Last Modified: Tue, 09 Dec 2025 20:46:34 GMT  
		Size: 338.1 KB (338079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d0088da8340135518f8acebfcebdee6b3d4f0667bb82c73681d8e1e40176c`  
		Last Modified: Tue, 09 Dec 2025 20:46:34 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03653331c81498eb8bbba739b80a7a84e502c00923c6271a4a7882501b427bd4`  
		Last Modified: Tue, 09 Dec 2025 20:46:42 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ef99eddcb3c99d6d41e25abf972704ef051d7edc7405c3cb4ddd718853d2b8`  
		Last Modified: Tue, 09 Dec 2025 20:46:34 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966b453b83ec37aefef177b8cffa39307388910e528b23dd27a4d90394f5dd6`  
		Last Modified: Tue, 09 Dec 2025 20:46:47 GMT  
		Size: 225.6 MB (225618324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c205b61bcdd9988b3c4925dc62efca88838c55a234cc2ac8e972718fd423ff`  
		Last Modified: Tue, 09 Dec 2025 20:46:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
