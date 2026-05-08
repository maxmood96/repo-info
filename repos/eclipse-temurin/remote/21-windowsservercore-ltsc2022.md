## `eclipse-temurin:21-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:623688f10feff4036496c832c37a789ee49bb5486a628d0938a377d97be40012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:21-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:befa3214dd15ed670a8a91d9fc8ec314edb33c0e9a4f0bb20bdfe96d67bbfa33
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2451798396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e7c46bceae2baa35337289b7808c42c9200f477b74596dd2f343943c651e05`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Thu, 07 May 2026 23:58:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 May 2026 00:16:03 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:16:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_windows_hotspot_21.0.11_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_windows_hotspot_21.0.11_10.msi ;     Write-Host ('Verifying sha256 (93a9c20f4ce967d78992edc5e6fdcc250a56019080553d5d20846decb51d9c01) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '93a9c20f4ce967d78992edc5e6fdcc250a56019080553d5d20846decb51d9c01') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 08 May 2026 00:16:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 08 May 2026 00:16:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fde2c0bc0fe84baca4fbfe521549b09e91916c26f6276a0e25f855a36a095c`  
		Last Modified: Fri, 08 May 2026 00:00:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca823d12cb67a12b0a88ef3dfe55f00ed1395323ef55bdba27c4a88173fc671`  
		Last Modified: Fri, 08 May 2026 00:16:40 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f712b2c93aefdaa3d42269d5e04aca269d0d951668b6b7d3ddf3f0f8f2a4ad0d`  
		Last Modified: Fri, 08 May 2026 00:17:03 GMT  
		Size: 381.2 MB (381216277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57e64033d177f7b2ff8da2da71307903f65ceb4e7c8a556e18d08b874480dd1`  
		Last Modified: Fri, 08 May 2026 00:16:40 GMT  
		Size: 366.9 KB (366939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5218059ca910e90682ea80a663ab001964d195c201ed5ecea0633fad667536d`  
		Last Modified: Fri, 08 May 2026 00:16:40 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
