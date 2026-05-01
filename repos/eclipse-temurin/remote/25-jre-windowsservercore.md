## `eclipse-temurin:25-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:df6a28215c22fa59760a4c1a33fc0d0c4125cd8acb936927e81f5b7f39629e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:25-jre-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:76019bfaef22dd5952b7f064c0a7a5d70313a2092b8d98bfb78656ae444fb582
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2231665585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5940a90a8d611486dc35aa35bf102b331c2a21c73ecceddb9e96fff90f7e830`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Thu, 30 Apr 2026 23:31:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 Apr 2026 23:31:50 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:33:23 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_windows_hotspot_25.0.3_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_windows_hotspot_25.0.3_9.msi ;     Write-Host ('Verifying sha256 (05975ec0d4df8722b30836af98d795a80f72d4cc37a2451943bd23304d5ac0fb) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '05975ec0d4df8722b30836af98d795a80f72d4cc37a2451943bd23304d5ac0fb') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 30 Apr 2026 23:33:31 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04aea3c19b4336092956854ada213c0ac22bc44dfe9f0b9979415551d3c318ee`  
		Last Modified: Thu, 30 Apr 2026 23:33:35 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0278b5da8cac7d8ac70dbe52219f48e1e068a3b9ca4e42344a1d1f20ec05b6f`  
		Last Modified: Thu, 30 Apr 2026 23:33:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655bed14ef18467ca645a9b4a6c1584a7ccf87fb02f96e3f2fab8ca569e0e1f1`  
		Last Modified: Thu, 30 Apr 2026 23:33:45 GMT  
		Size: 101.3 MB (101330571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068e201964534047665a1da13a29d01accc47307fa00024b618db734ba07b29d`  
		Last Modified: Thu, 30 Apr 2026 23:33:35 GMT  
		Size: 346.4 KB (346417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:25-jre-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:c3810eab80cec577d9c4831c4cc3c3cc27f19ef301335c9e0124304fd8e7c92f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2171878993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be859b2680defb096bc96d39c99dda5b7298a6a45700d8503c8c2f401306f53`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Thu, 30 Apr 2026 23:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 Apr 2026 23:29:49 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:48:08 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_windows_hotspot_25.0.3_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_windows_hotspot_25.0.3_9.msi ;     Write-Host ('Verifying sha256 (05975ec0d4df8722b30836af98d795a80f72d4cc37a2451943bd23304d5ac0fb) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '05975ec0d4df8722b30836af98d795a80f72d4cc37a2451943bd23304d5ac0fb') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 30 Apr 2026 23:48:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8b97918db09410609d8eabe475c20965bce390da9f39136230f78b66246203`  
		Last Modified: Thu, 30 Apr 2026 23:31:45 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9600e37c123113070d94b4a0958f61ed9e51dbd0423d6738b44bf7817da5852d`  
		Last Modified: Thu, 30 Apr 2026 23:31:45 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0352384c6c5bead5e635937e2d74914bbfde60efad8a786a9047f8907bf8bb`  
		Last Modified: Thu, 30 Apr 2026 23:48:30 GMT  
		Size: 101.3 MB (101298189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e718d8c99b4a8b29bcee28f3b11dd880948ea49b98eed78cc9ba9c160f492a6f`  
		Last Modified: Thu, 30 Apr 2026 23:48:20 GMT  
		Size: 366.9 KB (366907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
