## `eclipse-temurin:11-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:b747e2c96769b2237c715c4a4ae11a08e44fd36969810b8f0b91085ffe636ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:11-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:2467784ce6e34d77f325ef8f167410935c42b0643624a9556e99dabce1818ca5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2493497229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd57ca963ea62b4f5832c4fe2ccf9beabc3aa664d06221f6725ce3707e7e527`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:32:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:32:26 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Tue, 14 Jan 2025 23:33:22 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.25_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.25_9.msi ;     Write-Host ('Verifying sha256 (497d6959470a72c443bb0cfb1af5d0a11689bab8dbe4c21c29f55f453d81d860) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '497d6959470a72c443bb0cfb1af5d0a11689bab8dbe4c21c29f55f453d81d860') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:33:32 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:33:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176b52a8571c950a7bdabac53374fe632f1fa77b67ffbcc09d864b4cefae2acf`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77ad098e2b3f1aea589503c0589c2bc85bed9620a5f822e9e51dafad2309f63`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285e1f758361d11598f08e0e59187798c7ea50d695ea9a47d9f2769c3f3df97`  
		Last Modified: Tue, 14 Jan 2025 23:33:50 GMT  
		Size: 371.0 MB (370951030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c5902c03c4ec4d8530b495552dbbc52903e3ec8077424066d2da1fa665d9d0`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 330.1 KB (330116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9de76e1008e3633101ad6bfe26cce9f830a8edd466c40db1209a0206409d587`  
		Last Modified: Tue, 14 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
