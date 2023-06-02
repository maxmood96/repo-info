## `openjdk:21-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:71ecc2edfaa53b247b0209cb9ca091ebc97d6f0735d8450fca934c39cde434aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `openjdk:21-ea-jdk-windowsservercore` - windows version 10.0.20348.1726; amd64

```console
$ docker pull openjdk@sha256:d91d4d50aea37843c2f07aaec7bd61c38e570afdb8ad5888ff81fef6267e2465
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973774338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60403c4c1fa5a24e4228a6144cfbc98e13ec24441ae17f387d4b1050974a1bd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 02:50:46 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 May 2023 02:50:50 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 May 2023 02:51:20 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 01 Jun 2023 23:15:22 GMT
ENV JAVA_VERSION=21-ea+25
# Thu, 01 Jun 2023 23:15:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/25/GPL/openjdk-21-ea+25_windows-x64_bin.zip
# Thu, 01 Jun 2023 23:15:23 GMT
ENV JAVA_SHA256=cb61acaf8c0fa3b4ad9300a9607056ed17d839f154a21db7a96c2d585f102163
# Thu, 01 Jun 2023 23:16:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 01 Jun 2023 23:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6500851308f2a80744cfa1cca578e46041bad797f47ea2d8c83f894349fac438`  
		Last Modified: Wed, 10 May 2023 03:00:03 GMT  
		Size: 448.7 KB (448735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d15d3ceb58f655a9b9e1310abf5e4a03194602c97d6cbdfa450b22ffbc6d0f`  
		Last Modified: Wed, 10 May 2023 03:00:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74b424d7445673b30f720a5569aad1a4050cf8a0ad3c7ac1abe1f0576007898`  
		Last Modified: Wed, 10 May 2023 03:00:02 GMT  
		Size: 262.6 KB (262606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e36b2b66141a3b2fa661e35ce1edb8080cd7c42e11292dfeb298173e29746c4`  
		Last Modified: Thu, 01 Jun 2023 23:19:49 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d58ef9acb989fc44ee837cbf41d37c23a8ef80ce3c93f101051877d3f7c4b2`  
		Last Modified: Thu, 01 Jun 2023 23:19:49 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a1d899f8a524f4469be493bafceaac320b2780bce233df9a993dd8a5e50388`  
		Last Modified: Thu, 01 Jun 2023 23:19:49 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd8c09c8da1260b962f0c256f606edc1a9b578079b2695dc67bbcfa073b0774`  
		Last Modified: Thu, 01 Jun 2023 23:20:08 GMT  
		Size: 198.1 MB (198073052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0fd2f1a5e3d0ee778a1760c46921d9425ada844a11abbf4fd0e6865088cd9b`  
		Last Modified: Thu, 01 Jun 2023 23:19:49 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-jdk-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull openjdk@sha256:83dfcdded265036558a0fc2b80201731a07bd317e4684cde7e9c6396b86c6e17
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2270824738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01701298273aeacbc250be2a511317c9dfe60ae4ce2701647412c5eafcace4a4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 02:54:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 May 2023 02:54:19 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 May 2023 02:55:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 01 Jun 2023 23:16:35 GMT
ENV JAVA_VERSION=21-ea+25
# Thu, 01 Jun 2023 23:16:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/25/GPL/openjdk-21-ea+25_windows-x64_bin.zip
# Thu, 01 Jun 2023 23:16:37 GMT
ENV JAVA_SHA256=cb61acaf8c0fa3b4ad9300a9607056ed17d839f154a21db7a96c2d585f102163
# Thu, 01 Jun 2023 23:18:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 01 Jun 2023 23:18:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8712378a27a3538d7991a50dcb72abb565959575008a538c012500547b6acf3a`  
		Last Modified: Wed, 10 May 2023 03:00:47 GMT  
		Size: 441.2 KB (441178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34b75cb4c34981b4a471f423e801ccecb0e509ef934ebed87377603d134a0b0`  
		Last Modified: Wed, 10 May 2023 03:00:46 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0267ca94f1356d921f0a3b30e5336c9c1c0604b0f3cb81963ab715ba48ff81`  
		Last Modified: Wed, 10 May 2023 03:00:47 GMT  
		Size: 259.9 KB (259927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1423580f4370fe20b15beb936d014b31c5d53b9456f2171790b6e25711c902`  
		Last Modified: Thu, 01 Jun 2023 23:20:27 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c78d921704430a9d3a22e67e7b148042c895be4acb8e94304db27e8c60edac`  
		Last Modified: Thu, 01 Jun 2023 23:20:27 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82be4c016dc5bb428a2756495c2e3ad35263c11d11a76da3d467aef4cccb168`  
		Last Modified: Thu, 01 Jun 2023 23:20:27 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a558dc4bbed700d1c924d8e1b49396c496668a41480f53a8ed2377b007a690dd`  
		Last Modified: Thu, 01 Jun 2023 23:20:47 GMT  
		Size: 198.1 MB (198079863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b713d96b15fcf1c3f104131c6dd8abc864f76302d3d0177d7994a224646bddc4`  
		Last Modified: Thu, 01 Jun 2023 23:20:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
