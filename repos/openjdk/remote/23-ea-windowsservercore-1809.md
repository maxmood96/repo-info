## `openjdk:23-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:c53c9fc50bf83ac393395a861da4c32d6649bfa18c8d42b5b595dcb115d1dcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:23-ea-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:6ad28fa40857623c5a106ba95dd758bb58cd7e6e073eea9fc8c1e63de6e79b18
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2427989654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e697e76e8bf8defa9ea349eb4a83f4b28fbbbdf32dc872c4084637a26a93d485`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Tue, 02 Jul 2024 00:57:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 00:58:30 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:58:31 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 02 Jul 2024 00:58:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:58:54 GMT
ENV JAVA_VERSION=23-ea+29
# Tue, 02 Jul 2024 00:58:54 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_windows-x64_bin.zip
# Tue, 02 Jul 2024 00:58:55 GMT
ENV JAVA_SHA256=58846b365aa5e7c3baedfba5852277c20d27949d25686685aee0c5b6896f7d77
# Tue, 02 Jul 2024 00:59:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:59:40 GMT
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
	-	`sha256:fb977b62184d8883ac9d4e3daea6b282cfc1237e43a07cafe2a80bd49e9fe0bc`  
		Last Modified: Tue, 02 Jul 2024 00:59:45 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d33e4ce7a0b18cdba54559146c1b51b977526b82ce9d6015a7f453222a911d3`  
		Last Modified: Tue, 02 Jul 2024 00:59:45 GMT  
		Size: 500.0 KB (500013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac58816af801d4d5779bd93c716892bedb3e327d4c6479b7654c15d9627e63c9`  
		Last Modified: Tue, 02 Jul 2024 00:59:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e89f0d25e172e7c8f7588378afa1b1702a72bed69af928f7914f6d2c86086`  
		Last Modified: Tue, 02 Jul 2024 00:59:45 GMT  
		Size: 354.3 KB (354342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9678d5d56a4981d3b6a7a59b8e2b43b9dbdcc55346f996267af68fc017369894`  
		Last Modified: Tue, 02 Jul 2024 00:59:44 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75a1af750c9d4771c7ec39f26952298dff166b249eff49cb4deda573bf4fdf3`  
		Last Modified: Tue, 02 Jul 2024 00:59:44 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490583eaf4f3c4af56bfe469659a0d272ceb01b824700f52a9b1a1c14dd66db0`  
		Last Modified: Tue, 02 Jul 2024 00:59:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3164425146729a5047bf19e838e95bb69abd9ba99e8c169559d29ad0a1af38f`  
		Last Modified: Tue, 02 Jul 2024 00:59:54 GMT  
		Size: 206.4 MB (206446300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38059dea5b5967d3d244c444c3c02c7d0fdffa1e6200b496f9bfbc849881487e`  
		Last Modified: Tue, 02 Jul 2024 00:59:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
