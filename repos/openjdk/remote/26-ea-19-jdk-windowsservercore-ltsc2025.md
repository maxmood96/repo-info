## `openjdk:26-ea-19-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:91c9c63fa94db2e7906a49710bb6f07352c77130ae8f89ca921cf79285666646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `openjdk:26-ea-19-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:a11c28b420da137ff35ccec4aae692b550e32e59f7d29c0895b8a55d266cd7cb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3793803273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d596865be71e465de566632b9dde974cf112de10a448bc71aba277060f8ada17`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Mon, 13 Oct 2025 18:21:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 13 Oct 2025 18:22:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 13 Oct 2025 18:22:33 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 13 Oct 2025 18:22:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 13 Oct 2025 18:22:39 GMT
ENV JAVA_VERSION=26-ea+19
# Mon, 13 Oct 2025 18:22:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_windows-x64_bin.zip
# Mon, 13 Oct 2025 18:22:41 GMT
ENV JAVA_SHA256=b31dc1d0afdaba4c6b7a399e0a932fb1a4f5a61e7624aaad8ca40b85400f966a
# Mon, 13 Oct 2025 18:23:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 13 Oct 2025 18:23:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac58c0234c584817a261d280a90a93a32dcdff4099bfeae26d9cc974f8779939`  
		Last Modified: Mon, 13 Oct 2025 18:37:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d00ae36bb0ebef162f8a3563d9df78c2b405a328f61049d59d6b692cde3b4c`  
		Last Modified: Mon, 13 Oct 2025 18:37:21 GMT  
		Size: 389.2 KB (389178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8359e608c98bdd70e4f7d158dc8bfe26b2408404ed492ad61bdfb60125ea20e0`  
		Last Modified: Mon, 13 Oct 2025 18:37:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9e6a7e3492342a227e657e8fa825b76a4dfa55fe2098381494df88e185bd2`  
		Last Modified: Mon, 13 Oct 2025 18:37:21 GMT  
		Size: 362.6 KB (362609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e961f49153bf991b3312cb08ac4f7f4bc9fb35fb3ee3b23cd5d51351037982b8`  
		Last Modified: Mon, 13 Oct 2025 18:37:20 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be929c303663995905a5cbbead1cf0f74ae3e3665ea2e2e79adafa5d0a159c5`  
		Last Modified: Mon, 13 Oct 2025 18:37:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757e62759d0e5e7fc449e486542e4d73d97192f6bca59cfaec8b144f236b8a68`  
		Last Modified: Mon, 13 Oct 2025 18:37:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d4cba39ce9f4205b28adb15e2d5a0f07f8717a28287c9866df0dbd0cbc42c9`  
		Last Modified: Mon, 13 Oct 2025 19:23:30 GMT  
		Size: 221.6 MB (221603955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf618fb4b482343fd5ba9a6ee056c6701d2cff103b7a68e1e8023df0b9b01cc`  
		Last Modified: Mon, 13 Oct 2025 18:37:21 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
