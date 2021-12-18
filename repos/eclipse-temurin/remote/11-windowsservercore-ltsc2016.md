## `eclipse-temurin:11-windowsservercore-ltsc2016`

```console
$ docker pull eclipse-temurin@sha256:20fbfad32aa50c2bd7fa6102b850c24abafd734649a246493cfec7f98bc3f32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4825; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2016` - windows version 10.0.14393.4825; amd64

```console
$ docker pull eclipse-temurin@sha256:4aa070f549bdfd8ed2a13899f3e86c991306b04fd2fbd07ab384bb8d9fd7e26e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 GB (6640660935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14330a7ef27f409f93e3b2410e0a7cda60e3d6f700499067745bd6e3a9d1324f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 00:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 05:36:03 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Sat, 18 Dec 2021 05:38:09 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.13_8.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.13_8.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (b0edea638fd58c94d80abffd10bbb27731bf6fe1e2b3a9214fb68ab18237deed) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b0edea638fd58c94d80abffd10bbb27731bf6fe1e2b3a9214fb68ab18237deed') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 18 Dec 2021 05:39:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Sat, 18 Dec 2021 05:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7756a7a3024dbbb7cabda3151e8f8461ae808ae2ad3857f0c9235c5908ff7695`  
		Last Modified: Sat, 18 Dec 2021 01:22:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb7beca26fa4738b0559dc263b4190719f419c784bab7f272520e7f8eaeb084`  
		Last Modified: Sat, 18 Dec 2021 06:20:07 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f378980abd0f7a882365d63ecbf1e11b005b94d20e33ebb8a572b14311bb9b8`  
		Last Modified: Sat, 18 Dec 2021 06:26:46 GMT  
		Size: 365.6 MB (365635756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29da292c06704d7266438010b3ba80f0a76e6eeb3ea1e7d8d615e6cf29b6b64a`  
		Last Modified: Sat, 18 Dec 2021 06:20:07 GMT  
		Size: 306.2 KB (306158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373d7e6df89069b1b024e376a357015f0236fe465c2427d41742a9743ba2852d`  
		Last Modified: Sat, 18 Dec 2021 06:20:07 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
