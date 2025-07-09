## `eclipse-temurin:17-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:eae74f23429f2fbba10141345102a2503e16d3ea2d38a60bd2be49e7638c88fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:6d8f1fb280e28417fa71eda3a71221afa4fcb2c47402fe482c0629f26500ffd9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3566704999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f190c8f1fe6829f154349be6b419181354213f46784aca021777435cd880877`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:09:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:34 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 09 Jul 2025 18:09:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_windows_hotspot_17.0.15_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_windows_hotspot_17.0.15_6.msi ;     Write-Host ('Verifying sha256 (d89bf8a260d26ed7603ec1e79b43c1297cafd9d6b184a68646c54409285d6c2f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd89bf8a260d26ed7603ec1e79b43c1297cafd9d6b184a68646c54409285d6c2f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:10:02 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f82090e640f8926fdff3411fac3f4328c96fa24c6655a215ce7fff534ae214f`  
		Last Modified: Wed, 09 Jul 2025 19:10:00 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90a3ca5c58f8b7e4fcea894e6847cb3f5723c7cac8618c04f43c4bc04348dcd`  
		Last Modified: Wed, 09 Jul 2025 19:10:01 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61d2dbf7502b9bf19346550b38019d87236c3616a90f7bbe381df4fd4edb7fe`  
		Last Modified: Wed, 09 Jul 2025 19:10:05 GMT  
		Size: 75.1 MB (75142792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b4833ec4e27aa735a745cae143d0aed3c75e7a5f02f49037e3e84d01ed59fc`  
		Last Modified: Wed, 09 Jul 2025 19:10:06 GMT  
		Size: 386.2 KB (386157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
