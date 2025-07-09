## `eclipse-temurin:24-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:8124d91fed3be6f605320b11935fb82b8602cbc029ad04b05821d00b891296e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:24-jre-windowsservercore` - windows version 10.0.26100.4652; amd64

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

### `eclipse-temurin:24-jre-windowsservercore` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:81160a37e54ecffbbf271a547f0ccc665e5cefd7d198acd32d9a3b8087ddb804
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2380304455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d025ed6b3969c80f4571aa3ec140ee34404ac246cb496df07811e9581acf3ffb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:08:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:08:36 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 09 Jul 2025 18:08:55 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_windows_hotspot_24.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_windows_hotspot_24.0.1_9.msi ;     Write-Host ('Verifying sha256 (4562ea92299178db9966b7eb7abf9f8bb5269595f6627cede8fc77caf62a2789) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4562ea92299178db9966b7eb7abf9f8bb5269595f6627cede8fc77caf62a2789') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:09:03 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af21d994b59adb3f342a9099b8b371aba9ce5d4e3847e908f7f9f425c9920999`  
		Last Modified: Wed, 09 Jul 2025 19:08:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2135aef35188d2f34f2ddd52e5a7010c97e6d9d864e2eca15304cd21d882a3cf`  
		Last Modified: Wed, 09 Jul 2025 19:08:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeac22ac7f1c3af730e23a52ac62c547e58d83a2e68577baee0ed0b26f54fa6e`  
		Last Modified: Wed, 09 Jul 2025 19:08:27 GMT  
		Size: 99.4 MB (99350196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cb56dd3db936fa883727b3bb92f506da67920fe95ae57a1441c991bd0109d0`  
		Last Modified: Wed, 09 Jul 2025 19:08:18 GMT  
		Size: 348.2 KB (348165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
