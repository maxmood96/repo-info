## `eclipse-temurin:17-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:e3f70193e9dd4dc03572bf014e7ed145f79de829f878255ca968760e5a4bce3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:17-jdk-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:222f2307fa483c9303237fe06d61761d0dfd93ac9a2f91758c6132bc8d3f99e2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2482707393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fad3a6553d5b15b923e503da18704fe60e2435b3aea9b8c7448536fab62a6c`
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
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 14 Jan 2025 23:33:31 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_windows_hotspot_17.0.13_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_windows_hotspot_17.0.13_11.msi ;     Write-Host ('Verifying sha256 (09c8cd1d57681030acfd41105eaf5da2a9721f442cfc9655a3a9a7f382268d94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '09c8cd1d57681030acfd41105eaf5da2a9721f442cfc9655a3a9a7f382268d94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:33:41 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:33:41 GMT
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
	-	`sha256:035fc17aac1d9f51d60fc332ffabd1bd2b5ab4bd9b28b7e26aea7e3990878338`  
		Last Modified: Tue, 14 Jan 2025 23:33:45 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaab6714a4de99d4eba74160f667a4f07469607293ee633ec8dcdf19193cf24e`  
		Last Modified: Tue, 14 Jan 2025 23:33:45 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ca5e7bb1b66c331076b701d110e4b86cd9789c044112bd7b53cd76c7b6902a`  
		Last Modified: Tue, 14 Jan 2025 23:34:00 GMT  
		Size: 356.6 MB (356629938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cfcc72b05e67f2c5dc7695c4e63dfceaca58f056cde075d71cc4e446bd200b`  
		Last Modified: Tue, 14 Jan 2025 23:33:46 GMT  
		Size: 3.9 MB (3861162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a217495bee54e4d4bcdd582f47d054dee8b0bdd4ff1b3bf0154eee31e85ee797`  
		Last Modified: Tue, 14 Jan 2025 23:33:45 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
