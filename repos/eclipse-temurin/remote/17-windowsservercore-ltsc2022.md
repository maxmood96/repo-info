## `eclipse-temurin:17-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:359f1bbc8deb933647504cc65f493026f68c9645c05aac3c46c96ed212aa8042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:17-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:9dee58e64e776693459baab82998224dc9ef9e7a6fc4dc3eeb5b3ea4c6f713e7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2629228101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f4a164e88a912ad15ac8986ecd12eff477225a7083e2701c9ce820c2e8b771`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 20:58:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:58:44 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 14 May 2025 20:59:11 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_windows_hotspot_17.0.15_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_windows_hotspot_17.0.15_6.msi ;     Write-Host ('Verifying sha256 (f3cbf808924aa62280475821c1ec9c0b671f6f2c542408a6a21f6b84957daabd) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f3cbf808924aa62280475821c1ec9c0b671f6f2c542408a6a21f6b84957daabd') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 May 2025 20:59:20 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 May 2025 20:59:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedc9a5cd8386c3ad8a7ccaed71c6a904a5e54af0a4e104825efeb4d7415dcc7`  
		Last Modified: Wed, 14 May 2025 20:59:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bfb5c6de1771da6a3dbdf2fc908ab47e0c2c34fae14bf5c47de2b013553152`  
		Last Modified: Wed, 14 May 2025 20:59:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9ad9e1038075508611c406ce9881e6b359da921b30edbd9b45e0fdfd142b5`  
		Last Modified: Wed, 14 May 2025 20:59:37 GMT  
		Size: 355.2 MB (355244603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4717fbc58adfa0abfaaf6416ffd0af2f23b329cf2bddb8688cd8371fb04d9da7`  
		Last Modified: Wed, 14 May 2025 20:59:24 GMT  
		Size: 351.5 KB (351526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3312e0537b4f6cda5d5fca2e91be2b2ccf6ed413d963b4dff305879fe029475c`  
		Last Modified: Wed, 14 May 2025 20:59:23 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
