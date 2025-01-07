## `eclipse-temurin:23-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:baba8bab4fca3dcc6db63ecd39429ad811181d5919494cc60a68b22cec39fa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `eclipse-temurin:23-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:76ae199fe17a259929ae1dab9ab2058a1e1cd59cbf9c548286466e8eb8a32f53
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338711737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea21105ac269890a209dd5997475db18c59af386fdf03437177dace019efad42`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:42:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:42:05 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 11 Dec 2024 20:42:24 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_windows_hotspot_23.0.1_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_windows_hotspot_23.0.1_11.msi ;     Write-Host ('Verifying sha256 (4d1d7324ec320cf3a4843f208975c28d4136e3b951bccbb9cead4b0a0017147f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4d1d7324ec320cf3a4843f208975c28d4136e3b951bccbb9cead4b0a0017147f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Dec 2024 20:42:31 GMT
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
	-	`sha256:0e0a7d07a79943987068570f0b6685817f54eaef0a1f671d313bc10c7fc6f94e`  
		Last Modified: Wed, 11 Dec 2024 20:42:33 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995d0fc1c79e056344d4c776241735b1b90938b9f0e593fb5d11335ce269160a`  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29647c38226e88ec6f2c6cd2686f723f5e454275fb2625969dd5965984e755f1`  
		Last Modified: Wed, 11 Dec 2024 20:42:39 GMT  
		Size: 84.5 MB (84493989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6b5cdea8072f130ad8757ab4b09b7f7fe3a50a65260260a93f63a78cbffe48`  
		Last Modified: Wed, 11 Dec 2024 20:42:33 GMT  
		Size: 341.5 KB (341523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
