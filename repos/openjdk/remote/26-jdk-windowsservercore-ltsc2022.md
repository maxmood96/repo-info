## `openjdk:26-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:28fafba4509fa2b665831567e2204e91418cf64b10d36b0f1b078ad44024ac9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

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
