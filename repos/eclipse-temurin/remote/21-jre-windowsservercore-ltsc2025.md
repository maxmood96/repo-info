## `eclipse-temurin:21-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a157dc6b6f50099dba3bbe13eafca7cd3bfc77b06e2664c070898fe722ff22f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `eclipse-temurin:21-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:b25805a24ef3d6f6c0d46e57996d700ab82977519d8c32d951d7383a1c233d84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2048870416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83772dd5c1a214a3fd67874efb10dc3c186a1dad578ec6a985a42c8e06ca6133`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:53:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:57:08 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 10 Feb 2026 22:57:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.10_7.msi ;     Write-Host ('Verifying sha256 (a841118d4959b6b6eb6156fa1f2487f112afaecd124b1eb5bba203d5556efd32) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a841118d4959b6b6eb6156fa1f2487f112afaecd124b1eb5bba203d5556efd32') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 22:57:26 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:8fcfd35fb91d5c96c95008501f15273667b38b3c34c813a77275adb8e4064973`  
		Last Modified: Tue, 10 Feb 2026 22:53:48 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c0002e492a9f398119dcec058d3c96202ba71d2a33bf709792203c4d0eeb7`  
		Last Modified: Tue, 10 Feb 2026 22:57:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879be3c9572e0ae773f30ccc66fc4acdf65ffcd6c1e81354f71f38e12e604ebd`  
		Last Modified: Tue, 10 Feb 2026 22:57:38 GMT  
		Size: 83.7 MB (83748015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525a69aede142149875099110834f10e893f0df4067cf9306d166492fa31829`  
		Last Modified: Tue, 10 Feb 2026 22:57:30 GMT  
		Size: 359.9 KB (359936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
