## `eclipse-temurin:8-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e915b8c2ddbe987f8957ffd4903902daa2200e701bbde2d90ef7139d8b4d35cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `eclipse-temurin:8-windowsservercore-ltsc2022` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:c52355df8f080adaeab608ff827c6c7508a62c6535a7bdb6af058b8bc9ac0d57
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1928836976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72973d3dfcc58be71def49af3f720ef0ae447e0ff98f38527fd8e8d4c119786e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jul 2023 21:29:32 GMT
RUN Install update 10.0.20348.1850
# Thu, 13 Jul 2023 20:29:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Jul 2023 21:32:35 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 13 Jul 2023 21:33:22 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_windows_hotspot_8u372b07.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_windows_hotspot_8u372b07.msi ;     Write-Host ('Verifying sha256 (e75a4e4a70d0fb5c0f1ca4855cb2a7f3c9ccb3d5dea5af0f45d4608a563c45b8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e75a4e4a70d0fb5c0f1ca4855cb2a7f3c9ccb3d5dea5af0f45d4608a563c45b8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Jul 2023 21:33:44 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a7416e1317a892f4786a89c62493b21df55e0e06b82a4bb007cc79df0f949`  
		Last Modified: Tue, 11 Jul 2023 18:03:32 GMT  
		Size: 348.8 MB (348766456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3e3828ab9c4326158b6161915d8bad87619b3107529ab32863eb31b684d127`  
		Last Modified: Thu, 13 Jul 2023 21:07:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f19f35951285bdb61ad16e0ef066eb01145daeaf1c77e2473b1046ab68c4f4`  
		Last Modified: Thu, 13 Jul 2023 22:18:09 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b1a9806acb3bbc00b12583d9ad1ddca5cede8304d5f3fd32874db3aa46bb00`  
		Last Modified: Thu, 13 Jul 2023 22:18:25 GMT  
		Size: 191.2 MB (191192053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152bff0d82688d94aa6a405129abf56c7de230eae920d268d6253ae448e9214f`  
		Last Modified: Thu, 13 Jul 2023 22:18:09 GMT  
		Size: 276.9 KB (276853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
