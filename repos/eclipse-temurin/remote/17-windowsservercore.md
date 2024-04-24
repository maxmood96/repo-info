## `eclipse-temurin:17-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:e13d10d71578fbe575f9507c4db3572091e538df3038f27a02a350c1eb7b5aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:45f998d8898de40884d5e4143241010c69eb6ac9237caef54aec0daac9e8587d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2354962605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49840bc7c1ff64e71a8cbfb94c1bd84ef797995c52aba6fa684a088185f437e0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Apr 2024 18:47:52 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 24 Apr 2024 18:48:55 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_windows_hotspot_17.0.11_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_windows_hotspot_17.0.11_9.msi ;     Write-Host ('Verifying sha256 (99ad599eea572207026f2b85159ef4ec06c620cee88662ea108f0013697b0365) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '99ad599eea572207026f2b85159ef4ec06c620cee88662ea108f0013697b0365') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 24 Apr 2024 18:49:18 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 24 Apr 2024 18:49:18 GMT
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
	-	`sha256:6e6848cff0d3a417e34e0af02484770f9988ef235f3e0b09ab1c5ad3d5b626aa`  
		Last Modified: Wed, 24 Apr 2024 19:37:27 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09378ed114e42dfab66e5f76833e451968d7e216bd5feef7ba1cbf9389cdeb4e`  
		Last Modified: Wed, 24 Apr 2024 19:37:54 GMT  
		Size: 355.3 MB (355306099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318bcb4af02cb14aca4fbdb270c8624e4fb8ad595aaa54dca7edb4fde04455ec`  
		Last Modified: Wed, 24 Apr 2024 19:37:27 GMT  
		Size: 278.6 KB (278649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb1eb9d8cd15d9b09bf6faac61713d49859fe3d51eb2071015bfbf858a6c39a`  
		Last Modified: Wed, 24 Apr 2024 19:37:27 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:15dbb8f94bdd1a1ad41864de70407509febfb7642bc2bcb161d98b17bc7dd0c6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2523619536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719aa3bec366eaa01baa6ee9cb6366fbb41212041413da36653985d561db6c96`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Apr 2024 18:49:35 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 24 Apr 2024 18:51:40 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_windows_hotspot_17.0.11_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_windows_hotspot_17.0.11_9.msi ;     Write-Host ('Verifying sha256 (99ad599eea572207026f2b85159ef4ec06c620cee88662ea108f0013697b0365) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '99ad599eea572207026f2b85159ef4ec06c620cee88662ea108f0013697b0365') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 24 Apr 2024 18:53:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 24 Apr 2024 18:53:10 GMT
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
	-	`sha256:0ad79c591b0b60061ca84ca875a79b8e11c69625ce8ffe978f216f4f79e12c86`  
		Last Modified: Wed, 24 Apr 2024 19:38:05 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34f57640785e1f7323195670c754faaa2f90bc6a661167fb4cb3504231c46de`  
		Last Modified: Wed, 24 Apr 2024 19:38:32 GMT  
		Size: 355.4 MB (355364530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feacb3a5ebef54b6eec0dfd9e0dafaa0439b4d995e1975ceee529992bdefd74`  
		Last Modified: Wed, 24 Apr 2024 19:38:07 GMT  
		Size: 3.8 MB (3822816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd91df8470ebb4cdcb67abccf6e6b2afe416bc0352c0c1425e2c6e5129e6cc`  
		Last Modified: Wed, 24 Apr 2024 19:38:06 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
