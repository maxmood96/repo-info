## `eclipse-temurin:8u432-b06-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:9d8345c3412bb3848906db456e0a6d36eabbb1cfedad76ca3c6dee1f1101ea74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:8u432-b06-jdk-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:d36d2cc509725232e330374c2370c2064c953e0f1b74f9f1ffdf8cb1879a5390
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204247474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fac120fed93978718dc9f41a7358a8f16e2259accba5edcbe262211127a5d3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:13:30 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 14 Nov 2024 20:14:08 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u432b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u432b06.msi ;     Write-Host ('Verifying sha256 (c9280205858928756374d930d4b539c59b1cb470425d2cf300b943c56efe4d86) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c9280205858928756374d930d4b539c59b1cb470425d2cf300b943c56efe4d86') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 14 Nov 2024 20:14:16 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02920fd26383c9b394738e338b4e3b6c8b6e4807c4254529ab03f9abe749e62f`  
		Last Modified: Thu, 14 Nov 2024 20:14:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33486ccf5c7312a037ff8f9e92f44eaa6d134c86e1f36001fdda18c1257cef8`  
		Last Modified: Thu, 14 Nov 2024 20:14:20 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14a787d68f8ed9ddd91a2d534496ff15e4ad50d47700421c90fe3ebf9e12427`  
		Last Modified: Thu, 14 Nov 2024 20:14:30 GMT  
		Size: 193.3 MB (193253553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b94c54df81e06b94e3bcd6324fbb531773190f86726ee01a4bdc937b2dc4db0`  
		Last Modified: Thu, 14 Nov 2024 20:14:21 GMT  
		Size: 337.5 KB (337547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
