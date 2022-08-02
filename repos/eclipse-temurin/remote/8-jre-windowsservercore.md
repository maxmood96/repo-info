## `eclipse-temurin:8-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:bed8cd03f85ba80ff833a5dcdf2c89c0979a82a7227a250403cce54a6f732f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:8-jre-windowsservercore` - windows version 10.0.20348.825; amd64

```console
$ docker pull eclipse-temurin@sha256:3d4d32df10d33836dca155ddbb4bc1b4c3ae6e82fe0c812b6b5fb107319d4a8b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2372069263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb3c9808902f920da54d67543e8c918ed2deb6e444dd64432dbc14901a417ef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Aug 2022 18:16:17 GMT
ENV JAVA_VERSION=jdk8u342-b07.1
# Tue, 02 Aug 2022 18:22:25 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07.1/OpenJDK8U-jre_x64_windows_hotspot_8u342b07.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07.1/OpenJDK8U-jre_x64_windows_hotspot_8u342b07.msi ;     Write-Host ('Verifying sha256 (70e90ac93841ae85a966fb404343f89bf6518eac1e892eda5100da4d4433a95e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '70e90ac93841ae85a966fb404343f89bf6518eac1e892eda5100da4d4433a95e') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 02 Aug 2022 18:22:45 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da18b9f2fed96ac9c619df2e3c5b9f7843c52d1032f49f54f452f3cb3ece7d18`  
		Last Modified: Tue, 02 Aug 2022 18:41:47 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5899d1d1c3f92081459266672b4ce6a46776062155874b819d1249f5291e7a5`  
		Last Modified: Tue, 02 Aug 2022 18:43:18 GMT  
		Size: 71.3 MB (71263306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c409208a547dacdee8c71e25b275f8494988238d16bdc5d47b6a1db0e0460ce8`  
		Last Modified: Tue, 02 Aug 2022 18:43:09 GMT  
		Size: 571.6 KB (571584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull eclipse-temurin@sha256:6337e9d2c4e60495dd549d4f50b43a474ba5b1cd8a12d58269d5338be709196b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2743402215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b948020b57b5c378364f1a9360004233e573ff2f7e2f8b09e8251e7808a45e0e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Aug 2022 18:18:00 GMT
ENV JAVA_VERSION=jdk8u342-b07.1
# Tue, 02 Aug 2022 18:24:05 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07.1/OpenJDK8U-jre_x64_windows_hotspot_8u342b07.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07.1/OpenJDK8U-jre_x64_windows_hotspot_8u342b07.msi ;     Write-Host ('Verifying sha256 (70e90ac93841ae85a966fb404343f89bf6518eac1e892eda5100da4d4433a95e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '70e90ac93841ae85a966fb404343f89bf6518eac1e892eda5100da4d4433a95e') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 02 Aug 2022 18:25:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92297cee9eff9d29a76894f6eb33574fc2d54f50a15d5768d85234919e6a82f5`  
		Last Modified: Tue, 02 Aug 2022 18:42:16 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed142b5a323ab6596622cce0b7f298421aee66cfa37a1b9d6badbfc898e773`  
		Last Modified: Tue, 02 Aug 2022 18:43:35 GMT  
		Size: 71.0 MB (71010878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859c961707b4cae06b63c767835fa42726e88989dc5c169a556fbd5486a91abb`  
		Last Modified: Tue, 02 Aug 2022 18:43:28 GMT  
		Size: 344.7 KB (344743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
