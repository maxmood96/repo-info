## `eclipse-temurin:17-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:0b27d6918584b6c8646bd45f5934a079621f00422cec3a9ab0c5936a9edc4c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:17-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull eclipse-temurin@sha256:00cee9609218033c6f85a99b3cc17a31dd99ad545cbf9e97698a530854a4ff19
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2374797955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d50e8c467ca7b27e5f4232532e96eec6e9da2714598e18be655592c38f2127`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:34:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:34:36 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 11 Dec 2024 20:35:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_windows_hotspot_17.0.13_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_windows_hotspot_17.0.13_11.msi ;     Write-Host ('Verifying sha256 (09c8cd1d57681030acfd41105eaf5da2a9721f442cfc9655a3a9a7f382268d94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '09c8cd1d57681030acfd41105eaf5da2a9721f442cfc9655a3a9a7f382268d94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Dec 2024 20:35:43 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:35:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf30bb5559ff63ab58cc46eca4c689365d27d46ca49d5ccda196911f51d554ca`  
		Last Modified: Wed, 11 Dec 2024 20:35:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54a0237d8c964eb12542e73a698dd25b921a8cb746a9cf2d932a596cd0880b9`  
		Last Modified: Wed, 11 Dec 2024 20:35:48 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba92bc8edb54513d692222fadcccde38e6f3898bbc953dcea300ca8c7441d1e`  
		Last Modified: Wed, 11 Dec 2024 20:36:02 GMT  
		Size: 356.8 MB (356760687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf993ff0097d71bd44f1cb3ba50e8beaf4e3439e25bd9f27235eac3fd7a2e2cf`  
		Last Modified: Wed, 11 Dec 2024 20:35:48 GMT  
		Size: 3.9 MB (3863207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3dd9528c686b940e6dff7f9325ebce197d3b05f47def24122108f8a915d13e`  
		Last Modified: Wed, 11 Dec 2024 20:35:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
