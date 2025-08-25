## `openjdk:26-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:07b83bd842a595f721fd0731cea7c65d9c8ca15d227f860a054b5680a780d4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-jdk-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:775acd02a7f2bbbb3590c8bea58ff76b4b6393586f586de6cc1f88aeacd1ea7e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3718711149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374a8d2bcbf99bb0e03cc1349619f242fccec60e22ab4343b7d67d37c7fb2636`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 21:00:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 21:00:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 25 Aug 2025 21:00:45 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 25 Aug 2025 21:00:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 25 Aug 2025 21:00:52 GMT
ENV JAVA_VERSION=26-ea+12
# Mon, 25 Aug 2025 21:00:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_windows-x64_bin.zip
# Mon, 25 Aug 2025 21:00:54 GMT
ENV JAVA_SHA256=1998fd0551258ac7c1815fdf5d70e77c4d82759755d956bcc599f16636fb4c7e
# Mon, 25 Aug 2025 21:01:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 25 Aug 2025 21:01:16 GMT
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
	-	`sha256:60bc0e5fd26b11245901156f7160c8d412c98134fa6300162f30b68404f60699`  
		Last Modified: Mon, 25 Aug 2025 21:04:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0fc79da67ddca75a21fe7560bbd65f9940bbcca88192ffa6874698efbc5c13`  
		Last Modified: Mon, 25 Aug 2025 21:04:49 GMT  
		Size: 403.4 KB (403356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ac11e60f6e6c4bba9ccc483e5c322b12c45c00549544375eeb7df6a20dbe6f`  
		Last Modified: Mon, 25 Aug 2025 21:04:49 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6affdeb490f60585e423b9b63a4403f6a5302d3f5c68c77a6b583760b74d48`  
		Last Modified: Mon, 25 Aug 2025 21:04:51 GMT  
		Size: 382.8 KB (382779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6340ee96a2b42f83657c450e26975abb4fe0ca7513e7093d70ccb723d90c250d`  
		Last Modified: Mon, 25 Aug 2025 21:04:50 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f651d5c52128165bb104469cfefca3704c9b1bc54fc508b3e4b2eb5fd8fee8`  
		Last Modified: Mon, 25 Aug 2025 21:04:45 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877992c07fb0cc14789f1839e473fafc79c2759372ddbc0868a280db49dc4c02`  
		Last Modified: Mon, 25 Aug 2025 21:04:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3573a0f7d9e8ec4c512f25bbb099ba131a22eb6d864cdc46d1a0b9230ac0e6e4`  
		Last Modified: Mon, 25 Aug 2025 21:08:00 GMT  
		Size: 219.1 MB (219086781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93665e9b679f0a08e5c90eafa070a721d4f06d4cfce3dcca8488a12732eeae9`  
		Last Modified: Mon, 25 Aug 2025 21:04:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:cb28f769a236bd2d3fd7bb94f14c65d3ed59fc90fc947b4ebb0efc40e76b160f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2501437179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec7a09107e80ff0a6b1383be297ec7419efe1ac9851e1233aa9d77c12157a74`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 20:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 20:55:04 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 25 Aug 2025 20:55:05 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 25 Aug 2025 20:55:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 25 Aug 2025 20:55:14 GMT
ENV JAVA_VERSION=26-ea+12
# Mon, 25 Aug 2025 20:55:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_windows-x64_bin.zip
# Mon, 25 Aug 2025 20:55:16 GMT
ENV JAVA_SHA256=1998fd0551258ac7c1815fdf5d70e77c4d82759755d956bcc599f16636fb4c7e
# Mon, 25 Aug 2025 20:55:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 25 Aug 2025 20:55:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af6db690a6df5eab11b3c2d5b2b8c63cb734052e63335bbf101606fea21cc85`  
		Last Modified: Mon, 25 Aug 2025 20:56:28 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cf5e087446fdcc85b769cd0ad070f5f58d7ce18f14c9adb18dd760d3e20d70`  
		Last Modified: Mon, 25 Aug 2025 20:56:20 GMT  
		Size: 355.7 KB (355704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1286033d8f4352e89f58b84bc870c7b6294c839f96e9ce98aaf771378b27f742`  
		Last Modified: Mon, 25 Aug 2025 20:56:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7856ee342197f4f3ad70a737f7b0e599d226fe3af6789addce4af0e2d3dc9f`  
		Last Modified: Mon, 25 Aug 2025 20:56:21 GMT  
		Size: 341.8 KB (341786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff8e7a332babd9881ffffbb6f0b977005583582926a912a855c74dade0be3`  
		Last Modified: Mon, 25 Aug 2025 20:56:21 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742fe53256007c4b516a868864d6519afeec84c40968f789abf6fbd880f247f5`  
		Last Modified: Mon, 25 Aug 2025 20:56:21 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67b10e01f8b8702e732b3dbb7d34f85f8b56e28608116d5c87e2f3b1d5d2087`  
		Last Modified: Mon, 25 Aug 2025 20:56:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b664f9d65e7d65e84f3a64e17e5671d8e01c125b401c4af16db85796b9eddd4`  
		Last Modified: Mon, 25 Aug 2025 21:08:05 GMT  
		Size: 219.0 MB (219040038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b9b3a4e3edbe87bd9cfc5724ba53b7f020466f6edd6c5ae28d9c435fc98ec9`  
		Last Modified: Mon, 25 Aug 2025 20:56:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
