## `eclipse-temurin:25_36-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:3f1a991a4ca279769a85d3033cd61d3d049d8231b57c3a74c87e73c3e58ed72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:25_36-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:7e3f32b9b4440f22d18a6ff2b7716d2c59b65154f5683289b8fec337eb85ff37
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3825319453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eaddb3ec628b512ef22f4070ac772e7aeb954a161dc7de3b2937075015ae757`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Thu, 25 Sep 2025 20:56:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 25 Sep 2025 21:19:05 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 21:19:41 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_windows_hotspot_25_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_windows_hotspot_25_36.msi ;     Write-Host ('Verifying sha256 (d899afd9c8160b8de9dcf2cced8da33702e00104068eac50e33dd1cbf1df5248) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd899afd9c8160b8de9dcf2cced8da33702e00104068eac50e33dd1cbf1df5248') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 25 Sep 2025 21:19:47 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 25 Sep 2025 21:19:48 GMT
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
	-	`sha256:978e634536ba7ab9f22bc6e667c8b6f3dcc8f2fa26b00b1ed3f39e9198248252`  
		Last Modified: Thu, 25 Sep 2025 21:13:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b613e773d38fab1691730d403798e6dc4967808e0b858d88af657f0a8039cf`  
		Last Modified: Thu, 25 Sep 2025 21:20:17 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cc0bb4924261f985549fdaf0cc122d09c94fc6c1c1789b6888aa0e2fc7c806`  
		Last Modified: Thu, 25 Sep 2025 22:14:45 GMT  
		Size: 253.5 MB (253517178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c462468b115203c7fe5177e5564e80ccc2f3e9863851d7778c4d2127b4b131b3`  
		Last Modified: Thu, 25 Sep 2025 21:20:17 GMT  
		Size: 358.6 KB (358621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3226d5830a3698c432d0ec74586aa8b20d648b46386afd915acfe38c504e2c`  
		Last Modified: Thu, 25 Sep 2025 21:20:17 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
