## `eclipse-temurin:8u362-b09-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:12ec8cd62af79a7740d07c22b3e614cb88a2a180b863efe8c701364c149d0d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:8u362-b09-jdk-windowsservercore-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:5ba76b2a45e256d754e5e298c0b2f991404d2450d0099c038f1c391a9ac94b56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204986448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4391b74ccf0d1660bf8a66a0f7368447f1c7581cecc8a09cf1550ff3f871c8f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 00:41:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 00:41:19 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 16 Mar 2023 00:43:40 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u362b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u362b09.msi ;     Write-Host ('Verifying sha256 (07d6ff7bb5400a618e7e8c6e6104c04c1df6141fa85026526676aa8af011e44c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '07d6ff7bb5400a618e7e8c6e6104c04c1df6141fa85026526676aa8af011e44c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Mar 2023 00:45:31 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e4e0836091bdd33e8adb56d1e13b8096550727a20534e2a2ab9298c86fa09`  
		Last Modified: Thu, 16 Mar 2023 01:41:16 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397814120347f984a9317518ce2e0d48f8e86e4ec090c37143e646b5855692cb`  
		Last Modified: Thu, 16 Mar 2023 01:41:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff7a37a2686520cb1dedb45592b3c68c8e5e87c70bbeee2d370731f5604cc6a`  
		Last Modified: Thu, 16 Mar 2023 01:41:46 GMT  
		Size: 191.2 MB (191157575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d36641e983a6cf6efc60989aa845631b4e5461191baa7fe70f67c05e140e6e5`  
		Last Modified: Thu, 16 Mar 2023 01:41:18 GMT  
		Size: 317.0 KB (317046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
