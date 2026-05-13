## `eclipse-temurin:25-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:cebaee855b4c9c92c9ee613fc547f058b5b78fe9e093a0724f65d00e7f8e1c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `eclipse-temurin:25-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:cac5a7a93ad0e30aaa9f9ba9bbb9f964aa6b3c3cd52f0bd813d3bf4266e794a4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2307492310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b3ed54f1fdd046d8907f08a59332749687d1bed339ef7842bf61b726b39512`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:37:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:46:31 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 12 May 2026 23:46:45 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_windows_hotspot_25.0.3_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_windows_hotspot_25.0.3_9.msi ;     Write-Host ('Verifying sha256 (05975ec0d4df8722b30836af98d795a80f72d4cc37a2451943bd23304d5ac0fb) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '05975ec0d4df8722b30836af98d795a80f72d4cc37a2451943bd23304d5ac0fb') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 May 2026 23:46:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501f68ee4ec3df8e709de0c6a68dead6e0f2d4a50e602e1f955eb2c615012770`  
		Last Modified: Tue, 12 May 2026 23:38:02 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0015760742f8bcd30102c9e190e2e971623303a0d075d3df27ea33f32b98797`  
		Last Modified: Tue, 12 May 2026 23:46:55 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf988bf633fc81203782f8bb5bd0949b0da29b0ba5f712e0c966b2678bd1bb5`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 101.2 MB (101178672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7117231480455e6b711e2fdd031861a4b75dec5f4483f7b2568aaacc2bdaa70`  
		Last Modified: Tue, 12 May 2026 23:46:55 GMT  
		Size: 369.1 KB (369073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
