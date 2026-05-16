## `eclipse-temurin:26-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:7f6053dd352566d578a20e7a151165cbacb75ace30f74712f15579384039b928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `eclipse-temurin:26-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:2936504a330748742fc35e11a6397bf931a12d33fdd54d60b8ff9a6fefae5f99
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310296672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2955362ef3364eff6a1a7c83564d8209f56b1446005b85b3dfbf3734ba1c262d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 15 May 2026 21:05:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 21:05:15 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 21:06:45 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_windows_hotspot_26.0.1_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_windows_hotspot_26.0.1_8.msi ;     Write-Host ('Verifying sha256 (400bdf064a84e8cb47d442a054d8931fbfdf81a867ecb68c5b99541db32fabab) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '400bdf064a84e8cb47d442a054d8931fbfdf81a867ecb68c5b99541db32fabab') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-26' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 15 May 2026 21:06:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198ef1662db4a1a643804af5695215ee85c2c43a341e4ab12a398bed5a6fcba0`  
		Last Modified: Fri, 15 May 2026 21:06:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b599a8515b0d2ca3cb34a21fb3ca398613513514b9377f2614fee671283c7ca6`  
		Last Modified: Fri, 15 May 2026 21:06:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a38c5dbd495a714de4af0c77d2f54ed06c7d63a8e6cd1d8d91256592df4f6d7`  
		Last Modified: Fri, 15 May 2026 21:07:07 GMT  
		Size: 104.0 MB (103993172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be19f881357167cc00d7f6bd76d035573c36db33e1119b82b59949525e406bb`  
		Last Modified: Fri, 15 May 2026 21:06:58 GMT  
		Size: 359.0 KB (359034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
