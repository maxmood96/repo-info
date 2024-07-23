## `openjdk:23-ea-33-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:e6ff69ac3356145b44ad36131ee334297dbae68c33e384abdbf54e813dae53e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-ea-33-jdk-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:237de8f55d1bb262057e9508edbd66def69a8508d62f03de142bfc33b08cc44d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346714907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28234694c752436404ebf3c493687b2bb6f4ebfd7256344f1057fcc6ff6e1ba4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Mon, 22 Jul 2024 20:59:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jul 2024 20:59:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 20:59:59 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 22 Jul 2024 21:00:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:00:06 GMT
ENV JAVA_VERSION=23-ea+33
# Mon, 22 Jul 2024 21:00:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/33/GPL/openjdk-23-ea+33_windows-x64_bin.zip
# Mon, 22 Jul 2024 21:00:07 GMT
ENV JAVA_SHA256=b187293e4a2d22e9975c77c2a9fa5ac548e60fa92ac6f5a7185f697ab295d04f
# Mon, 22 Jul 2024 21:00:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:00:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48530a80c1e95122eda7fa97d581969e5e6d336a40c13fb463278d14e03ce107`  
		Last Modified: Mon, 22 Jul 2024 21:00:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fd961398cb53acbf19fff855abd50fbccda9fd3bf782535c277a92a5c8c0a7`  
		Last Modified: Mon, 22 Jul 2024 21:00:39 GMT  
		Size: 351.3 KB (351329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5687a91de709a2c123c85f34b436f60ba5216bdb3bc52e75d5ebf2b04912a89`  
		Last Modified: Mon, 22 Jul 2024 21:00:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d427695102dfd2eb62de54a2b91186d908e7be71fa8c31108541723805cec2c9`  
		Last Modified: Mon, 22 Jul 2024 21:00:38 GMT  
		Size: 336.0 KB (336036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9026bb08f17de4aa623658efb7d27a3caaabe731f3e4ab2831304bf579f8d2e3`  
		Last Modified: Mon, 22 Jul 2024 21:00:36 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880b601955633b3989738cb7d37634e30fc511fa777a687af0d7017f4bbf6cc7`  
		Last Modified: Mon, 22 Jul 2024 21:00:36 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22700fee0376f140fab62eea651f266087102df41b7049c38466e9c5deb4ee58`  
		Last Modified: Mon, 22 Jul 2024 21:00:36 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b8742bbd5a0234e46212557b980a76f788aa6c0a549e593ce066262da6abf8`  
		Last Modified: Mon, 22 Jul 2024 21:00:47 GMT  
		Size: 206.4 MB (206419483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fb54a62f657610ac38c091f8c108262635415cca3eb7778e564f10eee38e82`  
		Last Modified: Mon, 22 Jul 2024 21:00:36 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-33-jdk-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:5924ed5f907b8d3f828db662a8414a59738896bef6bb8cef46113113266535c3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2445724389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90319424db6042c11f03d8d0bc8a02125b474885fc4b69a1594caf3bc29d341a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Mon, 22 Jul 2024 20:59:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jul 2024 21:02:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:02:07 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 22 Jul 2024 21:02:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:02:34 GMT
ENV JAVA_VERSION=23-ea+33
# Mon, 22 Jul 2024 21:02:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/33/GPL/openjdk-23-ea+33_windows-x64_bin.zip
# Mon, 22 Jul 2024 21:02:35 GMT
ENV JAVA_SHA256=b187293e4a2d22e9975c77c2a9fa5ac548e60fa92ac6f5a7185f697ab295d04f
# Mon, 22 Jul 2024 21:03:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:03:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4492dbbb683465899fe47f991ab8bc2cd18a531a1b14ec578052b07941231b`  
		Last Modified: Mon, 22 Jul 2024 21:03:32 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0378b5b9361e1091fd3bdbc9ff9c378f6f3a1b81b8008f689dcf9afeed331196`  
		Last Modified: Mon, 22 Jul 2024 21:03:32 GMT  
		Size: 500.5 KB (500497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de3de2537607174ee5a0108307c7d0c2d4bcf6a0531ddacfc9c6635fcc752ef`  
		Last Modified: Mon, 22 Jul 2024 21:03:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed79ac91669a0f33a6fc74482d34e06131b3c09222018e01528678ec0d00d6fe`  
		Last Modified: Mon, 22 Jul 2024 21:03:32 GMT  
		Size: 344.4 KB (344398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779a0e43611bb7ed1193fe22fcf0d6a7c8fc0ccbee755268d8d1e73d2d355b77`  
		Last Modified: Mon, 22 Jul 2024 21:03:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1723be0c21485f2fa099a6d4f5413badf5540851a351fe6b0b2e802e0ccfce07`  
		Last Modified: Mon, 22 Jul 2024 21:03:31 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decd092d07e5a2d6b72133a3cebd801af5a09d80a1d17fd61f91d3cea3e47f30`  
		Last Modified: Mon, 22 Jul 2024 21:03:31 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba141e4cf2e5dd3382645778894d2c11746b25fdba9d1f5a02143a7f180c384`  
		Last Modified: Mon, 22 Jul 2024 21:03:41 GMT  
		Size: 206.4 MB (206442212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6738b5184765ce4589392d0d0e4634861521d513f099b720e154b198a1d064`  
		Last Modified: Mon, 22 Jul 2024 21:03:31 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
