## `eclipse-temurin:17-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0ea68e3d8c57f4365de06627c2e58e7090a569cd667d9edb2510619709d61d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:6d99630a31235678fcae5cb5f3aa64c877803d29ba9aff017ccdbd86cbe8d0d0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3574245490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4479805a2c058776a90e0fc62a512c0f35c7b4c234bd28b2dc026241ef5ab3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:37 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 12 Aug 2025 20:27:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_windows_hotspot_17.0.16_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_windows_hotspot_17.0.16_8.msi ;     Write-Host ('Verifying sha256 (9937d754d7157dcdb7ec70a83a5e6238ce093c71316435b4dd07ae38880980d2) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9937d754d7157dcdb7ec70a83a5e6238ce093c71316435b4dd07ae38880980d2') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:27:59 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff60f717b308ff2c24d1bb16c3118144b21dfc3cbc596dd823a4c540b9b8ca72`  
		Last Modified: Tue, 12 Aug 2025 20:45:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad1a4f1480d71e57a0fe296d984bae86992f2250393c1bb3204d291c8f35855`  
		Last Modified: Tue, 12 Aug 2025 20:45:19 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e087c9c4709bdcc0e3322392babf6f585dc72ee273b231d9975a8636257c5f7e`  
		Last Modified: Tue, 12 Aug 2025 20:45:26 GMT  
		Size: 75.0 MB (75047822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1609df310a4deb78fc0d7d7846920af0fe7aeb669a19a0951d34debbc7ba02c8`  
		Last Modified: Tue, 12 Aug 2025 20:45:27 GMT  
		Size: 364.6 KB (364590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
