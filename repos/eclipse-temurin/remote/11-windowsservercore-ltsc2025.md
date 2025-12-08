## `eclipse-temurin:11-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:096f5ca9fe83d6176011e64d5d3ce6ee67b1368fc4355ae280c143a3c14ebe48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:07a0185b523b542ae2e29175f35b707e1735adf43b9877bd80bbeb67262d8893
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605240741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1754296c058b39518bb70305d5c61922fd3f500152ab7cdd4e4a6e562c575556`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:14:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:14:19 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 11 Nov 2025 19:14:54 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.29_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.29_7.msi ;     Write-Host ('Verifying sha256 (219e88a862ccdde521c42d8ebc001cc711279cdef79157b568ec2ae16b3abde0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '219e88a862ccdde521c42d8ebc001cc711279cdef79157b568ec2ae16b3abde0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 11 Nov 2025 19:15:00 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d9f20afaa0479efd53d3dc07c1cbe1a562514b126a793ae1d25e5f63a4af41`  
		Last Modified: Tue, 11 Nov 2025 19:26:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfccd102ac6859b5f3ef046843d1db3ebe852b13c172d34b978ffa0e0028d21c`  
		Last Modified: Tue, 11 Nov 2025 19:26:04 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abf0e6520949347c742869b990f661bab1fccbb6ef81ca598e207e61b00cab7`  
		Last Modified: Tue, 11 Nov 2025 20:10:43 GMT  
		Size: 369.4 MB (369439192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3a5587cdcb1988669f7c4b8c003edf9205aee7b001d07105ac869af04983a`  
		Last Modified: Tue, 11 Nov 2025 19:26:04 GMT  
		Size: 341.9 KB (341892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cce03d835661a8116063a584a20ce149a62f19425fed2a6d4d36474196b278`  
		Last Modified: Tue, 11 Nov 2025 19:26:04 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
