## `openjdk:23-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:ada4a7a71eced6a62e57ab30246d627efa4cc4a50cd8948491a908108b2222f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:23-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:00b79c90acfe3e493401e521edc4c573630fccd5943634b941e28cad025171fd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268366673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86eec17e97d059515c3986ac9074f3d6ac8b705eb510fb454b3280db06f00b5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:05:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:06:02 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:06:02 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 11 Jan 2024 00:06:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:06:25 GMT
ENV JAVA_VERSION=23-ea+4
# Thu, 11 Jan 2024 00:06:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_windows-x64_bin.zip
# Thu, 11 Jan 2024 00:06:26 GMT
ENV JAVA_SHA256=14230e6d57a3b39a3b5e232e7095fe1821a48197f75b68ae0f09db29e5391216
# Thu, 11 Jan 2024 00:07:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:07:07 GMT
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
	-	`sha256:2ddd69853f8196922e8e23c70d2ba14a7349d4aa076f88e17f3f4ae96fd6c83f`  
		Last Modified: Thu, 11 Jan 2024 00:07:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e86a0a96929084896173eded50df0a42c5dfc0f58653e3f2a9ec86a014aaaa1`  
		Last Modified: Thu, 11 Jan 2024 00:07:14 GMT  
		Size: 487.6 KB (487583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd93d189f2cd720cc5a9e8556d5a582a109c9b2e40ba3610336eaf91d8701af4`  
		Last Modified: Thu, 11 Jan 2024 00:07:14 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562c23cc9c7ef632a9ead49e40096e27a14bae01b473c999a9847011bb1b63d`  
		Last Modified: Thu, 11 Jan 2024 00:07:14 GMT  
		Size: 340.3 KB (340268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba769df7dcc3ffd716295bab2ff07734ac9df51898e4ca21ca26c6177f70c0d`  
		Last Modified: Thu, 11 Jan 2024 00:07:12 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca84b7f9dac799ec366590beb4595ada1c42690853b9efd8e6486638152c9ae7`  
		Last Modified: Thu, 11 Jan 2024 00:07:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756d3c564c2030a500b10765049e9634bad015735adb01ce17a6c46900ed47a6`  
		Last Modified: Thu, 11 Jan 2024 00:07:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c6f972c7547d8b3c9e4cd79930ed242ff52b130c0f4c255d38148e235c51fd`  
		Last Modified: Thu, 11 Jan 2024 00:07:23 GMT  
		Size: 197.8 MB (197808540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742991286e01a4716e15cf8287b0a70a45fc25393c99e9667591ceb470e430bb`  
		Last Modified: Thu, 11 Jan 2024 00:07:12 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
