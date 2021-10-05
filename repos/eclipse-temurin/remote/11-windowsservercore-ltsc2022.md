## `eclipse-temurin:11-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c8470ce05bd62b4d37bb22134976f3e680d441d97c02bc39613294a942109b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.230; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2022` - windows version 10.0.20348.230; amd64

```console
$ docker pull eclipse-temurin@sha256:1b33b5c2ef914dfcd1ee2df6022ebb4fbcc2842b1092dd3b6bc16f74a892df58
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2491282547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ef4535ac76debde11ed185168dec532d1c5ce3bb9f01c76941b4e1c000b824`
-	Default Command: `["jshell"]`
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
# Tue, 05 Oct 2021 22:12:54 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.12_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.12_7.msi ;     Write-Host ('Verifying sha256 (80546d8a36ad0cdf69305f72f42465093b9d0388f45819b05cc640ecd1310b32) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '80546d8a36ad0cdf69305f72f42465093b9d0388f45819b05cc640ecd1310b32') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 05 Oct 2021 22:13:23 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 05 Oct 2021 22:13:24 GMT
CMD ["jshell"]
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
	-	`sha256:913dfab36a37863753da5a89f48614be1a4ab6677594fd5abb9ed31fe25abaf4`  
		Last Modified: Tue, 05 Oct 2021 22:26:39 GMT  
		Size: 365.8 MB (365830561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca1696413b6175d52b888d58fbb98dca977e0b68b6e4d28b7d6f61da1df4c81`  
		Last Modified: Tue, 05 Oct 2021 22:26:09 GMT  
		Size: 573.3 KB (573288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9291b50751fbbffa59b457dfcc75468bd6b100f2aa3c78ae9dfaca92e737010`  
		Last Modified: Tue, 05 Oct 2021 22:26:09 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
