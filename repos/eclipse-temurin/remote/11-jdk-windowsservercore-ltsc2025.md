## `eclipse-temurin:11-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:dbe2c2ddc2294d6fe7c98a0174b03eab10ffe2d3cade4ea0f855f6e22cf92d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:11-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:5b32a8f83dca94e2281fd5935fded1dc65c11181ea24dee15df19059a7f181c3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3764950532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c75a16014e7c1f8c66ebe05c68e77b037db33a7ec1bb90fd55ec25ab4b0027`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Wed, 23 Apr 2025 16:37:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 23 Apr 2025 16:37:02 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 16:37:26 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.27_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_windows_hotspot_11.0.27_6.msi ;     Write-Host ('Verifying sha256 (b34003048c6c3341ff0911663dc5d80822ffdb895b2fe4b6640ae39afa89b4ad) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b34003048c6c3341ff0911663dc5d80822ffdb895b2fe4b6640ae39afa89b4ad') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 23 Apr 2025 16:37:35 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 23 Apr 2025 16:37:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b8ccd6239be0d7eccdddd22b66de6b7ad03af551d0b10b47f52fe2856e43cb`  
		Last Modified: Wed, 23 Apr 2025 16:37:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfb97f2395a81f0c88a7372447e57d5d68fe89e1f5444b3e09c1bdc5efbfe34`  
		Last Modified: Wed, 23 Apr 2025 16:37:41 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf4df686f9239c55cea7b2d3f8260d6da38e8c3f3cf88ebb7c0003b61ba138`  
		Last Modified: Wed, 23 Apr 2025 16:37:57 GMT  
		Size: 369.4 MB (369387281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72b22e8ea8d72d0104a0ad19891add690d5652e70bd3d7bfc0fb037a93d4ede`  
		Last Modified: Wed, 23 Apr 2025 16:37:41 GMT  
		Size: 398.0 KB (397971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2448200bae2fe57897549ee9e21552a9ceeea1f99c03cbefef95077b0736abf`  
		Last Modified: Wed, 23 Apr 2025 16:37:41 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
