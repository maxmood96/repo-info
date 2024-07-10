## `eclipse-temurin:22-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:a25e112fc317395704bef6362055c123bfea3d5457036a4b28c3dd2495b978c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:22-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

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
