## `eclipse-temurin:21-jre-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:1aca23935b1855d933e336879ddd874bf100093cfda45346bd9a5953565e55fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull eclipse-temurin@sha256:8a7c50e5785c5da0b75c6bd5dcdf69db9e6dab8f06a65e60a3de872bfd6fdf09
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1994412446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b859bfbbdf46c9cdd239a1db60504181112b192b0cd484809764e97a8d88bcb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:09:31 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 14 Feb 2024 20:16:31 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_windows_hotspot_21.0.2_13.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_windows_hotspot_21.0.2_13.msi ;     Write-Host ('Verifying sha256 (20a07730d415bda3f90ebdd6270fd11f68ba60c082b23218ef79076f3fc8392c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '20a07730d415bda3f90ebdd6270fd11f68ba60c082b23218ef79076f3fc8392c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Feb 2024 20:16:52 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59801d1b9e096dd6dd0078036b1fdadf55d26b97df4b14007a093ca3c28d5508`  
		Last Modified: Thu, 15 Feb 2024 00:13:41 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79abdea962f79e0cabfe8594fdcaf405321cec0d7c9123c6709bfd0ef4235aef`  
		Last Modified: Thu, 15 Feb 2024 00:15:42 GMT  
		Size: 83.5 MB (83473206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f18e3ed17ffb3d0ad3850b6cd4ab56bbb6fb083652e13380b8d09bae94fe4`  
		Last Modified: Thu, 15 Feb 2024 00:15:30 GMT  
		Size: 282.2 KB (282228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull eclipse-temurin@sha256:44ccb232587fac0e99ac5e3f06e186e143c6e4971193b12cf3cb31210e0044bb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167533845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c183821a70f0603c37a4156fec4828242562b30f63f03d27ccfd09d6b8949d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:11:14 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 14 Feb 2024 20:18:49 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_windows_hotspot_21.0.2_13.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_windows_hotspot_21.0.2_13.msi ;     Write-Host ('Verifying sha256 (20a07730d415bda3f90ebdd6270fd11f68ba60c082b23218ef79076f3fc8392c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '20a07730d415bda3f90ebdd6270fd11f68ba60c082b23218ef79076f3fc8392c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Feb 2024 20:20:13 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c4fb479155d452b8fabcc07da77fd191b6fee1ac5e65f749ed498c3a58285a`  
		Last Modified: Thu, 15 Feb 2024 00:14:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e048d11f831b42ede85d97e01c81e6502fae2443c563dbb4881d3db8655d8f0`  
		Last Modified: Thu, 15 Feb 2024 00:16:01 GMT  
		Size: 83.5 MB (83507468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7806cffe0f15056e2df4f143f1f08323e420703e501d52897a093b7ad20497df`  
		Last Modified: Thu, 15 Feb 2024 00:15:52 GMT  
		Size: 3.6 MB (3574758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
