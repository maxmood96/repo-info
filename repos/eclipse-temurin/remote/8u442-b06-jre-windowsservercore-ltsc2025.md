## `eclipse-temurin:8u442-b06-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a3552c262e6cf65f5390e7068de0b09e46c7bbeb4b1ac356e9bf4c1b3ff4c1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:8u442-b06-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:fb6554902e4cb25a40be1344483288e1ba358595d36228b11cd5449d7ba0dd7d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2573460227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61561d353d686b19dde491adee5083f859d3ffe1176d66a1286bc601df982f8c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 01:33:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:33:17 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 01:33:30 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:33:37 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcbbcb8a015af9bdac5e4c165e31026b167068511eaea85478d32bca2016a86`  
		Last Modified: Fri, 31 Jan 2025 01:33:40 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36907a7b7c26a06343aa9bee8c8c91c81cb263518b2f927e78c02df231c3d906`  
		Last Modified: Fri, 31 Jan 2025 01:33:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a1153e98c80c8f14784c8536a8dbf6b901494890755eec2d5462a4f07e2059`  
		Last Modified: Fri, 31 Jan 2025 01:33:45 GMT  
		Size: 72.8 MB (72785521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23837ea8b907a9e8325f1a799a3dfa091e67f98fc749a4225eb784e2dfb55c20`  
		Last Modified: Fri, 31 Jan 2025 01:33:40 GMT  
		Size: 394.6 KB (394557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
