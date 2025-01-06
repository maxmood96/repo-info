## `eclipse-temurin:8-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:2e37051d708513982449ce56f43774efb62b66186601e39b416559fc9558421d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `eclipse-temurin:8-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:c7964a47dacade402af948659c025c9ef0bb319e82ab39160af685f9d94b4cc9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327534590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1043fed3f3973816c9c87bfaf2d29509afa700c20e5c6601a55dd5bafcf0453f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:39:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:39:22 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 11 Dec 2024 20:39:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_windows_hotspot_8u432b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_windows_hotspot_8u432b06.msi ;     Write-Host ('Verifying sha256 (34801770278c26045517fc1851396d7bf66c7c32fa6f9965b968d55adbebda4b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '34801770278c26045517fc1851396d7bf66c7c32fa6f9965b968d55adbebda4b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Dec 2024 20:39:48 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5e729112f52984fd520b2ed4acab0cbc243fac133919e0cbb14f3cda894f34`  
		Last Modified: Wed, 11 Dec 2024 20:39:51 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6013f9939b1c3f130029107b6bea051ac3f9f0057d928775368fac9004397e`  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9039e9153caab2d23aea8878880b7bfb6b22540b4914773a5aaa425a98e429c`  
		Last Modified: Wed, 11 Dec 2024 20:39:56 GMT  
		Size: 73.3 MB (73296424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283c38ebe2c52918512b4638f66585a6a6efa9067cbbb8afee8852a094cdd43b`  
		Last Modified: Wed, 11 Dec 2024 20:39:51 GMT  
		Size: 362.0 KB (361968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
