## `eclipse-temurin:8-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:5a1e193e567e0a6cd358632d55af48f43d8f20118d1493d0125050c33f9f4006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:8-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:887362407e5b55523dd6b133f11a8a4b2107a188dd5194cef77cc5d331f3ade2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2429337881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f86348c3d8505820962af615f0d566d2f7e8a99098daa74d3fcb0568ff467d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 16:36:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 25 Jul 2024 17:16:20 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 25 Jul 2024 17:17:39 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_windows_hotspot_8u422b05.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_windows_hotspot_8u422b05.msi ;     Write-Host ('Verifying sha256 (9944b308061827c8ad26bedd573eac334c12eaa72c8b7f5ee73a5795e7710204) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9944b308061827c8ad26bedd573eac334c12eaa72c8b7f5ee73a5795e7710204') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 25 Jul 2024 17:18:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:924fabd8f7ce548572e59eee69b136ebaf16c4342fd5f54c83655bce8541a28a`  
		Last Modified: Thu, 25 Jul 2024 17:29:52 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da3e6c1ae9cc5b89c6eb6365d0c533c555eafb476658020e36f68bf2bde1991`  
		Last Modified: Thu, 25 Jul 2024 17:30:06 GMT  
		Size: 190.6 MB (190618539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aee53b5e03f413bb77db8e0740e6d80ab207d85a3e00055ae4df24a99084920`  
		Last Modified: Thu, 25 Jul 2024 17:29:52 GMT  
		Size: 287.1 KB (287114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
