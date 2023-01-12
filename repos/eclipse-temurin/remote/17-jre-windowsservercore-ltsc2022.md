## `eclipse-temurin:17-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8129f8286e334ea3262276f62bbcbb39b35822cf8f05d76d9d9801e3de04b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull eclipse-temurin@sha256:54665565f056cc6a9a71358c27c9a884724b7f7552508483a036647d12ca3c76
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1461259428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be1142d5a748f1b689a6ec4768ee5e3fd4a9fbf0ba193d6c6e041f64435eca8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:01:43 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Thu, 12 Jan 2023 02:07:27 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_x64_windows_hotspot_17.0.5_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_x64_windows_hotspot_17.0.5_8.msi ;     Write-Host ('Verifying sha256 (f69d1ab80348509f5163edc1a54206771494742af1cd8a8dae4cd868d9065957) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f69d1ab80348509f5163edc1a54206771494742af1cd8a8dae4cd868d9065957') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 12 Jan 2023 02:07:49 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917264bff9dd61f41fb674eae46aa8b4e03e09c30ac0e7d1c1ab69133d600c38`  
		Last Modified: Thu, 12 Jan 2023 02:44:42 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f91dc4860ff31ef64b4afc9c1fde0214a227e95857ebac6b901d5269f22e19b`  
		Last Modified: Thu, 12 Jan 2023 02:46:53 GMT  
		Size: 74.7 MB (74661262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f42b32e216b90752ee04e22ec96ba5aede8bd845775e08e164395c292b6774`  
		Last Modified: Thu, 12 Jan 2023 02:46:43 GMT  
		Size: 566.2 KB (566217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
