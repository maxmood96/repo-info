## `eclipse-temurin:11-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:04ce402c8e1543d72017fe821820cc521434e5c7317b3583237b38a7dbefe981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:c47515dcc162dfd2fc50fce3976848d4029904578a921e14fca2d5225ac67927
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3278349610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645567059d1a776ac9e481699a3a15f59af41122404353032f015840116205b1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:20 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 12 Mar 2025 18:47:44 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:47:52 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:47:52 GMT
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
	-	`sha256:acdec1e1994aee590117339968870d6ae60a5f7d4e8579a81ea9cedae10c8879`  
		Last Modified: Wed, 12 Mar 2025 18:47:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b942e20543621a0bc08b38fef16ca24bd47c104723ce27a3af090716ca2e78c3`  
		Last Modified: Wed, 12 Mar 2025 18:47:55 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f404511ed7c15a4e647b085738c586414af4016bdd518ced625cddcb1e509be7`  
		Last Modified: Wed, 12 Mar 2025 18:48:11 GMT  
		Size: 369.3 MB (369319744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fc4084503694b8ef70f62cc79b7fba307de721392780ab500c7e614c2f4083`  
		Last Modified: Wed, 12 Mar 2025 18:47:55 GMT  
		Size: 378.3 KB (378277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a74704e56b25f194f31b1d6cead33b11dbb7dc597528f24196c9980ef61a64`  
		Last Modified: Wed, 12 Mar 2025 18:47:55 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:df8f850e3fe5c1e23badbda79758fcd947f1d26283bbfa040216691ccc82c573
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2639607207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454ed45a6d3a855f34c4584d4e9139d9ad879d4bd704accbaa8870c33d365636`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:56:58 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 12 Mar 2025 18:57:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:57:37 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677043d90a2ba943da579d4109dbfcce6b224542264b84e01f8659817c74a65b`  
		Last Modified: Wed, 12 Mar 2025 18:57:40 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c67427ff447598c1f04729a9d2a4db5f27fc1f3ad1d53d78537a67370f5b9`  
		Last Modified: Wed, 12 Mar 2025 18:57:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc420ef2bf63d61b97b5b11c1d6dc67f4c2fab6eb59c8ca78493eacdac6fe6e`  
		Last Modified: Wed, 12 Mar 2025 18:57:56 GMT  
		Size: 369.3 MB (369302048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbaa1b878ca1a8d80e8d3a75629b31f6c318c6d9142bdd1ec3a15c87a227b09f`  
		Last Modified: Wed, 12 Mar 2025 18:57:40 GMT  
		Size: 360.1 KB (360071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226a9c960aa60aabab57b87327bdfb6a3a4e6b87c1f70621927b01d624f589ee`  
		Last Modified: Wed, 12 Mar 2025 18:57:40 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:946675874a7b32e3a552dbc386c2e2a397cc764bcd32116e6b43cd87a3a1ce09
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2521262488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5d44eb2ab950fc87930f469aa6da961e842a7a05df744190c29bd6755de49c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:53:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:08 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 12 Mar 2025 18:54:25 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:54:35 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:54:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce318b55d5f1209100356531104716e5ad9b6fa793de69b47bb1e7fd68fe9d0`  
		Last Modified: Wed, 12 Mar 2025 18:54:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2728cd3d6b1bdf80335f86aa5e6cce91b5369b29aa8a8fbbc4d97bbcffff6fab`  
		Last Modified: Wed, 12 Mar 2025 18:54:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efea3979f6b9e5a7c6bf749d29a6cd2af60690cf750c26d650a3ea9bf7e585e`  
		Last Modified: Wed, 12 Mar 2025 18:54:54 GMT  
		Size: 369.3 MB (369293803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d853b29989d9dac5424a62edbec05ea6a40eaba4ae6ac3e49c1259433b3187a3`  
		Last Modified: Wed, 12 Mar 2025 18:54:39 GMT  
		Size: 330.2 KB (330170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bfc4d2c839a1f0865c2b77e3dfae65a6422aad1c02708d81165a0807ffe569`  
		Last Modified: Wed, 12 Mar 2025 18:54:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
