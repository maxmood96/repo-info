## `eclipse-temurin:25_36-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3490cc2d1c4d83f137227fc34fa5eb4bbf1e58bebd4efa7a0e63f1e8cf219e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:25_36-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:bf196e69eb0787be551d9d777658a84515d352cc128cf8ef51c4b9aaeb9427bc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1590303681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b499810e3f73c296f1d657c2c48dbc94d2f73f62c0b52d1b7cca9ef6d82fd140`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:48:02 GMT
ENV JAVA_VERSION=jdk-25+36
# Tue, 14 Oct 2025 20:48:16 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_windows_hotspot_25_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_windows_hotspot_25_36.msi ;     Write-Host ('Verifying sha256 (eeae2fb19dc8d778a324d9b5c879f7afe9732487516807b75584436b01e0d8c3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'eeae2fb19dc8d778a324d9b5c879f7afe9732487516807b75584436b01e0d8c3') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Oct 2025 20:48:22 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18660e3121d32e68a28ed63416232bd4de1cd875288b92ddf39b7185353f3ce5`  
		Last Modified: Tue, 14 Oct 2025 20:47:11 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfded8789a7403adec036f150bafe5e8fa56e55c6477747573132a948cad8040`  
		Last Modified: Tue, 14 Oct 2025 20:48:43 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1608e56f452c076adc3cd2a1d2252de50ef7b6a78258cf84f76abf6c1f6fade6`  
		Last Modified: Tue, 14 Oct 2025 20:48:51 GMT  
		Size: 100.9 MB (100927700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c33e689ad48c0d271d42106a207d7492134dbfe9e962eba072aea733e15022`  
		Last Modified: Tue, 14 Oct 2025 20:48:43 GMT  
		Size: 354.3 KB (354267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
