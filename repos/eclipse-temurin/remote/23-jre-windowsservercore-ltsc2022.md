## `eclipse-temurin:23-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:29e5ec398f9176bdf9dca4a6040ae994519d082d1f80c286760086e910bd256f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `eclipse-temurin:23-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:67d2522b0da885b286e7e4509ca1fffb2b60d3dcbb821f7fe71ec3a577d83321
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1546623427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ceac92bcf3e7bb752c6144c1d53e85ebae491ba50565b8321c96f7dcd473e16`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:35:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Sep 2024 21:17:40 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 21:22:16 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 18 Sep 2024 21:22:38 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0ff9a79ca5aec0b3e3be0c49c873a237847a9d74342acad1818e3f10647107`  
		Last Modified: Wed, 11 Sep 2024 01:13:29 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e7842774e6f3b7aa5d5da5f10556d5ee58d2ed3bcbaf492d583620158d1f45`  
		Last Modified: Wed, 18 Sep 2024 21:27:11 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd4000708c52382caea0488cc0083bd49cd714e3b94aaedef06cef6c3c1f59d`  
		Last Modified: Wed, 18 Sep 2024 21:28:40 GMT  
		Size: 84.1 MB (84149353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b826d21b0c8c196c18cee6b8e93ec8589bb2d8081c467832cca025b1e44a8b2`  
		Last Modified: Wed, 18 Sep 2024 21:28:30 GMT  
		Size: 278.9 KB (278853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
