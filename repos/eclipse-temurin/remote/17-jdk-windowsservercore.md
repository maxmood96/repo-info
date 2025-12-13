## `eclipse-temurin:17-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:91ddd3d68b899d30583921b358fe5728a7e5c388ea1dcab2ff0c5e0b5cb583b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:17-jdk-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:7d292239fbba7f5555efe79553872f26232c58f149a707533ebb1d881c1f6589
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3609049534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02245353c0cf9be77406b2f19fc293cdb04eb419f487e93bbeeeaec7e7ef1f8c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:36:21 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 09 Dec 2025 20:37:04 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.17_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.17_10.msi ;     Write-Host ('Verifying sha256 (df491b4dbad46dcb77fcba22a0edac4c53a89448f699b33a5cdd5349bd5865dd) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'df491b4dbad46dcb77fcba22a0edac4c53a89448f699b33a5cdd5349bd5865dd') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Dec 2025 20:37:10 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:37:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a705a6e8ee03f99b80a0bf2257b33ccbf03d0695038a45544f551b47f1bad3`  
		Last Modified: Tue, 09 Dec 2025 20:46:08 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3307104ccc76fb5fc9ac3c2a06954e0775fc5e1a8472b0cd26e5b203903d7d4d`  
		Last Modified: Tue, 09 Dec 2025 20:46:08 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d4f8e769552bb563ada9faf406b5630c4ab666b13689f198c4485ff1467166`  
		Last Modified: Tue, 09 Dec 2025 20:46:42 GMT  
		Size: 355.5 MB (355549457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae04dde39be47689962737d01682dde24fdecbcb7cde0a0754ba0b228e6af3dd`  
		Last Modified: Tue, 09 Dec 2025 20:46:08 GMT  
		Size: 375.7 KB (375718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdf86a0933750dfcdc5eee45ae23491142419fc4dbab9013a9e244ecc5e19d6`  
		Last Modified: Tue, 09 Dec 2025 20:46:08 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:46b11f1057917e1c5b8d267fd0263a807c07bff639d250f05dc16d2412680237
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2135913436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e140fe8422c6e01be3fa9b3f2cbcce96fcbec3ea6a217725b91cf9b37c2bddbd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:32:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:40:48 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 09 Dec 2025 20:41:36 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.17_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.17_10.msi ;     Write-Host ('Verifying sha256 (df491b4dbad46dcb77fcba22a0edac4c53a89448f699b33a5cdd5349bd5865dd) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'df491b4dbad46dcb77fcba22a0edac4c53a89448f699b33a5cdd5349bd5865dd') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Dec 2025 20:41:44 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:41:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21fc0656453627df8dfa5cad3ec054adb0bef73f2ed2e67af414c4644e90ba9`  
		Last Modified: Tue, 09 Dec 2025 20:40:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ee61c4a2ecf25a5e1ec1ae79c87d1ab884924739ac29984481f2c9561a2995`  
		Last Modified: Tue, 09 Dec 2025 20:42:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d592bef9f464ff872d1a222f35829d585f41e4223e7774b5945c311bd9fb4d`  
		Last Modified: Tue, 09 Dec 2025 20:42:30 GMT  
		Size: 355.7 MB (355677834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97d282e914ddda12983bc6cd0ab899c911ba535baac5dd40aef6f450ff2589f`  
		Last Modified: Tue, 09 Dec 2025 20:42:14 GMT  
		Size: 352.4 KB (352402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3927e4ecf6cda886e8dcfc23fef19e0f1058a7e2ca49c3f890256c2288ff0980`  
		Last Modified: Tue, 09 Dec 2025 20:42:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
