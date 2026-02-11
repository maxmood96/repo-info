## `eclipse-temurin:11-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0659b058e20b05785bca8c8dc4f1d4403b553dd6df6930fbe5a1ce01c7c1bd72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `eclipse-temurin:11-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:721120537dd3769a9a4d8e98601fb87af084beceff5607ab7dd552ea99cd4caf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334795471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf57697354b80b246a2953796d13c3351f52f91933813fe24f07dac7def55aeb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:53:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:53:40 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 10 Feb 2026 22:54:08 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.30_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.30_7.msi ;     Write-Host ('Verifying sha256 (5a7e985d6e89c864cf176c9ebf919ab1e97b40877b8e5290e4c51f532e37d1c2) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5a7e985d6e89c864cf176c9ebf919ab1e97b40877b8e5290e4c51f532e37d1c2') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 22:54:14 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 10 Feb 2026 22:54:15 GMT
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
	-	`sha256:943554d949064179b06929010e6f822fe26e474012f6ab8da20725e1a91eb4f0`  
		Last Modified: Tue, 10 Feb 2026 22:54:19 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4571389513ca7299a3a11efe1dca381283b508811f72d919be776978e1a785e`  
		Last Modified: Tue, 10 Feb 2026 22:54:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c758791f6d3a2174ab8219edbffd948df168a5827cd543badad5db90e61559c`  
		Last Modified: Tue, 10 Feb 2026 22:54:38 GMT  
		Size: 369.7 MB (369672792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4832b3e1ca3120e0337732b4ff9f0733e8e1fb1901a2f5d41026c9e27b3e9f7`  
		Last Modified: Tue, 10 Feb 2026 22:54:19 GMT  
		Size: 358.8 KB (358826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3598b770c57575bb89089bd998220db1d571e1cca6490a6579d0cb59a418a617`  
		Last Modified: Tue, 10 Feb 2026 22:54:18 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
