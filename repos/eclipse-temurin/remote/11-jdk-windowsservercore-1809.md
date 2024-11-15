## `eclipse-temurin:11-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:2bcee9ba0fbc8deee69260244415523c35715ef1e0a22d4cdcf9ca5ff25ada3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:11-jdk-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:75fddde8641bf08b01cfb12fdb17d3b4e4afd76a3840b0faf1e8b03c28c11d8f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2382091002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071b77949145e468244fb34de5560c6d970d64f8c93589c7a0018491ce16a4b5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:10:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:10:04 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 14 Nov 2024 20:10:43 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.25_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.25_9.msi ;     Write-Host ('Verifying sha256 (497d6959470a72c443bb0cfb1af5d0a11689bab8dbe4c21c29f55f453d81d860) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '497d6959470a72c443bb0cfb1af5d0a11689bab8dbe4c21c29f55f453d81d860') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:10:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:10:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e367200e6fefa290d7d0a76df80aa40ae647555842d97723d8838ea30aba271`  
		Last Modified: Thu, 14 Nov 2024 20:10:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c3bcf46eb9fcc11f2a367db718d752c236420adff2a75544fefadf9188baa7`  
		Last Modified: Thu, 14 Nov 2024 20:10:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd130a23f63f8ea583ab9fd3b088c3fde851bc395457c1f6b02d91ebd101aba`  
		Last Modified: Thu, 14 Nov 2024 20:11:12 GMT  
		Size: 371.1 MB (371095853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13189ecd13b5b70d2da76cca73ec8f077050f0c5097a78ad1e45fa8b12d5d4f4`  
		Last Modified: Thu, 14 Nov 2024 20:10:58 GMT  
		Size: 337.5 KB (337488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1408e24cb51dbad3f83faf82d0c11e3031c24dd63ae5e93389ed5e9b3d89c9`  
		Last Modified: Thu, 14 Nov 2024 20:10:57 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
