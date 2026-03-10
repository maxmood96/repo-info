## `eclipse-temurin:21-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:73c1f9537b27d2e218647eaaa201ad244895e17cd0ce379eabfbf72cb8eb9cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:bfebdd0df92607b06bb385658d70de2e17b9d732daeacc16630c7531ddd68755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2165453314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afb062c9f61c7e15822c2b622346241846f1512ac788021fe7b9bd3ef3d5fe6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 21:55:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:03:17 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 10 Mar 2026 22:03:30 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.10_7.msi ;     Write-Host ('Verifying sha256 (a841118d4959b6b6eb6156fa1f2487f112afaecd124b1eb5bba203d5556efd32) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a841118d4959b6b6eb6156fa1f2487f112afaecd124b1eb5bba203d5556efd32') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Mar 2026 22:03:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344cc8f410d425104b1ea3d4052161da9518d5e7cef041fc41b1dd5444177827`  
		Last Modified: Tue, 10 Mar 2026 21:56:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06b128beb00692b415c56b6a9474115ca1f46f9ce2fa8e8895f0b5e7b54d12e`  
		Last Modified: Tue, 10 Mar 2026 22:03:40 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34936f2cecde01cdeaebfbb497b1950feca01c9ef6c624dc5fee93d3a95901f`  
		Last Modified: Tue, 10 Mar 2026 22:03:48 GMT  
		Size: 83.9 MB (83890914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3906bea24188370fe6f50fb1afa0e75e2cd2e38dabb31c056d9be4ab18718e`  
		Last Modified: Tue, 10 Mar 2026 22:03:40 GMT  
		Size: 363.8 KB (363752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:62bd629555ec44ce5803917cc082d8f5722b9e55e65db64c25ee4912e8c2f602
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2066513779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d7cdd51dcb3009de24480c69324c2a3044b58a82b6873873bf7b618687bea3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:57:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:07:35 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 10 Mar 2026 22:07:58 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.10_7.msi ;     Write-Host ('Verifying sha256 (a841118d4959b6b6eb6156fa1f2487f112afaecd124b1eb5bba203d5556efd32) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a841118d4959b6b6eb6156fa1f2487f112afaecd124b1eb5bba203d5556efd32') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Mar 2026 22:08:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f982b44695c6c1cca851e9238aa8eceda2f7522e65a6a1df319239f66b3610fe`  
		Last Modified: Tue, 10 Mar 2026 22:00:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74611d37bf52175f2c442755a621f68c9885a27476d2da32e7e0d4601ec9816c`  
		Last Modified: Tue, 10 Mar 2026 22:08:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb42cdb90c4d8199cbe5d6c52570e82983fb1fc40b25ce80c371bbfd155dfff8`  
		Last Modified: Tue, 10 Mar 2026 22:08:16 GMT  
		Size: 83.9 MB (83877160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995026e1cab6a12f6a3010f46acffa9096a74d72952de574f2512531434eeaa7`  
		Last Modified: Tue, 10 Mar 2026 22:08:08 GMT  
		Size: 352.6 KB (352636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
