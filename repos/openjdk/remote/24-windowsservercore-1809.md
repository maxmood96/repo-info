## `openjdk:24-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:e9b59b5c0410968999d194ccafba160a6234b56a548bb7b6648bd81ba59ba631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:9e83892fbb8636b55ec6b81c742f2d3a7d799d4f2e24d1b53b81224bcdec2ece
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2428132332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7685361e79ed9a03691c7aff662894b8e5238eeb1c2b9603be8efd9006aca9e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Mon, 08 Jul 2024 20:56:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Jul 2024 20:57:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:57:35 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 08 Jul 2024 20:58:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:58:00 GMT
ENV JAVA_VERSION=24-ea+5
# Mon, 08 Jul 2024 20:58:01 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_windows-x64_bin.zip
# Mon, 08 Jul 2024 20:58:02 GMT
ENV JAVA_SHA256=6311a1a2de647471859f4eda1f035e7da59a26882c2bc3e456a97e88b9e9647b
# Mon, 08 Jul 2024 20:58:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:58:56 GMT
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
	-	`sha256:03f6032f3b64aecc584eb246371e0dbbf17c90a5b6a5554366fd9235c797bbcc`  
		Last Modified: Mon, 08 Jul 2024 20:59:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17aa3d7d72129f6ef32c7e8454c0e6695ec205efd5e8defb19af35caffeef772`  
		Last Modified: Mon, 08 Jul 2024 20:59:03 GMT  
		Size: 499.9 KB (499931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bf3dbfdd8caccdebcdb432ed731cfc8526995be0a96db5ba97aeaa001ec8d0`  
		Last Modified: Mon, 08 Jul 2024 20:59:03 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb749df4a0390d04e45fa5901c7dde1bd18500759a7e5fb0d4f9de11baec923`  
		Last Modified: Mon, 08 Jul 2024 20:59:03 GMT  
		Size: 355.0 KB (354967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa9303a7aca9812093b3421f2d68f5732d11c329fb7a77db60a8f598515cd8c`  
		Last Modified: Mon, 08 Jul 2024 20:59:01 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b256312bb4649dd394ecc2522f2e4e31709961eb24a712b8beb20805df9cfe7`  
		Last Modified: Mon, 08 Jul 2024 20:59:01 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52485716f5016887a660a380276adfa40a4acc30bbeeb9861b4ce1c4f04fc75`  
		Last Modified: Mon, 08 Jul 2024 20:59:01 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29eeaf502b9f722fc7866935f8074f375b4f8d3deab2ae41fa18de5aff2eace`  
		Last Modified: Mon, 08 Jul 2024 20:59:11 GMT  
		Size: 206.6 MB (206588484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310ed6c903e384fecfd8fd76c6669cbd5540347c679c6eaa400441821c5af02e`  
		Last Modified: Mon, 08 Jul 2024 20:59:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
