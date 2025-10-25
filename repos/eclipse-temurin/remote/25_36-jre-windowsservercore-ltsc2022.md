## `eclipse-temurin:25_36-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:98f1f0c5f467db2562287b002664bc1169551075f8b9a8a54b999a3b57b464b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:25_36-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:640de0059f623ae866d55d555f6e65c6114a8d431cf9f41a08a98fe708ca43fa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1678619391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a3722045c94a793cd8507a052869a10a2f3aa4df05c295349208b5c158704e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:22:13 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 24 Oct 2025 18:22:33 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_windows_hotspot_25_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_windows_hotspot_25_36.msi ;     Write-Host ('Verifying sha256 (eeae2fb19dc8d778a324d9b5c879f7afe9732487516807b75584436b01e0d8c3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'eeae2fb19dc8d778a324d9b5c879f7afe9732487516807b75584436b01e0d8c3') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:22:40 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f08447176c571c71f5dd46580286383413dff8404ab7f7e3d13a06ba4dac04d`  
		Last Modified: Fri, 24 Oct 2025 18:23:01 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e911ec2de99e7fb943b8639c84ac0077d39a0e2f57c30068bf5d12950d774c9`  
		Last Modified: Fri, 24 Oct 2025 18:23:11 GMT  
		Size: 101.1 MB (101071713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba0d14579976a651a4a5dc8582ac30e11afa4e592b9e0bfc2cfa8637bdb4f7`  
		Last Modified: Fri, 24 Oct 2025 18:23:01 GMT  
		Size: 352.1 KB (352105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
