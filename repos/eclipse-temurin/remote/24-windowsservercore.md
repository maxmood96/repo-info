## `eclipse-temurin:24-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:41ecc0a2926b6fb5e386fcb7812ce005c6e67588a606060ffc0e011f03a084e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:24-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:9013ff6ae2c0d31f15daae94f5140e6826468377c150e9ed15cb17f5e4b0017b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3824292079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d873de19b0bb1b4a13e4485423ce2370a672a9f40019fcaf1a965575e4f1a69f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:48:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:57:08 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Wed, 10 Sep 2025 21:57:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_windows_hotspot_24.0.2_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_windows_hotspot_24.0.2_12.msi ;     Write-Host ('Verifying sha256 (be608fa0c8a0b106b2051fbef941e8021d53d799d22172719b8f8b1eef4b361c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'be608fa0c8a0b106b2051fbef941e8021d53d799d22172719b8f8b1eef4b361c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 21:57:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:57:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae601f0777b06a06d8faad18910ce906d57fb27de067d609e4022dde683f85b1`  
		Last Modified: Wed, 10 Sep 2025 21:57:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a5047bd335d88a5d22421671d426fc8a9100fba67e325ae0e27d579090afa3`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a044e4c5e68398ec5f127c5273b28185339eab6076d42700ebf8a084e19d2ea2`  
		Last Modified: Wed, 10 Sep 2025 22:20:04 GMT  
		Size: 252.5 MB (252497986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91296cbf1248ea445975a2b3a2eccb1ccc05ca7bb730e1d3d4b0597f7ab939e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 350.4 KB (350440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204cc581ccc61ad480ce8037a7b3015c5229b665f0ca6a47e9d9b2f6f3b4cb09`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:e494faa9e4a767d4a1b63357382054aaa6fcf2d2e80e4c12966f6b498ce1482d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2535004583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4162e7d03c452420b8cd8fb35fad4a952309a3e1a845675dd1649e33fe98b925`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 20:20:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:01:19 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Wed, 10 Sep 2025 21:54:12 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_windows_hotspot_24.0.2_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_windows_hotspot_24.0.2_12.msi ;     Write-Host ('Verifying sha256 (be608fa0c8a0b106b2051fbef941e8021d53d799d22172719b8f8b1eef4b361c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'be608fa0c8a0b106b2051fbef941e8021d53d799d22172719b8f8b1eef4b361c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 21:54:17 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:54:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe60f506e392727a189c473ed3077c57345b082b3f502c4e12299121d8a339`  
		Last Modified: Wed, 10 Sep 2025 21:43:44 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f99e766edcb121a0a4795b8332ea911801ea02353a098de9160ac21da59707`  
		Last Modified: Wed, 10 Sep 2025 21:54:45 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d23887f1fe3e91a22a4f4f6e31f799af7fc0b6149390fedaeca443f408fb2d`  
		Last Modified: Wed, 10 Sep 2025 22:19:17 GMT  
		Size: 252.5 MB (252501009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a81d2079b84a893a04e56422c617fcb8f5243ec6958055d2de764a493c8008`  
		Last Modified: Wed, 10 Sep 2025 21:54:45 GMT  
		Size: 354.7 KB (354691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e17f7fa292f65a5bca2abe9fd06c01d70bffd6055216da10e25777deb73fd`  
		Last Modified: Wed, 10 Sep 2025 21:54:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
