## `openjdk:24-ea-18-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:d7ce73a57b8c768bbf2fc0c59c1fd6eb37714d1831c3baaa9f3588967e58f081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `openjdk:24-ea-18-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull openjdk@sha256:79dbaa720abd644ddd5904f923d3a99ccee5c0c2e9d57405a4f2d88fb7a8f2cc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2008540931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc46c26c6abb23300c3bb417c915bd518f02a768de4a7e1c11bcc9fe226ac619`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:12:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:13:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:13:20 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Oct 2024 23:13:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:13:26 GMT
ENV JAVA_VERSION=24-ea+18
# Wed, 09 Oct 2024 23:13:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_windows-x64_bin.zip
# Wed, 09 Oct 2024 23:13:27 GMT
ENV JAVA_SHA256=6146921a840c402763aa710b209d872b2b91ba63221f33e494fa1312cb2a706c
# Wed, 09 Oct 2024 23:13:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:13:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea4cded6c51c5d2de16e44113ff7e81d0b6960159733614efdc2d93ae10ab3e`  
		Last Modified: Wed, 09 Oct 2024 23:14:00 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bba16e12a30a7b77d45ced1f49d077367bca22fa9cc8098706720433ce0820`  
		Last Modified: Wed, 09 Oct 2024 23:14:00 GMT  
		Size: 482.4 KB (482435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17799a4f7c807fc3a5408cf3a69c4c9d15cd5debe2d730f800469b4b42c023e4`  
		Last Modified: Wed, 09 Oct 2024 23:14:00 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dc4dc74b352404e14b84de5256984192d3b36ee6ad1fb5cbafcc992faba9d5`  
		Last Modified: Wed, 09 Oct 2024 23:14:00 GMT  
		Size: 336.5 KB (336456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31ea4e4dab7f2bbcf3c63c31bf2b104b9cb133a9dc3e4b816e6a51527800469`  
		Last Modified: Wed, 09 Oct 2024 23:13:58 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da998d6def0f2762b760ef53765116d68a7c689499a24b70b447ac457ef48e81`  
		Last Modified: Wed, 09 Oct 2024 23:13:58 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be8a10348dc064109060da2dff8cf8c6ab31113e185801a62f8fdfff74867d7`  
		Last Modified: Wed, 09 Oct 2024 23:13:58 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3a602efb5e96a3d938a222737edee8a840422a74fb4ad710a29952e6b1fbd4`  
		Last Modified: Wed, 09 Oct 2024 23:14:09 GMT  
		Size: 208.4 MB (208372577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8deec14057ccff968cac7027293c5a97376fad41faa69503f99d3df8d4f8da`  
		Last Modified: Wed, 09 Oct 2024 23:13:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
