## `eclipse-temurin:19-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:9d7a373b60a11ab9922b64e5ee9dd0168d533d524450c82189ab7784e69f0813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:19-jre-windowsservercore` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:b001760244e25891f3626bc3839dbaea1d12d2e9e7be14ef929f4baa52b759a8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2560196764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07a81d88622eae911802ccc50d8bd0c5e50f8a7a1dcef9bee83ee7eb1487944`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Tue, 08 Nov 2022 18:28:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Nov 2022 19:12:11 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 08 Nov 2022 19:22:22 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_x64_windows_hotspot_19.0.1_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_x64_windows_hotspot_19.0.1_10.msi ;     Write-Host ('Verifying sha256 (9674e91db19657c2f4dbabde78bb78be1d9d3b3deaee53f3400a3653449f08d5) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9674e91db19657c2f4dbabde78bb78be1d9d3b3deaee53f3400a3653449f08d5') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 08 Nov 2022 19:22:50 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276673195ed11807395b0da51ac20ef31c925ce955c29ad1bab54f14617c25b`  
		Last Modified: Tue, 08 Nov 2022 19:41:53 GMT  
		Size: 1.0 GB (1007770983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3becc14271944025e3fa6c2ef2689bdfbf09bfc54ec339115d3082df315898e4`  
		Last Modified: Tue, 08 Nov 2022 19:38:57 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475fd7723281328e1b6805eca57c06af8c864c1bfc567d6e528f0dd9627a02f0`  
		Last Modified: Tue, 08 Nov 2022 19:54:07 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bee1baf1275d839d5d07a733302731440ffa6e0e27d2cf96c0ec358a8bbbb2`  
		Last Modified: Tue, 08 Nov 2022 19:56:31 GMT  
		Size: 77.9 MB (77866658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b301e4040a49588f10b3aaefaf56e168915a2348649f9e1c787033e9933f6c`  
		Last Modified: Tue, 08 Nov 2022 19:56:19 GMT  
		Size: 558.6 KB (558648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-jre-windowsservercore` - windows version 10.0.17763.3650; amd64

```console
$ docker pull eclipse-temurin@sha256:bde1e8b57d34930d55119b9bda88c28cc95a67ee04bce13eb8dae94136c5bbae
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2859566293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c596fc42eb8f11163d43650c3c2102c6d745eab203256de58cab3eb723249177`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Nov 2022 19:15:10 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 08 Nov 2022 19:24:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_x64_windows_hotspot_19.0.1_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_x64_windows_hotspot_19.0.1_10.msi ;     Write-Host ('Verifying sha256 (9674e91db19657c2f4dbabde78bb78be1d9d3b3deaee53f3400a3653449f08d5) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9674e91db19657c2f4dbabde78bb78be1d9d3b3deaee53f3400a3653449f08d5') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 08 Nov 2022 19:26:33 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e985ddaf32ace65d0eff12e6fb243efc3c2b42ed4459033b28e53418912e17`  
		Last Modified: Tue, 08 Nov 2022 19:54:55 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13f160e9adbea4e975dec68a774fac1389d22d36c803724303e96974809bede`  
		Last Modified: Tue, 08 Nov 2022 19:56:53 GMT  
		Size: 77.6 MB (77642104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fa67fa04b449e53112d46264870d40cd0359f24aa972c9aaab837a913f6d93`  
		Last Modified: Tue, 08 Nov 2022 19:56:42 GMT  
		Size: 3.3 MB (3334490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
