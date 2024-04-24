## `eclipse-temurin:21-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:d9cca003e04488949847facbefeece9ef1e8820224709994c438c8a0549b3d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:a1fb271332254a06b80aa2c58bd133beb87fd821dbecc1f96e0aed8a10dd4e6d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2380295848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d012bd0f98446f442227d0f1729f0dcf8cad9857211e7afe198e35bbe80355`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Apr 2024 18:59:32 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 24 Apr 2024 19:00:39 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ;     Write-Host ('Verifying sha256 (264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 24 Apr 2024 19:01:03 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 24 Apr 2024 19:01:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ac801a31c67fd39cb05fc346f35b772b78c2e21e7af8e509e011f7784a58e8`  
		Last Modified: Wed, 24 Apr 2024 19:40:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702bc9983b98d0a586576e1fd0de3f8d5a4827d30a5d29acf6f778f584631c09`  
		Last Modified: Wed, 24 Apr 2024 19:40:42 GMT  
		Size: 380.6 MB (380618554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a3eed501287f28c8fe54df2a8f0fcfd5805cd6ed5a011f3c2390919f235d79`  
		Last Modified: Wed, 24 Apr 2024 19:40:13 GMT  
		Size: 299.4 KB (299408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2535289aa7bfb367f71432d9d9b021dec6e540c097533abc5ec794003f9c4791`  
		Last Modified: Wed, 24 Apr 2024 19:40:13 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:1a107f3d57aa05f0f3a8515c49ae4ac9c2666bd69e217bf6c5bb58751ee52178
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2549076457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e7890d8c6a0d8a0de868876ba0a774114ea653328a867aced4695066a1edbb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Apr 2024 19:01:16 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 24 Apr 2024 19:03:29 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ;     Write-Host ('Verifying sha256 (264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 24 Apr 2024 19:04:58 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 24 Apr 2024 19:04:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e09a552fe9199029653b3de0d2d08a9fc650f0b44cea65a3394a1813622e4b`  
		Last Modified: Wed, 24 Apr 2024 19:40:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaa99446af75025fe70f67650d7a711d1d8a6640c13bd287b8bff6ca3017eae`  
		Last Modified: Wed, 24 Apr 2024 19:41:22 GMT  
		Size: 380.6 MB (380634013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5858547a861049e90c1062f8851129ec5f8786217a64882ef231b15f7ff93ce0`  
		Last Modified: Wed, 24 Apr 2024 19:40:55 GMT  
		Size: 4.0 MB (4010306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4a82d9229dd2b52ee9f595c78f88f9c575df98f89d3a85f5d0694a87dfeb5`  
		Last Modified: Wed, 24 Apr 2024 19:40:53 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
