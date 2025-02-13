## `openjdk:25-ea-9-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:685c1ece551b4488c1b12ba0dac2eceb0977403ff4c4c5aeac55c44a88d65a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-ea-9-jdk-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:688ab0752617388c50755343a9af66f9f118cda56ad25bceece7c5b6d03fa1a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708971131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ff67e6157fefe5aab235549319056de6d26f2702170fd34cf956e39cf77873`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Tue, 11 Feb 2025 00:31:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 00:31:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:12 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 00:31:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:18 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 00:31:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_windows-x64_bin.zip
# Tue, 11 Feb 2025 00:31:20 GMT
ENV JAVA_SHA256=422ffa84afebca61d5ff96e0459231633ad47f082eb11fbecdb64c76e37b35ea
# Tue, 11 Feb 2025 00:31:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d888f48b270b91ba422532bc2e36ee2c9009a235d31b933572c98fb2a11778`  
		Last Modified: Wed, 12 Feb 2025 21:50:16 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6d45a22f500395beb47e2cb7a4dc7f29a1e447ce85797c4159a693df9d9770`  
		Last Modified: Wed, 12 Feb 2025 00:09:50 GMT  
		Size: 394.2 KB (394200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2eb7def73c0a1a86fddb80a5f0af8612df3ca386325278d00fe8f140af191a`  
		Last Modified: Wed, 12 Feb 2025 21:50:17 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a82330af6585f3125be7439bbfa9509bed31588eab7be0e643bc314eec2739`  
		Last Modified: Wed, 12 Feb 2025 00:10:32 GMT  
		Size: 378.8 KB (378773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbda2a06236f1cefae22bfd35cc52b9fd2b3088850004b86e5b73a42f9fd26`  
		Last Modified: Wed, 12 Feb 2025 00:10:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fa0e475cfce3739a734760a24ab96600b94fb059c433743b787dceec2c25b5`  
		Last Modified: Wed, 12 Feb 2025 00:10:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f516a9976d165910d1d4701490e8f1c8b33267600c632a4af5e9359875cc1c`  
		Last Modified: Wed, 12 Feb 2025 00:10:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e32b4aee8d383ee361871904507d36d3c1a5640b2ea482a9649b5ceed66f8e0`  
		Last Modified: Wed, 12 Feb 2025 21:54:08 GMT  
		Size: 207.9 MB (207912795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14af3433982f0f9353873d19a6be00dbcd17b1b09c03cf9a35f516e89134ddcb`  
		Last Modified: Wed, 12 Feb 2025 21:54:10 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-9-jdk-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:1fea92a8ecd0a149cecebce5f00335d38107f7e29b5b9556ef8715715acb8453
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470904786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d28d754bdf77e87205f59b3968977948e0c91b6cab673bd24dda8c3ba5357e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 11 Feb 2025 00:27:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 00:28:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:28:36 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 00:28:49 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:28:50 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 00:28:50 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_windows-x64_bin.zip
# Tue, 11 Feb 2025 00:28:51 GMT
ENV JAVA_SHA256=422ffa84afebca61d5ff96e0459231633ad47f082eb11fbecdb64c76e37b35ea
# Tue, 11 Feb 2025 00:29:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:29:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 21:54:27 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20b4d605e705d3f47072b7d2766df33099177a0b668693003d19bdf3c6a9340`  
		Last Modified: Wed, 12 Feb 2025 11:41:45 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc94b17f055ae5d776d17833337cdb19f892b69e078438574804239ee3ea3bb`  
		Last Modified: Wed, 12 Feb 2025 00:09:50 GMT  
		Size: 365.0 KB (365034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99216bb37b1d08e1e59de495a3808e5f400e470cb619f68dbcf10f143ab2c714`  
		Last Modified: Tue, 11 Feb 2025 16:33:03 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8885f460c82d88e3fbc71353191e82c3f11d2a5a5f3f69268a62645771f400dc`  
		Last Modified: Tue, 11 Feb 2025 16:33:04 GMT  
		Size: 312.4 KB (312424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f6b9653fe28ad47ebbd26d417ab788c68f684fdf834da41b0f6672e04df365`  
		Last Modified: Tue, 11 Feb 2025 16:33:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f671062518fe644d4999c69ddc0b72f5ff59f4ff90fb26d4ff88beee1e87dea8`  
		Last Modified: Wed, 12 Feb 2025 00:10:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddecbdb2d2e8c88371cf678d724b8f18bc26f58257cb49d9a76c0c313765c7ed`  
		Last Modified: Wed, 12 Feb 2025 00:10:41 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8dabbc2b2320f85a5094a57d80cc2e3a116a500cbf6773a5f0276b91a940ec`  
		Last Modified: Wed, 12 Feb 2025 21:50:43 GMT  
		Size: 207.8 MB (207834366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146db06c36f6b9da5d3f925c3bc657440df28e0ab03f8a59292dff5fc21cc19a`  
		Last Modified: Tue, 11 Feb 2025 16:33:06 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-9-jdk-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:f650c51434d86949e95dfcdb2e1ba26dd45bee63c70f7bd9661135be36f36b64
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330761709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b15634b5d1bceb4fc9d47cf6decc9bb4a12d352bf6e9cb253c1e9b4453eccc1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 11 Feb 2025 00:27:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 00:28:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:28:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 00:28:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:28:51 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 00:28:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_windows-x64_bin.zip
# Tue, 11 Feb 2025 00:28:52 GMT
ENV JAVA_SHA256=422ffa84afebca61d5ff96e0459231633ad47f082eb11fbecdb64c76e37b35ea
# Tue, 11 Feb 2025 00:29:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:29:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 20:54:32 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d33258ab6e0502e72c64239e0dd5c590bf2a156c632b46d34c8127a39537053`  
		Last Modified: Wed, 12 Feb 2025 00:09:50 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31153d41017e64952ec3b550f20ddae4febdf7208e9c920eb50966f878ce8b4a`  
		Last Modified: Tue, 11 Feb 2025 01:26:52 GMT  
		Size: 353.9 KB (353902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d902c882c8a22b22919fb02bee9661449192ab8bcafc02a3deb447a8579855f7`  
		Last Modified: Tue, 11 Feb 2025 01:26:52 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c1d9a7f8ffc141b71076daa2443eb2de53d6ae203846992c96ecc9337998f7`  
		Last Modified: Wed, 12 Feb 2025 21:50:20 GMT  
		Size: 338.3 KB (338343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d69a662a2194044d3794bcac38bbf0cab7a1e380c515aaa5a5ba4755cc0932`  
		Last Modified: Tue, 11 Feb 2025 01:26:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1aec3a8d316b1c0b1671699bf88a707af5a877273e073bd5f44c2d390aa87a`  
		Last Modified: Wed, 12 Feb 2025 21:50:20 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0a46b2d5242b131507997b788234f375db8487fb01fade330ae6fbac38fddd`  
		Last Modified: Wed, 12 Feb 2025 21:50:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d98a337c23ed13506117abd3406da9b0627caf5b3d503d0806641b2304d541`  
		Last Modified: Wed, 12 Feb 2025 00:10:51 GMT  
		Size: 207.8 MB (207849350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dece062bf4bbdde052aec51e1c0265e371f08157140cb2846ca5bb6281714aa`  
		Last Modified: Tue, 11 Feb 2025 01:26:53 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
