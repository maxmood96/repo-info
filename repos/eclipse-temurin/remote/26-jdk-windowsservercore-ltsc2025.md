## `eclipse-temurin:26-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:71fa6d83605b992aea3f7c6fba057efd2f84f7256b58e1591e22e15d23e7f022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:26-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:fe0b17da95dba60b7dfab305a2da1f7f78cc264c2a093295e068089b4f6cae76
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2390254863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28d8ea25ad1423066c7ae8b9c8619ac40dd0f6d86a7e10fd03728c08938c61f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:11:29 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 14 Apr 2026 21:11:51 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_windows_hotspot_26_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_windows_hotspot_26_35.msi ;     Write-Host ('Verifying sha256 (d69a60a2b0f9193303590c8f5bb58ae259117bfff6c8435930127e6010c4cf3a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd69a60a2b0f9193303590c8f5bb58ae259117bfff6c8435930127e6010c4cf3a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-26' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Apr 2026 21:11:58 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:11:59 GMT
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
	-	`sha256:982c0a1d181edd98fb85a64a9f9444e83a7253a0cab0690df604b44be82edb84`  
		Last Modified: Tue, 14 Apr 2026 21:03:15 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ffda96c99afe5765dce9e8a244d5af73cddded7b1957018c00db31fcfa9dc9`  
		Last Modified: Tue, 14 Apr 2026 21:12:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d70a3ca3a94f1b6531f037944b6e9c41b86a9772c5de40e0475db6c1a02424`  
		Last Modified: Tue, 14 Apr 2026 21:12:20 GMT  
		Size: 259.9 MB (259906029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab8bfa87ec0caf7b3004e70569bfccc490e2cffc2673036a6d675c23d1e2dc7`  
		Last Modified: Tue, 14 Apr 2026 21:12:03 GMT  
		Size: 358.9 KB (358880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168273ce25b9312e2ad55ec66301bf8a5fcdfb4e1ad70d805b2c78db7409e6be`  
		Last Modified: Tue, 14 Apr 2026 21:12:03 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
