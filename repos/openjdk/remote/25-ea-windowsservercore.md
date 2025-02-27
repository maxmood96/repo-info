## `openjdk:25-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:b66307a3ec75d71553683a3f2637e777cf0563c1bc3d9e4baa35125662c261e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-ea-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:2403ea720741867eecabfa68f2ef392dc04373949dcf4a841b42c1e27e6aa131
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2472590100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa9191bbd4eeb51743ca0593fd0783b6d9e4bcee367da9dabace4b008d45f9a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Sat, 22 Feb 2025 00:35:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:36:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:36:10 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 22 Feb 2025 00:36:15 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:36:15 GMT
ENV JAVA_VERSION=25-ea+11
# Sat, 22 Feb 2025 00:36:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_windows-x64_bin.zip
# Sat, 22 Feb 2025 00:36:17 GMT
ENV JAVA_SHA256=7db003a6e122cc08ddd88b60142284f2461efe69b7007138277f55c2b4cf1d4a
# Sat, 22 Feb 2025 00:36:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:36:37 GMT
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
	-	`sha256:a45bc8c9cbb25c116eef37c13b8ade4fbcb56e7293f7f535233a54ddda954039`  
		Last Modified: Sat, 22 Feb 2025 00:36:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c309c47c6bc31a5f1b9c065524af9814a298e66b9e0cdd3284ac8d86b84046e`  
		Last Modified: Sat, 22 Feb 2025 00:36:42 GMT  
		Size: 390.1 KB (390084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e3388eb33e18d864906803dd1b20c573a91916f3d823de8887fe279639464`  
		Last Modified: Sat, 22 Feb 2025 00:36:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dbaf8bcae22d8dcf369d0ea0f18f67bf03df045cecfc662beb8b1358e16f75`  
		Last Modified: Sat, 22 Feb 2025 00:36:42 GMT  
		Size: 368.4 KB (368430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420cba2a981f01e3a4aecb389649d23d5d09f9baebbb6ec4b5f3a2ceab5c5309`  
		Last Modified: Sat, 22 Feb 2025 00:36:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f84f220a5f57aae7b3c8b8011603cc54d5ebaf2ea0a20494bb02414a1e0ecd`  
		Last Modified: Sat, 22 Feb 2025 00:36:40 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015b2546805846ff63a2c28502c0d01fc8c9136d009c6a33a97d21cff1caa53a`  
		Last Modified: Sat, 22 Feb 2025 00:36:40 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820497b72c0c22f4340b02bb837adbafa993517e1a397c00c34d91ed51e7f2db`  
		Last Modified: Sat, 22 Feb 2025 00:36:52 GMT  
		Size: 208.0 MB (207965878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39ea1cf6fdc4bb9c23a836d29942bcd2b5ae1d6fd89c198f344dd52d4610e2f`  
		Last Modified: Sat, 22 Feb 2025 00:36:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:b0044cb58ee10d3a29ae6308fffd8e8a72fe7bde1ff24af349fbe15fb6732802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345488805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0340b18ef1db8f1cb1b983667c00f0acd19d9b87c8df459d1d67ffe8ce6832bf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Sat, 22 Feb 2025 00:30:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:10 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:31:10 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 22 Feb 2025 00:31:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:31:17 GMT
ENV JAVA_VERSION=25-ea+11
# Sat, 22 Feb 2025 00:31:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_windows-x64_bin.zip
# Sat, 22 Feb 2025 00:31:18 GMT
ENV JAVA_SHA256=7db003a6e122cc08ddd88b60142284f2461efe69b7007138277f55c2b4cf1d4a
# Sat, 22 Feb 2025 00:31:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 22 Feb 2025 00:31:39 GMT
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
	-	`sha256:b4f50f6cbe3865f5c184d4ff2f5e9cf2093782b74aee23e6dee59fc855c4370f`  
		Last Modified: Sat, 22 Feb 2025 00:31:46 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fae8f29d1211bc98369b5b304ceb2cd8b3f6c577f51abdfd892e652b7c8d670`  
		Last Modified: Sat, 22 Feb 2025 00:31:46 GMT  
		Size: 334.1 KB (334091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9735253bb27cb86172a025e8832d097e76e61ff6d5b0162917b94dd3bbecc5a7`  
		Last Modified: Sat, 22 Feb 2025 00:31:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86283bb64395f3a921d08d687f1c2058371dd9ee7735230feea87b280620889`  
		Last Modified: Sat, 22 Feb 2025 00:31:46 GMT  
		Size: 322.6 KB (322623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2051c5c4267e597d26e97c3e209b90e77b1c7f8545a01140a982eaab0ad3183`  
		Last Modified: Sat, 22 Feb 2025 00:31:44 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3317a4fc74fc17152cb42a5c6ede2d09d0bc18b9139b42d3d625c84377e35ec`  
		Last Modified: Sat, 22 Feb 2025 00:31:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3153b53bb02f5ddbf36767449a154f140c5a3cc4aea674e9baa5f8aa43d828f2`  
		Last Modified: Sat, 22 Feb 2025 00:31:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f520d901b1489840f82c899ad0aeb80a4101c5e5f578dc6f911d92ca38385e5`  
		Last Modified: Sat, 22 Feb 2025 00:31:56 GMT  
		Size: 207.9 MB (207915459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e41c8a4199a949e0dd5dbd9269c1684ddd3aa36566dc32b560f55ee0fb3b89`  
		Last Modified: Sat, 22 Feb 2025 00:31:44 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
