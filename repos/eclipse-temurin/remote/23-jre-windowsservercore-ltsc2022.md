## `eclipse-temurin:23-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0f81b6cb7d1363ba45d9c2265d062dd3bdaec68d5796b00878527aed4dc36341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:23-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:9157353a144fedbd9d4021d6a3b23d236b64eed949f060d11db945332c29582c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2347253420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51bca955cee2c83496d3920167fb4857eb8fff77a5fd52b8c42f6a3e50b6181`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:41:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:41:51 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Tue, 14 Jan 2025 23:42:12 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_windows_hotspot_23.0.1_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_windows_hotspot_23.0.1_11.msi ;     Write-Host ('Verifying sha256 (4d1d7324ec320cf3a4843f208975c28d4136e3b951bccbb9cead4b0a0017147f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4d1d7324ec320cf3a4843f208975c28d4136e3b951bccbb9cead4b0a0017147f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:42:18 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:35092d63921ebb2aeaff08a1ca71cbeb503d314d84527d05ca9c17ae4fad69f3`  
		Last Modified: Tue, 14 Jan 2025 23:42:21 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bbe7fd1c8c8d2ecdf573fc86a1bbef2b505c9dbbd3f80f0cf3629a0bafc79e`  
		Last Modified: Tue, 14 Jan 2025 23:42:21 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba32676db86b523476eb395ad802dd8e5861711dfff14f273596051b8eca7833`  
		Last Modified: Tue, 14 Jan 2025 23:42:28 GMT  
		Size: 84.5 MB (84512904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa374bb1721e7d7b587c7a9623110e81cdba2bc8e58e7e106c9160841e0fd9f2`  
		Last Modified: Tue, 14 Jan 2025 23:42:21 GMT  
		Size: 352.7 KB (352662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
