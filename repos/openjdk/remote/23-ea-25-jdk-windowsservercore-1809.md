## `openjdk:23-ea-25-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:ced9c8e1f6d67839a71eb122dbf5bc26cd3867c60812a69b808011340352443e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `openjdk:23-ea-25-jdk-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull openjdk@sha256:9e891e44819141dc7013f7c57d68b5c7a25ddb3083bc3bf98afd09c2cd5037bf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386830973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d28b2645a2f1f85599fb5e01b811666af0bf2daf3582e5c5d4dd9687c91a1fd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Mon, 03 Jun 2024 19:00:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:03:38 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 03 Jun 2024 19:03:39 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 03 Jun 2024 19:04:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 03 Jun 2024 19:04:02 GMT
ENV JAVA_VERSION=23-ea+25
# Mon, 03 Jun 2024 19:04:02 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_windows-x64_bin.zip
# Mon, 03 Jun 2024 19:04:03 GMT
ENV JAVA_SHA256=31f40e7502496063307f37470402eeb3c2e5a3ee3babece396655f9e0056c8b1
# Mon, 03 Jun 2024 19:05:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 03 Jun 2024 19:05:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84bf49e635feeec97c29cb76250f0aa73164a0b775d8bf37fc5f47416d2684e`  
		Last Modified: Mon, 03 Jun 2024 19:05:12 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e142f5cd2963b48de3572e1a5da7b9f93bb508d80e49a9ce22f68b9588d70384`  
		Last Modified: Mon, 03 Jun 2024 19:05:12 GMT  
		Size: 497.2 KB (497199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd67751d4b5e5d8dcb6550d9988a25cfb30f9367ec1a35fadaf6e18fd511f4ec`  
		Last Modified: Mon, 03 Jun 2024 19:05:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d38e15e9df51ca2e7674f67b71b8b48bc9e16ae91f910460fcc68bc9eaa520`  
		Last Modified: Mon, 03 Jun 2024 19:05:12 GMT  
		Size: 311.4 KB (311356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0aa0ccd6cfbf4a22aff98124e3f920108b26cfc4299f6d825a4ffc9f3abe8f`  
		Last Modified: Mon, 03 Jun 2024 19:05:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debe29c46ca1a3eb3015aea711745f4705dab402cff64a0c34b1875364286394`  
		Last Modified: Mon, 03 Jun 2024 19:05:11 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9441508db5c58adce7583f89bf86ae692f1843020f3593ff1f1d8b2b4e8a992`  
		Last Modified: Mon, 03 Jun 2024 19:05:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d748d26448c106e8db20c174d3837f17f18a7836aecdc2bb02d2a612874b58`  
		Last Modified: Mon, 03 Jun 2024 19:05:21 GMT  
		Size: 206.3 MB (206303128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2617f1a68bef8b3abcdcd5b98dfb871f9a902a69d457e2ea1114cdf469ba4b04`  
		Last Modified: Mon, 03 Jun 2024 19:05:11 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
