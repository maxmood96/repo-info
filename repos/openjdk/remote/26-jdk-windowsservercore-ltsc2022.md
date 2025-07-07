## `openjdk:26-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:1f6b52c3f9293b089f5ec269c0ce93deb1eee7675b36ac0dfd92a9217a0e19c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:26-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:ca2646bc70a1448b3eb90677fd5d84f4adb6ab36620bf4be3a07bf1d65ae3cf1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499833540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2071821180349cb13a9973591a48b476ac15d753935fb3f9fefdde754b9228`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 07 Jul 2025 20:59:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Jul 2025 20:59:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 20:59:18 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 07 Jul 2025 20:59:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 20:59:27 GMT
ENV JAVA_VERSION=26-ea+5
# Mon, 07 Jul 2025 20:59:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_windows-x64_bin.zip
# Mon, 07 Jul 2025 20:59:29 GMT
ENV JAVA_SHA256=884a05860f9ed48a9a26e95900c90750b220618efe84857aa27061fd3657fee3
# Mon, 07 Jul 2025 20:59:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 20:59:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d6efd27b87cb2750c88b77ee1f329cb902e61e763e802e111f5923edb5f29`  
		Last Modified: Mon, 07 Jul 2025 21:00:24 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98142ff25d6a11b13e5a5a2505b73dcc49913cb31981a51544e42b64673c0c8`  
		Last Modified: Mon, 07 Jul 2025 21:00:24 GMT  
		Size: 362.7 KB (362748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38031bb3bd259458eeaa2d138a455041a410dc02744eba80ebdf5233909de8c6`  
		Last Modified: Mon, 07 Jul 2025 21:00:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1481fed0294f891b10586bc3c19967ae59e7d0d667c76a0116adafb6ea7b3e`  
		Last Modified: Mon, 07 Jul 2025 21:00:24 GMT  
		Size: 351.1 KB (351067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942ca1d6980d692c1592000ebe2a122a123149ae64e1b0f3ec69bf57c7aeae10`  
		Last Modified: Mon, 07 Jul 2025 21:00:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1fbab3e4e3ec2c704282381c66c630e044bf8563aaa8f79c5d91fe1745d815`  
		Last Modified: Mon, 07 Jul 2025 21:00:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1120e93145250a6f00eab1344a565ff2e381752afb91f5ecdf65626bb74ffe2a`  
		Last Modified: Mon, 07 Jul 2025 21:00:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec303233784604dcef8bbb9a4a15aa270352f5b306b5908f0f3f8b5514b975d`  
		Last Modified: Mon, 07 Jul 2025 21:05:51 GMT  
		Size: 218.9 MB (218860449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64ad2658bde5f656d9b23171e60726bac8dafa6d7f1b399de23d0b4907ba28f`  
		Last Modified: Mon, 07 Jul 2025 21:00:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
