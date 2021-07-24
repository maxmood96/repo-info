## `openjdk:18-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:3bbb8349259edd9436b5515539662d29297b41cb369d414555be961e6c2df607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2061; amd64
	-	windows version 10.0.14393.4530; amd64

### `openjdk:18-ea-jdk-windowsservercore` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:4df188aafa4ec70690ea6c2c5beb6875c68102749348329b284dae9087098055
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869157481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978edfe64ed00cdc636b62051e450e7f20a218c8ef625b3ce42441a34fb5f266`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 02:41:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jul 2021 02:43:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Jul 2021 02:43:13 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 14 Jul 2021 02:44:11 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 Jul 2021 21:14:36 GMT
ENV JAVA_VERSION=18-ea+7
# Fri, 23 Jul 2021 21:14:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_windows-x64_bin.zip
# Fri, 23 Jul 2021 21:14:43 GMT
ENV JAVA_SHA256=d1e9b6598b5b0e0e969f464820280fc94be007cc9f450ed401857129d3b18d58
# Fri, 23 Jul 2021 21:16:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 Jul 2021 21:16:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dd3b24b55401566ea01a5005138a23766b6b6408c2276b7ebd097da01de80897`  
		Last Modified: Wed, 14 Jul 2021 03:38:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60588ed228454a5b9a3ebf90d5ae7109392676a95ebab716cf7bd486f4e257ae`  
		Last Modified: Wed, 14 Jul 2021 03:38:04 GMT  
		Size: 365.3 KB (365286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2121b14e07fe4c6047b3da990c93bc98e05e8e5a6585d81ef2973841ca2eb183`  
		Last Modified: Wed, 14 Jul 2021 03:38:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23d09b9f1f97d76bdf221736fe3eea41783f3969bb3ae0601b6f159915c839d`  
		Last Modified: Wed, 14 Jul 2021 03:38:04 GMT  
		Size: 323.5 KB (323485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3030062b9a35bf08b6ad08856140ab69e68e5cf9cb54f7c4f478c17328c03be6`  
		Last Modified: Fri, 23 Jul 2021 21:24:20 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1c5253245c67db193533c0b972231610a5797bf475c911a94ba500762114b1`  
		Last Modified: Fri, 23 Jul 2021 21:24:20 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8181827d88f1650db4835a4ca5ad22125ac70be46076195f6d447c75e8d2df9`  
		Last Modified: Fri, 23 Jul 2021 21:24:20 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308e4e76fb37678d9601c7e01f62e3c4682736014a68ca912aa34163861fdcf7`  
		Last Modified: Fri, 23 Jul 2021 21:24:41 GMT  
		Size: 183.0 MB (183013414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa23d58e28fc556e8d4776374041dc7d230c619d37067b4aa29e181f7f18defb`  
		Last Modified: Fri, 23 Jul 2021 21:24:20 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-jdk-windowsservercore` - windows version 10.0.14393.4530; amd64

```console
$ docker pull openjdk@sha256:8efaf5c4b7ab5c4d09d1bd7401a339548a11c47c69cdb643a3cac28ddbd12243
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6453319818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe7f8d35055948b4706ff2555aa0885e49bb804ae82e5c15bda6dc68bed69ea`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 02:46:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jul 2021 02:47:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Jul 2021 02:47:33 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 14 Jul 2021 02:49:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 Jul 2021 21:16:33 GMT
ENV JAVA_VERSION=18-ea+7
# Fri, 23 Jul 2021 21:16:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_windows-x64_bin.zip
# Fri, 23 Jul 2021 21:16:38 GMT
ENV JAVA_SHA256=d1e9b6598b5b0e0e969f464820280fc94be007cc9f450ed401857129d3b18d58
# Fri, 23 Jul 2021 21:18:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 Jul 2021 21:18:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:624cc64d28951435759fcbbc930532718666f3285fc939c97e36c2cda79f80f2`  
		Last Modified: Wed, 14 Jul 2021 03:41:42 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4efeafa471485cac56b3d111ef85272828cab146a6a1ada3aeff81bcb4dda8`  
		Last Modified: Wed, 14 Jul 2021 03:41:42 GMT  
		Size: 328.5 KB (328523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c350ba545fbcd3b34762df7d779fa67615b2b172be3c9a4530584c67cb59c`  
		Last Modified: Wed, 14 Jul 2021 03:41:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aac3eb80df2b34c91daf21be91f90376456108b2df777598c0fee81ca546da5`  
		Last Modified: Wed, 14 Jul 2021 03:41:42 GMT  
		Size: 366.6 KB (366564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7ab94176cabb0d1728d4e01bbfd50bde3768ee9fcc7c1d03d624478578d817`  
		Last Modified: Fri, 23 Jul 2021 21:25:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0265783f41ada24e2dcbaf3598563f09857736287c2d6950e59f79e5b869fc`  
		Last Modified: Fri, 23 Jul 2021 21:25:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908dfd0e90a4d42f36c96eb8a6ff2dde77f03e2c1b545d3b993df84e4ee009a6`  
		Last Modified: Fri, 23 Jul 2021 21:25:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea572578a0edf12d1002a9331dcd6cd3e91850430ae02d7f7e4553c0019457d`  
		Last Modified: Fri, 23 Jul 2021 21:25:23 GMT  
		Size: 183.0 MB (182984445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cd1760d1c31864736d38581f04c1c5799e08d951a7d2a8382a059c2fffb4b6`  
		Last Modified: Fri, 23 Jul 2021 21:25:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
