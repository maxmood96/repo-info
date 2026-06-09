## `eclipse-temurin:8u492-b09-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:66dc0f2eb52be4b034c7f2034752add35317623bf79f16f4511d6481a600e835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:8u492-b09-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:79545f69fd1ba602c618cda1dd239378b5a1349450649d6b894e139f00f6f988
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323344486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f88ad535772962cf1a6a9d49a4727c4c47d4019ec25008a0cdcc4967152ebc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:19:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:19:20 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 09 Jun 2026 22:20:06 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u492b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u492b09.msi ;     Write-Host ('Verifying sha256 (e931546f0557e0735472e99c5f0a62d34854ab8a2fee9709bfcbc7ea6dcc5172) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e931546f0557e0735472e99c5f0a62d34854ab8a2fee9709bfcbc7ea6dcc5172') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Jun 2026 22:20:15 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e108fe1d7bd1461ed20f15355570961a9ae0df8116181394a77ba532742ec272`  
		Last Modified: Tue, 09 Jun 2026 22:20:19 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54824a4dfbd048ca3bf341a303d5ad41e2620c4bab921a4f98d276495d858d24`  
		Last Modified: Tue, 09 Jun 2026 22:20:18 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f9b59dd0384ec4e869493954509908471c52bddda3e6945bc6dd9c55ff7ce0`  
		Last Modified: Tue, 09 Jun 2026 22:20:30 GMT  
		Size: 190.9 MB (190862783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038266a9043b868ad9c80c023bc8b7b4e9e0ece65e34670268a6e9a5bb69185a`  
		Last Modified: Tue, 09 Jun 2026 22:20:19 GMT  
		Size: 353.6 KB (353555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
