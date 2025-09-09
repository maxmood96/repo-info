## `openjdk:26-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:30d74c1c2c86bc61e7c418c9178d502f101335f79dece31fef8e69ccd225fb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `openjdk:26-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:9e14bb2a394c7497d23a6cbf38da2f9d45600767c5d92e95165f8d264d21ed27
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3718804066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29c9f3dcd46c6c72a6bfda7d5a1a555718c2fd8a6b410898efd2c5376263cc6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 08 Sep 2025 21:33:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Sep 2025 21:33:30 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 08 Sep 2025 21:33:31 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 08 Sep 2025 21:33:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 08 Sep 2025 21:33:38 GMT
ENV JAVA_VERSION=26-ea+14
# Mon, 08 Sep 2025 21:33:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_windows-x64_bin.zip
# Mon, 08 Sep 2025 21:33:40 GMT
ENV JAVA_SHA256=a7542fc9e185b46aef40f54067948209eaeed10cc87b141740dc4b4236bf3d70
# Mon, 08 Sep 2025 21:33:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 08 Sep 2025 21:34:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668c2082a667bf0a02fe7b7d4f393c75215fc1dcda10d14609b2c9b912cbf42e`  
		Last Modified: Mon, 08 Sep 2025 21:57:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767f1bddd3410cc38b81f8d86e4dc43ffed48f39cf72b2fdfe43e389254b8b6`  
		Last Modified: Mon, 08 Sep 2025 21:57:17 GMT  
		Size: 398.7 KB (398654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcdc9d5ecaa544c162dc3267bc0e21961e13e4d8ecf0be1acfb65d0c46e074c`  
		Last Modified: Mon, 08 Sep 2025 21:57:18 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11abbbab1c4eec50c56da6adb68c519ec2be84955cae33f733d10b1ec0822963`  
		Last Modified: Mon, 08 Sep 2025 21:57:18 GMT  
		Size: 378.6 KB (378584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc29eae6d35b1c1ed60921038db29bc65ceeabc887618a816f3b24d0b03b8872`  
		Last Modified: Mon, 08 Sep 2025 21:57:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b648a8393e72737cbc693683a9b3253e2d7d22ab2b395cb0ac3dcf93e53a7623`  
		Last Modified: Mon, 08 Sep 2025 21:57:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b07c1bba29b7107d745eb1698157607783bf438f2bbc7ca14fd31da3668d75f`  
		Last Modified: Mon, 08 Sep 2025 21:57:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bd4c9f67e487f389e86c27b9fedfc88008a4f9de98f8b4056bb66bbdc38288`  
		Last Modified: Mon, 08 Sep 2025 21:58:28 GMT  
		Size: 219.2 MB (219188569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55edb3029e84143eb0203842ceca6829aa8cc6989091dd1ed6e747c75e3e3fae`  
		Last Modified: Mon, 08 Sep 2025 21:57:29 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
