## `eclipse-temurin:8-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:983b7db6b732c57fb639ab0f5f31c6ee51bf585750aa008ec793de2708cb241e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:8-jdk-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:4f9a20dc98256dddc6a3fd00c3169884c04d326d1e542cea3f380105bc68d3ab
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2092798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f60e84cbbbe098cc707a0a6a3756919b17549327505d95371685c53badcdea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Sat, 19 Oct 2024 00:54:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 00:54:59 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Sat, 19 Oct 2024 00:57:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_windows_hotspot_8u422b05.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_windows_hotspot_8u422b05.msi ;     Write-Host ('Verifying sha256 (9944b308061827c8ad26bedd573eac334c12eaa72c8b7f5ee73a5795e7710204) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9944b308061827c8ad26bedd573eac334c12eaa72c8b7f5ee73a5795e7710204') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 19 Oct 2024 00:57:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22b42eeaa9772fc7698758602522868e6ea62c572e2084e88e8d84bdd288ba5`  
		Last Modified: Sat, 19 Oct 2024 00:57:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56981370cf6d1f5c09ea2e6db519fdb0072d403afa1c9347144e9e3b7b3317f`  
		Last Modified: Sat, 19 Oct 2024 00:57:55 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aba61d4cc8ca04ad557a364a2b67cd2eee1fbf6cc2e651421c27412d0afdf2a`  
		Last Modified: Sat, 19 Oct 2024 00:58:03 GMT  
		Size: 190.7 MB (190651211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e83fe0db7ac42cb66d536e066d455827fa0fe240d83581b0e82189e051efea6`  
		Last Modified: Sat, 19 Oct 2024 00:57:55 GMT  
		Size: 319.4 KB (319359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
