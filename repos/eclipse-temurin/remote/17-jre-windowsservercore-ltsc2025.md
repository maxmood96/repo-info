## `eclipse-temurin:17-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:3a528751b7d32aa927112414dd5263c9dca4d328dcf76d9291cebb9b4c1bcab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:991fa87de417fc65002779b311e256dd9664ad4c81bc5297df8a240624fcad80
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3310901116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fcdd0d9d1ab5d8715cc1150606a8c27423a1b538f1ac3ae92128957c9503040`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:11:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:19:52 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 11 Nov 2025 19:20:09 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_windows_hotspot_17.0.17_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_windows_hotspot_17.0.17_10.msi ;     Write-Host ('Verifying sha256 (23eea3080b9545915b5af64807fd310ee7227688a179b33859530912cca4c1e6) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '23eea3080b9545915b5af64807fd310ee7227688a179b33859530912cca4c1e6') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 11 Nov 2025 19:20:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:a77d76091b7aac8a391dc15a412eec8b3ee40fe1bc86700413bb69bf1114e676`  
		Last Modified: Tue, 11 Nov 2025 19:22:17 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb67d123c391b44be0de25e1f6e959347c46d49938a872ee3d0cd1a05261574`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85ffca9737cfc3921f2f803b0719cfe2d9f007dfb171656f62a714b4a5dcbcb`  
		Last Modified: Tue, 11 Nov 2025 19:22:26 GMT  
		Size: 75.1 MB (75095554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a272c49a773012f6ec4f7366719505e45bd4e3fc751dc2842232b671afc871`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 347.2 KB (347175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
