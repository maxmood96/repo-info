## `openjdk:25-ea-11-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:5f28b172f0ecc5da9f61cd960464698b3bf5ec2464b6b4fabb156926dbd1dbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `openjdk:25-ea-11-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

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
