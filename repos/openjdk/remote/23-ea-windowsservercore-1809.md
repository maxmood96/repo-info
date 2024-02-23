## `openjdk:23-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:a5ab2743c68a8039ad882e52873591aa14b5e21e952f5a6af76b473ee09a6996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:23-ea-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:ad9ce7de2c92e5179d6c8d98f7ae7da9f898c358c8e7e0d8278c41bc2cac0e2a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279186044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df70b926204063cb98524a4af5f20ef9083ae407e9563768716817f5fb9d16f2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Fri, 23 Feb 2024 18:50:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 Feb 2024 18:52:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 23 Feb 2024 18:52:55 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 23 Feb 2024 18:53:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 Feb 2024 18:53:19 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 18:53:20 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_windows-x64_bin.zip
# Fri, 23 Feb 2024 18:53:20 GMT
ENV JAVA_SHA256=167f31bd2f9f57f80f3b9b1104f4dacd7e48a48492d29ef494a5fecba08656cc
# Fri, 23 Feb 2024 18:54:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 Feb 2024 18:54:17 GMT
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
	-	`sha256:6024fb4cd81d7ac90d91b84e2f28826df7f2b8b5e3fe552f3fed8c363c19a6bc`  
		Last Modified: Fri, 23 Feb 2024 18:54:23 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6534e187f4af2e39e55958f2f5b68908caca84bfd509779abd45ac3b1ee0e19`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 483.3 KB (483283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650e010b1102d08d44308a68e67331f2c51b633d2bab65247c3635744bf6aef7`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c674bdeb7f01c551e534200e4f915c966fd7b59cfa588436c3b5ee711700537`  
		Last Modified: Fri, 23 Feb 2024 18:54:22 GMT  
		Size: 330.3 KB (330277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e473ba1e5ed34ad0f7b441d0a87afb1d908100d9415e82b6780c00916dd1bf`  
		Last Modified: Fri, 23 Feb 2024 18:54:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9a4a94b2d8601ec66cdea170e44b00d0927b2ad69ad571e815e18c5bba47a7`  
		Last Modified: Fri, 23 Feb 2024 18:54:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8336069eea149677b07afc9edd0ff2a2e7a781c79ed89752bd7c354706dbcddd`  
		Last Modified: Fri, 23 Feb 2024 18:54:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cfe964e6d341fb8f51af759b0f64cc0e1f413a731c9f960e661e2791f2870`  
		Last Modified: Fri, 23 Feb 2024 18:54:31 GMT  
		Size: 197.9 MB (197915927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5cd0e93c49ade4a35bda4d524bd9e36f89dbc0f31af21a44759ec249783968`  
		Last Modified: Fri, 23 Feb 2024 18:54:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
