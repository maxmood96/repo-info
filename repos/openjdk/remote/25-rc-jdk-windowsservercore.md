## `openjdk:25-rc-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:020ccb62035ab70ef584ee48f855a5ee55a4ae3a4d267e756e072d51a6094954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:25-rc-jdk-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:2dd778463a093faef7e0c677f71fbea2b32e2c3e4445b444a46917122ea312b7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3718490239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c1b2e9281a353004c21c5ddf925bb2238dac3f0ff8d8942a1aa76108aae23b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:34:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:34:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:33 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 12 Aug 2025 20:34:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:38 GMT
ENV JAVA_VERSION=25
# Tue, 12 Aug 2025 20:34:39 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_windows-x64_bin.zip
# Tue, 12 Aug 2025 20:34:39 GMT
ENV JAVA_SHA256=1bf872a4dc38579963ad34a757b3077296c2d2ccfeeff041d1741a87e6bde898
# Tue, 12 Aug 2025 20:35:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:35:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9426ac85c32ef0ad96af672f710cb3b41cb0cbf264db70747e3408a9b17c6149`  
		Last Modified: Tue, 12 Aug 2025 20:38:40 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09540fcd91088f65aa2a7120dcd96aa22f6ca0c5efbf17799e13a8a61c0fb37`  
		Last Modified: Tue, 12 Aug 2025 20:38:42 GMT  
		Size: 368.3 KB (368274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8362291cec62306fa7727b47e26d887dccdc103282470498cabde4d6f91adfdc`  
		Last Modified: Tue, 12 Aug 2025 20:38:41 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e03dd2ecbccdb43db22f0a5c5cad3062682413bad6fc00430c30462c6e3fcb7`  
		Last Modified: Tue, 12 Aug 2025 20:38:42 GMT  
		Size: 354.0 KB (353976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a87cbc2e8285567edb90fff4cede6f60f838c01e0fcae28e9c78b4ab0309c96`  
		Last Modified: Tue, 12 Aug 2025 20:38:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0609bbbda2633bec90b336a0b90b1f9ab8da7e1aca76b3f30f6254b9de8f0e3f`  
		Last Modified: Tue, 12 Aug 2025 20:38:37 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f6cdfd6df9033c234b82fe75e36f1279fd8f1d8a6c1ea07550fba420fe7e43`  
		Last Modified: Tue, 12 Aug 2025 20:38:38 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40da4f1d72bbfaa765797d7df12fec22904584eaaced9ef4e3ebc9dd6804bb12`  
		Last Modified: Tue, 12 Aug 2025 20:47:01 GMT  
		Size: 218.9 MB (218929649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a8c7d540e59ceed9a8cfec7be93884be82f183a353f0e83166e730d483f93a`  
		Last Modified: Tue, 12 Aug 2025 20:38:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-rc-jdk-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:5c1e21d400397e8585578aef7ecb8518c78b0e81509bbe0820cc704269a246d7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2501296525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e3dc026535949468cfda6dd80ac2c47ad6ad3966118d90c21ac32d8796c67d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:34:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:34:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:33 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 12 Aug 2025 20:34:41 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:34:43 GMT
ENV JAVA_VERSION=25
# Tue, 12 Aug 2025 20:34:44 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_windows-x64_bin.zip
# Tue, 12 Aug 2025 20:34:45 GMT
ENV JAVA_SHA256=1bf872a4dc38579963ad34a757b3077296c2d2ccfeeff041d1741a87e6bde898
# Tue, 12 Aug 2025 20:35:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:35:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbec5ba5fbaf8526882e529bf6308a967876f12f49c4b2191c42409e5337636`  
		Last Modified: Tue, 12 Aug 2025 20:36:56 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea518cfccdcf12e8110d052c4ae08de06ac5c2f4305e5d63625c708f13e68a5c`  
		Last Modified: Tue, 12 Aug 2025 20:36:57 GMT  
		Size: 349.0 KB (349012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f55a317cf2d0b87b7f395b81d10531c6c98b96eb2b66b9cc024e01948dcced`  
		Last Modified: Tue, 12 Aug 2025 20:36:56 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbece82af0bb546b65f441f474fcae8ae7f0454db67a43bd1990a392e602c96`  
		Last Modified: Tue, 12 Aug 2025 20:36:57 GMT  
		Size: 334.7 KB (334717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d32ca0c40f91aa184dbb0a64b8b4e1b4ec2003cb1d107f0346c342ef6206b4b`  
		Last Modified: Tue, 12 Aug 2025 20:36:57 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba9f5c3e70478c94ec6d33ae6372eae9ad909dec35bc3194b14773b69fe2916`  
		Last Modified: Tue, 12 Aug 2025 20:36:56 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25afbc5eba7bba913b728859e49753f842026cb2eedaa11202dee8e28199c6ea`  
		Last Modified: Tue, 12 Aug 2025 20:36:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b139bd5a848d7e28616bdba81db7f152d4911d2f6133e3e99b7a66b79a3585f4`  
		Last Modified: Tue, 12 Aug 2025 20:46:09 GMT  
		Size: 218.9 MB (218913119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9773bd0082384ce4c3c48065ea3d012cabb450d4bf4cfb9124fa5855b5f60440`  
		Last Modified: Tue, 12 Aug 2025 20:36:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
