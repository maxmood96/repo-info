## `openjdk:27-ea-21-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:1500a510b86d4b1af3a478a6967ce5e286bac01346edc7f5ad03ebe13a194a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-21-jdk-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull openjdk@sha256:883fe314f14ff3d63fb228a4a41603bee2c88aafed46368c80cce4dcb0f5ac03
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2364884502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302efa22a8b52011bba0f163a8420cf9d751bbde4af455c7b4b74c7736d9d63a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 12 May 2026 00:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 00:36:53 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 May 2026 00:36:54 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 12 May 2026 00:36:59 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 May 2026 00:37:00 GMT
ENV JAVA_VERSION=27-ea+21
# Tue, 12 May 2026 00:37:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_windows-x64_bin.zip
# Tue, 12 May 2026 00:37:01 GMT
ENV JAVA_SHA256=c141a4db38b2d45883ed5d65a72f4444d1efa690d650027308594335dec2b07b
# Tue, 12 May 2026 00:37:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 00:37:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6b23346363cec7a7cfd6f2f7bb2fa6530936831a1694a1ed476cdda00236c2`  
		Last Modified: Tue, 12 May 2026 00:37:42 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d880d785988e73f4073e374354c16dbbbefe58f6fc2ab5187355f1299efd0e2`  
		Last Modified: Tue, 12 May 2026 00:37:42 GMT  
		Size: 406.1 KB (406075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448e42f7b38a4f939a35107391171735686d8d3c9c16bc7fecfaeeb70395b2b2`  
		Last Modified: Tue, 12 May 2026 00:37:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944b9229b39c1d502b5b48d3d30a575e29bb8d62b21007c629300c084ef250fd`  
		Last Modified: Tue, 12 May 2026 00:37:42 GMT  
		Size: 389.6 KB (389627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b820217ae77693da6783c4ce807e2b97865f340faf8110a2338ac604395295c9`  
		Last Modified: Tue, 12 May 2026 00:37:40 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b953f152a975644bba84385673ef19999a0b40eb3bbaa7ed60df8dac29c6a2e`  
		Last Modified: Tue, 12 May 2026 00:37:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fba26578c6b3efea5ee5e3261bf0b78576710590cfb3291cc97a8b2e2b80cf`  
		Last Modified: Tue, 12 May 2026 00:37:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c7f3ebffd63f4480961a5e6d85e50e6b6bfad1b66ab2b5fa9af1bf29470b5c`  
		Last Modified: Tue, 12 May 2026 00:37:57 GMT  
		Size: 234.1 MB (234094914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb93d38cf40e09eee42d90cd3f1efcd400ba916dec53279687e905f47e4097`  
		Last Modified: Tue, 12 May 2026 00:37:40 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-21-jdk-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:01187c3e503ea42c18fd6031650f8e93a2acf9608e94a60a8c1a19c084901418
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296230036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f532b9869c61e13f3dd4c4e90ec635614175e8137f64824e546f48ed51a6e66`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 12 May 2026 00:15:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 00:33:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 May 2026 00:33:32 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 12 May 2026 00:33:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 May 2026 00:33:40 GMT
ENV JAVA_VERSION=27-ea+21
# Tue, 12 May 2026 00:33:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_windows-x64_bin.zip
# Tue, 12 May 2026 00:33:42 GMT
ENV JAVA_SHA256=c141a4db38b2d45883ed5d65a72f4444d1efa690d650027308594335dec2b07b
# Tue, 12 May 2026 00:34:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 00:34:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa492a5535facf20fd9ea86ddfd2827b386ca74f28e0073a7b036eb7144c3259`  
		Last Modified: Tue, 12 May 2026 00:17:55 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5772b261a4c5a975fe1d657ae1eadc601ec02136546c380096e456d196ba86be`  
		Last Modified: Tue, 12 May 2026 00:34:31 GMT  
		Size: 504.0 KB (503958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cc1f33ae9f3dea7a86dbeb11177b6c3900d61941391c7e3ca6305728225ae3`  
		Last Modified: Tue, 12 May 2026 00:34:31 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fea60138e87b095c50fb9b289baaed3fe76d7a714d951db769ba9d34946c11`  
		Last Modified: Tue, 12 May 2026 00:34:31 GMT  
		Size: 351.0 KB (350985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729914896d2d1d4c7004e00e50b373ce339c7b1dac5a789ee590a1641abcc902`  
		Last Modified: Tue, 12 May 2026 00:34:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be735ce1c172e122d8f19c339a99452ff5af2c099d72ffe125af7ca2c1ee6a85`  
		Last Modified: Tue, 12 May 2026 00:34:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf0c36114160f5d9b2c058b2477406e3a3050100227fde571eb0859698b1d1d`  
		Last Modified: Tue, 12 May 2026 00:34:29 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bbf01946aa0221b3da1a858d9a56e1bed67aa751a5053a2fea2cd27ccd81fa`  
		Last Modified: Tue, 12 May 2026 00:34:45 GMT  
		Size: 225.2 MB (225155938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c436ef2d4451546d38f5d647ccae7726388f2ced06ef22f621d9721b5deda2`  
		Last Modified: Tue, 12 May 2026 00:34:29 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
