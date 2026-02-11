## `eclipse-temurin:8u482-b08-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:713628aa73709d490ded08f39b36056e613f2d64219e6529713e092d8906b5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `eclipse-temurin:8u482-b08-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:fe56007212a49507c66c67f0d463293cf2ebb5a9431ffc56d5155089cc4c0855
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2155812998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db076a4541bc0c48f2f96caa2543c71bf09bea4cb89945baf793869fb3f84cd3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:53:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:53:16 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Feb 2026 22:53:38 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u482b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u482b08.msi ;     Write-Host ('Verifying sha256 (f2c978b763c06a1e337918453e2ef1ab1a93a97fe41700c10979b348a7c3f475) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f2c978b763c06a1e337918453e2ef1ab1a93a97fe41700c10979b348a7c3f475') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 22:53:45 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:c3ebde3c20a30d0a7e244d6ad5a9fdd16b51d9c1eeb80e49dcb2ea2da6340dff`  
		Last Modified: Tue, 10 Feb 2026 22:53:49 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2c85eb7e693d6ed8b1593d0fda8617777ff9d05c1c6612e08f04157014cbb1`  
		Last Modified: Tue, 10 Feb 2026 22:53:49 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b779376e9c03959e9254e3cbb436728a912b53e3e994f57641614a6b622b495a`  
		Last Modified: Tue, 10 Feb 2026 22:54:00 GMT  
		Size: 190.7 MB (190703156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4652c01c3f29f1c6a332e05185c55c523e7247ebf2c1404eb96a5826e4e439a7`  
		Last Modified: Tue, 10 Feb 2026 22:53:49 GMT  
		Size: 347.3 KB (347299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
