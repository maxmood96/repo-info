## `eclipse-temurin:8-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ff8192b3f02781e44ef8fca1b90be16f3aaeaf742cd36e79f3d7c0c4c6c8fcca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:8-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:1ff18b52f02f18141b7633e4aeea884b2ff2fd9c206313a71fa110fddd2840a7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2053703730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34de9e2266227c1fc5f41f70d8b4342d88f57a0dd1ca137d8289bdccff8c567b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 22:52:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:00:00 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Feb 2026 23:00:27 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u482b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u482b08.msi ;     Write-Host ('Verifying sha256 (f2c978b763c06a1e337918453e2ef1ab1a93a97fe41700c10979b348a7c3f475) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f2c978b763c06a1e337918453e2ef1ab1a93a97fe41700c10979b348a7c3f475') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 23:00:35 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a1a68b70a6037a04683b570a391289e218225652d139b4c315a66941376ca1`  
		Last Modified: Tue, 10 Feb 2026 22:54:47 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fa74c63f2029fcaeb225cdcd28c6502c6f7c6bb034aa6bbdd316e2fcd8eaac`  
		Last Modified: Tue, 10 Feb 2026 23:00:43 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41637f6f79d973215dd758dc75521b3717c906cc12053ec3ae1673245c10c2`  
		Last Modified: Tue, 10 Feb 2026 23:00:52 GMT  
		Size: 190.7 MB (190702013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609a9c72f51eb8dad3bbe63af547e671f2dc925df7af8d0b627bcbce6b862996`  
		Last Modified: Tue, 10 Feb 2026 23:00:40 GMT  
		Size: 341.9 KB (341909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
