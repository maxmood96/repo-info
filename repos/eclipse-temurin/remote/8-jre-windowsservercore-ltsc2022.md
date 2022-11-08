## `eclipse-temurin:8-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0f3f1e94c1505d7d403e3bbb315defb3b50c6aafcb2f78ff6ca89b71933840fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1249; amd64

### `eclipse-temurin:8-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:83c13a8548053b24706bfdebf895116540876b7cb0badd77c0b105449e563b78
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2553439062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4501974a10ecb42f7660cfbc2f38c80fd892ad414c4d83ba72f2b64a58015952`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Tue, 08 Nov 2022 18:28:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Nov 2022 18:28:40 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 08 Nov 2022 18:39:02 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_windows_hotspot_8u352b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_windows_hotspot_8u352b08.msi ;     Write-Host ('Verifying sha256 (27bc5324a8d684e6afa286029c64e4d90e12d4f0b947093865b6c78ac83bd6ee) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '27bc5324a8d684e6afa286029c64e4d90e12d4f0b947093865b6c78ac83bd6ee') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 08 Nov 2022 18:40:12 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276673195ed11807395b0da51ac20ef31c925ce955c29ad1bab54f14617c25b`  
		Last Modified: Tue, 08 Nov 2022 19:41:53 GMT  
		Size: 1.0 GB (1007770983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3becc14271944025e3fa6c2ef2689bdfbf09bfc54ec339115d3082df315898e4`  
		Last Modified: Tue, 08 Nov 2022 19:38:57 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921d083ce3f0b724ae334f8a9aaf84b35c3f79393bb913548e4cbd194681944d`  
		Last Modified: Tue, 08 Nov 2022 19:38:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59264ee4ddbbda5784e917e2db28a57b0651bcae0a5c371ef22496998ba658`  
		Last Modified: Tue, 08 Nov 2022 19:45:47 GMT  
		Size: 71.1 MB (71108388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0ba4919765dcd623f1cfb783fb58edcf8014cc8f547543eb535e052074e2ba`  
		Last Modified: Tue, 08 Nov 2022 19:45:37 GMT  
		Size: 559.2 KB (559178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
