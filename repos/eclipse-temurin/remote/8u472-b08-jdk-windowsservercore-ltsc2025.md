## `eclipse-temurin:8u472-b08-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:971aa27f1e6c7729e81880189356456dae1e14126d38c4123b5e8609cb1b18bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `eclipse-temurin:8u472-b08-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:bb9cba0249d20ae4fcf80a9a1335bbb760cc871e8ddd3b64f77d95576a4f55e9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3427074431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f787ee2be1a2772fc980b9b85f3ac71937103fc793c87d7293d01f694b28060b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:23 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 11 Nov 2025 19:13:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u472b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u472b08.msi ;     Write-Host ('Verifying sha256 (810c04469e75c2f1cf83091e9dc78497b84e48ad21269291d9b7ff59b5cbb404) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '810c04469e75c2f1cf83091e9dc78497b84e48ad21269291d9b7ff59b5cbb404') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 11 Nov 2025 19:13:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:9ef403ccf6a06c5d6bccd87b689e94f0a23d74b0c4458a3fc098e12f03e64f20`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fd0943a70b7fc3c7d52bb3604fa4bd47f76075756bcb4e1b22098ff5099ccb`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47da12599df1ab8cb2a9144ca604601a418df5c25db08b3df498e64f2c45946e`  
		Last Modified: Tue, 11 Nov 2025 20:10:50 GMT  
		Size: 191.3 MB (191275700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d60407d1d92635c4e5a623e2d3ef4dc93f790809ca3d3eb2fe38b810eb8b3e9`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 340.4 KB (340351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
