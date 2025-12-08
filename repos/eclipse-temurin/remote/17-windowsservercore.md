## `eclipse-temurin:17-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:90a78192c003ee7c8c6e5dcc51823516d1b87c09683b0ea968f4b3e87fdea4fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:69d9c2b35e134cceb12bcb4b81aa0c94f766aacb841c087bdad302a21bd0624f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3591365403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9cdedce4c944027ff03d89639ed4a3d781b9e92670d193a1a112b3300e2d54`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:15:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:15:25 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 11 Nov 2025 19:15:56 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.17_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.17_10.msi ;     Write-Host ('Verifying sha256 (df491b4dbad46dcb77fcba22a0edac4c53a89448f699b33a5cdd5349bd5865dd) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'df491b4dbad46dcb77fcba22a0edac4c53a89448f699b33a5cdd5349bd5865dd') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 11 Nov 2025 19:16:03 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:16:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1c6f3867fe2805e4c0cf6c31e5ff051a46bd9790c9c2dc8c2eb99f48868de1`  
		Last Modified: Tue, 11 Nov 2025 19:25:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189fd125c54d972b486a88a28f67edf892429de78dc8bb8dd5b1e704e660375f`  
		Last Modified: Tue, 11 Nov 2025 19:25:07 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b56e331bd6345e4ec4320ba1372628e624c4d22ba1fe6d95ab8ae0b9d993124`  
		Last Modified: Tue, 11 Nov 2025 22:14:51 GMT  
		Size: 355.6 MB (355551526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540df86241a5d0c3d70937cdf799dcac80058155c931ef3e86b94abd81b97d5b`  
		Last Modified: Tue, 11 Nov 2025 19:25:07 GMT  
		Size: 354.2 KB (354198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a6f57ca682a4cb2a9d986842bc24499d92593abf8fdad7bc0b880213957d98`  
		Last Modified: Tue, 11 Nov 2025 19:25:08 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull eclipse-temurin@sha256:a71d35821392cb96832db8f561dfe9cdd39daa24c0dcefaf089bde4c0020de28
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125985554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5c4ec4417f659d0eee239fedd348671ceac80a7c64f36e7ab2aec9335fb8a8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:20:37 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 11 Nov 2025 19:20:59 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.17_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_windows_hotspot_17.0.17_10.msi ;     Write-Host ('Verifying sha256 (df491b4dbad46dcb77fcba22a0edac4c53a89448f699b33a5cdd5349bd5865dd) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'df491b4dbad46dcb77fcba22a0edac4c53a89448f699b33a5cdd5349bd5865dd') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 11 Nov 2025 19:21:07 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:21:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888556ffeec9436926f151de987c3a4423e30980b754c116540ae6e772e88e7d`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdf4b4e337c232961cda4cadfa6553dd805c68c82e156e20dd80c11a0f41f92`  
		Last Modified: Tue, 11 Nov 2025 20:11:22 GMT  
		Size: 355.7 MB (355667874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3bec31934974c97bb8c62425480263b541db85f8dfaab3b0870ab5c57fe210`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 352.3 KB (352284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89df424b101398ba69057bf923ede01f829e02cc2a2b9e17d59239522db7783`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
