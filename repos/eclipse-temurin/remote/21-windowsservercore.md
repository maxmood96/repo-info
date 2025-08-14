## `eclipse-temurin:21-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:f19582a39832aa707cd9fde45b08fba052322cd41572935086b616e4dc041870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:4b66aea1b768f33895129eb56ee3668f7e37caba22c53c71a95fcace1f794136
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3879725367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3064405481db2d3bb826d66407ebb71191272d97e14e1298aa75523785e376c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:45 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 12 Aug 2025 20:28:06 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.8_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.8_9.msi ;     Write-Host ('Verifying sha256 (d82030e8689b19efedfbce50ce38351ca81b302c06936584c6a27bda18339df8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd82030e8689b19efedfbce50ce38351ca81b302c06936584c6a27bda18339df8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:28:12 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:28:13 GMT
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
	-	`sha256:fb09770e76053f6de06c610dd14d00490d6512aa5797f5047136c2ee7f459017`  
		Last Modified: Tue, 12 Aug 2025 20:32:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8633dd8eaaee3c3e6d9aea7908a9fb5ccebcba186377de0bb2726d9f0d48719a`  
		Last Modified: Tue, 12 Aug 2025 20:32:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b787bb094e477a2f733b8a1523998d751e3638741cd16204d5ff830e3c4bf11`  
		Last Modified: Tue, 12 Aug 2025 20:45:48 GMT  
		Size: 380.5 MB (380516909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df7f81a07d74bca7b23cf59b2c725ed1642a5537ad4f71a00784e86978f2c4d`  
		Last Modified: Tue, 12 Aug 2025 20:32:11 GMT  
		Size: 374.1 KB (374106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cad94a0133f7ce9e9cfadf1e4c309abc0aed6f48b584f53311b791b83086d15`  
		Last Modified: Tue, 12 Aug 2025 20:32:12 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:d4cd95ccd0726eafce83bc09e23fe971c9ca47b6923f8573e4612eecd2710ad7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2662554991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369341e69931481dd1b55204c608c53c9ad38938008601380a1829c1e43d90c4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:28:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:28:52 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 12 Aug 2025 20:29:18 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.8_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.8_9.msi ;     Write-Host ('Verifying sha256 (d82030e8689b19efedfbce50ce38351ca81b302c06936584c6a27bda18339df8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd82030e8689b19efedfbce50ce38351ca81b302c06936584c6a27bda18339df8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:29:27 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:29:28 GMT
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
	-	`sha256:9dcdb6226581a487d8c390fc2ed19d2aaf29dea58083c7e490c0ce59f9990c9e`  
		Last Modified: Tue, 12 Aug 2025 20:31:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f1caa6f5a0b7f34f9f562eb3437290163b075be78a3ee18bb7051f9e4cebb3`  
		Last Modified: Tue, 12 Aug 2025 20:31:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906c2f9538a1df656a7a28e3ee54e08e3b23dc565c93775c747ab2212b7e79b7`  
		Last Modified: Tue, 12 Aug 2025 20:45:16 GMT  
		Size: 380.5 MB (380500425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366acd59035771c2b1a92d8717014d7fdb03452a2e199ab49529804fe7ceddd0`  
		Last Modified: Tue, 12 Aug 2025 20:31:03 GMT  
		Size: 358.7 KB (358746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5543cb9bb26b6c6e3c2f8eed98338d134f301269a918724b6157fba002299a68`  
		Last Modified: Tue, 12 Aug 2025 20:31:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
