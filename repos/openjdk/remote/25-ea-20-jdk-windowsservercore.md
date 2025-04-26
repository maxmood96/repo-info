## `openjdk:25-ea-20-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:ef8e23fe48afb148c4105d07fdb65e305e46f3bf67c7020513a6996feb51905c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-ea-20-jdk-windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:ac3ca599cefad714d36dbc05189ad61cb662351666bdcbe15d6cbc40267dcd2b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3604062240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016d105a650f0aff167c9af5c86757558a65b0817598a0215be9e87367b3257d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 25 Apr 2025 21:50:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 25 Apr 2025 21:50:42 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:50:43 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 25 Apr 2025 21:50:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:50:51 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 21:50:51 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_windows-x64_bin.zip
# Fri, 25 Apr 2025 21:50:52 GMT
ENV JAVA_SHA256=189b22f424bd7f7ef01de23f6e41fd183bc3b28da7db090dacba784054fe1f43
# Fri, 25 Apr 2025 21:51:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:51:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560f4f67a6412e5577071c0673b23d3d884e204c8ae8d79943638f9a45c357e2`  
		Last Modified: Fri, 25 Apr 2025 21:51:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b39ee62e7bcdbec8ded8f28c6e44b7ff06ca18c1579d0fefb0d1743a0b1869`  
		Last Modified: Fri, 25 Apr 2025 21:51:16 GMT  
		Size: 399.5 KB (399453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f476be7aec6524f25c899ce28b72b2068fd6046a9cfbc51c825668d98005b1c`  
		Last Modified: Fri, 25 Apr 2025 21:51:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6b08ae0f01699ca88c41b9c9d81a87077c39ad0545299011f505857e98080e`  
		Last Modified: Fri, 25 Apr 2025 21:51:16 GMT  
		Size: 377.7 KB (377695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe98608ace7f170d309a8905898285b361bafb1d76caa482f59c54b51bd0e3`  
		Last Modified: Fri, 25 Apr 2025 21:51:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e62039adc6f994c2c08e82645854653db5ec9ab12c5b463432d4898a923057`  
		Last Modified: Fri, 25 Apr 2025 21:51:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de89a6e1873d07bd42c2290e916e5edf9f247395291fac21573bdd8168c9a87f`  
		Last Modified: Fri, 25 Apr 2025 21:51:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7409f835fa67ba43a6f2c8ed671d4fd7da4a9ad1ef4a0d07090f6b45bd457c5a`  
		Last Modified: Fri, 25 Apr 2025 21:51:35 GMT  
		Size: 208.1 MB (208115874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df49e8adeaa0a41f47ed954af5bb42417de2e93867aa0bb865d5b030d2e483e`  
		Last Modified: Fri, 25 Apr 2025 21:51:15 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-20-jdk-windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:7926e68393a0a88ed64275f9619f19dd5d894ed86167702e0068b9fdae3ca8d5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2482417283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0281a2ce8bf29fdd475cb4eb78f105c852316bc6d686f0039c5718d25125aed0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 25 Apr 2025 21:54:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 25 Apr 2025 21:54:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:54:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 25 Apr 2025 21:54:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:54:31 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 21:54:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_windows-x64_bin.zip
