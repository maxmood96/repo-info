## `openjdk:24-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:065b2b6c2c0d744891fb67d06c0a9c68700af5872453de694739c6b38014cf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `openjdk:24-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:bc36940ca497d169a8c4ea2e31ff9b46ee13133fcfbf3ea7783dfa5ded35f9ec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2347255692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c367b69e3f3dd11d560453ab2312c0690a0c1817788a55931391ee47190410d8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Mon, 05 Aug 2024 19:52:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 Aug 2024 19:52:27 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 Aug 2024 19:52:28 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 05 Aug 2024 19:52:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 Aug 2024 19:52:35 GMT
ENV JAVA_VERSION=24-ea+9
# Mon, 05 Aug 2024 19:52:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_windows-x64_bin.zip
# Mon, 05 Aug 2024 19:52:36 GMT
ENV JAVA_SHA256=9143864076c1038d2c41165042490d5dfd5a1ccf8a1c730f247f877c1a94dbb0
# Mon, 05 Aug 2024 19:52:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 Aug 2024 19:52:58 GMT
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
	-	`sha256:75a55e17b1fe82bdb1cd9478d08a414579a9a666c1eb0da6214af36cab6d58ed`  
		Last Modified: Mon, 05 Aug 2024 19:53:05 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81113b641b6595582af2227fd727d5b38514cbe28dee6d33972d93c25e965eea`  
		Last Modified: Mon, 05 Aug 2024 19:53:05 GMT  
		Size: 367.3 KB (367282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f07d81b6d05b00b01ef313b7ed53e50f1f3d8c8b41b9ad342dc42be456ab79d`  
		Last Modified: Mon, 05 Aug 2024 19:53:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7e576f99e77bcc1e88d16ee0cd0b841789d92c8ba47f3c92e7cadda8b8b9bb`  
		Last Modified: Mon, 05 Aug 2024 19:53:05 GMT  
		Size: 352.9 KB (352861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0801581142c1b8451c1ea63a99d8b5caeb388b64a6ae412f25c2c0e5c36ca8c`  
		Last Modified: Mon, 05 Aug 2024 19:53:03 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1719d07794da27f3b7574349f0acbf8078f60b02b818d856a5bfb3a0090e7f`  
		Last Modified: Mon, 05 Aug 2024 19:53:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1515d5f0deecb7d5735affa5f0bd6b678f3a0588227165f5282a83c64400ce2f`  
		Last Modified: Mon, 05 Aug 2024 19:53:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede367d8ef0b4b3d6a48ed3e396904c5c2cb98ec8d0081b7613b2f49f189cd1`  
		Last Modified: Mon, 05 Aug 2024 19:53:14 GMT  
		Size: 206.9 MB (206927540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a53b542f8c072e3136c206d66372537ffa294b410a5397655067146be9aa5d8`  
		Last Modified: Mon, 05 Aug 2024 19:53:03 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
