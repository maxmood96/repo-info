## `eclipse-temurin:21-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:849baf5a0d386072ade547ecde129fd864efd99d26c65008c2d274ec965da3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:49403b6fe1c38dda28ac5ba8fa6e0c161260738aedb3ed845e89b27aa9a0b750
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2290132067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f9ff93858e58e51de799881609cb7068f10b2da2a3cbefe220d385b2fea4a4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:45:42 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 23:45:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.11_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.11_10.msi ;     Write-Host ('Verifying sha256 (570b2b7f4d39638afe416e14285e08f27fd14995e0716dcbc07f936a5b91868a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '570b2b7f4d39638afe416e14285e08f27fd14995e0716dcbc07f936a5b91868a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 May 2026 23:46:03 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabe5bc5c27614bd1b7957a3040d418c53f29c54b756fc8823f06747a0bccb00`  
		Last Modified: Tue, 12 May 2026 23:39:46 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba993ef275ba0728e179dc28d942081371fc89bcfff280d769bc2164f21874a`  
		Last Modified: Tue, 12 May 2026 23:46:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f16980d0d9b08a6a19b4a6b8c80a70b2837d10cd62e2e51158a7d1f00af181`  
		Last Modified: Tue, 12 May 2026 23:46:15 GMT  
		Size: 83.8 MB (83829855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b5dfad91a73f3e1372a460d4020fd3e19b0ffb6868c317d8118afc9ef5620`  
		Last Modified: Tue, 12 May 2026 23:46:07 GMT  
		Size: 357.7 KB (357717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:7d4cc823965662b3fb4c821b98c39490ddf78f3fbea587fc1af23c6708b5950e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206743721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d3ecc34e3fa2a949eeb2f1f7a0398818a782e4042bcf722bbb86ab68521a60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:50:00 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 23:50:14 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.11_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.11_10.msi ;     Write-Host ('Verifying sha256 (570b2b7f4d39638afe416e14285e08f27fd14995e0716dcbc07f936a5b91868a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '570b2b7f4d39638afe416e14285e08f27fd14995e0716dcbc07f936a5b91868a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 May 2026 23:50:20 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2e44e55275db5068cf0d4475ab7d854551417c468de6c97ae46ab66ae1067`  
		Last Modified: Tue, 12 May 2026 23:39:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c2ea3eb3c25c8bdf8be0c5923ff035840b2e47b1d98b09955e966f5a87b134`  
		Last Modified: Tue, 12 May 2026 23:50:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c763f10fefc3debbb82f10c4d29bc1a5b9e187ab02a21de1c16bccd635da6b`  
		Last Modified: Tue, 12 May 2026 23:50:32 GMT  
		Size: 84.0 MB (83967900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076381fa669aa6f6b30e95534bf31bef5af3fd3a545275858197d6a72c92f2d6`  
		Last Modified: Tue, 12 May 2026 23:50:24 GMT  
		Size: 352.6 KB (352615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
