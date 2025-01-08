## `eclipse-temurin:17-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:2bbd95ba9cd697bd58936565e9fe0652b300c02d1988ff2b6e226455d1dd17b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:9eca6eda3e051efe4091affaba410a501e6e4844bb802b5c757b854d6a7630f6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330037554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b4bc7f8622aa2fee43bccc94f2c2c591193b8aa122d8be70549f74c78dfe78`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:39:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:58 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 11 Dec 2024 20:40:18 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_windows_hotspot_17.0.13_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_windows_hotspot_17.0.13_11.msi ;     Write-Host ('Verifying sha256 (457194f803be9129eaa2f0d50ac62bbd6182bf4923f91000199d936fa04e40e4) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '457194f803be9129eaa2f0d50ac62bbd6182bf4923f91000199d936fa04e40e4') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Dec 2024 20:40:24 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebffdc136d161bd88596a995e5979f64cbf3b56082bc2bcd8315d6c76684b477`  
		Last Modified: Wed, 11 Dec 2024 20:40:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2aa72413945803e5d43831af013076b9b55614b8e5508d1bec403e004f74a5`  
		Last Modified: Wed, 11 Dec 2024 20:40:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7c1e701c26b8436639dc3e90deba3a251c6aca1b3baabd3a0723efaef4e7f6`  
		Last Modified: Wed, 11 Dec 2024 20:40:32 GMT  
		Size: 75.8 MB (75801225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149088a3b80c650f6eb71e5d50d0d50efa4043e2a687faad730e1d9952b0ae8b`  
		Last Modified: Wed, 11 Dec 2024 20:40:26 GMT  
		Size: 360.1 KB (360129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
