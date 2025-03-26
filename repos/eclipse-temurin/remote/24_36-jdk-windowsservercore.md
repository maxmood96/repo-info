## `eclipse-temurin:24_36-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:7ba6178d164dde4bbf64e99ac5ab69670ed4e025dee39e694a88b1147c9ba57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:24_36-jdk-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:96e4e596a495d69468b4b6297df44fed09bbf29f6ac083ad0abc851cffeece7b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 GB (3161623023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f42c14216cb04006bf2972692c673d87bbf809d1513fd77e11191017d98711`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 22:02:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 22:02:10 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 22:02:33 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 25 Mar 2025 22:02:42 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 25 Mar 2025 22:02:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a66e3d0f2fb30af04de3bf3c0a984c1bc9b24911e36c03fcca622ac39bd645`  
		Last Modified: Tue, 25 Mar 2025 22:02:47 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7a68aed1bf75d995f1a4246948c93a95235a02adc0bef5eafe1239dffd8371`  
		Last Modified: Tue, 25 Mar 2025 22:02:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabc5918d70d7d8ec662b968f403b8c5a6ff3c130cf097b7abd29f7e68d2ba81`  
		Last Modified: Tue, 25 Mar 2025 22:03:04 GMT  
		Size: 252.6 MB (252576394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c5a2570bb6461c4e7a9c7065736dbf5e9b9c7e90d43ae7ee1ec90f285cbe80`  
		Last Modified: Tue, 25 Mar 2025 22:02:47 GMT  
		Size: 395.0 KB (395026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803a03107195d819fdf73e1375bdcf9c95716dcb089f36f4e760dd86db162b3a`  
		Last Modified: Tue, 25 Mar 2025 22:02:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24_36-jdk-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:2bbae1f9264d057bedd2ba5dd4288db404da26105869b7875abf4bbbc9f0a65c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2522869417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2bc19428211827bd503a96e43cc42639d63c5e748656d7da787a4e3cf1fdb5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 25 Mar 2025 22:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 22:11:38 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 22:12:07 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 25 Mar 2025 22:12:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 25 Mar 2025 22:12:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822c4ef9e7d7b4e42106ffb946b1db45f41ec635401a8e64d8eaeac238c321ac`  
		Last Modified: Tue, 25 Mar 2025 22:12:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a0cc1f6c841087c17f8f24cc083835f69b68d2236e9f9822046101f0492173`  
		Last Modified: Tue, 25 Mar 2025 22:12:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2592a0351936d6f085a5e676170c99c4e7614259348cbdf3b98fdf9e7948fb`  
		Last Modified: Tue, 25 Mar 2025 22:12:30 GMT  
		Size: 252.6 MB (252552008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a586d8252ad803d704aa318d43d0793967fd4c4ad9732120d6fe7cb17dcd955`  
		Last Modified: Tue, 25 Mar 2025 22:12:18 GMT  
		Size: 372.3 KB (372335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bb14c0626119291182e8f7c1ac6360f9ca0f9b4deb7662008457294ae29b76`  
		Last Modified: Tue, 25 Mar 2025 22:12:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24_36-jdk-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:7d0e608d2e22cad27aad6678e39a7158497573af11978e33a433e295c410da4a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408831087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97491b26a4ae456f67a1f09095888871df096a8a04c45c886240e67df71859d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 22:04:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 22:04:51 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 22:05:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 25 Mar 2025 22:05:55 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 25 Mar 2025 22:05:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0b8b832f17bf00c30c823e66a45c6e1a99cb9d5324e71a48f21d92a9644d4e`  
		Last Modified: Tue, 25 Mar 2025 22:05:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64b775844c68bb12475a0f37f2ccc41af2c4d644c9f29f57b171e0e918b2213`  
		Last Modified: Tue, 25 Mar 2025 22:06:00 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe8a87aae7048a2eba83fd9b87674cd123a2a6f78b7e6fc0d7d68a74c18a141`  
		Last Modified: Tue, 25 Mar 2025 22:06:13 GMT  
		Size: 252.5 MB (252539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184b0c323b01f90d196020c287c215d608e9756b7d8629b249f2a700c4d08aef`  
		Last Modified: Tue, 25 Mar 2025 22:06:00 GMT  
		Size: 4.7 MB (4653294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9125f8b979f51d4d75cd073228028c774ebfb4f1dbc5d6128a25152c45547e`  
		Last Modified: Tue, 25 Mar 2025 22:06:00 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
