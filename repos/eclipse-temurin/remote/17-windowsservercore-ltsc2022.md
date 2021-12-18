## `eclipse-temurin:17-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b6d82b6485ff115e55b98a6414ba969dbacd4b3c963927520e617945e3699f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.405; amd64

### `eclipse-temurin:17-windowsservercore-ltsc2022` - windows version 10.0.20348.405; amd64

```console
$ docker pull eclipse-temurin@sha256:b1bb246040309d035f0633fe3f0b7e0796ede0c6de36a2913e3c895bfc02f01f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2543755504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e77f421fb4dfff68fa04b9ea0b13a936472e3f582c55381fe7c87f01a0e484`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 08 Dec 2021 01:54:07 GMT
RUN Install update ltsc2022-amd64
# Sat, 18 Dec 2021 00:09:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 05:53:25 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Sat, 18 Dec 2021 05:54:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_windows_hotspot_17.0.1_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_windows_hotspot_17.0.1_12.msi ;     Write-Host ('Verifying sha256 (f5241bb43b589e45b6c3133fae6cc8cbffec4cae2504c3b99c3fac0c50cbf11e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f5241bb43b589e45b6c3133fae6cc8cbffec4cae2504c3b99c3fac0c50cbf11e') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 18 Dec 2021 05:55:06 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Sat, 18 Dec 2021 05:55:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4d1d74adc6a92e44b3cd592ec9459f1fff926eaf6fc20bb7526360bec71aefc0`  
		Size: 939.1 MB (939072515 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5bc74beb7593c703ac99379d225f3a9a445549cc06a3fe18f44e356a45f225f3`  
		Last Modified: Sat, 18 Dec 2021 01:18:31 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb53896bf00a46575aab4e27a301422c98efbdb0e8d13f5b4a33dd93d5d07cf3`  
		Last Modified: Sat, 18 Dec 2021 06:32:48 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b8dad237fa5da3b7d741eea642dba83734758af7e91014478ffd499ecee4d7`  
		Last Modified: Sat, 18 Dec 2021 06:39:10 GMT  
		Size: 352.4 MB (352421058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2016534d506beee0fcd06e6d9fc8910656356d19453ac77116ccadf99b04dc19`  
		Last Modified: Sat, 18 Dec 2021 06:32:48 GMT  
		Size: 558.6 KB (558590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0c3b86960b95875655453c47f244b3d825277728f7e021447f442a2a809058`  
		Last Modified: Sat, 18 Dec 2021 06:32:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
