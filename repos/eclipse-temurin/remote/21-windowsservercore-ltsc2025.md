## `eclipse-temurin:21-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:b19aa6d129e12dfc2dffc801b97f60b0d05b5b022fd00a95bf06d3a1febc44e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:21-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:f269e37dbb607e31e4882792a52e5f1aafa8f16f0269b0e9ffcc71a47d2e7a3b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3775968619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62808dad3b1bb84e27b1930881d81074dddc687a72b9082e276bde2f30011ee`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Wed, 23 Apr 2025 16:37:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 23 Apr 2025 16:37:18 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 16:37:44 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_windows_hotspot_21.0.7_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_windows_hotspot_21.0.7_6.msi ;     Write-Host ('Verifying sha256 (168e3c710448dbdd7e6fe2463b867339a72be11a7c8615d72d19fb26572d3619) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '168e3c710448dbdd7e6fe2463b867339a72be11a7c8615d72d19fb26572d3619') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 23 Apr 2025 16:37:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 23 Apr 2025 16:37:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5a95f93d12718481a0c995e5615f9fdf6e828124c6bb02777ccea6b228b9f0`  
		Last Modified: Wed, 23 Apr 2025 16:37:59 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1a433d1b038143752c3cf669be7bbdca7bd2895c61f8e6ffac90cc6394db5`  
		Last Modified: Wed, 23 Apr 2025 16:37:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726da157c832c12a6f48ad17682510335af1e7d853ad3afc26aa1a8be3d82766`  
		Last Modified: Wed, 23 Apr 2025 16:38:17 GMT  
		Size: 380.4 MB (380416060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16da3ab61316fa76a5e692a915c18f1ff44d416f40d466e5a061c984fa121000`  
		Last Modified: Wed, 23 Apr 2025 16:37:59 GMT  
		Size: 387.3 KB (387277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29625ef73f5bdcbe8006303c29154d52ad8604f9884704b6009822be892f4e71`  
		Last Modified: Wed, 23 Apr 2025 16:37:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
