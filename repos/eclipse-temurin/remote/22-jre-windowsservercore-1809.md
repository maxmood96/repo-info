## `eclipse-temurin:22-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:fef3b9c49a97a6f450531a3fe2a62837c0905ceb69a611820c1b6bd3e4578bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:22-jre-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull eclipse-temurin@sha256:7fb015faf85b3d57a73643fca590973b3a9026d5a0829875c58fab7a4d0b289b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331668318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f15b43314e6024d6c1f6722ce11f46292babc46d0bdd7b19609a4a76eef034d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 19:36:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:12:42 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Tue, 13 Aug 2024 20:18:18 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_x64_windows_hotspot_22.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_x64_windows_hotspot_22.0.2_9.msi ;     Write-Host ('Verifying sha256 (976ca7a664831ac76cd956ce525e6c86ddcadb70c0bc29a3754c55c991955cb7) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '976ca7a664831ac76cd956ce525e6c86ddcadb70c0bc29a3754c55c991955cb7') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Aug 2024 20:19:11 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff016dbc7255d05f8f8e1599a5a13062173c7235efe1e9c1bcb59176beb33ccd`  
		Last Modified: Tue, 13 Aug 2024 20:28:42 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248acf0e42ea4455abfee4b6e9c9e97c26126255fd38bdbd29d27f46806fbbd2`  
		Last Modified: Tue, 13 Aug 2024 20:38:19 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d593d50333e9aa11a6ca4d6a9647759cb90cd752c75b74bfc0f4b5b539f8759e`  
		Last Modified: Tue, 13 Aug 2024 20:39:38 GMT  
		Size: 82.9 MB (82876667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd45d63762ed14157094ea1888dd35358e10d60dad59a48305d54d57ce085860`  
		Last Modified: Tue, 13 Aug 2024 20:39:30 GMT  
		Size: 3.6 MB (3585577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