# Fri, 25 Apr 2025 21:54:33 GMT
ENV JAVA_SHA256=189b22f424bd7f7ef01de23f6e41fd183bc3b28da7db090dacba784054fe1f43
# Fri, 25 Apr 2025 21:54:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:54:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78ca831e6fd2c4d3273ce91d60d3fcce010e154a3d4895e5fdacb5c3736c55e`  
		Last Modified: Fri, 25 Apr 2025 21:54:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6669f0f6bb1e83a15b05ece8feedcc5c3a9f93741c3e2462717f24739bbd99f`  
		Last Modified: Fri, 25 Apr 2025 21:54:56 GMT  
		Size: 373.1 KB (373107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b6f07b768aff9f2088e560a3fccb74b07f59c6321c9678f720b0e44a940166`  
		Last Modified: Fri, 25 Apr 2025 21:54:56 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f124f3b5f9b5948dae4a149f09c244567b108cc233541238bc9a72199e1ca5`  
		Last Modified: Fri, 25 Apr 2025 21:54:56 GMT  
		Size: 359.6 KB (359623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f95b25d0022835734f770cff22c4a522e9a6cacadf0b96d3ad4fb4d81bb58b`  
		Last Modified: Fri, 25 Apr 2025 21:54:55 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53d4bf7d9bade25ff02cc9f6a740aae65b3c4de25c9183a04fe482e3d741386`  
		Last Modified: Fri, 25 Apr 2025 21:54:55 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289816406037b43f59be21f45023fc6f5a18d84a00c17ce49c50ae53743fd011`  
		Last Modified: Fri, 25 Apr 2025 21:54:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe7f28ac1e3dc4125430cc7091eaf7478a28fbc069d9f86d1dd8bda77662e2`  
		Last Modified: Fri, 25 Apr 2025 21:55:06 GMT  
		Size: 208.1 MB (208094291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b21a81b08aafb65c68783286df7238a7a8c70e30d9e2686faf36465af11e4ae`  
		Last Modified: Fri, 25 Apr 2025 21:54:55 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-20-jdk-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:98d3b1b4fb38212cd0b0b379ab08926ec5f525eb75819bc5710879946ebc03f4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2374313465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e8af045d0304835e067d9cb0a76052badb0a7120dcab47c1598426e0652767`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 25 Apr 2025 21:53:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 25 Apr 2025 21:53:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:54:00 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 25 Apr 2025 21:54:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:54:07 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 21:54:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_windows-x64_bin.zip
# Fri, 25 Apr 2025 21:54:09 GMT
ENV JAVA_SHA256=189b22f424bd7f7ef01de23f6e41fd183bc3b28da7db090dacba784054fe1f43
# Fri, 25 Apr 2025 21:54:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 25 Apr 2025 21:54:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44708318aa6fa727bca5437e69a38ca42f81a8a38fb1386e9de5c7219ccb2a16`  
		Last Modified: Fri, 25 Apr 2025 21:54:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2139b257125f1e49adb9b165465a2fd98b4e43e0467a16d282f76ffbce34812d`  
		Last Modified: Fri, 25 Apr 2025 21:54:38 GMT  
		Size: 361.5 KB (361491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b45f999363531345643f51f22094404b375521b6c7f414f1f23d26f118e451b`  
		Last Modified: Fri, 25 Apr 2025 21:54:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bc4489557c3b6984ee55bbfb8b823ed9afa7a968bd755df438699774e4cd06`  
		Last Modified: Fri, 25 Apr 2025 21:54:38 GMT  
		Size: 340.4 KB (340404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c36f9f4a65b8a25c0b5a059bd7e14b7268a5bfb504d1c66cbf8c3265eb8302e`  
		Last Modified: Fri, 25 Apr 2025 21:54:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dab5f1f4dce2a82d514bee758bd61fe736a88c83929780b2504fdcb821a6eaf`  
		Last Modified: Fri, 25 Apr 2025 21:54:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe5ea44145253a3bade1c3535ab8ec54a7fa8f325ede936fe6c97b6c3f6e66e`  
		Last Modified: Fri, 25 Apr 2025 21:54:37 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846582d5c0b66811b53d57ac52d7d2a848f3366dd0b91868848a8a6cee947a14`  
		Last Modified: Fri, 25 Apr 2025 21:54:49 GMT  
		Size: 208.1 MB (208078001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2ad30f44bd17defd3c9b5ee6abfa57ef22a3586689c4a87eb2c1befe5f3668`  
		Last Modified: Fri, 25 Apr 2025 21:54:37 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
