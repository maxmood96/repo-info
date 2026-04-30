## `eclipse-temurin:11-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:8c7b2568e91d93d4c79b265c75da295590f1d4866ae838bfd1cfbc81105e3f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:aad45d3ba974e98b36391d9367e0d2b81d038e75ebc81870bb7d774175d6647e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2500312809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e83a3489f953c0a7aea1e45bf848b96a41d9123fcafd2e35b14a14237a200cd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Wed, 29 Apr 2026 22:46:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Apr 2026 22:46:44 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:48:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_windows_hotspot_11.0.31_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_windows_hotspot_11.0.31_11.msi ;     Write-Host ('Verifying sha256 (432d897f39766288a5747ec5f4927136ce89b743df2ab436cf7d230fbbcd596a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '432d897f39766288a5747ec5f4927136ce89b743df2ab436cf7d230fbbcd596a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 29 Apr 2026 22:48:26 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 29 Apr 2026 22:48:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a14b1ab823928f463b4116f5097425013fadfeafe8e1197e48a6fc31d0b442f`  
		Last Modified: Wed, 29 Apr 2026 22:48:31 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58ee3f9682c5208560950643c27df8146f711f6a0d2052c02808cb8d06d226d`  
		Last Modified: Wed, 29 Apr 2026 22:48:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c904db6727b6c02b68dbc30195f3026da3c345ffd75bd930eff9a5e83a6b9af`  
		Last Modified: Wed, 29 Apr 2026 22:48:48 GMT  
		Size: 370.0 MB (369962589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb27a1e6937a7df008ed69d95755b0d984d4927e5aff423d2b78637b4f6c9d8`  
		Last Modified: Wed, 29 Apr 2026 22:48:31 GMT  
		Size: 360.3 KB (360265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abbabe87ef1751ae74b3b4484e54d483a368abec211a213d4e29fbad1cf141f`  
		Last Modified: Wed, 29 Apr 2026 22:48:31 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
