## `eclipse-temurin:24_36-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:19a5f8c0c345e82ea0ed09e404b94b579de1febb41b8117e134438d5cbc486ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `eclipse-temurin:24_36-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:d7bd6ce49318dd0a0d1955ab7d074b0c0834d379dc64afa6237539d9a36bcac6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370699793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d209c616429048f16eaed4b200edf6103246181dbcf3ea51426461cea9704d5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:49:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:49:53 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 00:50:15 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Apr 2025 00:50:21 GMT
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
	-	`sha256:201c2d3fac5c5e25dedc60d804d7cabc5dab2917078afddd6f50dfa1f2e1e3fd`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c00d78da401918570957faf19ed0067d804135119c33e8623f2d324f1988fc0`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf7e92f8088ec16f4e66d7fcc5ee3014b44ffd57119422124bd8180dca8964f`  
		Last Modified: Wed, 09 Apr 2025 00:50:32 GMT  
		Size: 99.3 MB (99342358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2196833f4f4277f0bfa23aca319daea69e6f20c00e3c0368a028665ebc51e388`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 359.1 KB (359140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
