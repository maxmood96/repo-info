## `eclipse-temurin:24-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:198dc7d13ad0552f1b6756b6a2b3c50705e0c5d635ee1ebffeee7ae18226d109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:24-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:9013ff6ae2c0d31f15daae94f5140e6826468377c150e9ed15cb17f5e4b0017b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3824292079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d873de19b0bb1b4a13e4485423ce2370a672a9f40019fcaf1a965575e4f1a69f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:48:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:57:08 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Wed, 10 Sep 2025 21:57:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_windows_hotspot_24.0.2_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_windows_hotspot_24.0.2_12.msi ;     Write-Host ('Verifying sha256 (be608fa0c8a0b106b2051fbef941e8021d53d799d22172719b8f8b1eef4b361c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'be608fa0c8a0b106b2051fbef941e8021d53d799d22172719b8f8b1eef4b361c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 21:57:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:57:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae601f0777b06a06d8faad18910ce906d57fb27de067d609e4022dde683f85b1`  
		Last Modified: Wed, 10 Sep 2025 21:57:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a5047bd335d88a5d22421671d426fc8a9100fba67e325ae0e27d579090afa3`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a044e4c5e68398ec5f127c5273b28185339eab6076d42700ebf8a084e19d2ea2`  
		Last Modified: Wed, 10 Sep 2025 22:20:04 GMT  
		Size: 252.5 MB (252497986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91296cbf1248ea445975a2b3a2eccb1ccc05ca7bb730e1d3d4b0597f7ab939e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 350.4 KB (350440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204cc581ccc61ad480ce8037a7b3015c5229b665f0ca6a47e9d9b2f6f3b4cb09`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
