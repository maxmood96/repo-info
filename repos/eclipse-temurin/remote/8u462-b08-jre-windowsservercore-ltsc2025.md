## `eclipse-temurin:8u462-b08-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0d046ffd0a31976a8275f3ee52f5455c4815dfbc5b21549f2d3bca8839a43081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `eclipse-temurin:8u462-b08-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull eclipse-temurin@sha256:f0ec6517737d6385db2cb893d62812dca4ad6c771fc75bf391f2dc61a062aa1b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3293470719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35092c010c21fcbbd4cc1d06fd0151a3436f1d29306650ce146a2fa28d8b7175`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:38 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 14 Oct 2025 20:43:56 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ;     Write-Host ('Verifying sha256 (22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Oct 2025 20:44:02 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f932d6c77dfb1597daf851eaea0980e3b4dd60d90a5555c07c6a65507e2822`  
		Last Modified: Tue, 14 Oct 2025 20:51:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a98532333d4687a5cbc31bbdbaa71d24f851d7079c2428d894feab8fa5847e2`  
		Last Modified: Tue, 14 Oct 2025 20:51:14 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc48eed164f5304786c7a054f3d4588dad856005c3cefda74eba0c53bf00d63`  
		Last Modified: Tue, 14 Oct 2025 20:51:23 GMT  
		Size: 72.6 MB (72641287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa76473a19e0e634f5c7de80e2a5f1f4a4ead65ab4e6a0e08565cd749b01c2`  
		Last Modified: Tue, 14 Oct 2025 20:51:14 GMT  
		Size: 346.4 KB (346380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
