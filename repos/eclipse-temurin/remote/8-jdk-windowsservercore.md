## `eclipse-temurin:8-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:350cd01795b5809687faf5bd09d224f74d23cc8d227f043f9fa4f5e40c64e3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.230; amd64
	-	windows version 10.0.17763.2183; amd64
	-	windows version 10.0.14393.4651; amd64

### `eclipse-temurin:8-jdk-windowsservercore` - windows version 10.0.20348.230; amd64

```console
$ docker pull eclipse-temurin@sha256:bb41a925f4e1276301bc428b822766c8ae502a9bdf009014c975df677d8183e9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2315024385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7241dba65ca874ab68381e17f8f9edcbd10bb35e5deda53d6ce6b25e2d126c5f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Mon, 13 Sep 2021 07:01:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 15 Sep 2021 12:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Oct 2021 22:08:25 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Tue, 05 Oct 2021 22:09:25 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08.1/OpenJDK8U-jdk_x64_windows_hotspot_8u302b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08.1/OpenJDK8U-jdk_x64_windows_hotspot_8u302b08.msi ;     Write-Host ('Verifying sha256 (fe3546a8e8dd7d4e929028ef3794431748caddf7fc1cf481618e8d6f8aa15427) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fe3546a8e8dd7d4e929028ef3794431748caddf7fc1cf481618e8d6f8aa15427') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 05 Oct 2021 22:09:55 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:48a76b150a3a1ee8efbc87797c38de66d24a71421fce2754695fed8227d4cc3f`  
		Size: 873.2 MB (873175411 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3fda9a0667b0cb96fa50df6568908c70087df9372ac60c91c1ba417787ee1faf`  
		Last Modified: Wed, 15 Sep 2021 12:59:54 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cd90b28759b2715bba12424bca40ac721c899782145d61230e70cdc4ef061b`  
		Last Modified: Tue, 05 Oct 2021 22:24:03 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bc7aa534f543fec1e390b5d3ff4dcd718289ac2b58042609834df78542ed89`  
		Last Modified: Tue, 05 Oct 2021 22:24:23 GMT  
		Size: 189.6 MB (189573650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ec9d707efae98bedcc371fa052e858ee88bf01fada2c1678e651b9928f7a54`  
		Last Modified: Tue, 05 Oct 2021 22:24:04 GMT  
		Size: 573.4 KB (573445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-windowsservercore` - windows version 10.0.17763.2183; amd64

```console
$ docker pull eclipse-temurin@sha256:24b1628693574a215e9f29f7a24aa50b0d65222badb3a9290242764a39e81ce2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2876319180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e532d40b906b9f51ae765fd2e0eaddedc481127816a12a0078ea8356ee9d6f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 16:16:12 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Wed, 15 Sep 2021 16:17:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08.1/OpenJDK8U-jdk_x64_windows_hotspot_8u302b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08.1/OpenJDK8U-jdk_x64_windows_hotspot_8u302b08.msi ;     Write-Host ('Verifying sha256 (fe3546a8e8dd7d4e929028ef3794431748caddf7fc1cf481618e8d6f8aa15427) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fe3546a8e8dd7d4e929028ef3794431748caddf7fc1cf481618e8d6f8aa15427') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 15 Sep 2021 16:18:07 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2853f58bc32f8b40b3cdc6da554dccf3944c793a78ff5f14d61ca446736cab8`  
		Last Modified: Wed, 15 Sep 2021 16:38:34 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b05a085907b7dfcb9d902d40b6e1d05891a40b6fdd1858ce40ab05736c4d56`  
		Last Modified: Wed, 15 Sep 2021 16:38:49 GMT  
		Size: 189.3 MB (189296654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a264c35ad2f25c82a8e26fa4f2f031475f03e3beb60ceaa3586d58c92b8a00ac`  
		Last Modified: Wed, 15 Sep 2021 16:38:34 GMT  
		Size: 321.9 KB (321904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-windowsservercore` - windows version 10.0.14393.4651; amd64

```console
$ docker pull eclipse-temurin@sha256:eb8a526337ff6b121a34a462268c50424b7e97ed0cd5bc4a848dad3005c462f9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6460895524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb74fe89cdc3dc67956e0f0e24e93790d6e9d030fc19e31dd6b2099c30389cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 00:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 16:18:23 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Wed, 15 Sep 2021 16:19:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08.1/OpenJDK8U-jdk_x64_windows_hotspot_8u302b08.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08.1/OpenJDK8U-jdk_x64_windows_hotspot_8u302b08.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (fe3546a8e8dd7d4e929028ef3794431748caddf7fc1cf481618e8d6f8aa15427) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fe3546a8e8dd7d4e929028ef3794431748caddf7fc1cf481618e8d6f8aa15427') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 15 Sep 2021 16:20:26 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8721f004192f15fe71b8626ef3f3e34cbf2cfe1d15a63b6b544ab946162ef707`  
		Last Modified: Wed, 15 Sep 2021 01:10:18 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374a64236bc7e8e6315e9eb52690d1c0cadb55ac2ffc634ff4a0619797deebe6`  
		Last Modified: Wed, 15 Sep 2021 16:39:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1d055276ed3a42f9ed2467fab8915b088dc67b08a52cde8af1349db16260ff`  
		Last Modified: Wed, 15 Sep 2021 16:39:16 GMT  
		Size: 189.2 MB (189224086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626088b1f4933308e85d13b1a3da7527b5855d8687de85f7320aaee3ed65fc6d`  
		Last Modified: Wed, 15 Sep 2021 16:39:01 GMT  
		Size: 340.6 KB (340624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
