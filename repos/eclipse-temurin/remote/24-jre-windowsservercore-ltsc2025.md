## `eclipse-temurin:24-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:84c9240caacecee1a28b757b5a923e883191b5a93824f7b6922d333ef2c95cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:24-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:8f2e68961d304f47b45a4c5bddf5e271ac6141ab3d54b8d147af01ed6e050458
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3494948105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e50c4bb23f2515e140f8f7363afcfee6796fe3a83fc1b219a16986c5ed1c5e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Wed, 23 Apr 2025 16:36:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 23 Apr 2025 16:36:46 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 16:37:03 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_windows_hotspot_24.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_windows_hotspot_24.0.1_9.msi ;     Write-Host ('Verifying sha256 (4562ea92299178db9966b7eb7abf9f8bb5269595f6627cede8fc77caf62a2789) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4562ea92299178db9966b7eb7abf9f8bb5269595f6627cede8fc77caf62a2789') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 23 Apr 2025 16:37:11 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d92f14844deb07f67ae045578e5ce54ccb7987902869f2ec5c61207a7e493d`  
		Last Modified: Wed, 23 Apr 2025 16:37:13 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af477b0771e93096f007d60ddf4a1ede89f362030ce4ed339eb43c5a592a58a`  
		Last Modified: Wed, 23 Apr 2025 16:37:13 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7f1ca45c614d7c18a2a2707ae0a838f776dcf560081d733849ca67efb3f93a`  
		Last Modified: Wed, 23 Apr 2025 16:37:22 GMT  
		Size: 99.4 MB (99398960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17321b0002ac9f78a61eee696b6e51d3eb737eadc51c0b2a6e46b31b6a795ae4`  
		Last Modified: Wed, 23 Apr 2025 16:37:13 GMT  
		Size: 385.1 KB (385116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
