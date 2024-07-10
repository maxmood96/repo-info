## `eclipse-temurin:22-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:cf18d5de42e5dadc3b0d374e38a8800121e67ff82923409a35601beecc9fa627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:22-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

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
