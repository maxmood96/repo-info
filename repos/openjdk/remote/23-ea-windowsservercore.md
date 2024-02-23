## `openjdk:23-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:924c2cfd4545167ab74b933d0acf3cc302d9f2235c4d1356869fc1909437fbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `openjdk:23-ea-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull openjdk@sha256:5716d37f5f1d6491c4dc6341a6066674f30a1cc71f72da781ce0a27faeda4699
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2109351610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314cc6c156b8f642256fc228a6054fae85d682cc088e8c70dd6180dbb40e2ac6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Fri, 23 Feb 2024 18:50:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 Feb 2024 18:51:53 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 23 Feb 2024 18:51:54 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 23 Feb 2024 18:52:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 Feb 2024 18:52:01 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 18:52:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_windows-x64_bin.zip
# Fri, 23 Feb 2024 18:52:04 GMT
ENV JAVA_SHA256=167f31bd2f9f57f80f3b9b1104f4dacd7e48a48492d29ef494a5fecba08656cc
# Fri, 23 Feb 2024 18:52:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 Feb 2024 18:52:33 GMT
CMD ["jshell"]
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
	-	`sha256:7349fe05ff7b37958c58564666b63208fd99490f6809621778df398310e1d324`  
		Last Modified: Fri, 23 Feb 2024 18:52:41 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2045b1fe14867f64d77fef3ded9918b493294f25399c491fc2f0547dfba8e5c`  
		Last Modified: Fri, 23 Feb 2024 18:52:41 GMT  
		Size: 493.8 KB (493761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb9ea11d6c99a63ab265162d136331bafbeed6ff66956d17c7b39b4950c55c8`  
		Last Modified: Fri, 23 Feb 2024 18:52:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323d936be40f7a6065604bff9b819456b27e4fe3c7716e7c1542704cd2b462f6`  
		Last Modified: Fri, 23 Feb 2024 18:52:41 GMT  
		Size: 312.5 KB (312525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7d3976a538775a79d9605ae29b99e8a541f89d5b610ac73f2f0de2746f4011`  
		Last Modified: Fri, 23 Feb 2024 18:52:38 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578a7f9d1da82109f3182f0743e09fad6ed2f2a56e557418aaa916fc6aaf7e30`  
		Last Modified: Fri, 23 Feb 2024 18:52:38 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01edce806f9741e5d5c368ebcbf8a1126685ae3ac82ec7ec9ec607e794ccc1b1`  
		Last Modified: Fri, 23 Feb 2024 18:52:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9811c2d97fc5d4418f481618551f1e43932697a35598cb72748efe96fc710c95`  
		Last Modified: Fri, 23 Feb 2024 18:52:50 GMT  
		Size: 197.9 MB (197883267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7fa4c16a8feee766b4426db5d2dd160bec0060481e4e1f859edbddcdedd974`  
		Last Modified: Fri, 23 Feb 2024 18:52:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-windowsservercore` - windows version 10.0.17763.5458; amd64

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
