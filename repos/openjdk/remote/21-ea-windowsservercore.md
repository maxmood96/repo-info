## `openjdk:21-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:375e369a0b7e969a5d54c67865b7e9f05e545792f6e6fbaaff16c0193ce003ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `openjdk:21-ea-windowsservercore` - windows version 10.0.20348.1787; amd64

```console
$ docker pull openjdk@sha256:a9bc2bd00defa8a0dfa301ce8cd0ba53a471471382cf060bb2912da2b01365e7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1625120173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b6317f199fd5f9cb185cce5bba942bf6627998316e1879a6a8e4f989cf2bef`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:03:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:07:27 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 24 Jun 2023 03:07:49 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:07:49 GMT
ENV JAVA_VERSION=21-ea+28
# Sat, 24 Jun 2023 03:07:50 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/28/GPL/openjdk-21-ea+28_windows-x64_bin.zip
# Sat, 24 Jun 2023 03:07:51 GMT
ENV JAVA_SHA256=cf31047fdf44c7303408c4868c810af10ec573e926925041e621f0d5acca4583
# Sat, 24 Jun 2023 03:08:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:08:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de10d117b5ef80c7852b0714d37536955d84892882d5f3f97a4d53631493623`  
		Last Modified: Sat, 24 Jun 2023 03:12:27 GMT  
		Size: 318.8 KB (318813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eec6f45c20e189779c1a14ac267c15e9db3eefe85034e40b6f92372759a288a`  
		Last Modified: Sat, 24 Jun 2023 03:14:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb14372fe1d2fbfda13afae0e93eb2611308220211945e4daea088ac9989f16`  
		Last Modified: Sat, 24 Jun 2023 03:14:22 GMT  
		Size: 262.8 KB (262765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869df31a3297f47245f24644db804b87052e167ca814c38607b9c0fe307be50c`  
		Last Modified: Sat, 24 Jun 2023 03:14:20 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f0aa33d5bed85ad23deb10de330e5f0bdff672f0059dc084fda4699d7e0584`  
		Last Modified: Sat, 24 Jun 2023 03:14:20 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b890d99cd3820f9ba63cc332a38719a17bb0446377756d6f827b458554d824`  
		Last Modified: Sat, 24 Jun 2023 03:14:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6be8178551a27e534f8aed7c9fa95517e8fae7dd9e5632c3f35cffd9866bb5`  
		Last Modified: Sat, 24 Jun 2023 03:14:41 GMT  
		Size: 198.2 MB (198231930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bf66288ddd519e2329df75f7f31ce46b87af8731d5767feb9b7ccb6ffeb9b2`  
		Last Modified: Sat, 24 Jun 2023 03:14:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull openjdk@sha256:b599075b1eaaad605d6c9261d35ad9bb4b88c6390dd023204e6c15950ac97472
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849541574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18fc04e03e47ca2eac753106eba08d4615471585bc47fd577e4b785db44ea6c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:05:10 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:08:57 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 24 Jun 2023 03:09:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:09:25 GMT
ENV JAVA_VERSION=21-ea+28
# Sat, 24 Jun 2023 03:09:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/28/GPL/openjdk-21-ea+28_windows-x64_bin.zip
# Sat, 24 Jun 2023 03:09:26 GMT
ENV JAVA_SHA256=cf31047fdf44c7303408c4868c810af10ec573e926925041e621f0d5acca4583
# Sat, 24 Jun 2023 03:10:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:10:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aac08fa1b04894a4c928b70e656c1b7852ba8379bb8fe87ce2a32e04c6af9b`  
		Last Modified: Sat, 24 Jun 2023 03:13:06 GMT  
		Size: 307.3 KB (307316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45aa53985d3c6e3bd4fcce6d694b149911e0c5343f6380fd1ec2d15bb1785bc`  
		Last Modified: Sat, 24 Jun 2023 03:15:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ce23ce645a5dda4243eb19c02651350dc76a2c74b280bc5a856d95aed9c042`  
		Last Modified: Sat, 24 Jun 2023 03:15:00 GMT  
		Size: 258.0 KB (257954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc42b0169e329a9bedb220776ce841fbeab85808fefcb12953f0fc67dd7c1573`  
		Last Modified: Sat, 24 Jun 2023 03:14:58 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ab27da041f1d87c5ed008f7d126c3aa87b848a32afeebf886eefabd249444d`  
		Last Modified: Sat, 24 Jun 2023 03:14:58 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ebacb861c6488188816f937d01837ef7d82bd5a4ba82f335692fc8c420046b`  
		Last Modified: Sat, 24 Jun 2023 03:14:58 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b577f17062396d1e1a28c2b521dddac9c817c2c30dbfd6d560d852e7451c163`  
		Last Modified: Sat, 24 Jun 2023 03:15:18 GMT  
		Size: 198.2 MB (198231163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394d553905b9d2e03f253563d0fca80592db7726481bff29e06b2eba5b4cc7be`  
		Last Modified: Sat, 24 Jun 2023 03:14:58 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
