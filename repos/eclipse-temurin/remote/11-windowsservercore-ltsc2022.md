## `eclipse-temurin:11-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:48e3b80f8ff69d03f5c9eef0769eaf01f7874fe799cb48a4780e014843b3e484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:a1829962e6348899dba47938715d10018550f69a79edee045f9450a6cc6bb695
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2643280209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3001a26b7e8d2d53b66c90270345868a0a9ce5801592c5a0aeb28f12569caa12`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 21:00:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:00:01 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 14 May 2025 21:00:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.27_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.27_6.msi ;     Write-Host ('Verifying sha256 (b34003048c6c3341ff0911663dc5d80822ffdb895b2fe4b6640ae39afa89b4ad) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b34003048c6c3341ff0911663dc5d80822ffdb895b2fe4b6640ae39afa89b4ad') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 May 2025 21:00:41 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 May 2025 21:00:41 GMT
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
	-	`sha256:dfef8ccf877d5164cf4bd1f67350ab926ee621ea5c7edaee1e90eaa3b9d56981`  
		Last Modified: Fri, 16 May 2025 14:42:47 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4132675992f6ed77c81d220922bf592742ffc5295fd099b42c64604a504e6ce`  
		Last Modified: Fri, 16 May 2025 14:42:47 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd890826e5f59f0117f6a7456361e11773f058a13f4ba1903bb2880bee84c88`  
		Last Modified: Fri, 16 May 2025 14:43:25 GMT  
		Size: 369.3 MB (369311347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a75b724068d2a06bf8eb8251e1bde80aae17249d24aa95732bbda188653db78`  
		Last Modified: Fri, 16 May 2025 14:42:48 GMT  
		Size: 336.9 KB (336893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fca59e7b4ba1b3a217e78c2d2d5f8f5a1cb5d3a16e6dfdc1b33c405a25dfa1`  
		Last Modified: Fri, 16 May 2025 14:42:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
