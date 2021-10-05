## `eclipse-temurin:8-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:72da30e69a95f567020b4645ef2792c7304963a5504b1283d108ae7931ab4af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.230; amd64

### `eclipse-temurin:8-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.230; amd64

```console
$ docker pull eclipse-temurin@sha256:111733ad266cf2db60d8e298b6296772aff8997f91df686baba81e28ccdac251
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2196313797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f2b050fadb999825a701888557161841eb9930715a39c3cde78a36df758b26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Mon, 13 Sep 2021 07:01:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 15 Sep 2021 12:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Oct 2021 22:08:25 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Tue, 05 Oct 2021 22:10:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_hotspot_8u302b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_hotspot_8u302b08.msi ;     Write-Host ('Verifying sha256 (34e5eea737dfaca57ec5162e6fece5259f403fa419c7bcab572e9cdd2bcf8dd1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '34e5eea737dfaca57ec5162e6fece5259f403fa419c7bcab572e9cdd2bcf8dd1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 05 Oct 2021 22:11:23 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:64cd90b28759b2715bba12424bca40ac721c899782145d61230e70cdc4ef061b`  
		Last Modified: Tue, 05 Oct 2021 22:24:03 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20f7e99dfc0d2ed989e85ee0e9e50e51ebf58e1da8718af46f33f5b1ac62a`  
		Last Modified: Tue, 05 Oct 2021 22:25:52 GMT  
		Size: 70.9 MB (70862618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bcc93aab61c8bc253518c46724aa6ff6aacb5f066fabf903f391a1a0784f1c`  
		Last Modified: Tue, 05 Oct 2021 22:24:37 GMT  
		Size: 573.9 KB (573889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
