## `eclipse-temurin:20-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:3803d1106d1398098ddcee945faed81e7fa3d18931a99b71492e3fad2d319ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:20-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:7082f433e1e95b79332d78d28e349eb606093a2e760b36f5a681c331158f18a8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2369906893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80cd63912290bda8eb5092a015403339c9b5e689e59d81bdd072008304eb636`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:03:51 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Thu, 10 Aug 2023 00:05:29 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_x64_windows_hotspot_20.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_x64_windows_hotspot_20.0.2_9.msi ;     Write-Host ('Verifying sha256 (703be6194d2ae3fc90870497417e22a72ba9a65995aa84b63bca4f4e1fb8395a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '703be6194d2ae3fc90870497417e22a72ba9a65995aa84b63bca4f4e1fb8395a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-20' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 10 Aug 2023 00:06:33 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 10 Aug 2023 00:06:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d67511feb7dd186e3a60bc9e347fddab421a33169b1eaa67a701c13be1e589`  
		Last Modified: Thu, 10 Aug 2023 00:28:33 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6577df7230cc5fa80f8b8abed481d43fe049ac3346ec4d14b58eec2910233fd`  
		Last Modified: Thu, 10 Aug 2023 00:29:02 GMT  
		Size: 370.0 MB (370023526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65389f0c068d438a264b33588ce780f82f65cf0b081287420a31ed055a199279`  
		Last Modified: Thu, 10 Aug 2023 00:28:34 GMT  
		Size: 3.9 MB (3923836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95547aa0e997e406f0d383a3c1930761f5388ff3b637c0e7ae46a89a3baf615b`  
		Last Modified: Thu, 10 Aug 2023 00:28:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
