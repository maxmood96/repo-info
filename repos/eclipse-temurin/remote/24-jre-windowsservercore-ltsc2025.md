## `eclipse-temurin:24-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1b7eee88efda09b6290dbc8211c5240a196d8b21a47dcde9a27e19da2a0c54d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:24-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:0dc1b6db958bc0d1bc034452f196fcdd2f4d1052c80b6f52a6614107a6f7ed45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3590948930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709c87b280809be6c433d09d5752e956890ffdfb50c51e57c565dd9dfff43546`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:09:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:02 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 09 Jul 2025 18:09:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_windows_hotspot_24.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_windows_hotspot_24.0.1_9.msi ;     Write-Host ('Verifying sha256 (4562ea92299178db9966b7eb7abf9f8bb5269595f6627cede8fc77caf62a2789) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4562ea92299178db9966b7eb7abf9f8bb5269595f6627cede8fc77caf62a2789') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:09:28 GMT
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
	-	`sha256:29ffa779af9976e71324653851a4538461f3d1a018d6b68b53b595458186da3c`  
		Last Modified: Wed, 09 Jul 2025 19:08:42 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd952afb2b7277d5fc1fff8ab20044f7c34b6ba5669386a6364aa6e99361698`  
		Last Modified: Wed, 09 Jul 2025 19:08:44 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de191d2f1137c79f17d2b1bbbeee44a901504f748124463bfe30d06c0ff44e2f`  
		Last Modified: Wed, 09 Jul 2025 19:08:58 GMT  
		Size: 99.4 MB (99395052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5907c76803929cd917466975d7029b7d47002cd42c5ab1c130b92fd58f8989a2`  
		Last Modified: Wed, 09 Jul 2025 19:09:00 GMT  
		Size: 377.8 KB (377810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
