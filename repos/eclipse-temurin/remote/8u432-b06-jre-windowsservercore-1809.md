## `eclipse-temurin:8u432-b06-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:449b5bae7e5fb5b7156b02b574a94bcda5bf471f2b8e6161ebb43364de555e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:8u432-b06-jre-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:7e8fd75e621f80eda2c20fd382fa23952a03ac05779268ea0ba55d93a545611f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2084441564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8a5fc399768cbda21ee5e094a8b9283b6afd88e4e34d3365deeddd4379d213`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:12:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:12:52 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 14 Nov 2024 20:13:50 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_windows_hotspot_8u432b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_windows_hotspot_8u432b06.msi ;     Write-Host ('Verifying sha256 (34801770278c26045517fc1851396d7bf66c7c32fa6f9965b968d55adbebda4b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '34801770278c26045517fc1851396d7bf66c7c32fa6f9965b968d55adbebda4b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:13:57 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:f0dfb0c6a4024f942bed784e8bf3b36029326f32b8dde90b613fcb8c171e3318`  
		Last Modified: Thu, 14 Nov 2024 20:14:01 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5960b846422cec4eaa99540688c72692ba729d303dd4b4484d5f1f916982c0`  
		Last Modified: Thu, 14 Nov 2024 20:14:01 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ed8c3a373e2c3e47172da242a1d53a5759b564c9cc0375de6ca4e2f2ad7e3b`  
		Last Modified: Thu, 14 Nov 2024 20:14:06 GMT  
		Size: 73.4 MB (73439850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd20ce1e5c61fd7e5e5074cf59cd0c634a1c54e292bc9983f949c08b6e8e8d4`  
		Last Modified: Thu, 14 Nov 2024 20:14:01 GMT  
		Size: 345.3 KB (345334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
