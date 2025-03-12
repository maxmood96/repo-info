## `eclipse-temurin:17-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:96e289fbf69fd73c75b61ca88264628e5bda987b0131e29131cc7cf05c9ffddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:a51ebad9a8bc243770e6a1ce4ae11dfb3fc75c2c0d38b59bcce2c57257e1045b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2984115526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299656bd4207cf9cb9c6c812f4184dad4416a09b09599edc0a30b20bc185e26a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 18:47:56 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.14_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.14_7.msi ;     Write-Host ('Verifying sha256 (6a81df58247baeec4153e746b68af5b8618e50ed51a59b4c9e0c1b025edd4ad8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6a81df58247baeec4153e746b68af5b8618e50ed51a59b4c9e0c1b025edd4ad8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:48:03 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:57c8294105a7a77e3423a9838ffc29cb1c675128d4b50f512d3babd52004ed43`  
		Last Modified: Wed, 12 Mar 2025 18:48:07 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c147f06506b9462e453f0f393701e8e5b6a5cd81b491ea66c28fb0197277f565`  
		Last Modified: Wed, 12 Mar 2025 18:48:07 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27efc760cf47d48d337056fb56eec181cf5a452fe7c896aaa93b6050e69c35cc`  
		Last Modified: Wed, 12 Mar 2025 18:48:14 GMT  
		Size: 75.1 MB (75095627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218cc55dc5708f984f9a74d7a3dbc926fa7b3dfc5025b01d61b6fb814b4fa3a1`  
		Last Modified: Wed, 12 Mar 2025 18:48:07 GMT  
		Size: 369.6 KB (369588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:d723f5c81cbc7bf4ddb7dc73c07134644a429eb0232f9c3e437d68b9c75b6ef2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345349786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405d00be11278b248c9968599c503bae498ca4aa8519336b916d312c30e045dd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:58:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:58:21 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 18:58:47 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.14_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.14_7.msi ;     Write-Host ('Verifying sha256 (6a81df58247baeec4153e746b68af5b8618e50ed51a59b4c9e0c1b025edd4ad8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6a81df58247baeec4153e746b68af5b8618e50ed51a59b4c9e0c1b025edd4ad8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:58:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:853512039325103450cd440862d3b006e781cb8e657777b5c5bb34d0ec3a23ce`  
		Last Modified: Wed, 12 Mar 2025 18:58:55 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713efc5b525b1df2a31a9968b589fa47c685e256f917b23d68f9e3b74604d995`  
		Last Modified: Wed, 12 Mar 2025 18:58:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cc72bfd2e70f673960221dba4fee474daa8737aa338a385ea41e04f9410109`  
		Last Modified: Wed, 12 Mar 2025 18:59:01 GMT  
		Size: 75.1 MB (75064297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834a5fb0d69d76ac2b72365b17231f43e415a828c04da5eed60e4e9b2e9dd6ef`  
		Last Modified: Wed, 12 Mar 2025 18:58:56 GMT  
		Size: 341.7 KB (341719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:4bbc6dca56fe3de5144e43dd22af83ef726e06fc4a681da9b67ff62615794ff1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229980959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa49e26398f6a8af34dc365b10f7eadce7a6c922f3334469a9ae039a448139f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:50:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:50:23 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 18:51:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.14_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.14_7.msi ;     Write-Host ('Verifying sha256 (6a81df58247baeec4153e746b68af5b8618e50ed51a59b4c9e0c1b025edd4ad8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6a81df58247baeec4153e746b68af5b8618e50ed51a59b4c9e0c1b025edd4ad8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:51:28 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:0cd1bda31feffc89470f42b657737f700750a947e7ed2e7471bb9ed9995bf63c`  
		Last Modified: Wed, 12 Mar 2025 18:51:32 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f5b9a3d091f83c5796159320d368c3325448d9bd41a4842dd2c96fce992a99`  
		Last Modified: Wed, 12 Mar 2025 18:51:32 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e124ae392753d73637cfcd166d7b2873026e5a603a13c32f4dd8383e2f7db0`  
		Last Modified: Wed, 12 Mar 2025 18:51:38 GMT  
		Size: 75.1 MB (75097301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfa5f75a60127ee68c3e8f89d787bb9619b4af81ef30f24f8126bf985eecd8b`  
		Last Modified: Wed, 12 Mar 2025 18:51:33 GMT  
		Size: 3.2 MB (3246287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
