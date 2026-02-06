## `eclipse-temurin:8-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:1e2264f3376ed5d4df169c52d5178874c5495fbff08a65cebf63ea516c615dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:8-jre-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:ecee911b77781bb0a8db3636005c2362f54265d4084871c483bde7680cf922a4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1567982152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276b78ea5e1bd327660f70172fa8b8e1d191d07d40fef1c85dde2536d40ab482`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:16:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:16:17 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:16:56 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_windows_hotspot_8u482b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_windows_hotspot_8u482b08.msi ;     Write-Host ('Verifying sha256 (4e0dbdff6537f43b012e2376de59845968afc99f5901303a28a881b42d93d795) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4e0dbdff6537f43b012e2376de59845968afc99f5901303a28a881b42d93d795') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:17:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f8ef58c60a3f4378de62a99e666afcef5ed85c5999ded197b5373a42047afc`  
		Last Modified: Thu, 05 Feb 2026 22:17:08 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4085fcff0106717e0528971c55710b169d78cbb19b2e9cb4aad5fd41b5308c`  
		Last Modified: Thu, 05 Feb 2026 22:17:08 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d045b0c75ac2aaa4c13138aadb3a1b13f9589ce95dcc84fe41fc4f19145607`  
		Last Modified: Thu, 05 Feb 2026 22:17:14 GMT  
		Size: 71.8 MB (71838617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7e332c4b18e70f56af19a8015f911d883f7715cb177b92370a68d5f4aa891d`  
		Last Modified: Thu, 05 Feb 2026 22:17:09 GMT  
		Size: 380.6 KB (380615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:139cb61315fc8cf9e15e5c96a7dcc3857d715298003e43c0cca6bd4ee4c87418
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1907980336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5770def76a22e27e50ddaa8331c1a9e1e55adb3a6f5f4ae0fe5b67d20abcbcc5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Thu, 05 Feb 2026 22:17:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:17:17 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:18:01 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_windows_hotspot_8u482b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_windows_hotspot_8u482b08.msi ;     Write-Host ('Verifying sha256 (4e0dbdff6537f43b012e2376de59845968afc99f5901303a28a881b42d93d795) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4e0dbdff6537f43b012e2376de59845968afc99f5901303a28a881b42d93d795') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:18:10 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:bb982b305aa61007fc9ba1abd5dfef641c0b0d322238b207e0d82a8988e1a4f0`  
		Last Modified: Thu, 05 Feb 2026 22:18:14 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50887446924c7d0ec3711320148f432eca918f1b1f6a2beca2c79c431bfc9d6e`  
		Last Modified: Thu, 05 Feb 2026 22:18:14 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e973fb3b961932e969f46468c309453e3e096d3f82a3347bba11656759f68c82`  
		Last Modified: Thu, 05 Feb 2026 22:18:25 GMT  
		Size: 72.0 MB (71951708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797d80ac8cea80b47deae3269f12b83a8b953bcabbefcc33ae0dbf42a8cd1c73`  
		Last Modified: Thu, 05 Feb 2026 22:18:14 GMT  
		Size: 366.8 KB (366843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
