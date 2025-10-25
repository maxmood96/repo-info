## `eclipse-temurin:8-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d0ba130c5550c79dfca5e66a042d21876def5e29050b97a62906ba329de0577a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:8-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:f64d782f4f4992dfd7cad6bf0dfa41fe1c9cf7ee778de54b657bd010d9ce3723
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1650323049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba149c0ff4b2ef9fc75c4c036a2459f62c94c557517e796f9377b14b4bb6a64`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:04 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 24 Oct 2025 18:21:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ;     Write-Host ('Verifying sha256 (22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:21:35 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d53d3c20763f23480e45b67c6e6490bb19168bccc0dc0d6f3fdaebe72bdac8e`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910efe1ed5e5177522beb8ebbf0333b034d7f21966a4617f3f1e254ff4bf9bb6`  
		Last Modified: Fri, 24 Oct 2025 18:21:52 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96df73fbfd4f2b3272eadd9420a645cf746394cf3f28db03ac7de22f25d10df`  
		Last Modified: Fri, 24 Oct 2025 18:22:02 GMT  
		Size: 72.8 MB (72774834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc61366838047d375abeb5ab47b8dfa09e2d57995f95f2c951b1c0ca47b3398`  
		Last Modified: Fri, 24 Oct 2025 18:21:52 GMT  
		Size: 352.7 KB (352656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
