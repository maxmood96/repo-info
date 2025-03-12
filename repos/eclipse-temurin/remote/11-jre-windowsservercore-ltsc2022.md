## `eclipse-temurin:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:84247ccc1cf8329e8387c607b801d07909e678a9ee692410829a7b5b9d26938d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:e8ae21cfd00adfee87f6cf726997e925714433e431f9822789190d96424976fd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345274987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e884a3129cbb70aba7a55361ce00a8999f576ac6541c3834a9d097fcd1eec7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:59:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:59:48 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 12 Mar 2025 19:00:09 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (5e1e515f2625ab6c4bdc95a6a0f0928b3ace6034a60d811da3d701ebfaeaccf1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5e1e515f2625ab6c4bdc95a6a0f0928b3ace6034a60d811da3d701ebfaeaccf1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 19:00:16 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bfd19861bf4feefc687be25afb2021b4a4f3d224273bf3c54daabee4aee345`  
		Last Modified: Wed, 12 Mar 2025 19:00:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1d6cf386df4530872a71a03f89990bb845c81cc5c726967211604d98a22995`  
		Last Modified: Wed, 12 Mar 2025 19:00:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94b34d70a614b5479ce19f4c07f0265fb658beb77acff7b6671d5a9927475f9`  
		Last Modified: Wed, 12 Mar 2025 19:00:24 GMT  
		Size: 75.0 MB (74971577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe018d44c16202ef47336885704a081642d61a16d1bfac1ede218f9f9f3a2d4`  
		Last Modified: Wed, 12 Mar 2025 19:00:18 GMT  
		Size: 359.6 KB (359600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
