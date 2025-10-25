## `eclipse-temurin:25-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c442f44c8564a10221a6a56a8df9abe680a69ee9a6be53d2cfc44af82e85476a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:25-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:6bf1d57f59ed86d005f66a45865a7db21e4309a989a654bd4b06a945357d0c46
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1831208929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a5d246d6df582e8d5f13e632b3b4c6c160bdd34ed9ac245a241dcbeb4be5bd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:22:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 24 Oct 2025 18:22:55 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_windows_hotspot_25_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_windows_hotspot_25_36.msi ;     Write-Host ('Verifying sha256 (d899afd9c8160b8de9dcf2cced8da33702e00104068eac50e33dd1cbf1df5248) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd899afd9c8160b8de9dcf2cced8da33702e00104068eac50e33dd1cbf1df5248') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:23:03 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:23:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ef8febcbf9af9e2408e6ddf43ec9a58526e8eaf2f7ea79ae22a8a1001154c1`  
		Last Modified: Fri, 24 Oct 2025 18:23:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1595f5bcad7beb54d3f6ad9d149860e22280bc6607fa55ee04996ea389cb6be`  
		Last Modified: Fri, 24 Oct 2025 19:23:18 GMT  
		Size: 253.7 MB (253650737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3886a827776dff69e18a05bd4391bd55f6db7464c3b70cdb1582c4bdca5575df`  
		Last Modified: Fri, 24 Oct 2025 18:23:30 GMT  
		Size: 361.3 KB (361317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61476fecd869cfedcbe0eb00897d7938c31e2ad6c1f574f46760fd6c6cd0adb`  
		Last Modified: Fri, 24 Oct 2025 18:23:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
