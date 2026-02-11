## `eclipse-temurin:25-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:b2095e648742a23416ead166bcbaba75875c94bb1dcf8649ba97c41ae225b177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `eclipse-temurin:25-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:94a05bc8efea663ed5336948a4eebb7c6043fd1ad8e8d4ddf3e5c7a537f89a17
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2218798305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89b15d4dcb916110017a3427f88b85076d8da3459bede106fe28eeb4cd36223`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:57:17 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 10 Feb 2026 22:57:41 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_windows_hotspot_25.0.2_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_windows_hotspot_25.0.2_10.msi ;     Write-Host ('Verifying sha256 (c433b59ab42630634657ae273940183c2f95a115dd5bf6846a70dcd0a42b9c0d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c433b59ab42630634657ae273940183c2f95a115dd5bf6846a70dcd0a42b9c0d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 22:57:46 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 10 Feb 2026 22:57:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a5e7fbb08adcb3734489a8b4babdef763ffff52d029c414bc9a2dd8caee23d`  
		Last Modified: Tue, 10 Feb 2026 22:53:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf306b44c48d9a4165a5c7f64bfb2245a1e5c25879026de401ef775731bc70c`  
		Last Modified: Tue, 10 Feb 2026 22:57:51 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb313162e43337565abf2ae34639a27ee8e42587903915e4fcd10abfd925fbed`  
		Last Modified: Tue, 10 Feb 2026 22:58:07 GMT  
		Size: 253.7 MB (253671239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de2114acefef8aa3479456a44f1a610443fecd09d1c13a6928b888ba4242611`  
		Last Modified: Tue, 10 Feb 2026 22:57:51 GMT  
		Size: 363.3 KB (363273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32830ff4aa893f2d54fb8a19e5dd80cc342b5e6595b62ecb56d99f4132719043`  
		Last Modified: Tue, 10 Feb 2026 22:57:51 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
