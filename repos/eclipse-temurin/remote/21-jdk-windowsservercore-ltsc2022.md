## `eclipse-temurin:21-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9c6fac7352da02f3b1620dc7cc0b69b49dc93f72d2856a4d98856864c3329833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:21-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:87cf36afd4eaf0b60efbedc1777262a02f475b15593fad550300e5baaf04f7df
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216831054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8be0a4030a725746296baf6d58a68abab5d3bf598639aa34681c90a1ada73b0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Thu, 05 Feb 2026 22:21:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:21:01 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:22:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.10_7.msi ;     Write-Host ('Verifying sha256 (6be8643444ec20758a34ddb1231e998ac77e72f661a0d5525a8ac3e078bcbcb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6be8643444ec20758a34ddb1231e998ac77e72f661a0d5525a8ac3e078bcbcb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:22:47 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 05 Feb 2026 22:22:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a59fc8c7e415f2ed068d8d7c3e4506e5c984eee3a51653989c8ef50ccc06c6`  
		Last Modified: Thu, 05 Feb 2026 22:22:51 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60610f549c099b2c34c157f9c4865a165b38b9738e5a277d5002f869aa018be`  
		Last Modified: Thu, 05 Feb 2026 22:22:51 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e0912ae7a1c4f333ff93a28e77f06a4c0e2188b8e40ac01812606c73afb490`  
		Last Modified: Thu, 05 Feb 2026 22:23:12 GMT  
		Size: 380.8 MB (380800954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540948c656ee369262c60c85f3831f72dbacb280e503388b90ce1ff9a6e32e53`  
		Last Modified: Thu, 05 Feb 2026 22:22:52 GMT  
		Size: 367.0 KB (366976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb50f28f2a7243765a13c415877c4f29e83a3fcd53c0ce43336eb73fed76db0`  
		Last Modified: Thu, 05 Feb 2026 22:22:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
