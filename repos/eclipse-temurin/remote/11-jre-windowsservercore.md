## `eclipse-temurin:11-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:45e0b2aa4fde9a0cb9470a320c5c9c71f2fdafdef5e49a495818af9d865e4dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:0fac85e34e358d9e8440fcf1582dc7c334a32d392193dab1c072c730520344ef
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2193084028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7b4e6aed2de0d40355872caec32cddac41d906d862acee2a90cad201a29eda`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 17:36:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 17:46:19 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 12 Jun 2024 17:52:25 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.23_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.23_9.msi ;     Write-Host ('Verifying sha256 (6699a78e61c0d8208a6d43a3b4590fbabf77bb1c1b8b30d8140e62804fa286cb) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6699a78e61c0d8208a6d43a3b4590fbabf77bb1c1b8b30d8140e62804fa286cb') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Jun 2024 17:52:46 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045fa3135d89819dc64e63c6fd4e832a9b86fc2d37e11e64d811218c4a684924`  
		Last Modified: Wed, 12 Jun 2024 18:36:56 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a0aae7d2a042c66ad7298f6fea8fe9711ecda4223a6f37b3b73b61ae81e8d`  
		Last Modified: Wed, 12 Jun 2024 18:42:07 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e2e4edf93e38c57196bfb7d4d73a95995f3e0df616748dea0e001f65424cda`  
		Last Modified: Wed, 12 Jun 2024 18:44:01 GMT  
		Size: 74.6 MB (74624597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e26049ce3dd1fe7f579754ce68956eb1ae546a96a7a6a15ee3f217d0f839c6`  
		Last Modified: Wed, 12 Jun 2024 18:43:52 GMT  
		Size: 277.9 KB (277882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:ca9e591852f4cbae9eb202ed1ce74bf89d327aa53ec02a48da2076734c9bde05
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2295699047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87005d5c63869f1833ada848f2507b418842e608ff907dd7196735e16343af40`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 17:37:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 17:47:48 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 12 Jun 2024 17:54:30 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.23_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.23_9.msi ;     Write-Host ('Verifying sha256 (6699a78e61c0d8208a6d43a3b4590fbabf77bb1c1b8b30d8140e62804fa286cb) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6699a78e61c0d8208a6d43a3b4590fbabf77bb1c1b8b30d8140e62804fa286cb') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Jun 2024 17:55:41 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04390472505d81fa325a5cfd00620c5caa18dd222dd0a98f7a089b8c65b438b`  
		Last Modified: Wed, 12 Jun 2024 18:39:01 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bea0a37774d14a59cef4e018c3eb3bcb0a93eeaa42e6f39ec07ff6394d2a605`  
		Last Modified: Wed, 12 Jun 2024 18:42:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf1a7d646df4aeefcd55c003161d01f4dd90f995267e923807955ccbcb82a02`  
		Last Modified: Wed, 12 Jun 2024 18:44:19 GMT  
		Size: 74.8 MB (74758904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5952aaa3ca841d562a032b0b117307251b0a0e0ab339f5fb38205bcae5f73227`  
		Last Modified: Wed, 12 Jun 2024 18:44:10 GMT  
		Size: 256.3 KB (256258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
