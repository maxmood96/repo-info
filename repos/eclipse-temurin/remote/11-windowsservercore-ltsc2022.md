## `eclipse-temurin:11-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d31017726a377672f95b2be32f0e1d9d4df6be6c94c0e3f88b68944b528cba53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:9c0b56ba3076e1ab0f8fcdd1b13e80fc6a84fd12f43dd7c4cf3fd830c2f69ba9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2633675738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d708ef0b9ec48615abba1ec6db79efd38ab11d8e944e1d4906e390f6e0a98807`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:31:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:31:33 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Tue, 14 Jan 2025 23:31:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.25_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.25_9.msi ;     Write-Host ('Verifying sha256 (497d6959470a72c443bb0cfb1af5d0a11689bab8dbe4c21c29f55f453d81d860) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '497d6959470a72c443bb0cfb1af5d0a11689bab8dbe4c21c29f55f453d81d860') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:32:06 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:32:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebfe4fd10a761005262a3d0eb6a5f699a4cdfa3de1924dc5346917fdd1508f9`  
		Last Modified: Tue, 14 Jan 2025 23:32:11 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6248c09dccf28e6ee14f6ac1ff830f51b5d7453fa8533325fe5eb2471c1db5`  
		Last Modified: Tue, 14 Jan 2025 23:32:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdad8c384b34881db4da6e1325ba09fa1f02bce9c16ca4e809e9f572c6befb3`  
		Last Modified: Tue, 14 Jan 2025 23:32:26 GMT  
		Size: 370.9 MB (370939539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22983adb50b81bd6611280e57411e8d062652c6eb1130766cfc4fd58fe41459`  
		Last Modified: Tue, 14 Jan 2025 23:32:11 GMT  
		Size: 347.1 KB (347088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4394b54a87cdc9590ddfa8d1c907c84b81c65ee15ad3118ebf22788797bfc0e5`  
		Last Modified: Tue, 14 Jan 2025 23:32:11 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
