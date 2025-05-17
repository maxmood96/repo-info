## `openjdk:25-ea-23-windowsservercore`

```console
$ docker pull openjdk@sha256:a8cfcac26b46e3d5979cd21a71ee38910a68b271f5f0c55cf9556688b44d6390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `openjdk:25-ea-23-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:228e21ac00c39a5e8d17af4ddb05d8659b7579bd0674244e6c715f9068dd85ad
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3640793339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325f6c9cc049c232c4507ac71b05afec535b6568ebea79bbb69728cb454fc1cf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Fri, 16 May 2025 20:58:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 May 2025 20:58:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 16 May 2025 20:58:52 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 16 May 2025 20:58:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 16 May 2025 20:58:59 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 20:59:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_windows-x64_bin.zip
# Fri, 16 May 2025 20:59:00 GMT
ENV JAVA_SHA256=903e77b6d79a2c808e32a4111a54802e149b11e39d15629d7a04ccfb97e4c79b
# Fri, 16 May 2025 20:59:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 16 May 2025 20:59:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cae493650bffa903e0895e1f2e266ee4f823b5825e8b836d0d3f0750399930`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b4f788d335c5b01c14d439115092318bb6483081c3662a4bf1f79e7f58af57`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 368.3 KB (368322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7569509716153e89ee383313a5bac62c47f605594c9592c9572004d74d04f524`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46dfccfa9e8d36f9e96257ecfef309d620842a84280083b8bb77bcbf5de888a`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 354.8 KB (354839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4146acb6e913e0fe08dcf090868d95d9eeac5ebae7b830683665084bd14d5562`  
		Last Modified: Fri, 16 May 2025 21:02:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0ae521cc9be633578ee31e64a2eb8973901cd9cab2e4195a1e6537c6241688`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3a2a57af48d392d0664f2e04177490dfbf9629021ac31ed904168b31d2147e`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa58bcddb8231f97aa861905859cb434a8e717b840488b6be26d89125fe0c0c`  
		Last Modified: Fri, 16 May 2025 21:58:43 GMT  
		Size: 209.3 MB (209296578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f880421a49694c5468de61ca3815140d1662983afbffdb3d679718d36977990b`  
		Last Modified: Fri, 16 May 2025 21:02:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-23-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:9ed1333f2739e58ea04afb499c712535331f5dd11221ad2d7e88b9c93fd30bb0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2483666221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63944e66ccd7f3610aa8912b80832274655663f8302e8a84c98a44f047c4ae70`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Fri, 16 May 2025 21:04:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 May 2025 21:04:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 16 May 2025 21:04:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 16 May 2025 21:04:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 16 May 2025 21:04:32 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 21:04:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_windows-x64_bin.zip
# Fri, 16 May 2025 21:04:33 GMT
ENV JAVA_SHA256=903e77b6d79a2c808e32a4111a54802e149b11e39d15629d7a04ccfb97e4c79b
# Fri, 16 May 2025 21:04:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 16 May 2025 21:04:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb77149bb250a6a718022280db2075b45e6d815772aa1f3393fd87602fbd8be`  
		Last Modified: Fri, 16 May 2025 21:06:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a194cd0150b1cebd8ce8477b6680eb08f936eda8d9fc28c4676c4653240c465`  
		Last Modified: Fri, 16 May 2025 21:06:26 GMT  
		Size: 373.6 KB (373615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6109808ec595500f9243b380fe804cccc8d71ead6cedff824347ed463c73603d`  
		Last Modified: Fri, 16 May 2025 21:06:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac4a491f9c96211defff838b8ebd8839411cb77f801715c2ec9078fb4039853`  
		Last Modified: Fri, 16 May 2025 21:06:28 GMT  
		Size: 361.1 KB (361120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407f9d80a44d667a68966a54f8b5ce16c58d3ab9e89237050193e400d37532a8`  
		Last Modified: Fri, 16 May 2025 21:06:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99811b8a85c2d2cdfbc85488728290e617f0a6b5efba8cdd8a5bc71341f4944a`  
		Last Modified: Fri, 16 May 2025 21:06:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9e8ec9046dbd4a9c1e72ff6d45089472ea23de0fdf4566230684b957eaf2d6`  
		Last Modified: Fri, 16 May 2025 21:06:29 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173b58d3b42c3a3079caeef797937322909559f0fd7040ab00c6caf0ef799308`  
		Last Modified: Fri, 16 May 2025 21:08:18 GMT  
		Size: 209.3 MB (209295654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9947447cac5190ad87c1f2fa0f92870775e91bb2ed20c69375639671aac1a158`  
		Last Modified: Fri, 16 May 2025 21:06:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-23-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull openjdk@sha256:3a151d1910883934005c77c2a25ac085a53340792e666475fb70b663a28cb89b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2393745743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3391de461880779aceee2c7dc465c4c4237ff6c9c72ea8b5b3a3ffe2a9460f69`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Fri, 16 May 2025 21:02:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 May 2025 21:02:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 16 May 2025 21:02:56 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 16 May 2025 21:03:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 16 May 2025 21:03:03 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 21:03:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_windows-x64_bin.zip
# Fri, 16 May 2025 21:03:05 GMT
ENV JAVA_SHA256=903e77b6d79a2c808e32a4111a54802e149b11e39d15629d7a04ccfb97e4c79b
# Fri, 16 May 2025 21:03:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 16 May 2025 21:03:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c94e107aaec5a76637bb9d0822c9cf6b2ba8a57634d1749688bd1dc825789b`  
		Last Modified: Fri, 16 May 2025 21:04:33 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddd89a16a6372003ab30aba8de26edb75a9a24be6a9cf27943d0b396c5e121a`  
		Last Modified: Fri, 16 May 2025 21:04:33 GMT  
		Size: 365.9 KB (365877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e337606391fa081a0fb2d5933133352f37d773af4352f25ed94d74955b4c3a5`  
		Last Modified: Fri, 16 May 2025 21:04:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe4a761f944bd3a3d72fb28014db2c4303e811c7d5b19a8e25ed3bb8be879d7`  
		Last Modified: Fri, 16 May 2025 21:04:34 GMT  
		Size: 342.7 KB (342711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ccefbb2ed9e2cffe4fbeadaac0fd112efebb0ac08ea36f73d84c467a501572`  
		Last Modified: Fri, 16 May 2025 21:04:34 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c5cb9e3ef8d3bdc6eec3a5a43861d989bed9bcf867527dcd1492f94d50c37b`  
		Last Modified: Fri, 16 May 2025 21:04:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751e01f472e821f6a073a42f3e97d1f7a8a91475e364ce3240850c5228a792ca`  
		Last Modified: Fri, 16 May 2025 21:04:34 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4a64c519aff730c877c854a072bff5a984a0cca1871a29da710ba81035fd31`  
		Last Modified: Fri, 16 May 2025 21:08:24 GMT  
		Size: 209.3 MB (209311769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b55eb9e18404d9ac9178ea4b2bf47a852d1a2cdad51d15bfa3d50215e28ca0`  
		Last Modified: Fri, 16 May 2025 21:04:34 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
