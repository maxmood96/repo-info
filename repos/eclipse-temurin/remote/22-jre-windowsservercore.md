## `eclipse-temurin:22-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:ab21b68520163969b09cae8901ce1261afc547d087d782d7ded2eacab6fe22aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:22-jre-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull eclipse-temurin@sha256:d4679f02668b2983c17c3025738ad25d179f27a32e47ffb2e970951228c71f86
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224787140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9500458828ef12dd30ca090002f7aa5e8942625445560d853137f8aff96279be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 19:35:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:11:15 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Tue, 13 Aug 2024 20:16:43 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_x64_windows_hotspot_22.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_x64_windows_hotspot_22.0.2_9.msi ;     Write-Host ('Verifying sha256 (976ca7a664831ac76cd956ce525e6c86ddcadb70c0bc29a3754c55c991955cb7) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '976ca7a664831ac76cd956ce525e6c86ddcadb70c0bc29a3754c55c991955cb7') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 13 Aug 2024 20:17:00 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e300ced4fe41f30e1e3ad2f70267371105499fbbd08c968b2a967fd27e5859`  
		Last Modified: Tue, 13 Aug 2024 20:27:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4165460b4226de63608d6e03445ef071f5201035dac7a6dff5083c5eb836466`  
		Last Modified: Tue, 13 Aug 2024 20:37:48 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95a889381a117da5eda862842a4932aad609b356b6f31858b535bcf2c0abcf8`  
		Last Modified: Tue, 13 Aug 2024 20:39:22 GMT  
		Size: 82.7 MB (82732726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa83ff2c344997d9347cfd1773b29b155fc527c4480cda03e4ebb89dc80e4916`  
		Last Modified: Tue, 13 Aug 2024 20:39:13 GMT  
		Size: 286.6 KB (286596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jre-windowsservercore` - windows version 10.0.17763.6189; amd64

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
