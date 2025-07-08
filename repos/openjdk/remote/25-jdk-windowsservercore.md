## `openjdk:25-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:98f4c28230392104aa600b95d9c62ed5a8ac7ab6aef5ac865aedd21d50641e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-jdk-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:1c69e529ede3ab119e53a9701cb474cc8d1f8c9a9063d0374bc9fc83c4d12a62
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3695900861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6056fac987f4f9b090aadbb2adc483988f4dc559144dd2c90fd5bd2f0b15bffb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 07 Jul 2025 21:04:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Jul 2025 21:04:50 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:04:51 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Jul 2025 21:04:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:04:59 GMT
ENV JAVA_VERSION=25-ea+30
# Mon, 07 Jul 2025 21:05:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_windows-x64_bin.zip
# Mon, 07 Jul 2025 21:05:01 GMT
ENV JAVA_SHA256=917fc8ab9ae5f7aa7aa1d45bd5a8612a2fd33d6835b9a42728532d0a14f8b42e
# Mon, 07 Jul 2025 21:05:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:05:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e938d6b0e5edca79a5928df43e859a2a15a22090811426cdc69ac2f310ffa1`  
		Last Modified: Mon, 07 Jul 2025 21:09:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39ca2ae35f583f195c485d73ced4b3e8630948eaa76211b5996325e7c378a4d`  
		Last Modified: Mon, 07 Jul 2025 21:09:02 GMT  
		Size: 396.2 KB (396151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30dce903d7d0c48719fbff751e24f2e557b696c6efca989f4e69dd567213552`  
		Last Modified: Mon, 07 Jul 2025 21:09:02 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb21b589c9ed77c9f72fb7cb963350d12aecde199f606cbf7824ecea1e0d390`  
		Last Modified: Mon, 07 Jul 2025 21:09:02 GMT  
		Size: 381.2 KB (381244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41db697c19c1d0ab66b5408ad82dccbaeda0e6baf187283a21680b55d83cbfc`  
		Last Modified: Mon, 07 Jul 2025 21:09:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988e83c8a9bcd145930bc544c99e16f706af0448473d98b4d98320aaae4d08a8`  
		Last Modified: Mon, 07 Jul 2025 21:09:03 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac2d5b11295729549ce3d04541d90710929fa6a2c81ae644257aac33a82adf6`  
		Last Modified: Mon, 07 Jul 2025 21:09:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431fc89c7171ac6909d98b0213d2a14001c26f67731b36780c7d99efa11c212f`  
		Last Modified: Mon, 07 Jul 2025 22:08:55 GMT  
		Size: 218.9 MB (218941690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d1bb8c66f23651f4c061bcfceb97cb9e42f004255d495978220082ff8f6615`  
		Last Modified: Mon, 07 Jul 2025 21:09:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:b465a4175b4d5107f23fe193b13b3e54b12fe3cc34d7eca74dc6ee7074247b01
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499862580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae92283a71c98b78928e6d79e99b9bf26130dad670c448cb35271ed94e59301`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 07 Jul 2025 20:59:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Jul 2025 20:59:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 20:59:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Jul 2025 20:59:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 20:59:34 GMT
ENV JAVA_VERSION=25-ea+30
# Mon, 07 Jul 2025 20:59:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_windows-x64_bin.zip
# Mon, 07 Jul 2025 20:59:36 GMT
ENV JAVA_SHA256=917fc8ab9ae5f7aa7aa1d45bd5a8612a2fd33d6835b9a42728532d0a14f8b42e
# Mon, 07 Jul 2025 20:59:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:00:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f18c600e3f1e6920a9c13e2bc1cb85fe722ed3f4c485d7232ab8b219784bdb`  
		Last Modified: Mon, 07 Jul 2025 21:00:28 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eceaeca1107bb95fdc4e4cf9e11b6ab194048ffc8d2dcbac5d04a78f093cce5`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 356.7 KB (356728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff3c45c8aa311b9ea73d06c6812e68a19df67ef9b9620162bb77958a8cde4`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891d2c54236a297b70de340f1058bf553e9f801f477c9bf5f3f3a781810e731c`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 345.4 KB (345449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea667565e692cf293be7cb956420752cfa282d797157fe71009c15e4c6afcea`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0844edca565cc66cea58c88d52881bcf4ec81bf0d8597e8725497acf387b6a69`  
		Last Modified: Mon, 07 Jul 2025 21:00:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6426423c9c77930251dba727e82e1616b45f18e4dc07733653607065b30874`  
		Last Modified: Mon, 07 Jul 2025 21:00:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4142f979958b0d74dacddbf46f937781885770bc9abbf4116b435e3b72b25531`  
		Last Modified: Mon, 07 Jul 2025 21:05:52 GMT  
		Size: 218.9 MB (218901116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325bc6bc2c5ff81b9dab75b85fcea93ffe06f03ccec9027af8b78444a00a305d`  
		Last Modified: Mon, 07 Jul 2025 21:00:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
