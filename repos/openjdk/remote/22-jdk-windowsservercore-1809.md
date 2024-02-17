## `openjdk:22-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:716187b012aae561e8b35f3f3fcd3fcabaaa73c69bbe430ed5c05f9606e95a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:22-jdk-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:93da8acac2a10f5a5ec5000a1365f28e6fff7fec829d628bbe951c969c95e04f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278988647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9964abfc648ec59ecf313b658120a5fac5523c1e6e41a3b39f55c5ad31b05d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Sat, 17 Feb 2024 01:07:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 17 Feb 2024 01:09:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:09:07 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 17 Feb 2024 01:09:27 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:09:28 GMT
ENV JAVA_VERSION=22
# Sat, 17 Feb 2024 01:09:28 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_windows-x64_bin.zip
# Sat, 17 Feb 2024 01:09:29 GMT
ENV JAVA_SHA256=8f5138fecb53c08c20abd4fa6812f9400051f3852582a2142ffda0dff73a5824
# Sat, 17 Feb 2024 01:10:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:10:07 GMT
CMD ["jshell"]
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
	-	`sha256:54741948d684c2cf84f1babf4aedc31ba0ca3dc0d64b7adf3505e59a92f48b62`  
		Last Modified: Sat, 17 Feb 2024 01:10:11 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd53584de83e21bd6543fbd15e6631085f4fbd5412e9b43952ac49633af4b30b`  
		Last Modified: Sat, 17 Feb 2024 01:10:12 GMT  
		Size: 473.7 KB (473661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae48f4eb91d9b63d83f88289dcf9bd836832cc1ac7bb83d150e43db66264b22`  
		Last Modified: Sat, 17 Feb 2024 01:10:11 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d6944bf5a4d2950bc78f96656da2437f1d1ad3a9c64d85f498acf8de1d7374`  
		Last Modified: Sat, 17 Feb 2024 01:10:11 GMT  
		Size: 325.9 KB (325883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba5a3e24491186483f33b899fc4dc752a2f08208dfc5bceb50e61eda22baf13`  
		Last Modified: Sat, 17 Feb 2024 01:10:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a869ee8411dd74c168214deb3d8161a143fd4e44c0f5166ee27b3f111f16ec`  
		Last Modified: Sat, 17 Feb 2024 01:10:10 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a655dc6663c2af2d739609f26e2c7269346837b87ef4bdc50e7158b0baf6f904`  
		Last Modified: Sat, 17 Feb 2024 01:10:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d7bd202ab86057f72700a11d269c2db0b097b8dbac38c76157ef3235d7bd68`  
		Last Modified: Sat, 17 Feb 2024 01:10:21 GMT  
		Size: 197.7 MB (197732548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e0addaedddfe4f019a9ee22f42446a93688888391527b1f818664d63fa6e98`  
		Last Modified: Sat, 17 Feb 2024 01:10:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
