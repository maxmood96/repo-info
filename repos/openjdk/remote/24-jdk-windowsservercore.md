## `openjdk:24-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:64f84302eec5b7a469a749224374debc17f09dc288a9c534c8d2c37aefad585c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-jdk-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull openjdk@sha256:79dbaa720abd644ddd5904f923d3a99ccee5c0c2e9d57405a4f2d88fb7a8f2cc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2008540931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc46c26c6abb23300c3bb417c915bd518f02a768de4a7e1c11bcc9fe226ac619`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:12:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:13:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:13:20 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Oct 2024 23:13:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:13:26 GMT
ENV JAVA_VERSION=24-ea+18
# Wed, 09 Oct 2024 23:13:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_windows-x64_bin.zip
# Wed, 09 Oct 2024 23:13:27 GMT
ENV JAVA_SHA256=6146921a840c402763aa710b209d872b2b91ba63221f33e494fa1312cb2a706c
# Wed, 09 Oct 2024 23:13:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:13:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea4cded6c51c5d2de16e44113ff7e81d0b6960159733614efdc2d93ae10ab3e`  
		Last Modified: Wed, 09 Oct 2024 23:14:00 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bba16e12a30a7b77d45ced1f49d077367bca22fa9cc8098706720433ce0820`  
		Last Modified: Wed, 09 Oct 2024 23:14:00 GMT  
		Size: 482.4 KB (482435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17799a4f7c807fc3a5408cf3a69c4c9d15cd5debe2d730f800469b4b42c023e4`  
		Last Modified: Wed, 09 Oct 2024 23:14:00 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dc4dc74b352404e14b84de5256984192d3b36ee6ad1fb5cbafcc992faba9d5`  
		Last Modified: Wed, 09 Oct 2024 23:14:00 GMT  
		Size: 336.5 KB (336456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31ea4e4dab7f2bbcf3c63c31bf2b104b9cb133a9dc3e4b816e6a51527800469`  
		Last Modified: Wed, 09 Oct 2024 23:13:58 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da998d6def0f2762b760ef53765116d68a7c689499a24b70b447ac457ef48e81`  
		Last Modified: Wed, 09 Oct 2024 23:13:58 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be8a10348dc064109060da2dff8cf8c6ab31113e185801a62f8fdfff74867d7`  
		Last Modified: Wed, 09 Oct 2024 23:13:58 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3a602efb5e96a3d938a222737edee8a840422a74fb4ad710a29952e6b1fbd4`  
		Last Modified: Wed, 09 Oct 2024 23:14:09 GMT  
		Size: 208.4 MB (208372577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8deec14057ccff968cac7027293c5a97376fad41faa69503f99d3df8d4f8da`  
		Last Modified: Wed, 09 Oct 2024 23:13:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-jdk-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:20d8f19484574fd7c0313568c83b8776bd349971d90f8ad7de704fb6d88feca0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2110981576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4939b8049be70fc91b51f4ca9ca5ea61318a1f350980bcbbcce3fe9193b689ce`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:19:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:20:46 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:20:46 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Oct 2024 23:20:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:20:53 GMT
ENV JAVA_VERSION=24-ea+18
# Wed, 09 Oct 2024 23:20:54 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_windows-x64_bin.zip
# Wed, 09 Oct 2024 23:20:54 GMT
ENV JAVA_SHA256=6146921a840c402763aa710b209d872b2b91ba63221f33e494fa1312cb2a706c
# Wed, 09 Oct 2024 23:21:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:21:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17de2f54ae8a480d7465d9ba21b8537027faec0639949bc1df2742d9b2cec54`  
		Last Modified: Wed, 09 Oct 2024 23:21:29 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e40735dff60847543c05b44b58659102a22ca6bba4993ae1e22fd13e9abaec`  
		Last Modified: Wed, 09 Oct 2024 23:21:28 GMT  
		Size: 473.4 KB (473351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4c89678db59a50561cc1946932b9c06adaa853884071a06afcb02d21d003ae`  
		Last Modified: Wed, 09 Oct 2024 23:21:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf62954dc8132fcf4df7754da714153c08aec309b8966f7560befd5f39691e0`  
		Last Modified: Wed, 09 Oct 2024 23:21:28 GMT  
		Size: 319.0 KB (319014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe550a0ae48cbb166f675039aaa91ce089647de0c0b9bd359dd28189721811f7`  
		Last Modified: Wed, 09 Oct 2024 23:21:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b17c8be8bddb4ca2d0bb51e1a1bfefcb274193720948316662f7691e74a1a96`  
		Last Modified: Wed, 09 Oct 2024 23:21:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c7349b213e8b6fde4618d9267b7972163fb09ae5e9f50d413649d0215136f`  
		Last Modified: Wed, 09 Oct 2024 23:21:27 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d6b565fcc93d3f23dd9b1a3185dbf839723f1c8540c709e7c202d633bb0cc0`  
		Last Modified: Wed, 09 Oct 2024 23:21:39 GMT  
		Size: 208.4 MB (208356151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64500f101bc4a643bceb90b8ceea410313463b1240811a221ff6c935bf701a93`  
		Last Modified: Wed, 09 Oct 2024 23:21:27 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
