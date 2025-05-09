## `eclipse-temurin:11-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:beebf55f8665a475d751b770a0b5c72ac14245b6d97ed5f7207cb69828ea8f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:81555fae38cba4c584d89d8fefd74ce0f3fd7d70ddb7d06affac1816284d08a1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3470558490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b853309f664be0bc64955b3ebe5fb60b42e23b7b15fc6fa7dd8468c23469fd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Wed, 23 Apr 2025 16:37:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 23 Apr 2025 16:37:04 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 16:37:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.27_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.27_6.msi ;     Write-Host ('Verifying sha256 (08b8bcdf7f61f4276d90eccef6d70a4b73c25f0b4c2cdd2e6ddf15c24c087160) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '08b8bcdf7f61f4276d90eccef6d70a4b73c25f0b4c2cdd2e6ddf15c24c087160') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 23 Apr 2025 16:37:30 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4ad971ce706d0f4101ffed54b00c865cdb0d5de09076ec04b0a62b9c4e9e0b`  
		Last Modified: Fri, 09 May 2025 07:03:38 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf1a362c4788a9a1ebacfc35ae634ea4da4ba35750d4be2c13c92043b1be8f4`  
		Last Modified: Fri, 09 May 2025 07:03:37 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dec61b6f031a263c53c2f34561363160cfada07737fd84b02ab8b1ca6725f4`  
		Last Modified: Wed, 23 Apr 2025 16:37:42 GMT  
		Size: 75.0 MB (75006523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4ea13d988c5be80100a1ff20e6173fcb6e02b61018c7b7c798719ecde5dbd2`  
		Last Modified: Fri, 09 May 2025 07:03:38 GMT  
		Size: 387.8 KB (387849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:4ded91343b7280601925418c912fd87af97848ff5c51ff4c195d51ed13432b20
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348935917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1179f0efab8a302d87a86d06c661bd3cfc56a543acaa03f8b351d5a0031283b5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Wed, 23 Apr 2025 16:39:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 23 Apr 2025 16:39:16 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 16:39:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.27_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.27_6.msi ;     Write-Host ('Verifying sha256 (08b8bcdf7f61f4276d90eccef6d70a4b73c25f0b4c2cdd2e6ddf15c24c087160) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '08b8bcdf7f61f4276d90eccef6d70a4b73c25f0b4c2cdd2e6ddf15c24c087160') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 23 Apr 2025 16:39:40 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0839c717f914f8e1976bac117e194f5ca0bf09e2eea398da1f1b2f6f879388`  
		Last Modified: Fri, 09 May 2025 07:03:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a827573677c089718aded42af39b2d7c29d2c67ea289a85882415787f8db0d6`  
		Last Modified: Fri, 09 May 2025 07:03:38 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7c6b7ca14194b680f7b3e70de791c997ca2ec5007135d43c4871eebe186e2d`  
		Last Modified: Wed, 23 Apr 2025 16:39:49 GMT  
		Size: 75.0 MB (74981105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af07f81e2437b91cf597986ff0e53fbfedd5d808236f284747960fc3bc8ad48`  
		Last Modified: Fri, 09 May 2025 07:03:38 GMT  
		Size: 369.7 KB (369709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
