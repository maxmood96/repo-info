## `eclipse-temurin:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:26a2cdfb39be256837c3e7838bd9903a2d7b3d2cffe5894e864aebe7a53048c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:2144de19ab7cdb56a9cf74868ac1ce580f96241e90a512c9e2f3638c6d058fc8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348941931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ae055332d6669e1a2a25a53371c87fb1becda5ab0f4dd475ffc0f1efb829a3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 20:58:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:58:44 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 14 May 2025 20:59:02 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.27_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.27_6.msi ;     Write-Host ('Verifying sha256 (08b8bcdf7f61f4276d90eccef6d70a4b73c25f0b4c2cdd2e6ddf15c24c087160) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '08b8bcdf7f61f4276d90eccef6d70a4b73c25f0b4c2cdd2e6ddf15c24c087160') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 May 2025 20:59:08 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48201add875b9799ba83cdf6730cf3f1d2b26c22f1ba7add8e0d2b79902264bb`  
		Last Modified: Fri, 16 May 2025 16:21:33 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48ca428a5a58034ed45d86684b6145b02f71e87c8595b3ee06f3dd214101f27`  
		Last Modified: Fri, 16 May 2025 16:21:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34b1c2833945c24244ed1d8cc8bd2bd16df2b42f53ba5a59b7ea2e8e3a00942`  
		Last Modified: Wed, 14 May 2025 20:59:17 GMT  
		Size: 75.0 MB (74962231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0242b0c3a12fd5ddbf3b471d079b06a25092b4530b22552010cfea2e7b770eb5`  
		Last Modified: Fri, 16 May 2025 16:21:33 GMT  
		Size: 349.0 KB (349009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
