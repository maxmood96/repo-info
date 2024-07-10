## `eclipse-temurin:21-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:80ee7dfff1fbc45ec413ba383ca7641def723ad6909a6421b09a11148003191b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:21-jdk-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:2d6a9af103edff5f2f48ea10811e73104824448076762068bfe00bcaeebba521
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2520347195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d300324c7956238d77cc830f089011d0f45b3237639179ebb23872d718ba9ced`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 16:34:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 16:59:27 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 10 Jul 2024 17:00:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ;     Write-Host ('Verifying sha256 (264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Jul 2024 17:00:40 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:00:40 GMT
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
	-	`sha256:d44dc67eee22d9275a97ac90323c52d303feb0d6dba5a17fd827eddcd00e96b7`  
		Last Modified: Wed, 10 Jul 2024 17:33:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f015344b325d0254db29ebec8dcfc49c955f43ac3f490dfc4c66a663a2aff9ec`  
		Last Modified: Wed, 10 Jul 2024 17:34:20 GMT  
		Size: 380.5 MB (380464055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b4419d5a840497256def60a8605c0698c5413f7730baa49e8bbc19f779ca4`  
		Last Modified: Wed, 10 Jul 2024 17:33:57 GMT  
		Size: 278.6 KB (278591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f206e5c739d454cf868c60b4ee6a90023be3ab9cd581b80066fdc783766c2e`  
		Last Modified: Wed, 10 Jul 2024 17:33:58 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:5d18fa7a6e26769ed63c04c1486322643c89618002c002adb9b34d556208e27a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2623093630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67a7e3ad3d3bb9ca0651abc7b0824e022d7b1bab765e38b43e7c6a3b04771c2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 16:36:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:00:54 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 10 Jul 2024 17:02:41 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.3_9.msi ;     Write-Host ('Verifying sha256 (264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '264db89e74213f3ea2d7b7379d1c2ac346797d03b4d88cbf4ce72c3ff96477a1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Jul 2024 17:03:47 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:03:48 GMT
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
	-	`sha256:44a40161a8a2f495e572c2ff2787e080da16e6b3e631e9b8da24d2c98214b895`  
		Last Modified: Wed, 10 Jul 2024 17:34:30 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72d4b46f994d488c7545693b1cbdd27fffcace8f97c5e80e6817bd07330ad19`  
		Last Modified: Wed, 10 Jul 2024 17:34:54 GMT  
		Size: 380.6 MB (380635893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17f4504f99f1821d702b6506d8484860b9b2907058741a2089517b6c0efa668`  
		Last Modified: Wed, 10 Jul 2024 17:34:32 GMT  
		Size: 4.0 MB (4024086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc2cb075c24032f5253e0a63373fdedb3f37c108445345d545a2e07529c8cbf`  
		Last Modified: Wed, 10 Jul 2024 17:34:30 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
