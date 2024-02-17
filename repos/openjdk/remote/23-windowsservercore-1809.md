## `openjdk:23-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:abb7559499cb344d06b168f888feeef0822ba8d7d50e61bcc8ee9d1da2e35fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:23-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:3295b85bd59d6c701cecf7e2c8a41cd172afb86ce775aaf7bddd1dc16313aac7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279222255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8808dd3d86d4d2d233b945552714b97796377cc702b52fe1966669a089b8673a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Sat, 17 Feb 2024 01:05:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 17 Feb 2024 01:06:21 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:06:22 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 17 Feb 2024 01:06:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:06:43 GMT
ENV JAVA_VERSION=23-ea+10
# Sat, 17 Feb 2024 01:06:43 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_windows-x64_bin.zip
# Sat, 17 Feb 2024 01:06:44 GMT
ENV JAVA_SHA256=c8a55ee2916486b9f5f0000b52d73eab80af9b18f48a74bf8269f14057b12371
# Sat, 17 Feb 2024 01:07:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:07:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba29bb8dcee1baa98b602727cfc164c8fe08d760da2a4cdf58cb3e3812bf609f`  
		Last Modified: Sat, 17 Feb 2024 01:07:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bd7c1eeed165d1943860555c93f15fb165a96f02491f9dc22fd3c528e90550`  
		Last Modified: Sat, 17 Feb 2024 01:07:28 GMT  
		Size: 499.6 KB (499579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87945171e76d0fdde3f91630d0d14394f6b3e1963bd085ec39300b91ac0f06d2`  
		Last Modified: Sat, 17 Feb 2024 01:07:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b149db64415bd9b01b7635cfb3b6de4d11f73edd763e5d74f6824bff4d65807`  
		Last Modified: Sat, 17 Feb 2024 01:07:28 GMT  
		Size: 345.3 KB (345263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ed8988aa9396a3cc4ea7aa7cd4c237f7692dd5bde914daeb4b095dd5f9ae52`  
		Last Modified: Sat, 17 Feb 2024 01:07:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98dc1374388a087edb6e2475ea1b56bd1e75a645d33b37d996546cd22f55e79`  
		Last Modified: Sat, 17 Feb 2024 01:07:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a70e19496c8a32448c21826ccb99be74e2ddf896aad99230e700ce1a9a6f865`  
		Last Modified: Sat, 17 Feb 2024 01:07:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b7e863b6227428d807f8b7a96eadb718644edb96654a51ff2ff5509f2abb52`  
		Last Modified: Sat, 17 Feb 2024 01:07:39 GMT  
		Size: 197.9 MB (197920802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86553eaf7d06abac9c63fc828f08c71f853926ccb7fe6d1eef0392533f5ddaf`  
		Last Modified: Sat, 17 Feb 2024 01:07:27 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
