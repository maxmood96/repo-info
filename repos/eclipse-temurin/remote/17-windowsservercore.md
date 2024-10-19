## `eclipse-temurin:17-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:7d93a84ad00fefc1ff1f1fc66f45a82d442b336a47033d6ae92aeae2dad5aefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:031d27361831a3e8524a5469d0f81b41ac2b12f53537aec410fb281b2d2018e7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2153464941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc1780eb0af912d7a119ee60e6023f6144307adc2e84f2e8d8a3edd073f44d1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Sat, 19 Oct 2024 01:02:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 01:02:45 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Sat, 19 Oct 2024 01:03:26 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.12_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.12_7.msi ;     Write-Host ('Verifying sha256 (1e6df6b445d9e995e86fd8225c658df1411d3abab86b540ce4d2063c8a889835) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1e6df6b445d9e995e86fd8225c658df1411d3abab86b540ce4d2063c8a889835') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 19 Oct 2024 01:03:34 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Sat, 19 Oct 2024 01:03:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920acd27b52193b523b6a39105ccca8c4b1427cd29e65e26a8e0f19f540b431d`  
		Last Modified: Sat, 19 Oct 2024 01:03:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10db1e0907a15b50ff301ba9f56e3c37c727c362345ac3d7143e356a6fde9b06`  
		Last Modified: Sat, 19 Oct 2024 01:03:37 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7154b317c2bac1e0dc7a56be1d8c9dcf0288ce2055a95735f0c9e57ec9536ac2`  
		Last Modified: Sat, 19 Oct 2024 01:03:51 GMT  
		Size: 353.8 MB (353755584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0acae3ab4c50e09a1f26294323160e92f899e73bc60b79c0a75d063cb1af909`  
		Last Modified: Sat, 19 Oct 2024 01:03:37 GMT  
		Size: 364.0 KB (363954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5da843b962b9e801a86890fc7a5c0063faef6c915ea3fc8a67fa5e447275aa`  
		Last Modified: Sat, 19 Oct 2024 01:03:37 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:853a81ec467415e91d6f50ed2d9c54266584d3215be568bb0946f5db8fb75a3e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2259460292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4456e72ced61528cccf3a22392cc996417e054b76f7c116e71afeffcfa95870`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Sat, 19 Oct 2024 00:54:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 00:54:50 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Sat, 19 Oct 2024 00:56:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.12_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.12_7.msi ;     Write-Host ('Verifying sha256 (1e6df6b445d9e995e86fd8225c658df1411d3abab86b540ce4d2063c8a889835) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1e6df6b445d9e995e86fd8225c658df1411d3abab86b540ce4d2063c8a889835') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 19 Oct 2024 00:56:44 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Sat, 19 Oct 2024 00:56:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2d4494bc336551e741c53124554fc7fe8c347720c2a16d4ce081840e26d099`  
		Last Modified: Sat, 19 Oct 2024 00:56:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6aa06185d1782bd4a559a2755bfc03612067c1268bd3d365aa08b33cb18891`  
		Last Modified: Sat, 19 Oct 2024 00:56:49 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22663afed65a0c27b8f639cfc155e73928e76c78d0ca3a4d772c6d4b4d434a81`  
		Last Modified: Sat, 19 Oct 2024 00:57:03 GMT  
		Size: 353.8 MB (353781999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dfc6b2f42fef1adeff2fdb55c58a1eedac4e08f8a94ad065f3c130e3b97cae`  
		Last Modified: Sat, 19 Oct 2024 00:56:50 GMT  
		Size: 3.8 MB (3849148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffe50f6a619a986a4a2a40cd3c8a08e90e9dab75a51b0d99b1dfbad8bf98ba9`  
		Last Modified: Sat, 19 Oct 2024 00:56:49 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
