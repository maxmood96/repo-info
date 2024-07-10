## `eclipse-temurin:22-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:9c44a0fbc63228ead9377ec2e1c30ac2a3866e19e1a58e65d491653c5ecce404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:22-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:4b2dacea273f0219010b33c0b84a58b7a508599703fb8cc20ab7724fa241da30
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2519791068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee6dbb2211314de6c9869d736c178474f25476bdb07b241c83f0e321734747a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 16:34:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:08:47 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 10 Jul 2024 17:09:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_windows_hotspot_22.0.1_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_windows_hotspot_22.0.1_8.msi ;     Write-Host ('Verifying sha256 (89387f079e372b70a57c6a2f778a4020144cb19ae44f49b066c83d9410938e2f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '89387f079e372b70a57c6a2f778a4020144cb19ae44f49b066c83d9410938e2f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Jul 2024 17:09:52 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:09:53 GMT
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
	-	`sha256:5e3cac577bec9ee5e73dd478b8acee753e36108436010b1179c7540935a06f30`  
		Last Modified: Wed, 10 Jul 2024 17:36:23 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc1067a54bd18ddc459aac8adfaa220b7282092fad78df44fa8deb1713d889c`  
		Last Modified: Wed, 10 Jul 2024 17:36:49 GMT  
		Size: 379.9 MB (379897783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e38783fc51f5a31d894651543522e616362da2353ae99f79e594de1f68611af`  
		Last Modified: Wed, 10 Jul 2024 17:36:24 GMT  
		Size: 288.7 KB (288737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7db4f00678457441ddce5cdddbc73441ff852b187bdcc69f926b3f3b5d1d3a6`  
		Last Modified: Wed, 10 Jul 2024 17:36:23 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:8f3a9f0c02c3afc7740774b6a517f4d4737d0c51ba8b80d49b4e8b1951d03c6e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2622567275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85324411e6c390c56efec00d8c4b139344ef6f4180f2450c27e3cd5c6067d47c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 16:36:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:10:01 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 10 Jul 2024 17:11:30 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_windows_hotspot_22.0.1_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_windows_hotspot_22.0.1_8.msi ;     Write-Host ('Verifying sha256 (89387f079e372b70a57c6a2f778a4020144cb19ae44f49b066c83d9410938e2f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '89387f079e372b70a57c6a2f778a4020144cb19ae44f49b066c83d9410938e2f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Jul 2024 17:12:32 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:12:33 GMT
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
	-	`sha256:f1e373da1aea31b6837945fcfd0b8d5686a47d1941334576e282ba2eaaf851e6`  
		Last Modified: Wed, 10 Jul 2024 17:36:59 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c5b099292b1e26863a9d203d6fdbaacf34dcaa05e8922920d22b0d2395edc1`  
		Last Modified: Wed, 10 Jul 2024 17:37:22 GMT  
		Size: 380.1 MB (380079234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36849132934d5e0507bcac0594b01021abfbca226aef2d969319651a4406c3f`  
		Last Modified: Wed, 10 Jul 2024 17:37:00 GMT  
		Size: 4.1 MB (4054451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72af0bd22bf28daa2c9197b5f588d291a5fff3d1e95b4ac7a21f854097a8458`  
		Last Modified: Wed, 10 Jul 2024 17:36:59 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
