## `eclipse-temurin:11-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d7de4e9fa1b8d45fc698e8ebace6450d756b8c84e629d6770eb7b7fd9b1415f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.230; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.230; amd64

```console
$ docker pull eclipse-temurin@sha256:dd809c020c18c8832f462ec8a559df221266146eb1802f30a663ded843cbc263
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199238083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f0c4c5783b76c78c833df4576e81ad4392c7059e42caf4bd7841cecfdf662d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Mon, 13 Sep 2021 07:01:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 15 Sep 2021 12:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Oct 2021 22:11:46 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Tue, 05 Oct 2021 22:14:43 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.12_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.12_7.msi ;     Write-Host ('Verifying sha256 (665c22ab930ffa8a220c92b0c08f3cc993c864d7d0ddd8971ab2d738cc03db46) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '665c22ab930ffa8a220c92b0c08f3cc993c864d7d0ddd8971ab2d738cc03db46') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 05 Oct 2021 22:15:08 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:48a76b150a3a1ee8efbc87797c38de66d24a71421fce2754695fed8227d4cc3f`  
		Size: 873.2 MB (873175411 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3fda9a0667b0cb96fa50df6568908c70087df9372ac60c91c1ba417787ee1faf`  
		Last Modified: Wed, 15 Sep 2021 12:59:54 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09817778bc55231f74174e6d6eff2553308bc2f1aa4386252aa60a84a95fd9e0`  
		Last Modified: Tue, 05 Oct 2021 22:26:09 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7c180b384e38918d911a0cf631f6dd2f9a94fc72f8218377e495995c192898`  
		Last Modified: Tue, 05 Oct 2021 22:28:14 GMT  
		Size: 73.8 MB (73787410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a82eea9f651762e222abb3c9a0ab0d3acbbc99995f4abc68ba47e1423cbbc4`  
		Last Modified: Tue, 05 Oct 2021 22:26:54 GMT  
		Size: 573.4 KB (573395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
