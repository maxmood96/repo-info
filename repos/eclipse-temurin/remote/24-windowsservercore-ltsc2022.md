## `eclipse-temurin:24-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b9dfb3b4c87c13e94782eee08cac0fdee60b75fc084daf4272e859d6adf42015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:24-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:f9ef584e4a3f5ff5b4d90b0267c492b7f8dffb5b3256b1f888d6ffe21555dbeb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2526516044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b0ddf9e687c75addec01e8cba82f4e3830a36c0aa99053e3a67d38304dd3ec`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 20:53:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:53:21 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 14 May 2025 20:53:43 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_windows_hotspot_24.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_windows_hotspot_24.0.1_9.msi ;     Write-Host ('Verifying sha256 (c820fd88f666dbb56109095a7a82ce82ebc0aedb0a0d6d1dd9f75fe2b7ac0eb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c820fd88f666dbb56109095a7a82ce82ebc0aedb0a0d6d1dd9f75fe2b7ac0eb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 May 2025 20:53:50 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 May 2025 20:53:51 GMT
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
	-	`sha256:f607e3fb1d9c025b067163a34b99ed77eabf38049d8e7322b3fe7ca3fa3c1262`  
		Last Modified: Wed, 14 May 2025 20:53:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52208283bfc27480dc776daf2274b08390faa4717e4a840f90d0ac86a945c07e`  
		Last Modified: Wed, 14 May 2025 20:53:55 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4af65f3f1585b7ccd9550e74978aab99804b441df247d479e6720ae65e11a86`  
		Last Modified: Wed, 14 May 2025 20:54:08 GMT  
		Size: 252.5 MB (252535438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2cbe875d261f6d03a01f9442a1bb9aa8943c7764454c2f988035df42de236a`  
		Last Modified: Wed, 14 May 2025 20:53:55 GMT  
		Size: 348.6 KB (348597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753be5b196e99cf8e6a1d2474fd8f7a5a6c2705b4a939a2215c895e0a0fbfb73`  
		Last Modified: Wed, 14 May 2025 20:53:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
