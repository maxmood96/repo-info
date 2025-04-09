## `eclipse-temurin:24_36-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:29af9d5d92c90646d9f75eb48e48b465950eadf7dd7a6a01049f214b16677e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:24_36-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:89f8563056d3d58593d573ecccda0473f0c0166ae61f745359e70b6c42d4752d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3647615501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd9c46b5414d1f3ba5fd11dd9e9cc833a4931bbe69eb2d219145bb6112e5464`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:51:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:51:07 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 00:51:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Apr 2025 00:51:38 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:51:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab9c6fffc447accbd7c41c829c75984747c29c4ed53ae38fbdb818a8219e79`  
		Last Modified: Wed, 09 Apr 2025 00:51:42 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f34d5ddc51cd210121b70f4ed9c71cfd5a5d24f280561ae606531e6c75d951c`  
		Last Modified: Wed, 09 Apr 2025 00:51:42 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bd42e45777cb22255beb63e2fd4db67f3b193987eca8dd8e0365a4054896c3`  
		Last Modified: Wed, 09 Apr 2025 00:51:57 GMT  
		Size: 252.6 MB (252558172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829f002b9e202a40f45132f7ea8b92dd45b8dac79308dea71d13428fe36e5b59`  
		Last Modified: Wed, 09 Apr 2025 00:51:42 GMT  
		Size: 373.9 KB (373930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d42b4359f758eda63fba8177666469e5acefab0bd0583313a0d60538e7bcf4`  
		Last Modified: Wed, 09 Apr 2025 00:51:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
