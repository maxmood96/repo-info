## `openjdk:23-ea-5-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:23ef1cad8de2ad3d1dad8165fbbe7dcc5d38ae29f2e96d4d2dcdb086a99df52a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `openjdk:23-ea-5-jdk-windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull openjdk@sha256:1eae5a83d1991101c84235ec02b9674e50c5fc8b753484e236fd5c7d6f87e1ec
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098981052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa17e3c0f8f47f96e6224514b2a3dbdf05d05e4568eee2967b9b7de31d3fc441`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Sat, 13 Jan 2024 01:15:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 13 Jan 2024 01:15:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:15:57 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 13 Jan 2024 01:16:02 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:16:03 GMT
ENV JAVA_VERSION=23-ea+5
# Sat, 13 Jan 2024 01:16:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_windows-x64_bin.zip
# Sat, 13 Jan 2024 01:16:04 GMT
ENV JAVA_SHA256=b2bb5cc22adbca49cd0c94baec87d0a3fefa9c147b6407ac219e4fed98a099b8
# Sat, 13 Jan 2024 01:16:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:16:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c458c847529ac53ad442debc16bb688fde7f33bd6fa5561068c410c851266c40`  
		Last Modified: Sat, 13 Jan 2024 01:16:33 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7efa8d8ac85b8dca81ec66155f5d350b3efb14a7ba6a4ac33985d0d6efb877`  
		Last Modified: Sat, 13 Jan 2024 01:16:33 GMT  
		Size: 509.1 KB (509144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07d0d596e30465ab5d8570c9e0babdea6d7b1da72a3ab1eff90e6a2d8a862a6`  
		Last Modified: Sat, 13 Jan 2024 01:16:33 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478688699259c36dece5a7895b8bd4bb7a673e2b8f7a43c53c2199e87ebd3b47`  
		Last Modified: Sat, 13 Jan 2024 01:16:33 GMT  
		Size: 361.5 KB (361497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145ab25a9a99af656d6414e2eda7c4e9bb0e317710e15721cbc7fe5b444a0662`  
		Last Modified: Sat, 13 Jan 2024 01:16:31 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5e8e7f4449167b3f62f2921c48ab9bf5610afeb5d99e8c7a068d9ee1604fd2`  
		Last Modified: Sat, 13 Jan 2024 01:16:31 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6eabc4845d93feab4669a96027c3e3cd499712f70914cddb4f1e47d4b643ec`  
		Last Modified: Sat, 13 Jan 2024 01:16:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6598fc9ff08e484633e0c188366f00d43e74ebe6292ce148455d7b2b736a6f8e`  
		Last Modified: Sat, 13 Jan 2024 01:16:43 GMT  
		Size: 197.9 MB (197890002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1625258fecd57736c0df0cf9af0ad0c6cb45560d11fd6517ffa0b592c6bd71`  
		Last Modified: Sat, 13 Jan 2024 01:16:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-5-jdk-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:6fdae11d5b344d9ad693990c058ac1cbdcdd2f50a8a825a202e614a5216d913e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268457667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb1a5044bbc5e2a04a4d94ac08e3186051e21c9a77e121b8dfbbba36186249d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Sat, 13 Jan 2024 01:19:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 13 Jan 2024 01:21:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:21:06 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 13 Jan 2024 01:21:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:21:27 GMT
ENV JAVA_VERSION=23-ea+5
# Sat, 13 Jan 2024 01:21:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_windows-x64_bin.zip
# Sat, 13 Jan 2024 01:21:28 GMT
ENV JAVA_SHA256=b2bb5cc22adbca49cd0c94baec87d0a3fefa9c147b6407ac219e4fed98a099b8
# Sat, 13 Jan 2024 01:22:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 13 Jan 2024 01:22:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef73f1b9d460d899dafbea2b87046935dece615d1aa92761e0f906b8079090c`  
		Last Modified: Sat, 13 Jan 2024 01:22:17 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a81691f6b2299718c079b9e8c6369234ef6a37cfae11763e016dba3330c0e0`  
		Last Modified: Sat, 13 Jan 2024 01:22:17 GMT  
		Size: 489.6 KB (489646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b894884c336bec46f3872f51dbf07592f99c64f27c9dc493a2ad312a441f4ff`  
		Last Modified: Sat, 13 Jan 2024 01:22:17 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb5e738371cee60ef7f7b602759947237b50cab5a7d41fd42b70bc26a663633`  
		Last Modified: Sat, 13 Jan 2024 01:22:17 GMT  
		Size: 341.9 KB (341909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07846657a7caaebbb7e549399df110fd115e28a6aa859f72fa7a7d955228d72`  
		Last Modified: Sat, 13 Jan 2024 01:22:16 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d9feb7d98943f1a1bbc5edaafad0778179f0206062333f45c44052e43277cc`  
		Last Modified: Sat, 13 Jan 2024 01:22:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4010d0275f6a6f91d2d4fb9b8583f22d530930b26d0c25c4cc35da7f468aae`  
		Last Modified: Sat, 13 Jan 2024 01:22:16 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9fb18d68fb66eab0a1c8514c92172ad3e9ea95e4833f60fd0b594efcb04b5a`  
		Last Modified: Sat, 13 Jan 2024 01:22:27 GMT  
		Size: 197.9 MB (197895474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f8e64fc16fb261f46edb254ae148b7ea9295ac23bda4e573387b04b62a2f49`  
		Last Modified: Sat, 13 Jan 2024 01:22:16 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
