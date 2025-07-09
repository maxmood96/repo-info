## `eclipse-temurin:17-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1a9e4647ac5a610438ed7b5efeb124b4e11654b5b2eba4e162ce8509d31f21af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:17-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:26b1b5bb18d7fa6c8cfecaade1536aa27d372a3f905d16d29beb2a30196afafe
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3846840125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ff0be64134b0621af8977f68824bfdad5623c1d74d092fe78eddce673dd642`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:08:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:08:17 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 09 Jul 2025 18:08:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_windows_hotspot_17.0.15_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_windows_hotspot_17.0.15_6.msi ;     Write-Host ('Verifying sha256 (f3cbf808924aa62280475821c1ec9c0b671f6f2c542408a6a21f6b84957daabd) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f3cbf808924aa62280475821c1ec9c0b671f6f2c542408a6a21f6b84957daabd') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:08:50 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:08:51 GMT
CMD ["jshell"]
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
	-	`sha256:1dc7158c4e8b4bc4a957df646f3d2ba8e9d81b3e7a328f11a8fa3332a3b73c71`  
		Last Modified: Wed, 09 Jul 2025 19:09:29 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903288f98825144a56b53f000f71e619848da5d7f77f7060f82cd5c9065a3b82`  
		Last Modified: Wed, 09 Jul 2025 19:09:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c09af31833472b4a797997b1948893efc51c7eb16aa4e942de6d6040672d660`  
		Last Modified: Wed, 09 Jul 2025 19:09:49 GMT  
		Size: 355.3 MB (355283267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d057a2feda0f1de431cdae84a192935450500eb79a30ecdb588f6fe74c4561e`  
		Last Modified: Wed, 09 Jul 2025 19:09:56 GMT  
		Size: 379.6 KB (379607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed5d0eb2bb7bb86e8e3466bd6152705d8500a60d90cb2ee64a2d135e37852f2`  
		Last Modified: Wed, 09 Jul 2025 19:09:57 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
