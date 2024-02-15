## `eclipse-temurin:17-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:b347c1ffd51fb91caf707800b018458f07fc1cf926d0924bb6a2c8f75875d0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull eclipse-temurin@sha256:e3ca8e0381603036ed7d38ad0cfb1929941d3c9cf41f612e39d3d03417ea3323
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2266081773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f01e8430400b9f1d393278ac28600fdde84b411aad7c883ea1ab172f3ddf3c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:58:14 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 14 Feb 2024 19:59:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.10_7.msi ;     Write-Host ('Verifying sha256 (d45b610b1800e35fd667d144277272e3323c7fafa21c0312649fc60a86913a3d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd45b610b1800e35fd667d144277272e3323c7fafa21c0312649fc60a86913a3d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Feb 2024 19:59:45 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 Feb 2024 19:59:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d29d2bb415d199f50f47dc03359023937cb9ca4a732008a9a8c521cdbc08b2`  
		Last Modified: Thu, 15 Feb 2024 00:10:55 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8370808b901cad796db52766036a775cd70a58718039e961de8e93d2e4e4ae3`  
		Last Modified: Thu, 15 Feb 2024 00:11:22 GMT  
		Size: 355.1 MB (355125354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9023d617fdf49402ae5869f9898b15eb7bd19cbfbe5af338190448cf8818fb4c`  
		Last Modified: Thu, 15 Feb 2024 00:10:56 GMT  
		Size: 298.0 KB (298021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f913f493b97009eb9f7ceef647ddaeb2367317720e33b2be6b39f53f1dbfd25`  
		Last Modified: Thu, 15 Feb 2024 00:10:55 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull eclipse-temurin@sha256:f50933c3d49414362c5f45d561ba25732fa35fee85d9312da2adc2040b8bc18e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2439409813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ed4d22a664fc723ec3a5ff5a680f2c5a123e236dce220a9363e90a1ea85425`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:59:56 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 14 Feb 2024 20:01:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.10_7.msi ;     Write-Host ('Verifying sha256 (d45b610b1800e35fd667d144277272e3323c7fafa21c0312649fc60a86913a3d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd45b610b1800e35fd667d144277272e3323c7fafa21c0312649fc60a86913a3d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Feb 2024 20:03:23 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:03:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc7a6342ef92dea8060ae6b2eda54ecc93153f11b1556103f7a03165f0797c5`  
		Last Modified: Thu, 15 Feb 2024 00:11:33 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d259e0cb13af6773bac5646b662a9a6f87500489b48d903f06d609dec5d734`  
		Last Modified: Thu, 15 Feb 2024 00:11:59 GMT  
		Size: 355.1 MB (355147381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f48f15cfcff7696d0303c36c684abe5ee9680b2d2bb69275215c94682cbb41`  
		Last Modified: Thu, 15 Feb 2024 00:11:34 GMT  
		Size: 3.8 MB (3809377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc9e558657c10e63bf1ac7a0ea2659060fc542f69ad0e65c0ffc81a9661514a`  
		Last Modified: Thu, 15 Feb 2024 00:11:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
