## `eclipse-temurin:24-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:a42a8868119f7400286633dadc7ad13182cd6e0cb418934690a9c7efc5351471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:24-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:f278c6ba3dfea9e5aa0b1783949d668d227b45c568537b320b11f34294fee252
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3751706996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3736679799c5ab86c4d76802623118d43a1ddaa58013e1b0dc739b6178d531`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:32 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Tue, 12 Aug 2025 20:27:55 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_windows_hotspot_24.0.2_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_windows_hotspot_24.0.2_12.msi ;     Write-Host ('Verifying sha256 (be608fa0c8a0b106b2051fbef941e8021d53d799d22172719b8f8b1eef4b361c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'be608fa0c8a0b106b2051fbef941e8021d53d799d22172719b8f8b1eef4b361c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:28:02 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:28:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a6aefab36e76bf7b6ddaab844257d1c097da16629c23d46868eb1ca43d71a`  
		Last Modified: Tue, 12 Aug 2025 20:32:09 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25a2023faee03289b5ad0b0de94630c879f6b3feaa2d6d026990800413dda6c`  
		Last Modified: Tue, 12 Aug 2025 20:32:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edd9ab5044ee8493159aaa3b2685c8e18a9210d4315bb929e4f75bd0466ac48`  
		Last Modified: Tue, 12 Aug 2025 20:45:28 GMT  
		Size: 252.5 MB (252506808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556221149a9778a1c9aec5e57b6ba3aeaa5b682b63e942d6caa1520aded83278`  
		Last Modified: Tue, 12 Aug 2025 20:32:11 GMT  
		Size: 365.9 KB (365852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810a97d32527c9bd3156522cc44e0a50fd5b1e15ddc202b2035ab4b809d5863`  
		Last Modified: Tue, 12 Aug 2025 20:32:07 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:4d2c32ffe8bc1bbf4b1b1b8ec4f0a14d0acea4719f112c8aa83791e419d86c12
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2534524754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a7b04023ee5958bd49635705dc0a9e692267b1efccdb742d37b65349069218`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:57 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Tue, 12 Aug 2025 20:27:19 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_windows_hotspot_24.0.2_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_windows_hotspot_24.0.2_12.msi ;     Write-Host ('Verifying sha256 (be608fa0c8a0b106b2051fbef941e8021d53d799d22172719b8f8b1eef4b361c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'be608fa0c8a0b106b2051fbef941e8021d53d799d22172719b8f8b1eef4b361c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:27:28 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:27:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ba991321401941592a8475cb419469264968b7d319c48a3f2e07fae3f33607`  
		Last Modified: Tue, 12 Aug 2025 20:29:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f2f126a592dd299e2a3b0de8c6a53c62fbfc308e1ebcdae4706a737910d890`  
		Last Modified: Tue, 12 Aug 2025 20:29:03 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfca669bc809848bb51055d8c5eb961d7383aaa661b96935150ae0cd5aa6031`  
		Last Modified: Tue, 12 Aug 2025 20:45:41 GMT  
		Size: 252.5 MB (252482445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cef8a961c4634a14f58226f7cbf5c39989b5725dd2f25794dde741da715b64`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 346.5 KB (346489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff74d287bfca478a6e860f207e6dd06b132852ddd7237547212aeba61d24a1b5`  
		Last Modified: Tue, 12 Aug 2025 20:29:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
