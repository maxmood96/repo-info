## `openjdk:22-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:95458699dbc665b264ec9ed851e670ba9aa34d6b22f46b6dd0fad35e188b86bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `openjdk:22-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:ace3a485cc43b95130d753c5f10cf0ab84de3f303e3cae20790a81e683be5849
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323721062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f449edb0e6083efcdc1d5c0779c890db3d25613c9827fda66b5de51a0c7d455e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:06:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 00:06:56 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Mar 2024 00:06:57 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 13 Mar 2024 00:07:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 13 Mar 2024 00:07:25 GMT
ENV JAVA_VERSION=22
# Wed, 13 Mar 2024 00:07:25 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_windows-x64_bin.zip
# Wed, 13 Mar 2024 00:07:26 GMT
ENV JAVA_SHA256=8f5138fecb53c08c20abd4fa6812f9400051f3852582a2142ffda0dff73a5824
# Wed, 13 Mar 2024 00:08:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 13 Mar 2024 00:08:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8a15734c0eaec184cda3413f2571154d9bb80bf601da921d83dd4a706f1ab4`  
		Last Modified: Wed, 13 Mar 2024 00:08:23 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d116fd28edfe867fbeb6b0d96dcb2644e35555fa1755edb08118b0d6ad3e288a`  
		Last Modified: Wed, 13 Mar 2024 00:08:23 GMT  
		Size: 503.2 KB (503167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d859574128f0ca1278e8047c236a00be3638a162f547d3d73f0a2516c11533d`  
		Last Modified: Wed, 13 Mar 2024 00:08:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de71e0a000e3174e22fde939bddb653ca9788a280e310863b125205ebf0fd3c`  
		Last Modified: Wed, 13 Mar 2024 00:08:23 GMT  
		Size: 354.6 KB (354615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e215510ccb449cfca569d0cebd98d0d50ebbd2c13319fa2b31a37bb9e5090ce`  
		Last Modified: Wed, 13 Mar 2024 00:08:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608b300cd6072c1cddd49cab29b228d761d71b17eef5915171eb9ddd90aab02e`  
		Last Modified: Wed, 13 Mar 2024 00:08:20 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3012331e0199a29bba0f7cfdd6db888bfc1bc02bbca3e3e91bf0e91b20cc6f`  
		Last Modified: Wed, 13 Mar 2024 00:08:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a748726622a545777d3127c34d8cdaabe2aab21f44bc479b3960106d2af3f6b`  
		Last Modified: Wed, 13 Mar 2024 00:08:32 GMT  
		Size: 197.8 MB (197755546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592104761c6adf65d0857211221d2b07a7299ce86224bee59d9c010146098f6f`  
		Last Modified: Wed, 13 Mar 2024 00:08:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
