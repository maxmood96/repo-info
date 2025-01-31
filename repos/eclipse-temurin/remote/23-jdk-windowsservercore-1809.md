## `eclipse-temurin:23-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:783faaba80865021fd8765359e55bf168d636046bab51b419573dc32918ab1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:23-jdk-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:95d9f550c35c9e36b9590d322d563736b56360d989d30d8791e4fdc58a3d0f66
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2523395974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32ac21995f8ea2dded83d19d30dbe037f5fcb7c1e120aa4914b0aefc1650d25`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 01:30:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:30:40 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 01:32:49 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:33:00 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:33:01 GMT
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
	-	`sha256:8d1a883cb00c69d0bdb519d430ade95100a427618db0faba1aa3f4f3db345fff`  
		Last Modified: Fri, 31 Jan 2025 01:33:03 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195248e9049375b50543b3e7aab0eab614002615ae8dcaf2a2f550a91e680b6b`  
		Last Modified: Fri, 31 Jan 2025 01:33:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6da4a065c4484ac514c389dc25b97cfc8d4935d97349030ed7d5fc2e9df79c`  
		Last Modified: Fri, 31 Jan 2025 01:33:20 GMT  
		Size: 396.9 MB (396850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce263a9a4faf3e0a138a0b2f42290f6fd488a5f51c3d99e433908652e0dcffef`  
		Last Modified: Fri, 31 Jan 2025 01:33:04 GMT  
		Size: 4.3 MB (4329578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb601002c74f8a1064097ac53c0bd778b8fb45643fb74b11c8514ea1e2d942`  
		Last Modified: Fri, 31 Jan 2025 01:33:03 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
