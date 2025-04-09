## `eclipse-temurin:24_36-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:06ae7ac8908e16e75e1dd76d07ae034b31d4c4f727d46dcb731bac3c833a09c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:24_36-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:44ceb30a36e3d2f5501af930738ab372e4ef358cd640a6307d881a613f6a01d6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3494414377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d886224c4975026fdef7d1c3da961d119cef2f4ec5b37b52d00b1669430eb1a0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:44:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:44:15 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 00:44:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Apr 2025 00:44:40 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd4124b95c0013563f2a51bfe1e2b164722c31b03e4d0ab1647fef3311d3f8`  
		Last Modified: Wed, 09 Apr 2025 00:44:45 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1ab3da87cfda678056923d48457eec1261b9b755bdb333ea8b8f3accad4902`  
		Last Modified: Wed, 09 Apr 2025 00:44:45 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea46d46be23b1e594169e4a3f69b8ed7133647f72d35e798f68bcca65d78f334`  
		Last Modified: Wed, 09 Apr 2025 00:44:54 GMT  
		Size: 99.4 MB (99359573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44556a554244cc2de6246eba4f9595b03e9c5af44818fb39df3ca05e7254f876`  
		Last Modified: Wed, 09 Apr 2025 00:44:45 GMT  
		Size: 372.7 KB (372719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
