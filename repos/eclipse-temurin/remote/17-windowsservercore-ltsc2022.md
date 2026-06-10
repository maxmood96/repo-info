## `eclipse-temurin:17-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:2e3bf0b5145354247e7ab8ab71d3de824984bb71f723bde8db17686237469573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:17-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:3d70003a9dac8f0103960452d6f7e1fe531b329f162ad91b113a9f61c57e4c08
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2488513477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b589346aca626ff1e4fe35895a4161fbe9ef14958bf0aa4b4a706aa90a725184`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:11:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:19:24 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 09 Jun 2026 22:20:55 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.19_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.19_10.msi ;     Write-Host ('Verifying sha256 (ccd97a7e313381a84e3567ffe10ad562884e399cc1fb1b4c5fa417de49efac78) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'ccd97a7e313381a84e3567ffe10ad562884e399cc1fb1b4c5fa417de49efac78') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Jun 2026 22:21:07 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:21:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354e304744e47d6cfec491d68edefe77789999c5b468118749899f734cce9a2`  
		Last Modified: Tue, 09 Jun 2026 22:11:56 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b58bb4716e8ca8a434508e0a98fdd58eeb33e305b6c7d5418254e8c1ca3fa3`  
		Last Modified: Tue, 09 Jun 2026 22:21:11 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76554dafebbb83c2299da5dbd0d16fad843cadadb8adec30d2e15ef978f967bd`  
		Last Modified: Tue, 09 Jun 2026 22:21:27 GMT  
		Size: 356.0 MB (356029859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e73429f36b8aa5c7effcc534ac495d7dde240c50b2ad2a6df4b70de27f4b69`  
		Last Modified: Tue, 09 Jun 2026 22:21:11 GMT  
		Size: 354.2 KB (354171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3295ed3fa51c4d2d8c6be44eb8240f4d9ec11edc6a2372bf934082ff196bbca3`  
		Last Modified: Tue, 09 Jun 2026 22:21:11 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
