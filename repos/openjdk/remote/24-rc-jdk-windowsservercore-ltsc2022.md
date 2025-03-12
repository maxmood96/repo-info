## `openjdk:24-rc-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:840e692c3e2dfd5571d2f65acd47dd9ca1c1b7a711a9e05b0e396baa437f7c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `openjdk:24-rc-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:dd47200727fca4222a9c255c3187475bead5b2a14ef9b137cf0fa4d101fcbe80
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2479504650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8519d17e6d5a603cbc6b1e9d31316993fcf8d833f76e504debbd0678dc051a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:59:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 19:00:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:00:08 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Mar 2025 19:00:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:00:14 GMT
ENV JAVA_VERSION=24
# Wed, 12 Mar 2025 19:00:15 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_windows-x64_bin.zip
# Wed, 12 Mar 2025 19:00:15 GMT
ENV JAVA_SHA256=11d1d9f6ac272d5361c8a0bef01894364081c7fb1a6914c2ad2fc312ae83d63b
# Wed, 12 Mar 2025 19:00:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:00:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da374c7100fbdaf0d4265a324fc4eba242d059c54d71208e6561b18c821df010`  
		Last Modified: Wed, 12 Mar 2025 19:00:41 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f76186b5caaf7ba32c4c00772d7570f911ea6be24fe8fb0032cc56c84ee72d`  
		Last Modified: Wed, 12 Mar 2025 19:00:41 GMT  
		Size: 345.0 KB (345026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af30b98f82ba5cab58aeb6c6b9bf5e1ba73e50410948e8d7e004f1a0c9b886`  
		Last Modified: Wed, 12 Mar 2025 19:00:41 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e0868a785fc264628e19bb031444929e6d4689a30b10ecf50b33c54ffaab35`  
		Last Modified: Wed, 12 Mar 2025 19:00:41 GMT  
		Size: 328.5 KB (328457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c932898f67f00af531d49f7f5d47c257c1d82801afd3e245ea829dcd31d4e84b`  
		Last Modified: Wed, 12 Mar 2025 19:00:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8298a211243536378251e8e08b66863ba3b05513d204620e9a8decfd9fd6d27`  
		Last Modified: Wed, 12 Mar 2025 19:00:39 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbd5154aadc46ad51202024edb65bec94bb980f2720ef80ef220fc8b4b1bddb`  
		Last Modified: Wed, 12 Mar 2025 19:00:39 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39695a1fa07190f26b502fb0b9db87aee71ee90e378206b7c9bc5dcb564fc022`  
		Last Modified: Wed, 12 Mar 2025 19:00:51 GMT  
		Size: 208.9 MB (208882259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be525680bee3a0b0d8cb78c248fcb73f9471df7497d20bbcbc7743cbf3edd6e`  
		Last Modified: Wed, 12 Mar 2025 19:00:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
