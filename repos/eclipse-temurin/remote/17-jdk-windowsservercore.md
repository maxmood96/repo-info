## `eclipse-temurin:17-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:9f664f5da4bcde43d56a106b7d37878bee9e2bb57c57e5b6a379a3e6655f641e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:17-jdk-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:3a79ee6457ca660437fb8cd511c5353674e0f92a2acb2cfd74b04b57492c3fd0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2495073712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d537d2d8148eab12982e1104879cb47e2fb83bfbcc5e9f3a5c6c0069076363c0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 16:34:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 16:51:07 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 10 Jul 2024 16:51:53 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_windows_hotspot_17.0.11_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_windows_hotspot_17.0.11_9.msi ;     Write-Host ('Verifying sha256 (99ad599eea572207026f2b85159ef4ec06c620cee88662ea108f0013697b0365) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '99ad599eea572207026f2b85159ef4ec06c620cee88662ea108f0013697b0365') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Jul 2024 16:52:11 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Jul 2024 16:52:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d9de6992053b5598e6e6ffdf2a54d935d71057f5cc79ff86d167df37475ed8`  
		Last Modified: Wed, 10 Jul 2024 17:24:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c9319abca7932f83ef0014a5e4aa12b772428d475d6678faf1d6930f7becc6`  
		Last Modified: Wed, 10 Jul 2024 17:31:34 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e156e1addf67cceef4fd0fe1d0740f73cf4fbc24fafb455cdcfa28cb75aaee`  
		Last Modified: Wed, 10 Jul 2024 17:31:58 GMT  
		Size: 355.2 MB (355179262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfb27bc2a87135e1117e105a7885b9eace52b5bdf567e114b6be380d1712933`  
		Last Modified: Wed, 10 Jul 2024 17:31:34 GMT  
		Size: 290.0 KB (289962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908280284fe3feb2ffa17d929c53e2713ebdbf28da11aba44b5689daf9a4f474`  
		Last Modified: Wed, 10 Jul 2024 17:31:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:b8e295dd6fe5a4ba426a2b54520b660dbfd91e1ea4f8d813e633ad122fe9d350
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2597590876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ee1cdd46657c16b7fd51a2b5abba218fe704aafb974b3a8642a2c25a68d0fb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 16:36:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 16:52:20 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 10 Jul 2024 16:53:44 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_windows_hotspot_17.0.11_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_windows_hotspot_17.0.11_9.msi ;     Write-Host ('Verifying sha256 (99ad599eea572207026f2b85159ef4ec06c620cee88662ea108f0013697b0365) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '99ad599eea572207026f2b85159ef4ec06c620cee88662ea108f0013697b0365') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Jul 2024 16:54:41 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Jul 2024 16:54:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396e1b977f1ec2790de6e1bcdd9b0272d3ab46f70fdbef2ae277b7f99b83d0b3`  
		Last Modified: Wed, 10 Jul 2024 17:26:34 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a488ad333e51ffec50d7476cedf61ef50c0ab94b8e3e082dffa3d8805c9b3f`  
		Last Modified: Wed, 10 Jul 2024 17:32:09 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126cebbdd627b577f5fc0ba0dc0057d0c58620186b69d2c451e6db420245ba3d`  
		Last Modified: Wed, 10 Jul 2024 17:32:31 GMT  
		Size: 355.3 MB (355347898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba91c115882b8a96513d6149bbe9989b1e04a916bc39233237825fa3abd3f7`  
		Last Modified: Wed, 10 Jul 2024 17:32:11 GMT  
		Size: 3.8 MB (3809362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd31362902f19e1062c218cb18f68c3e6152401744cb8021c04e88f7298729aa`  
		Last Modified: Wed, 10 Jul 2024 17:32:09 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
