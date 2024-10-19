## `eclipse-temurin:8u422-b05-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:2096431b4aaf7d3cfc8da75073a8b50e18a6c3fe323787a4a861abde85a6397d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:8u422-b05-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:a243b2b3c3689b51085f2c6d15729ad32993e8e4dfffab86a88a567c3c7db02e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1990304011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514943caad5de8aa3cdb430ab4f0caff4e5cb53b28207a8e64252f6a0724acf9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Sat, 19 Oct 2024 00:54:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 00:54:48 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Sat, 19 Oct 2024 00:55:50 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_windows_hotspot_8u422b05.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_windows_hotspot_8u422b05.msi ;     Write-Host ('Verifying sha256 (9944b308061827c8ad26bedd573eac334c12eaa72c8b7f5ee73a5795e7710204) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9944b308061827c8ad26bedd573eac334c12eaa72c8b7f5ee73a5795e7710204') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 19 Oct 2024 00:55:56 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f056a8359be18bbc6af85dbb189709024eb0b8777a4a0099871b4af39c2a10`  
		Last Modified: Sat, 19 Oct 2024 00:56:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1baa4d791a4bc9631b1bc355d43cfec99d766a48768185c80bf55eb39099f17`  
		Last Modified: Sat, 19 Oct 2024 00:56:00 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17352cb9d8af34f10563ce96186b8f3b1ba8da395f6fa812397222329154f609`  
		Last Modified: Sat, 19 Oct 2024 00:56:08 GMT  
		Size: 190.6 MB (190633944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cb19ab0f675960a1f175895a932d421c7e464ed92e066710c335ce2c136a58`  
		Last Modified: Sat, 19 Oct 2024 00:56:01 GMT  
		Size: 326.0 KB (325954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
