## `eclipse-temurin:8-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:24a474aca772d4f0df2c31fcf4d0b2dabcc363713255d65462d264b8b6fe555f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:8-jdk-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull eclipse-temurin@sha256:52de6673b57a61ee4a8d6fb89a90762b03e56678bd1dd99fd53b92a56aeedbd3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2102591079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d900293d3c5fcb086a2fab38fb3c2a0ac76947ddf1a634a119805ac7d48084`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:36:26 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 14 Feb 2024 19:37:29 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u402b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u402b06.msi ;     Write-Host ('Verifying sha256 (ddfbd420322c634e8524720846f6b1eb02435cc77875e2d3af1ac3398784c797) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'ddfbd420322c634e8524720846f6b1eb02435cc77875e2d3af1ac3398784c797') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Feb 2024 19:37:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f61454a6c750ec71b397f851f890c98bdfbbf6b0b14dea13bf6494a6d63fb0a`  
		Last Modified: Thu, 15 Feb 2024 00:06:01 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05555bb7897bac053c9628839d16035801ca8c78dbb23d8db7b7bf3fbf7b7cc6`  
		Last Modified: Thu, 15 Feb 2024 00:06:17 GMT  
		Size: 191.6 MB (191644370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005a640eb7c16723c3ea9a4486cb42dcdb4cfd22225dbc271483633472be83da`  
		Last Modified: Thu, 15 Feb 2024 00:06:01 GMT  
		Size: 289.7 KB (289721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull eclipse-temurin@sha256:80e6fe8d7509ea7902f110460c2066dc5343ffc95209a24bf72f4f92e10f9c18
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2272405048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a63a5d0533786a82d6d829a74effe53edf2fa9f5d42528bfa38440883fce22a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:38:10 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 14 Feb 2024 19:40:16 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u402b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u402b06.msi ;     Write-Host ('Verifying sha256 (ddfbd420322c634e8524720846f6b1eb02435cc77875e2d3af1ac3398784c797) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'ddfbd420322c634e8524720846f6b1eb02435cc77875e2d3af1ac3398784c797') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Feb 2024 19:41:42 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c38eaa458272eff494ba83f63c247837c990738a8da80ab74a313128b1be86`  
		Last Modified: Thu, 15 Feb 2024 00:06:29 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db7ff3e825f1e3f584ed03fcd92d13ea4377df7d47243fcf7545cc393563bb8`  
		Last Modified: Thu, 15 Feb 2024 00:06:45 GMT  
		Size: 191.7 MB (191664084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77cc5bbfbed3f9f38c87e65dcec3617ca939062affb1496fb34d0e36fe936a3`  
		Last Modified: Thu, 15 Feb 2024 00:06:29 GMT  
		Size: 289.3 KB (289310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
