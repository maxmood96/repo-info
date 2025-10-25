## `eclipse-temurin:17-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:65f2f320084e68e839825e09fde29756170dfab4152e746b687acf3494d55203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:17-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:e17502144914589d14187e229a9688e0e7d35fad84d4addf4fe50388e5c7b3cd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3575927101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf63614dd2970145c5b7849f2f41edaa21c6626dcc51e755eb87a2a381dd1d6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:14:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:14:08 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 24 Oct 2025 18:14:45 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.16_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.16_8.msi ;     Write-Host ('Verifying sha256 (1c3701f074d75036650731bcf6b08d69b1e3567bfa853f0ddd7aaba44da5b595) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1c3701f074d75036650731bcf6b08d69b1e3567bfa853f0ddd7aaba44da5b595') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:14:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d1f9d056117a0def7237d546c4b3f5a0e8f95466eb9605fc225aa8dcde690f`  
		Last Modified: Fri, 24 Oct 2025 18:23:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ad3b65c078908b11df95b125ca9e4eb96ca4e000b132aa30f90695675452d8`  
		Last Modified: Fri, 24 Oct 2025 18:23:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699de3c13f61d1c10aa858049b9d4e8773ca496ba7460bf6f907b4ce0abd1882`  
		Last Modified: Fri, 24 Oct 2025 19:19:24 GMT  
		Size: 355.2 MB (355227847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b2458f1ee55deca2b312b112efa27c4faaeecf6ce4b0eb4fc8221ef2fff293`  
		Last Modified: Fri, 24 Oct 2025 18:23:18 GMT  
		Size: 348.3 KB (348298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5282df071bb6470eb2ad9bfb0441226123e60b38ed4c94b5b4eaa399e39c75d`  
		Last Modified: Fri, 24 Oct 2025 18:23:18 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
