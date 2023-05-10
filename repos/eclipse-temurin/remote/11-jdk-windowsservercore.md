## `eclipse-temurin:11-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:e61bcb715da966d02d44fe74d5d27d674b6df943202645d1934179ead894c163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `eclipse-temurin:11-jdk-windowsservercore` - windows version 10.0.20348.1726; amd64

```console
$ docker pull eclipse-temurin@sha256:1d4c91fbba003120b9dccb089072730e3bd5d8ec1dc23a312fbbd46d42d9c355
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2142415357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08140bfeb0c9781a9e19286fba1b9ab68f87df93de3e19bda1ca8f51fb46b29a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 00:44:54 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Wed, 10 May 2023 00:45:55 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.19_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.19_7.msi ;     Write-Host ('Verifying sha256 (8f8f136e2071591c6ea7bc58d629a5c8ad23c829bb1878200fdff0c0fe97712c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8f8f136e2071591c6ea7bc58d629a5c8ad23c829bb1878200fdff0c0fe97712c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 May 2023 00:46:18 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 May 2023 00:46:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77130a94ac7b52f6637a988477a9b68d93ee8e3999f5f6a70d1b63470bc9264`  
		Last Modified: Wed, 10 May 2023 06:56:24 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6301e8e4fe6d7b9cb3a9ffbdfddf18b531206a35ed335c3bd824a91c33b91df3`  
		Last Modified: Wed, 10 May 2023 06:56:48 GMT  
		Size: 367.2 MB (367164391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc81b932b6a2cbf96b60413a245b36b5fd36baa8791eae26af484fcc69db941`  
		Last Modified: Wed, 10 May 2023 06:56:24 GMT  
		Size: 265.2 KB (265206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c823f42ddb0f99d7826cbe01447146f02593718be769a971f15b3f80cbfdcdc9`  
		Last Modified: Wed, 10 May 2023 06:56:24 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull eclipse-temurin@sha256:f8ed81f616940e0fd3ef07b9e300b6f8216d07cbee2967f7a8fa0b603675b698
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2439473329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43e45c323b74bf1add48e1fb0176192a00551f9875181ec6bcf0c3c44ce7829`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 00:46:36 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Wed, 10 May 2023 00:48:17 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.19_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.19_7.msi ;     Write-Host ('Verifying sha256 (8f8f136e2071591c6ea7bc58d629a5c8ad23c829bb1878200fdff0c0fe97712c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8f8f136e2071591c6ea7bc58d629a5c8ad23c829bb1878200fdff0c0fe97712c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 May 2023 00:49:27 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 May 2023 00:49:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9f2c4564fc1aeccc35bea75e9c7cd9f59117883e76d5ea270544caa6e17e34`  
		Last Modified: Wed, 10 May 2023 06:56:58 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9472b43040b5e17cf6c41de64428c03f120bdfeb7cdc70a026c69c15b99f6353`  
		Last Modified: Wed, 10 May 2023 06:57:23 GMT  
		Size: 367.2 MB (367180434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7d4a1222b2c3d41b95d1d2fae524aefdada3c35048e34e25bccb3fb96dff1d`  
		Last Modified: Wed, 10 May 2023 06:56:59 GMT  
		Size: 253.4 KB (253435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4bd4e548db05797036352212b13b76e2dde5424cf14316a43dff90fed1c733`  
		Last Modified: Wed, 10 May 2023 06:56:58 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
