## `eclipse-temurin:24_36-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:2328c80a8d4f38b2a35377bc5d92d952a50e2dabd8b32afe7c282983a105d3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:24_36-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:35dba47656d2e23becce7b1c3ec75e47f62840e1239ebea5f28ba035ee35d29f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3008439196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b5ae0055dbd34593f6b7964c6dc49b838445b3661036cae4ac5ecf60970648`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 22:01:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 22:01:51 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 22:02:08 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 25 Mar 2025 22:02:14 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16d0bef5c889b065ba40e1d82efe689fd50ef51e0c0cf26e9b2515557c89f28`  
		Last Modified: Tue, 25 Mar 2025 22:02:18 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dbb2d07cc82bcd8a81781eb87a077c4c2872391bfbd974694768f18ab3636c`  
		Last Modified: Tue, 25 Mar 2025 22:02:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f293f5b512801ae230b2f0e5334427e3c3088b20205d0682f9278c291335c96`  
		Last Modified: Tue, 25 Mar 2025 22:02:27 GMT  
		Size: 99.4 MB (99385759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dc4579489605fe9e213fc9e398ea861f45138632920df8c39074be91cda8a5`  
		Last Modified: Tue, 25 Mar 2025 22:02:18 GMT  
		Size: 403.1 KB (403149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
