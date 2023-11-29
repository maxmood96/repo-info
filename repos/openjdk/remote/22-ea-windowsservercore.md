## `openjdk:22-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:572a0a012ef919be9a3f6237998aa417a879410f5b271dc635fa23deba5eb458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2113; amd64
	-	windows version 10.0.17763.5122; amd64

### `openjdk:22-ea-windowsservercore` - windows version 10.0.20348.2113; amd64

```console
$ docker pull openjdk@sha256:5870ae7585eef0acd86c21431a8d50915fd343c01848f2c69b8e46c9556ae1a9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086784809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c72c5600366c073232500c4ebfe41a5dbaae366ea1e6b4824952a3f46089b4b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 05:18:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Nov 2023 05:18:37 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 16 Nov 2023 05:18:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 29 Nov 2023 02:11:54 GMT
ENV JAVA_VERSION=22-ea+25
# Wed, 29 Nov 2023 02:11:55 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/25/GPL/openjdk-22-ea+25_windows-x64_bin.zip
# Wed, 29 Nov 2023 02:11:56 GMT
ENV JAVA_SHA256=3fb62ee630aa69a8ca5c7a2734a69e9fcb251519872ebca5eb03f64f60f90f66
# Wed, 29 Nov 2023 02:12:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 29 Nov 2023 02:12:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c484d21f80984bc956d2a7ca187c7250676fd3af73a362efb91125bb6255aa10`  
		Last Modified: Thu, 16 Nov 2023 05:26:11 GMT  
		Size: 453.2 KB (453223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaf9eb81e5d07980ecf0f7d31f640ebd53980837baa8588ca770fa56963edd6`  
		Last Modified: Thu, 16 Nov 2023 05:26:11 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be91ce40f73c6eaafd338b1fc738f4394dc6542fd074fc12e651a47dfd49e6f3`  
		Last Modified: Thu, 16 Nov 2023 05:26:11 GMT  
		Size: 263.4 KB (263380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270942698b9e9bf39ad171b35eb2501688e1054401544ed2f8a80d2b965aa4d9`  
		Last Modified: Wed, 29 Nov 2023 02:16:25 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746437e2b6fc08e52f61274104099bd5e1072f61dc24d673eb9311b6c3ceb512`  
		Last Modified: Wed, 29 Nov 2023 02:16:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b641bce141ed7afa022a823289eb3c0a7072483475744b72aad4e7b8ca6b860f`  
		Last Modified: Wed, 29 Nov 2023 02:16:25 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad90f42c1ea2fa6a3e0409aa7c8132f0741281b58f96100a5c19a9ec69120313`  
		Last Modified: Wed, 29 Nov 2023 02:16:45 GMT  
		Size: 199.3 MB (199278431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57cd9746262aaacef8eeaf470546ab8e2f0f6e0c0d820fb3bd9321171b1d3f4`  
		Last Modified: Wed, 29 Nov 2023 02:16:25 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull openjdk@sha256:9378d641bc6e05808e2b81bb51bfe1dd7fafe7f1fa8b5874466ef2feb7c8207d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2257410535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df81daf0b9e717d531f89ac2bf3b81a7b906795195f29cbc7efc2dc53d756d5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 05:21:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Nov 2023 05:21:27 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 16 Nov 2023 05:22:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 29 Nov 2023 02:13:12 GMT
ENV JAVA_VERSION=22-ea+25
# Wed, 29 Nov 2023 02:13:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/25/GPL/openjdk-22-ea+25_windows-x64_bin.zip
# Wed, 29 Nov 2023 02:13:14 GMT
ENV JAVA_SHA256=3fb62ee630aa69a8ca5c7a2734a69e9fcb251519872ebca5eb03f64f60f90f66
# Wed, 29 Nov 2023 02:14:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 29 Nov 2023 02:14:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93b4cb5d6725beac934401f77fbf989141c12afa232cff1f25429b1a301ba73`  
		Last Modified: Thu, 16 Nov 2023 05:26:50 GMT  
		Size: 442.0 KB (441969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22088bf48f3bbce80960887fe94d86c11b50b864e902347298416ae9c621501`  
		Last Modified: Thu, 16 Nov 2023 05:26:50 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8f6249f95be0911abdfd12a1f9bc8f3dc024f415c40647b843b72d714e2530`  
		Last Modified: Thu, 16 Nov 2023 05:26:50 GMT  
		Size: 257.3 KB (257301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638025c50dd2d65eeeeda4c66fb5c5d8769157367c323f8401104cb08a223033`  
		Last Modified: Wed, 29 Nov 2023 02:17:08 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdf7ef05d18174c551d292e22aba2ba92f471ff441523fb7e07a6b6fc5c353f`  
		Last Modified: Wed, 29 Nov 2023 02:17:08 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27e191016df84b3e3155617dd2a8cad98f3bafad21f8165bbb2ca4e092d69b`  
		Last Modified: Wed, 29 Nov 2023 02:17:09 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a92489c140f6e264411d62c4a28bed57a30b99200054cf49a5b38b8aebfb43b`  
		Last Modified: Wed, 29 Nov 2023 02:17:29 GMT  
		Size: 199.3 MB (199271342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e855d831f46b50a57fdfacdc8ddff115a224387da6d7d929d4d065a08baad2`  
		Last Modified: Wed, 29 Nov 2023 02:17:08 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
