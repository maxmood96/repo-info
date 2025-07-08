## `openjdk:26-ea-5-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:d05664f8b061038290f4adcd91acfc132f151c4691e2d7574d71613761622fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:26-ea-5-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:4d969c86d23d9e64b3451ba906d8a951498e4fabd1e61d4c80a1dfecec12cdc7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695915455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4e50ddecd67406b78609053c071a043a9b34fc2eb8277b47388dfc893b3b00`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 07 Jul 2025 21:04:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Jul 2025 21:04:37 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:04:38 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 07 Jul 2025 21:04:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:04:45 GMT
ENV JAVA_VERSION=26-ea+5
# Mon, 07 Jul 2025 21:04:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_windows-x64_bin.zip
# Mon, 07 Jul 2025 21:04:47 GMT
ENV JAVA_SHA256=884a05860f9ed48a9a26e95900c90750b220618efe84857aa27061fd3657fee3
# Mon, 07 Jul 2025 21:05:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:05:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d12c0d944112949269911af87ab2b0880632b0283d0807be1bb18fff8b88fd6`  
		Last Modified: Mon, 07 Jul 2025 21:08:37 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317eedd8988a79049bde403be18f37983d2e9b318181fa4c4359297254f75363`  
		Last Modified: Mon, 07 Jul 2025 21:08:38 GMT  
		Size: 418.1 KB (418095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11247a85091dae1705f75e493b1291e2ed6c7d7a88762a034e55ba072c60ec3d`  
		Last Modified: Mon, 07 Jul 2025 21:08:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b02afcaae5c268a0b439afff3e090574bcb1cf8fcc3010103ce0a647cea549`  
		Last Modified: Mon, 07 Jul 2025 21:08:38 GMT  
		Size: 399.8 KB (399830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e541b88016d4e2239b5d6c91d7c076b442c2e0eba6a85de6a870c23090d8decc`  
		Last Modified: Mon, 07 Jul 2025 21:20:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29707814469dc161578e64cbadefaa77e8a9c349d3c92783b1fde02492cf6daf`  
		Last Modified: Mon, 07 Jul 2025 21:08:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0796602f5c3304cd1d18b8d4f8f614d73df443d57661389b0caf3fcbf7dbd794`  
		Last Modified: Mon, 07 Jul 2025 21:08:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dfc36619f91d8319d59bc4d3842fac5c878260c43c117350e6859350650205`  
		Last Modified: Mon, 07 Jul 2025 22:08:51 GMT  
		Size: 218.9 MB (218915637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06134b54f07a963a339547679636f7d1c1faba0f8a282ed089bdf91da9c57f76`  
		Last Modified: Mon, 07 Jul 2025 21:08:38 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
