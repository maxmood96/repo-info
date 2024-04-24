## `eclipse-temurin:11-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:bd5e47ae7652ea5f3a2ea0d11b7d28b978952f9258ee77994b51bdbc342e622e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:e7614c98ea9867f08cf633a9adf40d65978dc5c51954caaa1c6adc8964c49e8b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2368997575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f325eb201837de3b2c2251cd4266bc5516d2136bb5bce7dcb6b2f2a757e72fc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Apr 2024 18:36:26 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 24 Apr 2024 18:37:25 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.23_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.23_9.msi ;     Write-Host ('Verifying sha256 (cacbe31a3921e52f4ff6d031d6f37d8a7c58f20a136fccf1754565f8aa403ed8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'cacbe31a3921e52f4ff6d031d6f37d8a7c58f20a136fccf1754565f8aa403ed8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 24 Apr 2024 18:37:47 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 24 Apr 2024 18:37:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f372a5b1abfde365dd4ffaf2f4dca445b95eb0d5920e11341f29fb3f79e8e0f5`  
		Last Modified: Wed, 24 Apr 2024 19:34:42 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260d0fe3126e8ee0c6cc30a96b22b6c9e811155b382f7cd72ef0593817076700`  
		Last Modified: Wed, 24 Apr 2024 19:35:12 GMT  
		Size: 369.3 MB (369331227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92657472bdfb0cbcf6da6eb677e9afd2eba24e1d073b705c3f3a9b362aa82f75`  
		Last Modified: Wed, 24 Apr 2024 19:34:43 GMT  
		Size: 288.7 KB (288660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec9263122e0c4aa8eca147b445857882138b96b2c4cd9dd94be17293908acd7`  
		Last Modified: Wed, 24 Apr 2024 19:34:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:a5b3e985a2c0caa5d1cafcc0afc17fb27e2141f109651fbc17f84b2d0153d08a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2534125023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407086c321c96a421141126647b10b02cfc1d2699194a5e6b29dca04ea1cf19d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Apr 2024 18:37:56 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 24 Apr 2024 18:40:00 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.23_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.23_9.msi ;     Write-Host ('Verifying sha256 (cacbe31a3921e52f4ff6d031d6f37d8a7c58f20a136fccf1754565f8aa403ed8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'cacbe31a3921e52f4ff6d031d6f37d8a7c58f20a136fccf1754565f8aa403ed8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 24 Apr 2024 18:41:30 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 24 Apr 2024 18:41:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391e481e0de825c3bdcfa9b146aec20f197bd9ff469a64bca118ab043b255aad`  
		Last Modified: Wed, 24 Apr 2024 19:35:23 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40294493eedf1581e638da7c48a6f07f06d24b4d5cf20720ba63d4f8165b9f4`  
		Last Modified: Wed, 24 Apr 2024 19:35:50 GMT  
		Size: 369.4 MB (369385949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50fd987433e3d53bad929bbc6a33fa877a40521e4afa38d4eccde3a8b3cad81`  
		Last Modified: Wed, 24 Apr 2024 19:35:24 GMT  
		Size: 306.8 KB (306846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875f66aef4da961a15698b9b7b941bf11761887b361d024c7134ebaf3a2ce9a4`  
		Last Modified: Wed, 24 Apr 2024 19:35:23 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
