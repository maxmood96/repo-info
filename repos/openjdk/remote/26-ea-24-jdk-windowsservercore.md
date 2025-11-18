## `openjdk:26-ea-24-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:0cefc2af52554e485e9b084ba2bb24b5a9e7e5785acd0a7e311f27106806a594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-24-jdk-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:09e4231cf6f2c44b0da2cd621af1d9b5515f987c2c53cf03e82c714eb934df0e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459773353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2ea8c7ca9828d7d4c742ec3b84ccc0a98b8b521abff5b2146129f8ac33d00d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 18 Nov 2025 00:19:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 00:42:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 18 Nov 2025 00:42:02 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 18 Nov 2025 00:42:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 18 Nov 2025 00:42:08 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 00:42:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_windows-x64_bin.zip
# Tue, 18 Nov 2025 00:42:09 GMT
ENV JAVA_SHA256=9b59e5ab2fbe51399288d84d2710135e705f8399b618a54aa95498654a9841c1
# Tue, 18 Nov 2025 00:42:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 18 Nov 2025 00:42:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7cef4a3415e4a64bcfbd4e853e4a6f58af113e4c2fe90d11e7cbba12594bc6`  
		Last Modified: Tue, 18 Nov 2025 00:41:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d267b8462ce57eb7da712d3f47f6f1111cb523e1e2586a15256bf8ae2c2b6b6`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 393.3 KB (393335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159990fca1045705e08dec5fd194d505fc905e391f4c8bea878fe6e5048daf73`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa613f0c8c857853c786dd0e34e8606e7f88ecd27df78c02a35eefc08adac02`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 358.2 KB (358174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8282b585c05eec76f85649a10ae9f95e34265f2bf433a8f49560d26f62c7a4`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a723b72e39bfe6feb6a12473386ab2705f6864e79dad996f51833c54e09e439`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d5bb8a2b7aa7600bbfd9e32951c1565fc21cd158393bc48a8c72e92a02137`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aa0d0d338f3e83aa7ae535d881c8c239fc23fe008f1b2b2091e0399d119bec`  
		Last Modified: Tue, 18 Nov 2025 01:24:03 GMT  
		Size: 223.6 MB (223558282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45032a2d12d52d71b5e3c8fb6840ffa44b4d0eba46ce53b04e35c6b6e9c7e7f`  
		Last Modified: Tue, 18 Nov 2025 00:43:19 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-24-jdk-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull openjdk@sha256:2116d1be67c05a1f3cab179415e675e108e29e35c9cebf3dc46c3da059cc2b78
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1994387506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa6c87dc33f41c82750b9f0bd8995334f92ffe8d60a707811145bdc7c81a4ca`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 00:17:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 00:42:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 18 Nov 2025 00:42:06 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 18 Nov 2025 00:42:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 18 Nov 2025 00:42:15 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 00:42:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_windows-x64_bin.zip
# Tue, 18 Nov 2025 00:42:17 GMT
ENV JAVA_SHA256=9b59e5ab2fbe51399288d84d2710135e705f8399b618a54aa95498654a9841c1
# Tue, 18 Nov 2025 00:43:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 18 Nov 2025 00:43:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4537a095e899824b1fc0fddf2320afc3e1181c5906c1acee8f9fdb54417e8ac3`  
		Last Modified: Tue, 18 Nov 2025 00:34:53 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c824d423a3ae61e8048693c5489c84b49c12caa7e7a4d6ba9e520b0d188d377d`  
		Last Modified: Tue, 18 Nov 2025 00:43:58 GMT  
		Size: 507.4 KB (507381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435859f1616ff278a58f008c8efad264b1e178ebc3996fe7018d348ee2dd0ea0`  
		Last Modified: Tue, 18 Nov 2025 00:43:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51890a89d2bd47c324619cbdb10836b8f49fbd8b4714f5052551fcf14b1185ed`  
		Last Modified: Tue, 18 Nov 2025 00:43:58 GMT  
		Size: 358.4 KB (358359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c8e0b48c1c6edba56073b793fe616e0e1635680832cd722a3c06596c0973bd`  
		Last Modified: Tue, 18 Nov 2025 00:43:58 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7276b59fd40eb42394c75361e9617089c67be8a23d92b496a264f9b8cda9c0`  
		Last Modified: Tue, 18 Nov 2025 00:43:58 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f18d58ea9a9ca1a05b7399f7ff0fef8edd621ff3e1f14abc5c6c2ce9110184`  
		Last Modified: Tue, 18 Nov 2025 00:43:59 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27480019e1c4df935bb9033b37c459b335a82cbcaae744b91050f0f96f95359f`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 223.6 MB (223552340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd9ee2b84a9f3edaf2c6681efd4e711bb672c151791c7094f235de05b098e99`  
		Last Modified: Tue, 18 Nov 2025 00:43:58 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
