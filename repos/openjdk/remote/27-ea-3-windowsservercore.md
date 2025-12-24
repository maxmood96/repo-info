## `openjdk:27-ea-3-windowsservercore`

```console
$ docker pull openjdk@sha256:89a9f4292bae51fcbd99b6538ea50ad08c4f2d53871934bdd438c7dd51c959ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `openjdk:27-ea-3-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:75d7dd33e0c15af79bfbf29e16275c36872739212ee4cbf149002b35277c2fda
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3478256408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480f763219ed032bb8b63c43bcda78eabe7566572e3a4af4062d05c327a8010f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Wed, 24 Dec 2025 05:18:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Dec 2025 05:19:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:19:10 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 24 Dec 2025 05:19:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:19:17 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 05:19:18 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_windows-x64_bin.zip
# Wed, 24 Dec 2025 05:19:19 GMT
ENV JAVA_SHA256=b40619c93cd4c56c31387444551cdaf5d2fe61ff5e8a10cc43ac1159ad3a69a6
# Wed, 24 Dec 2025 05:19:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:19:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3d525d0293f0c6ec260ea3e548281f51d5e75db31202d01297a9c362bf896e`  
		Last Modified: Wed, 24 Dec 2025 05:33:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d2de42b0e26bf29ce180659081408d6efafecac8fc74e3b769e0a25f14a7f6`  
		Last Modified: Wed, 24 Dec 2025 05:33:04 GMT  
		Size: 405.6 KB (405604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc385c79ad1d5d394e02ebc84c382c2010ce9f9cfdd664bcde9d313af8ee498`  
		Last Modified: Wed, 24 Dec 2025 05:33:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7024ce36b5bff6ea629ffdb5bcd235d5e707886d23e246780381c19897be80e`  
		Last Modified: Wed, 24 Dec 2025 05:33:04 GMT  
		Size: 387.2 KB (387214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a3424f1b1b2634a0636c20b97edec7c390cb1da7830dee058bc1cf9a212cdb`  
		Last Modified: Wed, 24 Dec 2025 05:33:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cb6d43787f5b5dda903158b020a94bac36626bf2de0b11a0fb4b52e8452412`  
		Last Modified: Wed, 24 Dec 2025 05:33:03 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c951029cf95fd470e2363e345977e723cc49c977ac95f4cd78ba2b859a8c813`  
		Last Modified: Wed, 24 Dec 2025 05:33:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d52241fbd08444b22df3aa7c9326a8edf81076d67b17498a9e0c9d501681ad`  
		Last Modified: Wed, 24 Dec 2025 05:33:21 GMT  
		Size: 224.3 MB (224335349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8710de7998d6dc3459bb43780761e3888b6638c78207e33acfefcf4252172b`  
		Last Modified: Wed, 24 Dec 2025 05:33:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-3-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:2eec1ff61d130772de87bee94cf0ae5fb4726c2b0daa270fd2ba6f8d6e4556c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2005060927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb76d02f6262e88b19c1b96fdc46b6631fbc092b902ac5de10a612501f3ea5f3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 24 Dec 2025 05:21:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Dec 2025 05:21:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:35:36 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 24 Dec 2025 05:35:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:35:45 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 05:35:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_windows-x64_bin.zip
# Wed, 24 Dec 2025 05:35:47 GMT
ENV JAVA_SHA256=b40619c93cd4c56c31387444551cdaf5d2fe61ff5e8a10cc43ac1159ad3a69a6
# Wed, 24 Dec 2025 05:36:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:36:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5e1e7094f7d15a86b575087b9ef75e5c8056b26b193f2835b0bb746e105e0c`  
		Last Modified: Wed, 24 Dec 2025 05:35:17 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c6c072091e6f8cbfdbba0b2f363767075da4c70a3a6f6a8f284efe5639dc18`  
		Last Modified: Wed, 24 Dec 2025 05:35:18 GMT  
		Size: 504.0 KB (504010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419d3b84c6b4505b99366775986f9bd2d844849fff0252cf714fa78e1e28015d`  
		Last Modified: Wed, 24 Dec 2025 05:37:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6c922d400dc997149a184c1dbeeaf6977443ab02671ca3996a93e3ffccdc45`  
		Last Modified: Wed, 24 Dec 2025 05:37:08 GMT  
		Size: 352.1 KB (352125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153813f883ab05a0c9aa15b0aee5a5e40e81b064cdb547c1be45a0cbfa807314`  
		Last Modified: Wed, 24 Dec 2025 05:37:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ff14adbf7e7cc3e3da9c5fc59db08ff4b763d0c0ca428b49697b5acb53f935`  
		Last Modified: Wed, 24 Dec 2025 05:37:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575daae52a315908b25abab1f1c27d1d95c8566da17cdce73e1641aa0e4f633e`  
		Last Modified: Wed, 24 Dec 2025 05:37:08 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9465a464881e2987904b73e0767e25eb6de8484d46849c7f8cda3af3646ffe5`  
		Last Modified: Wed, 24 Dec 2025 05:37:33 GMT  
		Size: 224.3 MB (224317740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45254fed2d3b0b45cd10e83450f2005f3e0185c6814686bffab139263d29d2db`  
		Last Modified: Wed, 24 Dec 2025 05:37:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
