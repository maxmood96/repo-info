## `eclipse-temurin:19_36-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ca3fede833ec83f6991ba7cab750aaa3b9cbf5e6cd5c066f0ae36c71422a49b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `eclipse-temurin:19_36-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.1129; amd64

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
