## `eclipse-temurin:24-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:da974ef2acc230cbb431cbe03626cfa8910d5f3aee58f952576d0ce305a797f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:24-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:96e4e596a495d69468b4b6297df44fed09bbf29f6ac083ad0abc851cffeece7b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 GB (3161623023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f42c14216cb04006bf2972692c673d87bbf809d1513fd77e11191017d98711`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 22:02:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 22:02:10 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 22:02:33 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '168a9d9ead2f75de44f6d49ac35a58879066c1215375824ada6e6dc4a9ad0b95') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 25 Mar 2025 22:02:42 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 25 Mar 2025 22:02:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a66e3d0f2fb30af04de3bf3c0a984c1bc9b24911e36c03fcca622ac39bd645`  
		Last Modified: Tue, 25 Mar 2025 22:02:47 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7a68aed1bf75d995f1a4246948c93a95235a02adc0bef5eafe1239dffd8371`  
		Last Modified: Tue, 25 Mar 2025 22:02:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabc5918d70d7d8ec662b968f403b8c5a6ff3c130cf097b7abd29f7e68d2ba81`  
		Last Modified: Tue, 25 Mar 2025 22:03:04 GMT  
		Size: 252.6 MB (252576394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c5a2570bb6461c4e7a9c7065736dbf5e9b9c7e90d43ae7ee1ec90f285cbe80`  
		Last Modified: Tue, 25 Mar 2025 22:02:47 GMT  
		Size: 395.0 KB (395026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803a03107195d819fdf73e1375bdcf9c95716dcb089f36f4e760dd86db162b3a`  
		Last Modified: Tue, 25 Mar 2025 22:02:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
