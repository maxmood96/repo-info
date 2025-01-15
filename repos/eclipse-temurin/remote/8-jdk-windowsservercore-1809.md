## `eclipse-temurin:8-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:e9ce8bee9d7bb50afa25f9aaa42b26a51b64b94da6c630f94c3d8b3a37c2ced1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:8-jdk-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:dafe31c81e8fd134fc2ed785d15620206be4044d6c84d967578ad0287ed49884
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2315642085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c72c2d4946e7d400485be76eafd5e404ab29332599f557e746d2d7cdc2a1f6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:44:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:44:09 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Tue, 14 Jan 2025 23:45:50 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u432b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u432b06.msi ;     Write-Host ('Verifying sha256 (c9280205858928756374d930d4b539c59b1cb470425d2cf300b943c56efe4d86) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c9280205858928756374d930d4b539c59b1cb470425d2cf300b943c56efe4d86') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:45:58 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:a32ac8b083887926f6476748612bb15999753b0a6b13cca964cc89298c8f43d6`  
		Last Modified: Tue, 14 Jan 2025 23:46:00 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0287fe4703f6100d4208c867a09212e50375c83f80b5ceba882b7b3faa9845e7`  
		Last Modified: Tue, 14 Jan 2025 23:46:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e1156f126534d01846f9de5fb2c1c3b7087c7f01b57a16389a4bc7b88037f6`  
		Last Modified: Tue, 14 Jan 2025 23:46:09 GMT  
		Size: 193.1 MB (193107158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f65af1248cd2c5f80cddb254283995f6d49353f1ddca3aa4daac1ef00dafc11`  
		Last Modified: Tue, 14 Jan 2025 23:46:00 GMT  
		Size: 320.1 KB (320129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
