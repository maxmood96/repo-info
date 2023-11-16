## `eclipse-temurin:8u392-b08-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8eb0c3a798a0660508a9e7879d99ec1f7b2071ef5089acd4cdfe98ccb2591e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `eclipse-temurin:8u392-b08-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull eclipse-temurin@sha256:2787cbaeaa66c803af49178335289fa27745bfd4b32b9427b881fe04e4968812
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1959501109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d03136b12060613c7ffa47f6f0e444540cab223fae8a298d824db6f49499954`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 01:36:16 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Thu, 16 Nov 2023 01:42:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_x64_windows_hotspot_8u392b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_x64_windows_hotspot_8u392b08.msi ;     Write-Host ('Verifying sha256 (7dd4dcc7feac3d7632c1d2336bf65e914b3aa62a0bd9d87a682ce294e964de65) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '7dd4dcc7feac3d7632c1d2336bf65e914b3aa62a0bd9d87a682ce294e964de65') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Nov 2023 01:43:08 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df88c83918c4c43229c6bf1e65088264d9715f53d6bb6cb48d70b55b3573f041`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345999d462c4f6cd096e92ebc5f6155e4cf667bc83dda244b64818989fcb39ad`  
		Last Modified: Thu, 16 Nov 2023 02:28:48 GMT  
		Size: 72.4 MB (72439376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513c3f8f8623c4e26a38fa94d4a76f15f2a882d4e6a1c8b80059ba99a86f3faa`  
		Last Modified: Thu, 16 Nov 2023 02:28:40 GMT  
		Size: 277.6 KB (277564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
