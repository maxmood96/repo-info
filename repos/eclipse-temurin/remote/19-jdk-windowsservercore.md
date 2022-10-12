## `eclipse-temurin:19-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:f72872698631b33f3bfa2688f56828094d050a1237e5dabb236169d901fa819e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:19-jdk-windowsservercore` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:a371848f59aef8780f98c65eb9c4891982b610bc4b47468979a2cad063b8ab6b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2783888464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f9b58e8edd5bfa339de8d37e9b8af28aabb77c81ff08bdb43dc575404585de`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:45:15 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 12 Oct 2022 15:46:15 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_windows_hotspot_19_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_windows_hotspot_19_36.msi ;     Write-Host ('Verifying sha256 (7921d7aedef1ae9c5746b481799c34187dab9e61d7c47eb03dabd0ee34889200) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '7921d7aedef1ae9c5746b481799c34187dab9e61d7c47eb03dabd0ee34889200') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Oct 2022 15:46:37 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:46:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f463948dc70c49daeabdf3a3ee0bc99618308729bea7a91f4eca188b14b6e9`  
		Last Modified: Wed, 12 Oct 2022 16:09:54 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5688873447d3b6378be8a1d0a29e73762f795657d2d063cfbd7d59f335b893`  
		Last Modified: Wed, 12 Oct 2022 16:10:22 GMT  
		Size: 367.1 MB (367123686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7bd4bf12fa7c0095f3134a0363e7ef729a4f53641145da086ad4eb010b3f5c`  
		Last Modified: Wed, 12 Oct 2022 16:09:54 GMT  
		Size: 537.3 KB (537329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b944dad41632ae6ceeb7e29b793aac595484df761579fb88956944ce183daa51`  
		Last Modified: Wed, 12 Oct 2022 16:09:54 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-jdk-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:4fe2efa688226cab5001197cb08205c6e77bd85a3695d7f4afa934226a4f066f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3082006042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420e46b28a537fef12724b5d776d337e93176ba7b42a631df3e7d138dc4b2055`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:46:57 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 12 Oct 2022 15:48:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_windows_hotspot_19_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_windows_hotspot_19_36.msi ;     Write-Host ('Verifying sha256 (7921d7aedef1ae9c5746b481799c34187dab9e61d7c47eb03dabd0ee34889200) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '7921d7aedef1ae9c5746b481799c34187dab9e61d7c47eb03dabd0ee34889200') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Oct 2022 15:49:25 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:49:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dee8b9b3dd566ea929a35fa67b2ac465b6d1cb9366aabe0ca02008ba24990c`  
		Last Modified: Wed, 12 Oct 2022 16:10:35 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e9db9df51066058061dcf03039fd275bc1290e9c6547f1e1705798eaf00214`  
		Last Modified: Wed, 12 Oct 2022 16:11:04 GMT  
		Size: 366.9 MB (366893980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb43e5358c16330530c4ab40ae0ef0028eaf459d66fd032d2746f8b0634039af`  
		Last Modified: Wed, 12 Oct 2022 16:10:36 GMT  
		Size: 3.9 MB (3943850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4fa82f3f1791945b78f35c8e7870203e4d10ae91caf75438a6d46f3251543`  
		Last Modified: Wed, 12 Oct 2022 16:10:35 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
