## `eclipse-temurin:21-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:5ffe91d58c9dc93804f88560651acd5f8edfc695473db60c02fe18a62ba32fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `eclipse-temurin:21-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:eceb0146f44de7d0dd633c5d5842d9ba72016be16735cfebb9bfdc3c15748d49
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345934020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c4b64125ecd384359c0da11235b5d8fdf4e91947a4aaffd380b76e432cc730`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:51:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:56:09 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 10 Feb 2026 22:56:33 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.10_7.msi ;     Write-Host ('Verifying sha256 (6be8643444ec20758a34ddb1231e998ac77e72f661a0d5525a8ac3e078bcbcb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6be8643444ec20758a34ddb1231e998ac77e72f661a0d5525a8ac3e078bcbcb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 22:56:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 10 Feb 2026 22:56:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f3641b48551abf691e707ba76f8b07a225d509249237749ad0c13cbcab89a6`  
		Last Modified: Tue, 10 Feb 2026 22:52:23 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2388ea5a7a532c33eeb6c2932133b551323b09c80110344f566c22b8f14732ad`  
		Last Modified: Tue, 10 Feb 2026 22:56:43 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242644399d8a9503a599581725f82ba0376eaebe383ad2e607712993d3061f2d`  
		Last Modified: Tue, 10 Feb 2026 22:57:03 GMT  
		Size: 380.8 MB (380801270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e9ff3d58fb788e65b992a920c9cdf820c91c4ac7c00df34be65d14059e58d3`  
		Last Modified: Tue, 10 Feb 2026 22:56:43 GMT  
		Size: 368.9 KB (368941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20daef0944e5d2c88ac01b9fa5e4dbe5dc680ec9976692216b709be64079e18b`  
		Last Modified: Tue, 10 Feb 2026 22:56:43 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
