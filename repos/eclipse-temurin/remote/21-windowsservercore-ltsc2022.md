## `eclipse-temurin:21-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:fff98b68036b28f400dc18398a5db78f9487aa0e884f4ef75f5780c484e402a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `eclipse-temurin:21-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:be1070f049c29ce9e947efd54bb1b66bfb3484a913132fba5b1fc11e439735bd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2634668628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0a156b3b6f9b67c9ef43d257cb8e3ff7961889bf7e60db6e66a9a94f43e421`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:11:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:50 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 14 Nov 2024 20:12:14 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_windows_hotspot_21.0.5_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_windows_hotspot_21.0.5_11.msi ;     Write-Host ('Verifying sha256 (8ef78a37811529d73d37e29a9fa24bf2d46d0d5d97c4f6e403ea9adebc55eaf3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8ef78a37811529d73d37e29a9fa24bf2d46d0d5d97c4f6e403ea9adebc55eaf3') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:12:23 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:12:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa174910df251a97ed974d2a1faf9759772e917d649719d317f863d0514d38c8`  
		Last Modified: Thu, 14 Nov 2024 20:12:28 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1bfeb336c4590ee1f45b151755c2e35e4b80334b1a4fdb097d43280f65ff3`  
		Last Modified: Thu, 14 Nov 2024 20:12:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264cebcc96165373aed42a37ac7282ff1a6de3e515c998c50ce5bce0c3975a65`  
		Last Modified: Thu, 14 Nov 2024 20:12:44 GMT  
		Size: 381.8 MB (381819473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b94a7066565f78b412038125d9b47be22c586a57d4dff1f5cb8e6b94f94926e`  
		Last Modified: Thu, 14 Nov 2024 20:12:29 GMT  
		Size: 361.1 KB (361083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e193f3a6f827deafa61d2a2e603bc3c446815d93ad9fa9cf8b0dc39e12a36b`  
		Last Modified: Thu, 14 Nov 2024 20:12:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
