## `openjdk:18-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:db7a6327f46ef3ceaa26f4e8942dea9aafd54c2b89cded4b05ad2e1d09fa0113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `openjdk:18-ea-jdk-windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull openjdk@sha256:8e5d98e6488bf89685c62cec60260ac64673b290998f231dc86417fab0526b21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869652496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70bca6b9cdd518cb78692021e25160c5557da1afc3da09cf994d987459dc442`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 17:21:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Aug 2021 17:21:46 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 11 Aug 2021 17:22:48 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 13 Aug 2021 18:14:35 GMT
ENV JAVA_VERSION=18-ea+10
# Fri, 13 Aug 2021 18:14:37 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/10/GPL/openjdk-18-ea+10_windows-x64_bin.zip
# Fri, 13 Aug 2021 18:14:39 GMT
ENV JAVA_SHA256=ebb61201944bef5edd2faa880c947aef2e21db417e501d39e01f2cf473245a02
# Fri, 13 Aug 2021 18:16:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 13 Aug 2021 18:16:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93339de9664b8795350d24edfc9da5614b2c1711961e94e1cb0ca7cf7fae74a`  
		Last Modified: Wed, 11 Aug 2021 18:16:44 GMT  
		Size: 360.5 KB (360455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c74e3eb523942e0a9d7759e2b01e97ab8666b3f5e3de6d2bc3f0af7ba05a733`  
		Last Modified: Wed, 11 Aug 2021 18:16:43 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02991b19a6d7da3867281c2401153bfb9a7890b6a53aa493ae4839fa4dcbf97`  
		Last Modified: Wed, 11 Aug 2021 18:16:43 GMT  
		Size: 317.3 KB (317277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41973bd74cd9d9ea8523561fcc96f46b838cecd729052b1fb22bed136bc21b30`  
		Last Modified: Fri, 13 Aug 2021 18:23:57 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6528e3e5bb7ce8bed37faee3e0821e521824ca6d53bbb0e42868bc74798d0280`  
		Last Modified: Fri, 13 Aug 2021 18:23:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfb56eb8fc906539dccd215ce9bd17336c413afcd32d48202c2d9e7504ade6b`  
		Last Modified: Fri, 13 Aug 2021 18:23:57 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d3b477d76c08e87a529fccdc192715269617c5b893c3bbeb32f8825afe57d4`  
		Last Modified: Fri, 13 Aug 2021 18:24:16 GMT  
		Size: 183.0 MB (182968284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60728b7e1cfb16e2d9ab70cba9bbec1cd416a694c7eb5b37b752cc7da3cd4f0b`  
		Last Modified: Fri, 13 Aug 2021 18:23:57 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-jdk-windowsservercore` - windows version 10.0.14393.4583; amd64

```console
$ docker pull openjdk@sha256:518586418d9b21b035d50e52baf5351d91fd0836a2792157add8f83f013ed5f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6454513618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dcb83c79f119ac59f35f8a6a3a98988cd5a35950b974da39559e49430066590`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Aug 2021 12:51:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 17:26:21 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Aug 2021 17:26:23 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 11 Aug 2021 17:27:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 13 Aug 2021 18:16:32 GMT
ENV JAVA_VERSION=18-ea+10
# Fri, 13 Aug 2021 18:16:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/10/GPL/openjdk-18-ea+10_windows-x64_bin.zip
# Fri, 13 Aug 2021 18:16:37 GMT
ENV JAVA_SHA256=ebb61201944bef5edd2faa880c947aef2e21db417e501d39e01f2cf473245a02
# Fri, 13 Aug 2021 18:18:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 13 Aug 2021 18:18:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d4b5c087d85e7fbeffd8b282ecd862da1fb7ff00c37657c5712888936292097`  
		Last Modified: Wed, 11 Aug 2021 13:30:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85818d8ae526f813cf82bc85044b12bcf64737f7bce6c6b2d983a6db1251a488`  
		Last Modified: Wed, 11 Aug 2021 18:20:44 GMT  
		Size: 348.4 KB (348421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97555b86e64e63a554a03c6f11081f8cbdf6c342fcc22e636805874c5bc3621`  
		Last Modified: Wed, 11 Aug 2021 18:20:44 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170015a5368a4254730393e471c1266819b31109af34e6a507a6ba90f74c3bdf`  
		Last Modified: Wed, 11 Aug 2021 18:20:44 GMT  
		Size: 300.6 KB (300628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcf81409724c3613ffdfb9c1f482a4d5fac443f01e3d99235c41d1b626d4f4e`  
		Last Modified: Fri, 13 Aug 2021 18:24:36 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fbb9ea42ea107af4c4bd471cc4c4ec42a1e2bb7dc0848f5011b43fe5e8bb00`  
		Last Modified: Fri, 13 Aug 2021 18:24:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce648a1b3d49a859c21fa9a2ee2ebca22fea75d4d72fe06994c355eb36229f9e`  
		Last Modified: Fri, 13 Aug 2021 18:24:36 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90d2598f250b024d299e99c4f49a269187f7e940d98ebfa3441b27ef32e31b4`  
		Last Modified: Fri, 13 Aug 2021 18:24:56 GMT  
		Size: 182.9 MB (182890056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c66691ff5d01e3cc7468b6d5210a731f9aa384b32b8302fde4721fb80e5d6a`  
		Last Modified: Fri, 13 Aug 2021 18:24:36 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
