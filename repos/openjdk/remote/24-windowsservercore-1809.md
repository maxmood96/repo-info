## `openjdk:24-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:1661f2a8cdfb74924b0227d67882ac21544d9acb8a87e6562a899e4a793572e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:b37a707c3a6c0cf670aa51a58757988f48344785042a968991db413781ecd859
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452970727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0de14bf0f97d22d36db3ad47da5fa1bfdd77b4bf71630ff180abf12fedc3e3d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:19:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:20:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:20:23 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 13 Aug 2024 20:20:40 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:20:41 GMT
ENV JAVA_VERSION=24-ea+10
# Tue, 13 Aug 2024 20:20:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_windows-x64_bin.zip
# Tue, 13 Aug 2024 20:20:41 GMT
ENV JAVA_SHA256=a4e5b50291add1d88baf1093f1a4822dc3ee939111b1e039214cd2fcd729dc27
# Tue, 13 Aug 2024 20:21:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:21:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bbc6a3aa98c991beb51d75c3b0738eeb4fe060ae94448aa6e66a570d9ced86`  
		Last Modified: Tue, 13 Aug 2024 20:21:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a497c9508b4b83debe0298bdf5e425c0f5023a475045ac6787a533cdad9fc3d`  
		Last Modified: Tue, 13 Aug 2024 20:21:20 GMT  
		Size: 492.0 KB (492004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ed5838d7ab36f025c6d3fad97291e181a9fcc588be25ee8f94459a68508d34`  
		Last Modified: Tue, 13 Aug 2024 20:21:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89efff1f8dde9819449f91230d92702e4d75bc71c6577d0e571d4d1197ded16`  
		Last Modified: Tue, 13 Aug 2024 20:21:20 GMT  
		Size: 339.1 KB (339101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a22b772fa78396e7af8ed9842da3d87496b6b424c22e6bbd7bb31ff170538b7`  
		Last Modified: Tue, 13 Aug 2024 20:21:19 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad8b1368970f0ff7b2449a6d9cfdcc75139ecf30377cd2f9968492bd31b2d9a`  
		Last Modified: Tue, 13 Aug 2024 20:21:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff08f9d2ab02fe49a596aca68a3ddbedd40504d1247d9bb44c01b94c3ae20bb`  
		Last Modified: Tue, 13 Aug 2024 20:21:19 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a2cf64d23941c627096e36287d3b6c289935d808dd5e999a97e5240387c05`  
		Last Modified: Tue, 13 Aug 2024 20:21:30 GMT  
		Size: 206.9 MB (206928563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67019946cf2c72aa747350fa34b6eafdb20ee685626e48d76387df2d5b9ec4e`  
		Last Modified: Tue, 13 Aug 2024 20:21:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
