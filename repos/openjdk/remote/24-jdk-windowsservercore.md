## `openjdk:24-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:221b42553c1d7fe8796242009522e15acba64a9a17696653368ce806352220fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `openjdk:24-jdk-windowsservercore` - windows version 10.0.20348.2582; amd64

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

### `openjdk:24-jdk-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:e151f59338b052bfc0e8b0cc56b29f18ddd1e41b2e1c27b6e28d4a70b4b10f85
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2446234882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6de64bdabd9c9ef35f5d384009265ab39d8b93f081ca37f7f3b422731925bb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Mon, 05 Aug 2024 18:57:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 Aug 2024 19:00:08 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 Aug 2024 19:00:09 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 05 Aug 2024 19:00:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 Aug 2024 19:00:31 GMT
ENV JAVA_VERSION=24-ea+9
# Mon, 05 Aug 2024 19:00:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_windows-x64_bin.zip
# Mon, 05 Aug 2024 19:00:32 GMT
ENV JAVA_SHA256=9143864076c1038d2c41165042490d5dfd5a1ccf8a1c730f247f877c1a94dbb0
# Mon, 05 Aug 2024 19:01:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 Aug 2024 19:01:20 GMT
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
	-	`sha256:3e993543fd14f88c32550fef381bbb48e6fd8c5f565990782ddc5521a8f4ed90`  
		Last Modified: Mon, 05 Aug 2024 19:01:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e20ea80d067650e41d36b91ed7b3ced07047bedabc80e94397ec092cece2486`  
		Last Modified: Mon, 05 Aug 2024 19:01:24 GMT  
		Size: 511.0 KB (511031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fb94a9e883e521ce6440ca75a7e4c4205a69d25db03e4f2a0c108b7263a56e`  
		Last Modified: Mon, 05 Aug 2024 19:01:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b33ad2d605028c98fd81a77dd47ad188bb950421f2d3175faeffc3c9648511d`  
		Last Modified: Mon, 05 Aug 2024 19:01:24 GMT  
		Size: 355.2 KB (355244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56bb2d896bf14b0a4a319e943e570d897c4ea2ce5d493dcec442a0735503a97`  
		Last Modified: Mon, 05 Aug 2024 19:01:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8a305a65b2ab17bf95b960574dea813de0a1e91f9f1f889b6791babcc0065c`  
		Last Modified: Mon, 05 Aug 2024 19:01:23 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f7c911064e1685913dad7ec12a872ca55eab74ce0d30e9d39ea1f34e8dfa1f`  
		Last Modified: Mon, 05 Aug 2024 19:01:23 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723070babafdbf00646caad9b6f1f62368d5f20eb1153ede368cd22b009ad212`  
		Last Modified: Mon, 05 Aug 2024 19:01:39 GMT  
		Size: 206.9 MB (206931432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953bf30f294d22e4b8ee8d7be868601bcbe3cbe368ff81a721b1c04e9451507d`  
		Last Modified: Mon, 05 Aug 2024 19:01:23 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
