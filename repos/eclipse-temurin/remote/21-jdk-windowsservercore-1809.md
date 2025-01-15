## `eclipse-temurin:21-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:4aaaa20443edda309e0bd908e086d524d5c353e265c9f30b9b438bbdbcb36e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:21-jdk-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:c1cdcdc78f20222ecad1ec53319f238f482b25a47f9b3ba5f242050e59867631
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2508087735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b3d194441583f826a59f82c5cb1bd8ecc8d9191806c074989a18c04b97eadd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:32:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:32:40 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Tue, 14 Jan 2025 23:33:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_windows_hotspot_21.0.5_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_windows_hotspot_21.0.5_11.msi ;     Write-Host ('Verifying sha256 (8ef78a37811529d73d37e29a9fa24bf2d46d0d5d97c4f6e403ea9adebc55eaf3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8ef78a37811529d73d37e29a9fa24bf2d46d0d5d97c4f6e403ea9adebc55eaf3') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:33:41 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:33:42 GMT
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
	-	`sha256:4e58d576b374b6818603ec725dc6e3d27f6c86861f96bd6b3383ee2b064d1e11`  
		Last Modified: Tue, 14 Jan 2025 23:33:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc81293405432c142203daea91356338ee1c474e0e6d1e70e700a1cba859ea`  
		Last Modified: Tue, 14 Jan 2025 23:33:46 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6376628f5875d7de7bdd6f63740ce9b1160edfd56d687c82d0ad48bea4cef8c9`  
		Last Modified: Tue, 14 Jan 2025 23:34:02 GMT  
		Size: 381.8 MB (381814849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84c2517bee7ae7460f8641f77c6e48748cd294e66b1c70750008f59e2d14b5c`  
		Last Modified: Tue, 14 Jan 2025 23:33:47 GMT  
		Size: 4.1 MB (4056811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cf249ca37021fb5c184c045cf6aa32052f93f680fda1dbedf20878c078681c`  
		Last Modified: Tue, 14 Jan 2025 23:33:46 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
