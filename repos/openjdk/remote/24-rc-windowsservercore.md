## `openjdk:24-rc-windowsservercore`

```console
$ docker pull openjdk@sha256:0d0da25719a4ca58615430da34131dc9b56d6f9c22cbcedd445136902169c92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:24-rc-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:04ebeba240aa22d687e4a2b719f67346d103f87ab2f91acd4f6289ac88fd5142
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709986938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590aea82123aa8e9e2749528909cb9240db53a967c6595bb6d3931fb1c53cff9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Tue, 11 Feb 2025 00:31:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 00:31:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:19 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 11 Feb 2025 00:31:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:25 GMT
ENV JAVA_VERSION=24
# Tue, 11 Feb 2025 00:31:26 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_windows-x64_bin.zip
# Tue, 11 Feb 2025 00:31:27 GMT
ENV JAVA_SHA256=11d1d9f6ac272d5361c8a0bef01894364081c7fb1a6914c2ad2fc312ae83d63b
# Tue, 11 Feb 2025 00:32:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:32:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d7dcf2bcddbdad7557da19e4234025bb6a672cf3b88d03d0878b8727c1bce8`  
		Last Modified: Tue, 11 Feb 2025 00:32:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c89eca89aa9b4ff4cfaa8458d6aee96174fd7c425a419c78542549083b507b`  
		Last Modified: Tue, 11 Feb 2025 00:32:25 GMT  
		Size: 385.6 KB (385592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ec3d96e893ae4cf1140e0c0ae61870b8f8c519be0eb742121d270436321f75`  
		Last Modified: Tue, 11 Feb 2025 00:32:25 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400d617e06805df508fa1d5d31e2d49009c61e98ff9346d6f5d376659579e92d`  
		Last Modified: Tue, 11 Feb 2025 00:32:25 GMT  
		Size: 374.4 KB (374419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7a5cc4ea843ab82cfaf65322b1e954c32866d55945930f43bda5ab255817f2`  
		Last Modified: Tue, 11 Feb 2025 00:32:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca19dc597d5c6c429a93c8942fb9e69e24a066b6fbc0a4d672479547439db5f9`  
		Last Modified: Tue, 11 Feb 2025 00:32:24 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d36d047931df06992b594d27cc88cc0155a495db3dcca47df8e43daab8c01d`  
		Last Modified: Tue, 11 Feb 2025 00:32:24 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc012a3383812a106bee99c2a72766783a951c214f3f919f8bb542dec6b73a`  
		Last Modified: Tue, 11 Feb 2025 00:32:37 GMT  
		Size: 208.9 MB (208941499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081f56f2a7db3acf106d80ad462a353e2ec78a9010bea88735231d862eaf05bb`  
		Last Modified: Tue, 11 Feb 2025 00:32:24 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-rc-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:dbd310fa8c9a143457931c62f1227b78dc0af70541b0edc78ea2b2f81018a4fe
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2473452909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147ddccb4f3a1c1b52b3ab70f5e4775c85f6098aa5b05241050e067e337b4811`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:44:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:44:28 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:44:29 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 13 Feb 2025 00:44:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:44:35 GMT
ENV JAVA_VERSION=24
# Thu, 13 Feb 2025 00:44:36 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_windows-x64_bin.zip
# Thu, 13 Feb 2025 00:44:36 GMT
ENV JAVA_SHA256=11d1d9f6ac272d5361c8a0bef01894364081c7fb1a6914c2ad2fc312ae83d63b
# Thu, 13 Feb 2025 00:44:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:45:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f8491ac0764676a31a9ca542f28ff77d33c41360022d12faa4146d4ec83800`  
		Last Modified: Thu, 13 Feb 2025 00:45:04 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b3b2ffc0778175ac2bbef45d92d94d755bbed684fadf9778fcc4b0b60b95b6`  
		Last Modified: Thu, 13 Feb 2025 00:45:04 GMT  
		Size: 357.5 KB (357504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75299c43cce9196f5ad623666999a2aeab7946ea525f72e8f300feda4f7f1495`  
		Last Modified: Thu, 13 Feb 2025 00:45:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615c5797bac28589910968fec6b38467ee1324b6642ca03a220836cf2d8e2e7b`  
		Last Modified: Thu, 13 Feb 2025 00:45:04 GMT  
		Size: 336.8 KB (336800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a7abb6139aacf6df2ed9489a26de81a281a8318d145be3425038c1e14a6bb`  
		Last Modified: Thu, 13 Feb 2025 00:45:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0be84dc123e3d8b4c2de0ac29abc501fb897cf34ddc30f47572f0a0811a0b0`  
		Last Modified: Thu, 13 Feb 2025 00:45:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0676af04befdf7c26d7ee49c119d8b753b095dc84c9b6a3f4a76896db07c5926`  
		Last Modified: Thu, 13 Feb 2025 00:45:03 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77a8548b3c12fafcb6bf10d2fc36f67d766274da0519712ef123a3de59b8ccb`  
		Last Modified: Thu, 13 Feb 2025 00:45:14 GMT  
		Size: 208.9 MB (208892900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bfb8a1317016ff6d127a3f02ac68af478c7bd5b5c12251a7cfa96dbcadf8f`  
		Last Modified: Thu, 13 Feb 2025 00:45:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-rc-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:25694d35528c91fe01db3499f91965f40ca8110f4043a4c3633f14d60b87d642
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346492020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6438cd1157e60ba3c39de1e3357fbbd1f5e739a6e6bcd131f4552f2fed4299`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:42:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:43:04 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:43:04 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 13 Feb 2025 00:43:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:43:11 GMT
ENV JAVA_VERSION=24
# Thu, 13 Feb 2025 00:43:11 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_windows-x64_bin.zip
# Thu, 13 Feb 2025 00:43:12 GMT
ENV JAVA_SHA256=11d1d9f6ac272d5361c8a0bef01894364081c7fb1a6914c2ad2fc312ae83d63b
# Thu, 13 Feb 2025 00:43:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:43:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59e7cb2f62d3ca1d2757aa07b43050cdda0aace6c3a7c146447f56f7dbb6be8`  
		Last Modified: Thu, 13 Feb 2025 00:43:39 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2d27469f40aab79d4d3299885df66666ef0813aa9ea0c6787d01a97e0156d5`  
		Last Modified: Thu, 13 Feb 2025 00:43:39 GMT  
		Size: 346.9 KB (346929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc25ade87dd2f091d7f34c0fa9d5748173d7608deb415ef2f42a42ac6854447`  
		Last Modified: Thu, 13 Feb 2025 00:43:39 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76707d48dffe35b117a39312702b0279c644514e400b67f3841559be4c7285c`  
		Last Modified: Thu, 13 Feb 2025 00:43:39 GMT  
		Size: 329.3 KB (329327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b17ec1bc8b5892e08af7aa89a01850c3722831bac79e83fe575249c7b0db89`  
		Last Modified: Thu, 13 Feb 2025 00:43:38 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02abd5f6b0dc6b84975c71385c18c52ec05e69637cb94e4ec6293dcad6feb656`  
		Last Modified: Thu, 13 Feb 2025 00:43:38 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779683b99488fec228227d490079317a08e9bfef0b530951098328169b92ccc4`  
		Last Modified: Thu, 13 Feb 2025 00:43:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b995b9ee44c3800b99be70b7716b82aa91383a3bf22309af3e10d56f239e7e43`  
		Last Modified: Thu, 13 Feb 2025 00:43:49 GMT  
		Size: 208.9 MB (208899229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe70d0375ff31f8ef2f5a4d206a15549b5cbb1bce97545fc3d46b8f0c6981d6`  
		Last Modified: Thu, 13 Feb 2025 00:43:38 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
