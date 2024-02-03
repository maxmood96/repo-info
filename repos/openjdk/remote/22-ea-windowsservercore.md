## `openjdk:22-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:c204742c939e50810a9ee67d4c2f760ed58de6887deb41ac6ae3a8eaf48df039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-ea-windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull openjdk@sha256:0fac0c1157cb1c6ab607635dd48d870cf7770275a25901d9bfecd797b17a951d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098740414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a5ceb93a60f07a917cda717fcd79612cdc4e112b2df34c8ac1e686106906a5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Fri, 02 Feb 2024 22:53:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 02 Feb 2024 22:54:29 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:54:31 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 02 Feb 2024 22:54:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:54:43 GMT
ENV JAVA_VERSION=22-ea+34
# Fri, 02 Feb 2024 22:54:44 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_windows-x64_bin.zip
# Fri, 02 Feb 2024 22:54:45 GMT
ENV JAVA_SHA256=12ee86b08be5cff14ecd89338b34d561c86a064e51083df43d4369c60cc8b99f
# Fri, 02 Feb 2024 22:55:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:55:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a6a96ea8a0c9224344e2fab15d90a9d1144f92c42d13fce5d03881efa2921d`  
		Last Modified: Fri, 02 Feb 2024 22:55:27 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200f4103a1fd1f3561d8e1a042c0492b11caf68052060b46b1bc99c14bf1818c`  
		Last Modified: Fri, 02 Feb 2024 22:55:26 GMT  
		Size: 495.6 KB (495629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c3bf6975b86c2c64876f2b922f224a5c8b748176e069e8ca7af39173699978`  
		Last Modified: Fri, 02 Feb 2024 22:55:26 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129f308f14ae9ea492880300e2c846eff1a6b54d507d2de3a115ff5688ed1b8d`  
		Last Modified: Fri, 02 Feb 2024 22:55:26 GMT  
		Size: 313.7 KB (313708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6de5d655eb3730debb79e4c3259e4664e5f214c037369e131619ab50a3ee0c`  
		Last Modified: Fri, 02 Feb 2024 22:55:25 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbeb1b1a01bebefdf179d2ef066a3dcea58f2f2d3fdf4346ea8d5ab25a6a6214`  
		Last Modified: Fri, 02 Feb 2024 22:55:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d9e56461c9cda0375f32ea3ed8f23a930b108d8cfa282ceed3aff09d637ea3`  
		Last Modified: Fri, 02 Feb 2024 22:55:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc4a36e93d3517cbaeb18c5daa3ed43c691a1d0012f78a2351b844fdfc17636`  
		Last Modified: Fri, 02 Feb 2024 22:55:35 GMT  
		Size: 197.7 MB (197710676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28197292d6648c8acbb75a434ddfe5bca3a274309988206c8a13de42fc31690`  
		Last Modified: Fri, 02 Feb 2024 22:55:25 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:802ce74784537af6a42a34110dfeb48ec2272b0876ee4dd9022f3dfde82ec7fe
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268344531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c69c828e9b0ebd451f4354e496092465d1ad07af51a7b877f32d84597a50b92`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Fri, 02 Feb 2024 22:53:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 02 Feb 2024 22:55:42 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:55:43 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 02 Feb 2024 22:56:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:56:07 GMT
ENV JAVA_VERSION=22-ea+34
# Fri, 02 Feb 2024 22:56:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_windows-x64_bin.zip
# Fri, 02 Feb 2024 22:56:08 GMT
ENV JAVA_SHA256=12ee86b08be5cff14ecd89338b34d561c86a064e51083df43d4369c60cc8b99f
# Fri, 02 Feb 2024 22:56:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 02 Feb 2024 22:56:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca26554e8da250956f06f6b8c4b0cd822339c41c80230218f07c4ed98e3372e`  
		Last Modified: Fri, 02 Feb 2024 22:57:07 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf49dddfcb81c93ef1b80d6d2bc8994ada5c47a91066ede5fa1b0fcb1737641d`  
		Last Modified: Fri, 02 Feb 2024 22:57:07 GMT  
		Size: 500.5 KB (500467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9547eb6a8f767dd4fc0503983d923a20dafdb5e60a3dc8aba6b6a946585dcffc`  
		Last Modified: Fri, 02 Feb 2024 22:57:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed3fc1386c8010b08dd6f3cc46453b3b85a7a176e943a363d481a6d29853936`  
		Last Modified: Fri, 02 Feb 2024 22:57:07 GMT  
		Size: 347.2 KB (347250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f048059228d8e4b4894dd1a6e587bf986ffb1bd4124c668edfbcb4f5ea1631`  
		Last Modified: Fri, 02 Feb 2024 22:57:04 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915d6990d86a99a9be5495fcb2411301a3ee77d1494ad05fe9c923e74c871603`  
		Last Modified: Fri, 02 Feb 2024 22:57:05 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a93d1d43a7859f237f24d32646fbd0724d3b768f37628707ed7eac42bb3aea`  
		Last Modified: Fri, 02 Feb 2024 22:57:04 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd609dec4f9a86cce5b9e970c383219a0b6bb93d885421ab748b75b33849ed65`  
		Last Modified: Fri, 02 Feb 2024 22:57:15 GMT  
		Size: 197.8 MB (197766184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898865fe6afea94596e4acffb6c0df1f470a9e206d148aca885fbf592d531b18`  
		Last Modified: Fri, 02 Feb 2024 22:57:04 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
