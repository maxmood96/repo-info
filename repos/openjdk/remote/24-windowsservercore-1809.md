## `openjdk:24-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:92c6337dc1ee67aaea2d65361bc84e244c9ccce766aea905b543334af925124c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:724da096bede9221f23474009aab5d407da23fc0bba24ee2777640f9fe019fcc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2428039368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc9c72e968e66279df511c0d4f24cc673fcfbc29655d26dd36e04bc02b8aad4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Sat, 22 Jun 2024 01:05:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 01:05:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:05:59 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 22 Jun 2024 01:06:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:06:17 GMT
ENV JAVA_VERSION=24-ea+3
# Sat, 22 Jun 2024 01:06:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_windows-x64_bin.zip
# Sat, 22 Jun 2024 01:06:18 GMT
ENV JAVA_SHA256=dadb681c56ce901258f2c4dc34514ff6eb2b62bddf51f507bebdabac55556dbb
# Sat, 22 Jun 2024 01:06:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:06:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65df50674fcb3583cf9f30e86675e3af91ee62fa3b4667aa3cb801f564bbe7ea`  
		Last Modified: Sat, 22 Jun 2024 01:06:59 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4ab91cf5180bfb888113be71b494d2d3b9a705ca2e9fd7bfc244e7edffffbb`  
		Last Modified: Sat, 22 Jun 2024 01:06:59 GMT  
		Size: 482.7 KB (482694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56c48c7f1d2d6b1863fed5010ae70c850fea68d073311c9f00e65dd188106c5`  
		Last Modified: Sat, 22 Jun 2024 01:06:59 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bbcc6305feb2161848d9186fa681e2dd5d9cd6d564b80be43fc0674255671c`  
		Last Modified: Sat, 22 Jun 2024 01:06:59 GMT  
		Size: 329.3 KB (329327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07799742efd75ef9d1340934392e3a4c64f17d4d69af40bb071079abfb595f2`  
		Last Modified: Sat, 22 Jun 2024 01:06:57 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fa1fdf33f0155b2f957d781e98faf3cbce7e6573588bdb4916bb3915a231de`  
		Last Modified: Sat, 22 Jun 2024 01:06:57 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff97dac9a3556251d08f3d837f7c6584d7d0efaafe2c6ca2b896f7daf53f0cc`  
		Last Modified: Sat, 22 Jun 2024 01:06:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea5b01ef4d25ee608bc474a5b382a9d2e8bec4ae36c1b8ffec72113a12ac080`  
		Last Modified: Sat, 22 Jun 2024 01:07:08 GMT  
		Size: 206.5 MB (206538388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ec74986f089dbd11e2b9df97fddc5fc2b22cac0a471183e79aefa2a0b8839c`  
		Last Modified: Sat, 22 Jun 2024 01:06:57 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
