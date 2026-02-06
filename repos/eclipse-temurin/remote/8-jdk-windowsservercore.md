## `eclipse-temurin:8-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:6ad0edb1ab113037772ca3a038e37fde5b348f66bfadfd2b79f96e0c8e8cafd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:8-jdk-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:cd3885a469bce44cd8eff080a95feaaa55c1a5665037ea0887b0398c9193494a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1686781215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817ea2ff05028b1a60990bf82e18770c67b239a253c31c23b5a41c5e73e125e1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:15:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:15:25 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:16:24 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u482b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u482b08.msi ;     Write-Host ('Verifying sha256 (f2c978b763c06a1e337918453e2ef1ab1a93a97fe41700c10979b348a7c3f475) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f2c978b763c06a1e337918453e2ef1ab1a93a97fe41700c10979b348a7c3f475') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:16:30 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44d69c678badb93152470f01c5b4d107abca210160fcd0e709dce44a8550a6b`  
		Last Modified: Thu, 05 Feb 2026 22:16:35 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1f3fa4d66a701b8c23e6d632765c859f804661a5630486c3170dba3727e23a`  
		Last Modified: Thu, 05 Feb 2026 22:16:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481f8ad3b416a9eb5018ecf8c65fdf336fb179e4e02d872257b8e7b0d40e1481`  
		Last Modified: Thu, 05 Feb 2026 22:16:46 GMT  
		Size: 190.6 MB (190618895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0222bea306fb80767a727acd1fbc286a23606a613dc96dac0d4afa18de1683b8`  
		Last Modified: Thu, 05 Feb 2026 22:16:35 GMT  
		Size: 399.4 KB (399394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:8cf19907c9a5910dbc90bec7836ff43159514a87d8663c377c7be9b7b27c3d83
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2026733978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bd1c7d632bf5decca36d3ea94afbc48188798cf7471130b78e06ccf97e6bb6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Thu, 05 Feb 2026 22:15:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:15:42 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:16:45 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u482b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u482b08.msi ;     Write-Host ('Verifying sha256 (f2c978b763c06a1e337918453e2ef1ab1a93a97fe41700c10979b348a7c3f475) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f2c978b763c06a1e337918453e2ef1ab1a93a97fe41700c10979b348a7c3f475') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:16:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21173afceaa1d09b3f3f4b9c1c2664db824e745b9cacafb8be63e9c677fdfa78`  
		Last Modified: Thu, 05 Feb 2026 22:16:57 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba720cf5dba74a1e90a36fd662ec713da1a0e069c62ef1c7aa7b96f6db0ad3f`  
		Last Modified: Thu, 05 Feb 2026 22:16:57 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1011ac70dcece36c5777a439dd247f317df63e7804ada99203f8c14a12ffe1bb`  
		Last Modified: Thu, 05 Feb 2026 22:17:08 GMT  
		Size: 190.7 MB (190716696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2043e2f0137cad3c704e70699c9b0425c836ff4759688e7b84bfaa8b7e7e2734`  
		Last Modified: Thu, 05 Feb 2026 22:16:57 GMT  
		Size: 355.5 KB (355480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
