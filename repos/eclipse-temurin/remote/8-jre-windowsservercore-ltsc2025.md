## `eclipse-temurin:8-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:89deb2062a35235b4b85b267f315dc01590853408956f95a0920065fdff43e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `eclipse-temurin:8-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:21395d8606d7db0983ebb16cfc814e93725e1675f07e819bcf8906f7f74f4091
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3571852430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e499d5c3931a9a87cb31d8af9d02772c519ba1b89184846f72afbfe7ddc4e4b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:00 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 12 Aug 2025 20:27:12 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ;     Write-Host ('Verifying sha256 (22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:27:18 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be328fb2f337e308c2eea011998147c0c86d5fa1801a4e1467276d4c33a88`  
		Last Modified: Tue, 12 Aug 2025 20:31:04 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70f0840dc7ef18194998126ba5d756ea4f8e08b8f750d5c232995ccc314ce38`  
		Last Modified: Tue, 12 Aug 2025 20:31:05 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e15968d3912cf00a30c053919aec264a485fe5b51f75db7ddf85eddc356fc`  
		Last Modified: Tue, 12 Aug 2025 20:31:15 GMT  
		Size: 72.7 MB (72653595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842141c08d7f6280e8052befdaddeec8e50d6eb8b57a0800262180de45e4b4ca`  
		Last Modified: Tue, 12 Aug 2025 20:31:07 GMT  
		Size: 365.8 KB (365772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
