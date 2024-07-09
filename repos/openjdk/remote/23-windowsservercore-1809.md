## `openjdk:23-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:674832ff6e00cfbd24b72a149801f6464f4c1bdf62499a5ccb829c198f657d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:23-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:f4cdb916f604d02949209b4f414905ce26cc35cf41ab03df256a028208cd0f0e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2428027912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d9834731cf00b529e6e6228612af7b067cf0ac453dc2be190d9764c52c1d39`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Mon, 08 Jul 2024 20:56:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Jul 2024 20:58:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:58:52 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 08 Jul 2024 20:59:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:59:15 GMT
ENV JAVA_VERSION=23-ea+30
# Mon, 08 Jul 2024 20:59:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_windows-x64_bin.zip
# Mon, 08 Jul 2024 20:59:16 GMT
ENV JAVA_SHA256=bbefe5300370b3a67927c127a1e24a08b8cb1dd37d41b428ed931836e092652b
# Mon, 08 Jul 2024 21:00:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 08 Jul 2024 21:00:03 GMT
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
	-	`sha256:809bedf4f669af1ca0810b50bd172037725ebabd496fad72374355850790ef3f`  
		Last Modified: Mon, 08 Jul 2024 21:00:09 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20e848496453ff70dce38c1ad6715e48ef1b3b59e671dc5ff9c7e5eee9694c6`  
		Last Modified: Mon, 08 Jul 2024 21:00:09 GMT  
		Size: 513.0 KB (512987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221463581ed7cb0c6cf55ad53177e133c4dfd7497d0b7693d2cc1ff093d17302`  
		Last Modified: Mon, 08 Jul 2024 21:00:09 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395347908a1478efaf5efdba08b8664c209c421262a80e06f1f0b0c2bdc73937`  
		Last Modified: Mon, 08 Jul 2024 21:00:09 GMT  
		Size: 367.2 KB (367162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca8456a882a1252e88032ae3a3103cd2cf2ae215b1ad54cf4330db2bc92178d`  
		Last Modified: Mon, 08 Jul 2024 21:00:08 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e711b8bc813970a13cff576f9a7cb9d2736670081fe389a95333be7f9b201907`  
		Last Modified: Mon, 08 Jul 2024 21:00:08 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa857c4a7ab9838cbaef85addae511ca3201e9b44415235e679b55a53597443`  
		Last Modified: Mon, 08 Jul 2024 21:00:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ae21c8ee9e4276bbd1645de0229aad15d4af2dfe7b77a9d54b519a9ed6dbd1`  
		Last Modified: Mon, 08 Jul 2024 21:00:18 GMT  
		Size: 206.5 MB (206458818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a4ca98f33305d3ac2511c0ae6c9f908b35151f5afc8b9232a83e42841d454a`  
		Last Modified: Mon, 08 Jul 2024 21:00:08 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
