## `eclipse-temurin:11-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:19f06554f4714e4d67d881b07702f94ccca46617268520ee077b038c8c76e68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:11-jre-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:112a9b6735d5e662069eafa557a3b8cb51462499c568c03dcefe376670b727d8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313540327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b1a3247a9ee722bcd786ad19adb9cf6798bf2d6ff3f7669ff81c77704ecbdb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 16:36:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 10 Jul 2024 16:49:31 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.23_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.23_9.msi ;     Write-Host ('Verifying sha256 (6699a78e61c0d8208a6d43a3b4590fbabf77bb1c1b8b30d8140e62804fa286cb) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6699a78e61c0d8208a6d43a3b4590fbabf77bb1c1b8b30d8140e62804fa286cb') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Jul 2024 16:50:27 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:0b4442396053a6a8a1be361aae1a21ab5dbe0ee9714974622f5d4f17fd5dad79`  
		Last Modified: Wed, 10 Jul 2024 17:29:48 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae0432587f9f5b49ad67ce2be21503bc00d03a3458c121011caab03ed12aed3`  
		Last Modified: Wed, 10 Jul 2024 17:31:11 GMT  
		Size: 74.8 MB (74808547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdd58b6059547657b6807bfd47d28ff78b58ec18e6b91164e5ee51a8e3f0c9b`  
		Last Modified: Wed, 10 Jul 2024 17:31:03 GMT  
		Size: 299.6 KB (299563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
