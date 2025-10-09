## `eclipse-temurin:21-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d4856e87c1a7091c5e5c53f1fed6d283c15ca404bc4efab1328ceec3d8b0cb2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:21-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:1bfb6ec6d2ebb77775ecabe32c20cff5618f229980e42bdc84e12d37f349b13e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 GB (3952286569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe81d37bd475a0b38776e8320b3d214241c5218abd6381c64bddc7d9e2bbd93`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:48:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:56:26 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 10 Sep 2025 21:56:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.8_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.8_9.msi ;     Write-Host ('Verifying sha256 (d82030e8689b19efedfbce50ce38351ca81b302c06936584c6a27bda18339df8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd82030e8689b19efedfbce50ce38351ca81b302c06936584c6a27bda18339df8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 21:57:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:57:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b46f99bf24fa286feb298caca522f226b7edcadf9f5fbfe6ced69e99e66309a`  
		Last Modified: Wed, 10 Sep 2025 21:56:35 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ad3a2ed81b99f34c9287f412ada811174e5d4d80adcd3f6e6d39e48f4681b6`  
		Last Modified: Wed, 10 Sep 2025 21:57:45 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40ff2ff0a1d45ed7379a2fdc955c95139d04209a73d925404d2a534775bbda2`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 380.5 MB (380493377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5613621d62d41a0921f4b494ffc5ad061c55051f8befbec5e670caff4baf9f7b`  
		Last Modified: Wed, 10 Sep 2025 21:57:45 GMT  
		Size: 349.5 KB (349516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db39e2abfe81c31da574a2fd6a26b5e9a376edb8df7b0c9fe6fab8b6c59f1cc`  
		Last Modified: Wed, 10 Sep 2025 21:57:45 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
