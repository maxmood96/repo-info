## `eclipse-temurin:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ba3230574b4f763dc03ddc9970a1b40f4c32877af071565ea5f4531ea5724d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:aa7d0fbc9f3838c0ce447d5e268ab772d06eb0035ba94be3a4c43969bb8b6682
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346331657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8df50e6e53c53f94bf624a59f03689fba60f4a898321c5fd797d9f329c50b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:55:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:55:52 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 09 Apr 2025 00:56:13 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (5e1e515f2625ab6c4bdc95a6a0f0928b3ace6034a60d811da3d701ebfaeaccf1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5e1e515f2625ab6c4bdc95a6a0f0928b3ace6034a60d811da3d701ebfaeaccf1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Apr 2025 00:56:19 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd085f38ac9f1f46301e45c3c38ff5a4bc7e4d6df84311537651d999b4588d6`  
		Last Modified: Wed, 09 Apr 2025 00:56:21 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e33b46ac3e8c83f4fb8b1cda7b1f3658a0c0d780ac27289d2c0db21bfc0db7`  
		Last Modified: Wed, 09 Apr 2025 00:56:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57653d3c475c15c9f1b2fab0d4c8dd1c02c6fd294ab05d22725fc0444e51fba0`  
		Last Modified: Wed, 09 Apr 2025 00:56:27 GMT  
		Size: 75.0 MB (74970690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb628b6eb6ac5ab8e08f0961aacb9b448f4a0adb8d5c23bed0847d371ec6a52`  
		Last Modified: Wed, 09 Apr 2025 00:56:21 GMT  
		Size: 362.7 KB (362702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
