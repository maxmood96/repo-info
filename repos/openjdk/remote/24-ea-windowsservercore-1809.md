## `openjdk:24-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:ade68aaaffbad18330a3fc0eb4280a91cec792ef8519ccff54a980de7d4e61f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-ea-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:aac5a172999ef5b62d92091b324a34b04cdce7efef56016fa2612857a32303c0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2428002171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461abe05513f960adeba3b4a8bf8979809f03a7ea4df6e0ca2df6c96f669f884`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Fri, 14 Jun 2024 01:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jun 2024 01:14:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:14:08 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 14 Jun 2024 01:14:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:14:26 GMT
ENV JAVA_VERSION=24-ea+2
# Fri, 14 Jun 2024 01:14:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_windows-x64_bin.zip
# Fri, 14 Jun 2024 01:14:28 GMT
ENV JAVA_SHA256=2c752f59e33501f0541d669dc181c84fc2c5d736884e3b1ff58a74fb6412081b
# Fri, 14 Jun 2024 01:15:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:15:05 GMT
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
	-	`sha256:1ee97bfb36e6b8b495f5d7140ee6d45366f3d42c627d16310db22731a42e8fe0`  
		Last Modified: Fri, 14 Jun 2024 01:15:12 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b509fd6e2ad5e4b013f8036d88f4bd256ab38cabda7a0d0037f5c23ef32c1b6`  
		Last Modified: Fri, 14 Jun 2024 01:15:13 GMT  
		Size: 471.9 KB (471878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb938c90ebde823428ba538613f3b3827009a761ab911194524240c5f1f8d432`  
		Last Modified: Fri, 14 Jun 2024 01:15:12 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a5878d628bba78aabb9a5234b6217bd701e3ef9e475988603b81a991483600`  
		Last Modified: Fri, 14 Jun 2024 01:15:13 GMT  
		Size: 319.1 KB (319144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b3535b0d52eb9d1067c247d4337a260c62a88c7306b7ce1103ee17969c97fa`  
		Last Modified: Fri, 14 Jun 2024 01:15:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52decf21fa68ecc024bcc2acc3202acc00c613cb8c0cd647c03b13b5c0cb7737`  
		Last Modified: Fri, 14 Jun 2024 01:15:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9725df9e89b226208cae8613c3548fb4a25fdf4c12c3e9d70c73e008430c0c`  
		Last Modified: Fri, 14 Jun 2024 01:15:11 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405222f72ace2e8a9486bcce7d760548e37860f705c010d766bfd321e392c7b9`  
		Last Modified: Fri, 14 Jun 2024 01:15:22 GMT  
		Size: 206.5 MB (206522215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b2acdb0746c63e0933f541aaa4d2de58507aaf256b1367cdbc843fd532bd4`  
		Last Modified: Fri, 14 Jun 2024 01:15:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
