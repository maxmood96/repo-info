## `eclipse-temurin:19-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b7fc1c0e53bb149b81d28dd07cdb3f90ea36821d99adef8fd3bc6404333fcdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1366; amd64

### `eclipse-temurin:19-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1366; amd64

```console
$ docker pull eclipse-temurin@sha256:168fc9531b786bf3746120a9ae60a420114def11c3b7ecca1de4abd6bfdec231
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574018334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afa551df3bb5644f89ba54e3b2e611e45152f065c7c7abad4278669c22ebddc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 09 Dec 2022 09:36:47 GMT
RUN Install update 10.0.20348.1366
# Tue, 13 Dec 2022 22:45:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Dec 2022 23:28:35 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 13 Dec 2022 23:37:39 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_x64_windows_hotspot_19.0.1_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_x64_windows_hotspot_19.0.1_10.msi ;     Write-Host ('Verifying sha256 (9674e91db19657c2f4dbabde78bb78be1d9d3b3deaee53f3400a3653449f08d5) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9674e91db19657c2f4dbabde78bb78be1d9d3b3deaee53f3400a3653449f08d5') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Dec 2022 23:38:12 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfa20ce142ecceb471dc070d9582fff942cef447b7c8ff22f2223ffe3737c99`  
		Last Modified: Tue, 13 Dec 2022 23:54:14 GMT  
		Size: 1.0 GB (1021665190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb8b9a4ec3ca516cfaa44f64e80b1e3aaecdbde870177411ff046f81f991dd2`  
		Last Modified: Tue, 13 Dec 2022 23:51:33 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94f8244fa8c8df1bbbdb6ce7a67be818dbd50d8f133c10019011090d360b4c8`  
		Last Modified: Wed, 14 Dec 2022 00:04:33 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408e81b63b91bd20f5ba885b73c9723a045891b6dc285451f804166c1e7fc08b`  
		Last Modified: Wed, 14 Dec 2022 00:06:52 GMT  
		Size: 77.8 MB (77825871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825948c0b79e99491381e5c36a35c92f07cf8b52bad7963b2b1fb4f485f69d04`  
		Last Modified: Wed, 14 Dec 2022 00:06:40 GMT  
		Size: 526.8 KB (526787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
