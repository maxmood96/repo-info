## `eclipse-temurin:8-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:01018f518627c90611af1405d34ac3b3ebdfcceb036512698a693f2740dcbeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:8-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:0f017812a976985531189c7e9cb1abf111ecbe8fcb1243d7a68c258a954725a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3412077713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01fa95b180fe9892e5fa4a97f07def04ad9f92c7f4836eaac1ba018e65533dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Sat, 08 Nov 2025 18:08:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 08 Nov 2025 18:08:53 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 18:09:51 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u472b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u472b08.msi ;     Write-Host ('Verifying sha256 (810c04469e75c2f1cf83091e9dc78497b84e48ad21269291d9b7ff59b5cbb404) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '810c04469e75c2f1cf83091e9dc78497b84e48ad21269291d9b7ff59b5cbb404') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 08 Nov 2025 18:09:58 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61723912e6b6d35fcf918f706a6a5fe816bc8b309a86b75f7a41639f866cc32`  
		Last Modified: Sat, 08 Nov 2025 18:20:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd44312aead36992a616488203d245190e0ce055b14cada6d9203516b8f80d`  
		Last Modified: Sat, 08 Nov 2025 18:20:07 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adb8ada2026226dd38cb1f2af2a95b07edfc9ea19a6c3f1e44d2d78b2eca337`  
		Last Modified: Sat, 08 Nov 2025 19:16:57 GMT  
		Size: 191.3 MB (191337998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc249d9670bcb31e157463a7793ad22d9ddcf5ce5b2230983352ebd2b68d900f`  
		Last Modified: Sat, 08 Nov 2025 18:20:07 GMT  
		Size: 390.1 KB (390120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
