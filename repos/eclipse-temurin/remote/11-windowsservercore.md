## `eclipse-temurin:11-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:d1a822959d2f7f5395f19cfc1c2ef5639d6223f138afaec2df2aadd75bb1e70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:020c4dda1098631f22bf6cfd8f95840f2dbe4c5df6153814a59c93a42919f260
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2871689426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4ba545b5d6968f95716fa1ac4dbb202b21f1c60c32d27618cea7d1c94bdf1d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 18:30:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 18:30:51 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 22 Jan 2025 18:31:23 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.25_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.25_9.msi ;     Write-Host ('Verifying sha256 (497d6959470a72c443bb0cfb1af5d0a11689bab8dbe4c21c29f55f453d81d860) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '497d6959470a72c443bb0cfb1af5d0a11689bab8dbe4c21c29f55f453d81d860') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 22 Jan 2025 18:31:32 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 22 Jan 2025 18:31:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd882d3e628943fbcbafd148b792ce7ea5caf60334b8ae72b97c29a5c4d736d`  
		Last Modified: Wed, 22 Jan 2025 18:31:35 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030c618988a6a6e3f34740170feecacb4d579ebb6c0a808cedd59a88d4075768`  
		Last Modified: Wed, 22 Jan 2025 18:31:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7c9ad444e63c29edbe7b169fb0c798d3c242d1b1cf80d0501612f135446f36`  
		Last Modified: Wed, 22 Jan 2025 18:31:52 GMT  
		Size: 371.0 MB (371007381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2299e01f8ed596bcbc5ac26010c41ab7091e84ad3301333252155e03460b2226`  
		Last Modified: Wed, 22 Jan 2025 18:31:35 GMT  
		Size: 400.5 KB (400539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fac486b0f38d884cde2cdd8181e926ac4e19b04aa49ca7e4f8cf6783ed19d7`  
		Last Modified: Wed, 22 Jan 2025 18:31:35 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:9c0b56ba3076e1ab0f8fcdd1b13e80fc6a84fd12f43dd7c4cf3fd830c2f69ba9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2633675738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d708ef0b9ec48615abba1ec6db79efd38ab11d8e944e1d4906e390f6e0a98807`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:31:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:31:33 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Tue, 14 Jan 2025 23:31:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.25_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.25_9.msi ;     Write-Host ('Verifying sha256 (497d6959470a72c443bb0cfb1af5d0a11689bab8dbe4c21c29f55f453d81d860) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '497d6959470a72c443bb0cfb1af5d0a11689bab8dbe4c21c29f55f453d81d860') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:32:06 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:32:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebfe4fd10a761005262a3d0eb6a5f699a4cdfa3de1924dc5346917fdd1508f9`  
		Last Modified: Tue, 14 Jan 2025 23:32:11 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6248c09dccf28e6ee14f6ac1ff830f51b5d7453fa8533325fe5eb2471c1db5`  
		Last Modified: Tue, 14 Jan 2025 23:32:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdad8c384b34881db4da6e1325ba09fa1f02bce9c16ca4e809e9f572c6befb3`  
		Last Modified: Tue, 14 Jan 2025 23:32:26 GMT  
		Size: 370.9 MB (370939539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22983adb50b81bd6611280e57411e8d062652c6eb1130766cfc4fd58fe41459`  
		Last Modified: Tue, 14 Jan 2025 23:32:11 GMT  
		Size: 347.1 KB (347088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4394b54a87cdc9590ddfa8d1c907c84b81c65ee15ad3118ebf22788797bfc0e5`  
		Last Modified: Tue, 14 Jan 2025 23:32:11 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:2467784ce6e34d77f325ef8f167410935c42b0643624a9556e99dabce1818ca5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2493497229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd57ca963ea62b4f5832c4fe2ccf9beabc3aa664d06221f6725ce3707e7e527`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:32:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:32:26 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Tue, 14 Jan 2025 23:33:22 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.25_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.25_9.msi ;     Write-Host ('Verifying sha256 (497d6959470a72c443bb0cfb1af5d0a11689bab8dbe4c21c29f55f453d81d860) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '497d6959470a72c443bb0cfb1af5d0a11689bab8dbe4c21c29f55f453d81d860') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:33:32 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:33:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176b52a8571c950a7bdabac53374fe632f1fa77b67ffbcc09d864b4cefae2acf`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77ad098e2b3f1aea589503c0589c2bc85bed9620a5f822e9e51dafad2309f63`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285e1f758361d11598f08e0e59187798c7ea50d695ea9a47d9f2769c3f3df97`  
		Last Modified: Tue, 14 Jan 2025 23:33:50 GMT  
		Size: 371.0 MB (370951030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c5902c03c4ec4d8530b495552dbbc52903e3ec8077424066d2da1fa665d9d0`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 330.1 KB (330116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9de76e1008e3633101ad6bfe26cce9f830a8edd466c40db1209a0206409d587`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
