## `eclipse-temurin:8-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:ccf6ccc9f4b30b4f6a83a9ff1286752b9516067101be3553add29edaeab01dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:8-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:f8b7bb41253f4699366d6a4639943eb68c01fefbc384c3f582c8ae523b5c4567
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2412579633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7096a7406ff1b75a62641033656addfe618255ac7e470541ff41849a355674c7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 17:37:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 17:37:37 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 12 Jun 2024 17:39:31 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u412b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u412b08.msi ;     Write-Host ('Verifying sha256 (52bd4d7aeed31a6ea52cf7f8f271dbbfa28163636a46815c1ba81f12fd4971c8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '52bd4d7aeed31a6ea52cf7f8f271dbbfa28163636a46815c1ba81f12fd4971c8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Jun 2024 17:40:45 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04390472505d81fa325a5cfd00620c5caa18dd222dd0a98f7a089b8c65b438b`  
		Last Modified: Wed, 12 Jun 2024 18:39:01 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3795c6499246131e90e90aa6c5d18f058c7578c20b2bd5f3807ab89cbfeacb`  
		Last Modified: Wed, 12 Jun 2024 18:39:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852e9b8e2b9a30dcd3276774754175c07586bb8ea387f8ece4994ece4dbc2495`  
		Last Modified: Wed, 12 Jun 2024 18:39:19 GMT  
		Size: 191.6 MB (191629279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd89a69e5e26b47ef72f6c8a8a48f7543b0e7e33789381cb1d24ec9f007ee6`  
		Last Modified: Wed, 12 Jun 2024 18:39:02 GMT  
		Size: 266.4 KB (266362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
