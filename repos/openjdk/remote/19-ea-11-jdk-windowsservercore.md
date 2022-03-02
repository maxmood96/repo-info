## `openjdk:19-ea-11-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:e2b5a1d9c98e1d16185f73fa242cd72bb7fddb942fac2e6edd41f629e7e72a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.524; amd64
	-	windows version 10.0.17763.2565; amd64

### `openjdk:19-ea-11-jdk-windowsservercore` - windows version 10.0.20348.524; amd64

```console
$ docker pull openjdk@sha256:be2eca47c7b9fb0afa9a325304317a17868361b4a485ad512d339e042d5aaa0e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2404380588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7a677a90cd6a6a42d8c586e1ccfa89ac1a1baf4ab8212120b1a69eeb7caab2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Tue, 01 Feb 2022 02:49:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 09 Feb 2022 13:37:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 18:40:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Feb 2022 18:40:18 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Feb 2022 18:40:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 02 Mar 2022 01:16:49 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 01:16:50 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_windows-x64_bin.zip
# Wed, 02 Mar 2022 01:16:51 GMT
ENV JAVA_SHA256=14d6f94b755321e7d1024aa1038ec0bc89e9ba6568fe250f0368698662ed5220
# Wed, 02 Mar 2022 01:17:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 02 Mar 2022 01:17:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:898469748ff68223ab87b654b29fb366c1f4f2b7cfad7a37426346ea16db8dfa`  
		Size: 963.2 MB (963225591 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7062696b7aef1ca33afdf32084a532f7e3151a844eb7cb2455bcc907e0f42a58`  
		Last Modified: Wed, 09 Feb 2022 14:28:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fc5298c05f3e14d89c86be0ac333bd8cfa150ada3565e9f2736c19d8cac25b`  
		Last Modified: Wed, 09 Feb 2022 19:16:25 GMT  
		Size: 616.4 KB (616433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21971a484cbb6138250125b67d62f83b05a4770a5da18e51e7b3ac8e5743e725`  
		Last Modified: Wed, 09 Feb 2022 19:16:24 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0be28f1a2b136367cb8f8044ec174a09f9976e0f389c7fe25cd4e12f2e59b5a`  
		Last Modified: Wed, 09 Feb 2022 19:16:25 GMT  
		Size: 532.5 KB (532549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cadb837ca2aba0402ecf128fc8fc3320d25d8f58d63e3f4600697dd1bb3b02`  
		Last Modified: Wed, 02 Mar 2022 03:21:07 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ee8a1fc88fe1f7704a1f2dc3f853de23031115c05623de4910730b33f05e6f`  
		Last Modified: Wed, 02 Mar 2022 03:21:07 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cc3aae3f6778afd5f0229da116f64cfdb90f1f3fd05c74a10c3ba7a1082ba2`  
		Last Modified: Wed, 02 Mar 2022 03:21:07 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf53a5b545860edb41110306beeba4a923a6b286739bb19cbb5c23a8e853438`  
		Last Modified: Wed, 02 Mar 2022 03:21:27 GMT  
		Size: 188.3 MB (188298478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045bc86d68464728528354abb9d7b47b0cd84d153b6f987736b45f6d1376d4bc`  
		Last Modified: Wed, 02 Mar 2022 03:21:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-11-jdk-windowsservercore` - windows version 10.0.17763.2565; amd64

```console
$ docker pull openjdk@sha256:f4859eab7974ad1875e2c38777c1e8ffb3b3fc750d9f135148b85f9b53470edd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2902507983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc36b0a94ab247fb20c39dbc8076d7bc11282896b8be056f3ae23d6635403`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 13:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 18:42:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Feb 2022 18:42:46 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Feb 2022 18:43:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 02 Mar 2022 01:17:52 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 01:17:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_windows-x64_bin.zip
# Wed, 02 Mar 2022 01:17:54 GMT
ENV JAVA_SHA256=14d6f94b755321e7d1024aa1038ec0bc89e9ba6568fe250f0368698662ed5220
# Wed, 02 Mar 2022 01:19:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 02 Mar 2022 01:19:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f0c1566a9285d9465334dc923e9d6fd93a51b3ef6cb8497efcacbcf64e3b93fc`  
		Last Modified: Wed, 09 Feb 2022 13:26:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b68a1fe6e4f618e81fe842c9b07d5a79ffffc2c21933db69d5c9e6105091560`  
		Last Modified: Wed, 09 Feb 2022 19:20:09 GMT  
		Size: 358.3 KB (358257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08343ea9810774eba7bea5b402b825bbbb597f2cb7dc0b9958270839899f0886`  
		Last Modified: Wed, 09 Feb 2022 19:20:08 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1318a28fd7f970bded95d3db9d726254043dd9127e1055fac6d3909627f9ab10`  
		Last Modified: Wed, 09 Feb 2022 19:20:08 GMT  
		Size: 311.5 KB (311525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec8936d345d913563518e950cd32287b59cf8d69d1644338d2719daa2ecc892`  
		Last Modified: Wed, 02 Mar 2022 03:21:49 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70e6b70dd1e123575a819c6ca077e9c6047e5ec5bc15f1f9878c7b225df4a27`  
		Last Modified: Wed, 02 Mar 2022 03:21:49 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20db5b758d5cbad60f6dc6bce675b707fecfc167c9c63db8deca5e7ae287e7fa`  
		Last Modified: Wed, 02 Mar 2022 03:21:49 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae96e8568b22a9e120bf01b8c0308f5de85726a3a6c3e7bdf9ff5717a26405`  
		Last Modified: Wed, 02 Mar 2022 03:22:09 GMT  
		Size: 188.1 MB (188114915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8b03ddf86dde80aec610bd9310f0bcec9e9cb7dd5dc9b120b8ac8074e5a890`  
		Last Modified: Wed, 02 Mar 2022 03:21:50 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
