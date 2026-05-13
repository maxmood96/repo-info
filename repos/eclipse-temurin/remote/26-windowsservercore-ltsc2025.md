## `eclipse-temurin:26-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:b773423cbb5f3b0d98a6c01c3b2139401077de95ad36c053cf5c88e10902cd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `eclipse-temurin:26-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:e7a35b7ca70afca84c3b83abf6d1abaaf0ec60e8073eed14187e4e6aa74f7154
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2466105743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee61cbd5b1627250289380af7c11aab1bc74d5944ce4763a63525318a62140ee`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:38:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:46:32 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 12 May 2026 23:47:08 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_windows_hotspot_26_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_windows_hotspot_26_35.msi ;     Write-Host ('Verifying sha256 (d69a60a2b0f9193303590c8f5bb58ae259117bfff6c8435930127e6010c4cf3a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd69a60a2b0f9193303590c8f5bb58ae259117bfff6c8435930127e6010c4cf3a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-26' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 May 2026 23:47:14 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 12 May 2026 23:47:15 GMT
CMD ["jshell"]
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
	-	`sha256:ba4dd54f79cbefa3530b8e98b6bb6c3e632e539c28a48c5857c0af8bbb8f7bb6`  
		Last Modified: Tue, 12 May 2026 23:40:24 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04666075c073f191689c48ed223dfebd89a75d19e3f47de5725f15541c2b4f27`  
		Last Modified: Tue, 12 May 2026 23:47:19 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b251fd4af61011a01af5ca22d349d10d7ad053d6658588606c2210f86ad4fd`  
		Last Modified: Tue, 12 May 2026 23:47:36 GMT  
		Size: 259.8 MB (259786909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb3ca35eb9f510702664b31306e2689bf9bc1ddb269d4b930425c89e96b6071`  
		Last Modified: Tue, 12 May 2026 23:47:19 GMT  
		Size: 372.9 KB (372942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec963b4984ff43d5d05c6f229b616768cef68f3e7a8a7ad1bbedb7c5f32c254b`  
		Last Modified: Tue, 12 May 2026 23:47:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
