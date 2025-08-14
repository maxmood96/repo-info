## `eclipse-temurin:11-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:7d8e448225cdd5597909c15525dd9fec7ef90dc7f5d03941a4ff9af886199b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:ff5e52400e828f4c93ce80cca410a6eb744b5080f4010e13d96cbe7f94768142
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3574130814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d1180814b6adcfd4d6ed65f438e95d5b15af4408f8cb6659a6d4e428748604`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:02 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 12 Aug 2025 20:27:14 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.28_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.28_6.msi ;     Write-Host ('Verifying sha256 (a093e7c3b7754bcf61140764eddb11343e3810890dcc3b96195b7d695cd1358b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a093e7c3b7754bcf61140764eddb11343e3810890dcc3b96195b7d695cd1358b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:27:20 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:332919e2fe9d03e978fca81fbfc7ce0a55ccc651ec7fe12a3359adf27180cc5f`  
		Last Modified: Tue, 12 Aug 2025 20:31:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c09745e2a304ab4e35127d54012f1bbf2f1de5be9b33b16cde9d63a8687cc4`  
		Last Modified: Tue, 12 Aug 2025 20:31:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf064087ede68cbe972ffc0431a65e44f23c7a2149ba3a877a5c46591e9c409`  
		Last Modified: Tue, 12 Aug 2025 20:31:12 GMT  
		Size: 74.9 MB (74923903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc60ad06a37db5549bb8abf8ed0617ae2922bae6a017e94ae89028765ddae743`  
		Last Modified: Tue, 12 Aug 2025 20:31:03 GMT  
		Size: 373.9 KB (373865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:f8c87c5a5dbdfcf1319eeed9cec537a856fd87861ac3f6ce7898bb7bcfa4359f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356939326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a6d9658a6e8f2c51e713f5a4b17b13ae31d745522ef18882d8f72d3dee2a98`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:39 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 12 Aug 2025 20:26:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.28_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.28_6.msi ;     Write-Host ('Verifying sha256 (a093e7c3b7754bcf61140764eddb11343e3810890dcc3b96195b7d695cd1358b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a093e7c3b7754bcf61140764eddb11343e3810890dcc3b96195b7d695cd1358b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:27:05 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:cc675ff91b4ddbf375bbc13d9f434ca4099b79424b2214155c137b65b4d0b71d`  
		Last Modified: Tue, 12 Aug 2025 20:28:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3261b49c25a3d0df3ddc25931d27486ca5625e0a9b0cfc3d26568396a70869f8`  
		Last Modified: Tue, 12 Aug 2025 20:28:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c06bb97301ff90ada2ccf6af9a730d574760c8f4ddc56c1de94674446c72dbe`  
		Last Modified: Tue, 12 Aug 2025 20:29:09 GMT  
		Size: 74.9 MB (74895001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c99242bd82c5f3c8d48b8b5c46785bceced4b0a2bf27286fc5860f2a5c3408`  
		Last Modified: Tue, 12 Aug 2025 20:28:45 GMT  
		Size: 349.8 KB (349796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
