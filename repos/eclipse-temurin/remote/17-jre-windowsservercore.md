## `eclipse-temurin:17-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:a5531ca7283ab3b7a3f24ec52541e97abcf4061f01a2cfab3b8eb6d82ab6b6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:6d8f1fb280e28417fa71eda3a71221afa4fcb2c47402fe482c0629f26500ffd9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3566704999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f190c8f1fe6829f154349be6b419181354213f46784aca021777435cd880877`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:09:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:34 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 09 Jul 2025 18:09:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_windows_hotspot_17.0.15_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_windows_hotspot_17.0.15_6.msi ;     Write-Host ('Verifying sha256 (d89bf8a260d26ed7603ec1e79b43c1297cafd9d6b184a68646c54409285d6c2f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd89bf8a260d26ed7603ec1e79b43c1297cafd9d6b184a68646c54409285d6c2f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:10:02 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f82090e640f8926fdff3411fac3f4328c96fa24c6655a215ce7fff534ae214f`  
		Last Modified: Wed, 09 Jul 2025 19:10:00 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90a3ca5c58f8b7e4fcea894e6847cb3f5723c7cac8618c04f43c4bc04348dcd`  
		Last Modified: Wed, 09 Jul 2025 19:10:01 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61d2dbf7502b9bf19346550b38019d87236c3616a90f7bbe381df4fd4edb7fe`  
		Last Modified: Wed, 09 Jul 2025 19:10:05 GMT  
		Size: 75.1 MB (75142792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b4833ec4e27aa735a745cae143d0aed3c75e7a5f02f49037e3e84d01ed59fc`  
		Last Modified: Wed, 09 Jul 2025 19:10:06 GMT  
		Size: 386.2 KB (386157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-windowsservercore` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:56a7d7e2a002c63743897dbe84b84bafbcb1afbd365071a081519f8caf128013
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356066434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69b46056c954005dc9a813e1c1df8356cf2db4a37ef7aaa89fccb171679cb5b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:07:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:07:46 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 09 Jul 2025 18:08:06 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_windows_hotspot_17.0.15_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_windows_hotspot_17.0.15_6.msi ;     Write-Host ('Verifying sha256 (d89bf8a260d26ed7603ec1e79b43c1297cafd9d6b184a68646c54409285d6c2f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd89bf8a260d26ed7603ec1e79b43c1297cafd9d6b184a68646c54409285d6c2f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:08:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af392344db7cebdda120f5b0d857a360b5cd81b20476525e98517088edcb6be7`  
		Last Modified: Wed, 09 Jul 2025 19:08:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c84ab15cb1dd9039771be31eae0eea04d815520469bfd84d6d9e33d6dce114`  
		Last Modified: Wed, 09 Jul 2025 19:08:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e9d75f62c8ae701128554698af29d39feba82631ddec42ebb07b2318f0c050`  
		Last Modified: Wed, 09 Jul 2025 19:08:19 GMT  
		Size: 75.1 MB (75104184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76c539d224866334b31626631d87bfe1193b9ed3a38cb97123fa547e1a718c3`  
		Last Modified: Wed, 09 Jul 2025 19:08:15 GMT  
		Size: 356.2 KB (356194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
