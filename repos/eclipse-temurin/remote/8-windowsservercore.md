## `eclipse-temurin:8-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:78b615f89ea673e051bfe36c5c91d28cabb7e4b14178a70dc7bbfc58801ca629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:8-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:6e91122008b3139b134ef059946a4d1b67eefea837947e0cfdbfe2cfeee829e1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2445975069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c378c1c9c2092c601fdd4e60a83ff917ca3b34c66f925b0df01f021279af7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:15:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:15:53 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 14 Nov 2024 20:16:19 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u432b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u432b06.msi ;     Write-Host ('Verifying sha256 (c9280205858928756374d930d4b539c59b1cb470425d2cf300b943c56efe4d86) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c9280205858928756374d930d4b539c59b1cb470425d2cf300b943c56efe4d86') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:16:27 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a384db9cc0897a1257f625f23acce2aa576cea79b7c9f10632a9401937d1f212`  
		Last Modified: Thu, 14 Nov 2024 20:16:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f043a9f1d704a2466902715be1d6c3e1f5ce811a0ad3a1dbaa825173ef9c6171`  
		Last Modified: Thu, 14 Nov 2024 20:16:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01760d484420dcc0d25ad04a6ecab5f847defdf70988b970796980c440267a44`  
		Last Modified: Thu, 14 Nov 2024 20:16:39 GMT  
		Size: 193.1 MB (193119492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994dae3af643747a46ab7a493c56e7bdfc7ca4530ea182a452557f36d33df6af`  
		Last Modified: Thu, 14 Nov 2024 20:16:30 GMT  
		Size: 368.8 KB (368767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:d36d2cc509725232e330374c2370c2064c953e0f1b74f9f1ffdf8cb1879a5390
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204247474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fac120fed93978718dc9f41a7358a8f16e2259accba5edcbe262211127a5d3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:13:30 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 14 Nov 2024 20:14:08 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u432b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u432b06.msi ;     Write-Host ('Verifying sha256 (c9280205858928756374d930d4b539c59b1cb470425d2cf300b943c56efe4d86) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c9280205858928756374d930d4b539c59b1cb470425d2cf300b943c56efe4d86') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:14:16 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02920fd26383c9b394738e338b4e3b6c8b6e4807c4254529ab03f9abe749e62f`  
		Last Modified: Thu, 14 Nov 2024 20:14:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33486ccf5c7312a037ff8f9e92f44eaa6d134c86e1f36001fdda18c1257cef8`  
		Last Modified: Thu, 14 Nov 2024 20:14:20 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14a787d68f8ed9ddd91a2d534496ff15e4ad50d47700421c90fe3ebf9e12427`  
		Last Modified: Thu, 14 Nov 2024 20:14:30 GMT  
		Size: 193.3 MB (193253553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b94c54df81e06b94e3bcd6324fbb531773190f86726ee01a4bdc937b2dc4db0`  
		Last Modified: Thu, 14 Nov 2024 20:14:21 GMT  
		Size: 337.5 KB (337547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
