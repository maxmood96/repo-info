## `openjdk:23-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:6571fedd04f9252e0fe875b74e76df88115e2f6926fa74071b0f7bf5d901c027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-ea-jdk-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:d73a560f8b05a461e435d2ebec98c46853c672fc47d13829bc7ac30ddb3d5ffb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346738951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20afc727557b13123f4bbd0cc7d77c84d9f872b4efd664d49a5d1552af5bc62`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Mon, 05 Aug 2024 18:59:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 Aug 2024 19:00:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 Aug 2024 19:00:12 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 05 Aug 2024 19:00:20 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 Aug 2024 19:00:21 GMT
ENV JAVA_VERSION=23-ea+35
# Mon, 05 Aug 2024 19:00:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_windows-x64_bin.zip
# Mon, 05 Aug 2024 19:00:22 GMT
ENV JAVA_SHA256=e1fa138d49607123c4e62f03c9356310076b88219d5ebcabea9975e755293e7b
# Mon, 05 Aug 2024 19:00:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 Aug 2024 19:00:50 GMT
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
	-	`sha256:1c9387be85ed0c2dd5ace98d415c2d03aba571727545c47b96a635c3c930b1af`  
		Last Modified: Mon, 05 Aug 2024 19:00:56 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77b2c10fc4ae213b52c7f1a3d7e4dbee74c3961ccbdefc8d412bd86284ea0e1`  
		Last Modified: Mon, 05 Aug 2024 19:00:56 GMT  
		Size: 359.4 KB (359435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b1a757e5241dcc11ed6845d1337de8195ea5c9612a9cc4c0ac0459acce5452`  
		Last Modified: Mon, 05 Aug 2024 19:00:56 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ee85b577a82eaea1e8e2aef80679a77636427819f44b3d0c54dbde5beda4bd`  
		Last Modified: Mon, 05 Aug 2024 19:00:56 GMT  
		Size: 345.1 KB (345135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdb73b5e8e8f7f99761229d0f243290af989a82d6dd9b67b9dc59b266c8bded`  
		Last Modified: Mon, 05 Aug 2024 19:00:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac14edb3e4bf9c9485c42995da8f215315994e91daa72b44751056d0a3bb9e26`  
		Last Modified: Mon, 05 Aug 2024 19:00:54 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bdb5bc1da9f1b0d05bba97670e802d622afa19dce7b84813f49c828555b58f`  
		Last Modified: Mon, 05 Aug 2024 19:00:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717c499d4fe3882d4cbcc8f973dcb43dbdb5929eecd0b7bda8e58667ca507298`  
		Last Modified: Mon, 05 Aug 2024 19:01:05 GMT  
		Size: 206.4 MB (206426365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a906829976c48a04818284b165b1a0741ce1bf49909f736efb037f3a4702af1e`  
		Last Modified: Mon, 05 Aug 2024 19:00:54 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-jdk-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:7b0aa88b3715a5db359b56ea4881b074ad469925a3b57b3849796b6bb20644e9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2445734437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0019867a8fd39188ecaf1bbdab0e72d42a113200dd24ed006302c64d4eb47acf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Mon, 05 Aug 2024 18:57:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 Aug 2024 18:58:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 05 Aug 2024 18:58:54 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 05 Aug 2024 18:59:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 05 Aug 2024 18:59:15 GMT
ENV JAVA_VERSION=23-ea+35
# Mon, 05 Aug 2024 18:59:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_windows-x64_bin.zip
# Mon, 05 Aug 2024 18:59:16 GMT
ENV JAVA_SHA256=e1fa138d49607123c4e62f03c9356310076b88219d5ebcabea9975e755293e7b
# Mon, 05 Aug 2024 18:59:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 05 Aug 2024 18:59:59 GMT
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
	-	`sha256:a191d86340d7e727f8e38f931aead8b90eb5fd3c63b9a3f0e7298cc9e8cd48bc`  
		Last Modified: Mon, 05 Aug 2024 19:00:10 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c463b090a82414d0c42fb86c6a188348a73df29fe3c77c8fa2ad334105ce9378`  
		Last Modified: Mon, 05 Aug 2024 19:00:10 GMT  
		Size: 502.2 KB (502205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e12d92964822d452c82bd32e648c7e985663e87e203631b6012b3872a48c08f`  
		Last Modified: Mon, 05 Aug 2024 19:00:10 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7defea164f0ad09d5ceb9de7c4d2753f7a0022da1ecc3edf585c4d5f3c8e7c`  
		Last Modified: Mon, 05 Aug 2024 19:00:10 GMT  
		Size: 345.9 KB (345940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a0be3c1651c15cebe46cf3d227b03b49bb544e26aff1cf98c7458a5a89a32e`  
		Last Modified: Mon, 05 Aug 2024 19:00:08 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f977554fbc5e413b2dfeb0cf71e7292cafeb8c1a28ba15cac3a8fb7a5a475f9`  
		Last Modified: Mon, 05 Aug 2024 19:00:08 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295c3fc78f3046884df197f063f5e6da3449cc62ea4757f77cddd5c88a62d07d`  
		Last Modified: Mon, 05 Aug 2024 19:00:08 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2918ddc6175e772bce72535dcb2258e66a02f9ad0d4cda4f9c1c5f625f602fcc`  
		Last Modified: Mon, 05 Aug 2024 19:00:19 GMT  
		Size: 206.4 MB (206448830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df523e6551b826b128764b0f0ce01a596655c33f91de0d9aece02c4c8acc510`  
		Last Modified: Mon, 05 Aug 2024 19:00:08 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
