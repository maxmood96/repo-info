## `eclipse-temurin:11-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9d2fc847f019a148fe50bac2543355372701d9237e3b0561ccead72cf8e402f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1249; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2022` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:03490e015eefb6b774cf6ae062b424f8fe259cf4fc63e7a45308821bb90b9945
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2848816372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8c363059a8bd6b46fc1c15bfb7f5800c4f16b682c45a0ab53baaaa9e030901`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Tue, 08 Nov 2022 18:28:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Nov 2022 18:44:10 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 08 Nov 2022 18:45:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.17_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_windows_hotspot_11.0.17_8.msi ;     Write-Host ('Verifying sha256 (9b74536f2475b67e53c83ecf41f80ac9f1ba29cef91c6e261e10d1223da42d69) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9b74536f2475b67e53c83ecf41f80ac9f1ba29cef91c6e261e10d1223da42d69') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 08 Nov 2022 18:46:37 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 08 Nov 2022 18:46:38 GMT
CMD ["jshell"]
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
	-	`sha256:d78a4b974546d14f26166fdc4db4761a851f37346016fe90e815d7d342d7df0e`  
		Last Modified: Tue, 08 Nov 2022 19:46:34 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d26531911060f1b66d4e63623e1f54721b44610415e6c511f385bb8c6e1a1c`  
		Last Modified: Tue, 08 Nov 2022 19:47:06 GMT  
		Size: 366.5 MB (366484447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdb5d0bca946caab9f12a9c5037bb838082ebf48a20b8b1349c8578ab1620b9`  
		Last Modified: Tue, 08 Nov 2022 19:46:34 GMT  
		Size: 559.0 KB (559049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe6abbdd80dcded97d26105ffd28e2ccfd41b7e59dc679440d1974faad6c02`  
		Last Modified: Tue, 08 Nov 2022 19:46:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
