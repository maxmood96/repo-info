## `openjdk:25-ea-24-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:09a17fb91fafa6b3eed67538d26069edaaffe345ad7fb02ea117252097f7155b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `openjdk:25-ea-24-jdk-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:b27edeae83ddc998a1515671c83f47cf27d64b68de4ada820211de7f90510f25
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3641335921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3a5a412926df4cf04ca0b64a35a631a80872beb8273e28cd493f4bed515cb8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Fri, 23 May 2025 19:59:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 20:00:08 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 23 May 2025 20:00:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 23 May 2025 20:00:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 May 2025 20:00:16 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 20:00:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_windows-x64_bin.zip
# Fri, 23 May 2025 20:00:18 GMT
ENV JAVA_SHA256=2a8b2ea51b3b0b3751867a3117e7fde1235189e6d7601f5ffdb9b9160b270bf2
# Fri, 23 May 2025 20:00:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 May 2025 20:00:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fc0b84d26e30b055265d570016acc872eb918b3dc685633eb5a945ff5d9519`  
		Last Modified: Fri, 23 May 2025 20:00:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ced7210166d8ca282c967c19e06c9934eff0cd2026e9ecc9a48949f186ee895`  
		Last Modified: Fri, 23 May 2025 20:00:50 GMT  
		Size: 416.5 KB (416461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96b6276c842ddf2c61166a92006f21cdcc78a0bea24970d01f99429d63dd134`  
		Last Modified: Fri, 23 May 2025 20:00:49 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7019a459234c72b2cda0ed941313b212746d64d8001e9fe31a7d41b41147195b`  
		Last Modified: Fri, 23 May 2025 20:00:50 GMT  
		Size: 394.0 KB (394048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e0ac3c903f146a6bd3ec678289e8bf469afaa097ef6cd1e89e6ead07918a22`  
		Last Modified: Fri, 23 May 2025 20:00:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78fb3c71952f2b6fed8b9cb1ae913e7e29b37dc28d932197f8af3bcd8220d3a`  
		Last Modified: Fri, 23 May 2025 20:00:47 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eeebb7dc30d68005a19a9dd53f72704bade49df9b2322120a49d2f84edb7ca`  
		Last Modified: Fri, 23 May 2025 20:00:47 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edf7a8fbd5addaf0731c0740a2c6126eaaf269fbc8a77f7e1bf778141d96bf3`  
		Last Modified: Fri, 23 May 2025 20:01:00 GMT  
		Size: 209.8 MB (209751822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6042805c66aaa27ed75aa8e67be33547c142d9d226120442aef8dcf6bb412e`  
		Last Modified: Fri, 23 May 2025 20:00:47 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-24-jdk-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:fcf190c415f8041fb35b4a5d8d1828874682cd86d245f908350b8e587fd58027
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484049371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357604f9091509899cb2b7d05f936a2abb7047fad5675c371c0e0badda562b47`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Fri, 23 May 2025 20:11:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 20:11:28 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 23 May 2025 20:11:28 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 23 May 2025 20:11:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 May 2025 20:11:35 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 20:11:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_windows-x64_bin.zip
# Fri, 23 May 2025 20:11:37 GMT
ENV JAVA_SHA256=2a8b2ea51b3b0b3751867a3117e7fde1235189e6d7601f5ffdb9b9160b270bf2
# Fri, 23 May 2025 20:11:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 May 2025 20:11:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f67237879c096267e1200856bf037f3f29aa56b28033a80f0932dd27895f082`  
		Last Modified: Fri, 23 May 2025 20:12:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28834b2922b677c8fd3b8da93b8710de1c2e15e7fb95e4277fdd08b2f1bf5b5e`  
		Last Modified: Fri, 23 May 2025 20:12:03 GMT  
		Size: 357.8 KB (357825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0477140b8639c611b5f6419232a874a96116bde038349af232aa52c43f761a`  
		Last Modified: Fri, 23 May 2025 20:12:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7610db4ab5004086ee0062d9a4dcaa3fa58be6b2d94adbd1da78dc3d0d8f72e`  
		Last Modified: Fri, 23 May 2025 20:12:03 GMT  
		Size: 345.8 KB (345787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487672f1881a7ed5cbabf7c0e710dc179fa8611168e4b83cc3bf06e5920cf4fd`  
		Last Modified: Fri, 23 May 2025 20:12:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f9e6cad41ac51225d604c82ae062af0c0857808f49372f51558b4c6cd72154`  
		Last Modified: Fri, 23 May 2025 20:12:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de805c3c8194da08542d957c906f5606d24570fb482796003010792a178963c`  
		Last Modified: Fri, 23 May 2025 20:12:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c638d3864bd87ed514894184ed4789df81eeaa7024f0fd79192326d2a7423c`  
		Last Modified: Fri, 23 May 2025 20:12:15 GMT  
		Size: 209.7 MB (209709936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062e5b3fc45b5eadba5bd34a424cb019549939d0bbf6c37263969021140bb156`  
		Last Modified: Fri, 23 May 2025 20:12:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-24-jdk-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull openjdk@sha256:a8c045e18efdfef509843c78786c9df99d3e985aab677127931b1d37f69449ea
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394141875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7367bdef89c0a64d3c3e1dbb3525e79dd4dba154f5df61af3b7a7d744eea02a7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Fri, 23 May 2025 20:03:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 20:04:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 23 May 2025 20:04:18 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 23 May 2025 20:04:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 May 2025 20:04:26 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 20:04:26 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_windows-x64_bin.zip
# Fri, 23 May 2025 20:04:27 GMT
ENV JAVA_SHA256=2a8b2ea51b3b0b3751867a3117e7fde1235189e6d7601f5ffdb9b9160b270bf2
# Fri, 23 May 2025 20:04:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 May 2025 20:04:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9943b418bf9ba8a51291773118fc42a541e34c1f4fab78a959894cf3d229c79`  
		Last Modified: Fri, 23 May 2025 20:04:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0500c85686b5f06b955c9bf960500d90550d0ae49d9cc7c40529a50b8934f3`  
		Last Modified: Fri, 23 May 2025 20:04:55 GMT  
		Size: 364.8 KB (364752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c6af7931fce13ebf09dd412719b0c8f1cbe3ac08e344e29bb910bb28683282`  
		Last Modified: Fri, 23 May 2025 20:04:55 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6829592eda084943395b0537fade00b78048df09b1d5b7fc4184cb0150a44098`  
		Last Modified: Fri, 23 May 2025 20:04:55 GMT  
		Size: 341.4 KB (341375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382562d7a098abf3220647f7f930d7d1dc1de751a4c9785de53d3b7906c0a682`  
		Last Modified: Fri, 23 May 2025 20:04:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c900365e44f0d2921f75484b6b3da31a3c92936c7edf70837b0dd95c5307c5d`  
		Last Modified: Fri, 23 May 2025 20:04:54 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbb806032cc5270aa321033b0edfe5846a33208ac4b4e5855e70a033974f14e`  
		Last Modified: Fri, 23 May 2025 20:04:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8d090f7b049f0293a4344207801671b9f04d4cf78689b9a45adaf9e9d32b24`  
		Last Modified: Fri, 23 May 2025 20:05:05 GMT  
		Size: 209.7 MB (209710512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881fd87838d847d57f6386bb83cb105696e72ebdd7e1aa83bc3730c43d2473d0`  
		Last Modified: Fri, 23 May 2025 20:04:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
