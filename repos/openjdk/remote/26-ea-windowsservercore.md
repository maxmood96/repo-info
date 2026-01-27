## `openjdk:26-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:ee6dbd1e2f4c8f89118a6c277a99a0db228dedbe901b5dc75e9796e70a05df37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:b0a862c7030f4c64c53560cc76536ceaf8b1dc180f1c984ba4227d003da51e48
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1720894267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662a4647a293f8ebe9f0a8d12df8470f945e118ddb091f6edeba4f350861b2f3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:06:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:07:29 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:07:30 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 26 Jan 2026 22:07:36 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:07:37 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:07:37 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_windows-x64_bin.zip
# Mon, 26 Jan 2026 22:07:38 GMT
ENV JAVA_SHA256=02a8f8920550b69cdbebb0d7b6eb675d5f597bc5feb7513ae61038c856c19cb8
# Mon, 26 Jan 2026 22:08:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6f0fe5c2ded94d05d8850f2bf11e84d6153343ff1a72da11b95d4b3c0f58dd`  
		Last Modified: Mon, 26 Jan 2026 22:08:30 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430b534904c1592a1870feed501cbaa637066644d88aa3cb2f832f9f03a44dc8`  
		Last Modified: Mon, 26 Jan 2026 22:08:30 GMT  
		Size: 413.3 KB (413332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d1eadc999be4fee3969bbbc6e5dee497f8375711163b205b725063626604f`  
		Last Modified: Mon, 26 Jan 2026 22:08:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c194857e881cea86ab58516eeabed9b9ba428e65fb28777d03debc89f42481`  
		Last Modified: Mon, 26 Jan 2026 22:08:30 GMT  
		Size: 399.0 KB (398953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d562648f8bbd99fa227cee1815c1cf6aa0ab41b2c0b83667d821387bd9223d`  
		Last Modified: Mon, 26 Jan 2026 22:08:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e9512af59058ee7507f7eec02856eed7fb6506bd81b68897169d482bc6aae1`  
		Last Modified: Mon, 26 Jan 2026 22:08:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642a5fe9c3d2c0a7d6bca0129a914333dd883f14be305363b12af6815f48b3e1`  
		Last Modified: Mon, 26 Jan 2026 22:08:28 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788e599a8d87366f32a34a1e6815d12514a6ea23411478529cfd3ac9dc25421`  
		Last Modified: Mon, 26 Jan 2026 22:08:44 GMT  
		Size: 224.3 MB (224313810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fc57a17f0c78c89c6ae4f8098299cbe8028b9aeb2a61958fda26192a2afa76`  
		Last Modified: Mon, 26 Jan 2026 22:08:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:58d9bbf5142fd55adb994619c7c1aa1d432ced27da1b80cac88d2d1ee815e696
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2060788968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b397fa34425cd7e164d9992f2cc6cbd9dc32c76a82cf3f92f95ab4e64e8707`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:08:48 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:49 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 26 Jan 2026 22:08:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:08:58 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:09:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_windows-x64_bin.zip
# Mon, 26 Jan 2026 22:09:01 GMT
ENV JAVA_SHA256=02a8f8920550b69cdbebb0d7b6eb675d5f597bc5feb7513ae61038c856c19cb8
# Mon, 26 Jan 2026 22:10:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 26 Jan 2026 22:10:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fa8db78906ea6fbf10041de1ed15ff81c180a21a4f65ae404226dece2460a4`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 503.7 KB (503709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284a6959273d9ba6a25688b512b9013204f189023c9eb7022f9ac08eaf3d26c6`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06de4c3e24ae6000dddba236b23f22ef27aeb99e16ced180f3cda2d49aeb55e8`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 351.8 KB (351761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5206495a19cb6b0ce0a5a53657bf7ae9d3536b05259466c892ca6884b49b93ee`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6ec380a32cfcc46f5ff1f36e377ca8a30b0614e5807d08cca274d6ef6750bf`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc845909244c84e6066c4b57225fc7f4dc3a13926e3980d8eeb906e647e19c66`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f814cb8506ce154ec001ddaf56ceef947e401882612c8e7b2143cbbede126153`  
		Last Modified: Mon, 26 Jan 2026 22:10:43 GMT  
		Size: 224.3 MB (224266490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe6edc21e1d71fac10b10e5aa52ee2b1c4b76aeaf2bb358b9bf9c922992b5f1`  
		Last Modified: Mon, 26 Jan 2026 22:10:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
