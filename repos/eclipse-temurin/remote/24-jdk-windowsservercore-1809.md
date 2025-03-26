## `eclipse-temurin:24-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:98d5edc293135382bf4b1b8d924e467b1ced1309cbe88eac1a3c77b94ee5fc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:24-jdk-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:7d0e608d2e22cad27aad6678e39a7158497573af11978e33a433e295c410da4a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408831087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97491b26a4ae456f67a1f09095888871df096a8a04c45c886240e67df71859d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 22:04:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 22:04:51 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 22:05:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 25 Mar 2025 22:05:55 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 25 Mar 2025 22:05:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0b8b832f17bf00c30c823e66a45c6e1a99cb9d5324e71a48f21d92a9644d4e`  
		Last Modified: Tue, 25 Mar 2025 22:05:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64b775844c68bb12475a0f37f2ccc41af2c4d644c9f29f57b171e0e918b2213`  
		Last Modified: Tue, 25 Mar 2025 22:06:00 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe8a87aae7048a2eba83fd9b87674cd123a2a6f78b7e6fc0d7d68a74c18a141`  
		Last Modified: Tue, 25 Mar 2025 22:06:13 GMT  
		Size: 252.5 MB (252539268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184b0c323b01f90d196020c287c215d608e9756b7d8629b249f2a700c4d08aef`  
		Last Modified: Tue, 25 Mar 2025 22:06:00 GMT  
		Size: 4.7 MB (4653294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9125f8b979f51d4d75cd073228028c774ebfb4f1dbc5d6128a25152c45547e`  
		Last Modified: Tue, 25 Mar 2025 22:06:00 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
