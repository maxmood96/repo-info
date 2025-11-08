## `eclipse-temurin:21-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:c4fb6ca14d733494c7dedc5ed1a93839f5d44188df6b48d71c57778f15056b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:814fe7a0ac104621d49af37c7aba53861db14f4d45b00f14665bec0de6f530da
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3601473077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fc1af6831ae82c2913a270466c6dc59870902cd0c20921063dbd04cefeba63`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Sat, 08 Nov 2025 18:11:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 08 Nov 2025 18:11:19 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:12:04 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_windows_hotspot_21.0.9_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_windows_hotspot_21.0.9_10.msi ;     Write-Host ('Verifying sha256 (e97f44c7915866c3127565a91373d03adb639916186b24fc5e0f818a3bde8d3f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e97f44c7915866c3127565a91373d03adb639916186b24fc5e0f818a3bde8d3f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 08 Nov 2025 18:12:12 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Sat, 08 Nov 2025 18:12:12 GMT
CMD ["jshell"]
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
	-	`sha256:d09a73463b24c4494c284913dd066b5af115e70d3b8f8634d98d16d41172396c`  
		Last Modified: Sat, 08 Nov 2025 18:20:18 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56b076aa0494d204c8d0f70c79e6e7352920f1de429de21be95fc7faf06540d`  
		Last Modified: Sat, 08 Nov 2025 18:20:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c559bceb73b2434811548080e5c912b593cdbb4b88d91f77ecdb6dac827c52c`  
		Last Modified: Sat, 08 Nov 2025 19:18:29 GMT  
		Size: 380.7 MB (380746914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7d7221cd58878d91ff3645bc6d285cc0111cffeb8951dad3687aa19965d67f`  
		Last Modified: Sat, 08 Nov 2025 18:20:18 GMT  
		Size: 375.3 KB (375262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d945d1ba1116c264b0ee1914cd8dd80db7e6e682ebcc50d8ef0c17ffc9270c`  
		Last Modified: Sat, 08 Nov 2025 18:20:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:a574d8d6391d0c2d5be477be98287798c27f7ffc510f7d64dbbd225ee62c0700
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958431183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a24ecb12f41ce61e67c7e198197925e6a6144e7e0c150b650a3d05304f9896`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Sat, 08 Nov 2025 17:50:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 08 Nov 2025 18:09:59 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:10:30 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_windows_hotspot_21.0.9_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_windows_hotspot_21.0.9_10.msi ;     Write-Host ('Verifying sha256 (e97f44c7915866c3127565a91373d03adb639916186b24fc5e0f818a3bde8d3f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e97f44c7915866c3127565a91373d03adb639916186b24fc5e0f818a3bde8d3f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 08 Nov 2025 18:10:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Sat, 08 Nov 2025 18:10:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e9059525ffdb388ecb5e55bce62b363c192756a62a419a4006c0933aca5393`  
		Last Modified: Sat, 08 Nov 2025 17:59:27 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7001b56dcb6767b09558691944b6000946c04ddb0f6d0345fa9cf7d7c16109`  
		Last Modified: Sat, 08 Nov 2025 18:11:10 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc183cbc6dd6ef2b56b0fb748bbb55634544f8da223d270fffff1dc171ea12`  
		Last Modified: Sat, 08 Nov 2025 19:18:57 GMT  
		Size: 380.9 MB (380867770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6a93d14c3f4345c6e75b55ae367172ce4f19650f9d8dc9138fcfa5fb14978c`  
		Last Modified: Sat, 08 Nov 2025 18:11:10 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15547c0e458677b68aac1b7ac34d56e76c197534a35fc1676e074fbf3ca2b938`  
		Last Modified: Sat, 08 Nov 2025 18:11:10 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
