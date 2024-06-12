## `eclipse-temurin:11-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a5c7586b4517cebcd346489e2e1845ce5ec312a47956419ff0edd0a5df3a7409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `eclipse-temurin:11-windowsservercore-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:75645ba2f85f205162ee139e1f067422977851c8c0572ab2bba6e35709940457
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487654367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad70b5a91b924d38b8e16bc2f82d4e9db034098aabe3ec417a204993901730c8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 17:36:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 17:46:19 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 12 Jun 2024 17:47:14 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.23_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.23_9.msi ;     Write-Host ('Verifying sha256 (cacbe31a3921e52f4ff6d031d6f37d8a7c58f20a136fccf1754565f8aa403ed8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'cacbe31a3921e52f4ff6d031d6f37d8a7c58f20a136fccf1754565f8aa403ed8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Jun 2024 17:47:34 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Jun 2024 17:47:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045fa3135d89819dc64e63c6fd4e832a9b86fc2d37e11e64d811218c4a684924`  
		Last Modified: Wed, 12 Jun 2024 18:36:56 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a0aae7d2a042c66ad7298f6fea8fe9711ecda4223a6f37b3b73b61ae81e8d`  
		Last Modified: Wed, 12 Jun 2024 18:42:07 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9397672799de3d4bfca22f17561ebea92d68b85896fcadd636bb195b7ff7452e`  
		Last Modified: Wed, 12 Jun 2024 18:42:35 GMT  
		Size: 369.2 MB (369193570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae69b468daa75f6ab34f808de7ec254b1f7d7450bac1465de24355cd72f6ce0`  
		Last Modified: Wed, 12 Jun 2024 18:42:08 GMT  
		Size: 278.0 KB (277958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a3b9842fdb848a1ea9a243bc5069453bdd385f730d9be5f5caded669d04867`  
		Last Modified: Wed, 12 Jun 2024 18:42:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
