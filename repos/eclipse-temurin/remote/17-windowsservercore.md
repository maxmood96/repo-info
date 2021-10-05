## `eclipse-temurin:17-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:0a8894eb0b1b3edc98646a3aa3c4320ef52dd5fa57e469d0b88f4448b13277e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.230; amd64
	-	windows version 10.0.17763.2183; amd64
	-	windows version 10.0.14393.4651; amd64

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.20348.230; amd64

```console
$ docker pull eclipse-temurin@sha256:23e283f860fd53d8f9ffad25f9020ea7f494dd0194f31c4f37611f85c60757f5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2477896338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b38c6e09d13b5c7e8519808eda9b6332a6a9fc78b9fd08efd9e0695a551048`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Mon, 13 Sep 2021 07:01:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 15 Sep 2021 12:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Oct 2021 22:15:50 GMT
ENV JAVA_VERSION=jdk-17+35
# Tue, 05 Oct 2021 22:16:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_windows_hotspot_17_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_windows_hotspot_17_35.msi ;     Write-Host ('Verifying sha256 (4a0350a9e3e0cf3bba9a57890bb0b223b7c47883169730f122100fc31d61d486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4a0350a9e3e0cf3bba9a57890bb0b223b7c47883169730f122100fc31d61d486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 05 Oct 2021 22:17:25 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 05 Oct 2021 22:17:26 GMT
CMD ["jshell"]
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
	-	`sha256:5f4590dd4af80a57c4eacb969b7e8742fe20ca0f81d3d80c324ed348723687f8`  
		Last Modified: Tue, 05 Oct 2021 22:28:28 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d490220f31555195db5f62c6f745ba30e7083da6fc64a44c81b6ceb356b96b`  
		Last Modified: Tue, 05 Oct 2021 22:34:48 GMT  
		Size: 352.4 MB (352443678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda018a0b4481d39fd82ebc6502b8d2ae549c892c70ff88f24229cf1ed3e021a`  
		Last Modified: Tue, 05 Oct 2021 22:28:29 GMT  
		Size: 573.9 KB (573906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a9689150af988f6c4ee7568756b1a1985d25f96076ca6f4609394c48caa0b8`  
		Last Modified: Tue, 05 Oct 2021 22:28:28 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.17763.2183; amd64

```console
$ docker pull eclipse-temurin@sha256:a82784dae7d4d1aa931a17ba9148472efb57395b3c368cb74f7a461235644112
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3042804057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d2b943b9d173cc14dd17f03155a8dc2a7d681d888ebd65276c6d7f6f5e4cbc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Sep 2021 19:15:34 GMT
ENV JAVA_VERSION=jdk-17+35
# Wed, 22 Sep 2021 19:17:30 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_windows_hotspot_17_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_windows_hotspot_17_35.msi ;     Write-Host ('Verifying sha256 (4a0350a9e3e0cf3bba9a57890bb0b223b7c47883169730f122100fc31d61d486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4a0350a9e3e0cf3bba9a57890bb0b223b7c47883169730f122100fc31d61d486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 22 Sep 2021 19:18:48 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 22 Sep 2021 19:18:49 GMT
CMD ["jshell"]
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
	-	`sha256:8c7bc84dd2ef854244ef9f7b1caee8d74639379e182ee9e4f3a6a2c184069654`  
		Last Modified: Wed, 22 Sep 2021 19:24:58 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709113e5bf3e2809b5096023ece3c9e088bcef42c216e30e4098103056a70895`  
		Last Modified: Wed, 22 Sep 2021 19:25:29 GMT  
		Size: 352.2 MB (352199477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff708a91afddfce768ffad2f5a814cc77bf95b73106cbb6356db91f105eedc5e`  
		Last Modified: Wed, 22 Sep 2021 19:25:00 GMT  
		Size: 3.9 MB (3902550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09db3cb2244bb78aefea4c2a1996890b1471ea8d7d939d461b8416102600a4e9`  
		Last Modified: Wed, 22 Sep 2021 19:24:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-windowsservercore` - windows version 10.0.14393.4651; amd64

```console
$ docker pull eclipse-temurin@sha256:6924b3cac13f1ac82af6e1c40e25b5cde82c8a82a9fd2c6965e5ef67d75e62a5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 GB (6627329938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6fc83bd90649092deac8e4f8399da9ddfe35a4bab8fd44e34bcf411b0a885d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 00:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Sep 2021 19:19:00 GMT
ENV JAVA_VERSION=jdk-17+35
# Wed, 22 Sep 2021 19:20:47 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_windows_hotspot_17_35.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_windows_hotspot_17_35.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (4a0350a9e3e0cf3bba9a57890bb0b223b7c47883169730f122100fc31d61d486) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4a0350a9e3e0cf3bba9a57890bb0b223b7c47883169730f122100fc31d61d486') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 22 Sep 2021 19:22:04 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 22 Sep 2021 19:22:05 GMT
CMD ["jshell"]
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
	-	`sha256:f49d9944f0ee26658bd3b061f70175331db2d135498f135b51e2d56bc91296f0`  
		Last Modified: Wed, 22 Sep 2021 19:25:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe1184e431040d16efe337b3e1c033ffd44b3e31e8c40cf3280dd67725cc262`  
		Last Modified: Wed, 22 Sep 2021 19:26:11 GMT  
		Size: 352.1 MB (352119229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0068fbe946985173169c879030f09738015917ae0723f10296e944cde09ec9`  
		Last Modified: Wed, 22 Sep 2021 19:25:43 GMT  
		Size: 3.9 MB (3878599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d22dcfef501c6b259fb677722a930d25a48b97a0eba137de4b785c00ae0221`  
		Last Modified: Wed, 22 Sep 2021 19:25:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
