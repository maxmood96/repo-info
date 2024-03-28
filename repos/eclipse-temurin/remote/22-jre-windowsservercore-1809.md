## `eclipse-temurin:22-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:e7a70017023320cd30d538977ddc77051b894e1ba6f249e2b47ad1d642600421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `eclipse-temurin:22-jre-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull eclipse-temurin@sha256:439eb8fb1c104bc3c4dd2112237f0589ed14d0bcf962383a740964f79a21b54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2211906330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cf79df63c693395105cdf576d8cfc86e18af369f838f35e5185da7b9a1e38b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 28 Mar 2024 01:20:56 GMT
ENV JAVA_VERSION=jdk-22+36
# Thu, 28 Mar 2024 01:29:00 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_windows_hotspot_22_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_windows_hotspot_22_36.msi ;     Write-Host ('Verifying sha256 (fa6b75f1dbd9eca8bfbd955d2a78d4fc8c678127790caf4340ce2991c7b668c9) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fa6b75f1dbd9eca8bfbd955d2a78d4fc8c678127790caf4340ce2991c7b668c9') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 28 Mar 2024 01:30:30 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a685c5969554d9ebfd3d37a78edff8b239bcbc0f0189340fb9bbff062442ae`  
		Last Modified: Thu, 28 Mar 2024 01:38:07 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d79e4ba1cdc75f8abbb27daa44d9bbfe930202555cc63a75dc974241d486b7`  
		Last Modified: Thu, 28 Mar 2024 01:39:49 GMT  
		Size: 83.2 MB (83223429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f073dc38fc048ca9089c06f374e3351f825363963638fe869f5fafeac3fba54`  
		Last Modified: Thu, 28 Mar 2024 01:39:39 GMT  
		Size: 3.6 MB (3580112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
