## `eclipse-temurin:8-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:eb9a5155f52a67c140177b0e8baf0e655e8cd3636e0e3fc79d93e138836fe0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:8-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

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
