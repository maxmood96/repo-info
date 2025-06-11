## `eclipse-temurin:8u452-b09-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:28ea768e1a8b8e1a4403f0d833573246074281a050b84fb86e8bd6beefcec0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `eclipse-temurin:8u452-b09-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:8f6e65ac72127254b586e86205ce5f9e5de0ff30596ab6c918bf0bf1214a7b4d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3667963165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162ecec26b50008ddfa4b08b568f3942fc12450eb05019aaa070f9b51cc385d3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 10 Jun 2025 21:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:28:54 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Tue, 10 Jun 2025 21:29:14 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u452b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u452b09.msi ;     Write-Host ('Verifying sha256 (989f085584ca58701eab2d2b2f5576b7594325f0a6f85572b34586774963c46c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '989f085584ca58701eab2d2b2f5576b7594325f0a6f85572b34586774963c46c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Jun 2025 21:29:22 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac38a69b43b336900902aa469936012e75b8746f9fcc470a25b998374213020`  
		Last Modified: Tue, 10 Jun 2025 21:33:04 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c102c80e8d1f44da6b28d7dab36f2085e6c37ab45a3490b82c15a4733a2ff4c7`  
		Last Modified: Tue, 10 Jun 2025 21:33:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494286b1dcc5135a66b3f8d3e1f35f6138917c80bc4ba7fdb2cc6144904ef8e2`  
		Last Modified: Tue, 10 Jun 2025 22:09:52 GMT  
		Size: 191.4 MB (191403714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247f25f988a5c6a98af6b685919e849e4f4919a9b2b352a64ff921b926fc1c2f`  
		Last Modified: Tue, 10 Jun 2025 21:33:05 GMT  
		Size: 382.8 KB (382788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
