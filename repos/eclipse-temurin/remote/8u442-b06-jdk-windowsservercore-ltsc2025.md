## `eclipse-temurin:8u442-b06-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:63ebe69ed17dd2afce273c1c2300872968f13bb0ec90a56bf45929e5a564b410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:8u442-b06-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:21a6974f19bfe2c01771be407fa64b6c4a42507086a4b47c89a1ef8958dcf4c5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3586455442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b836776310e3553e6b5ed7cc078458e615cbb3cabf8be529a1ee8e2016d53f6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:47:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:48:00 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 09 Apr 2025 00:48:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Apr 2025 00:48:27 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d389909ccb0544d95d7b01aa79f975762a0adc8875f40ccb7d29f05e78c81d4`  
		Last Modified: Wed, 09 Apr 2025 00:48:31 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489df0ee8bfb757bf62a1c3dc76c10fa88608c8f82167e5af2b339227c8381ac`  
		Last Modified: Wed, 09 Apr 2025 00:48:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b976afcaf8129c4d277a10148e22446a01831803f16c08be382c58385eb5c5`  
		Last Modified: Wed, 09 Apr 2025 00:48:41 GMT  
		Size: 191.4 MB (191392553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b06c0d60ac7a2f8bb7b6a3e0fc6d48afd6e92f23feec65962ae7bca96eeb99`  
		Last Modified: Wed, 09 Apr 2025 00:48:32 GMT  
		Size: 380.8 KB (380807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
