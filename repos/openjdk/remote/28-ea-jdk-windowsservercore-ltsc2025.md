## `openjdk:28-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:6e0686964863c5d5c4ef9a6543ba99b07efb659731ef4f54cfd69dd3f99089e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:28-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:421decb31cc635e309ad3f8d3ab5acfefbaa523ec23aa62082cdcd71854cc538
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2503407185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101f0539ec18a520156c47334280dd1a4fdc4b4e361bde9f4838e5871f84791d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Wed, 10 Jun 2026 20:32:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2026 20:32:50 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Jun 2026 20:32:51 GMT
ENV JAVA_HOME=C:\openjdk-28
# Wed, 10 Jun 2026 20:32:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Jun 2026 20:32:59 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:33:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_windows-x64_bin.zip
# Wed, 10 Jun 2026 20:33:00 GMT
ENV JAVA_SHA256=4aaad6cb26305877733b973a209216ad1ed529c381dd88c56e3ab87f579f96cc
# Wed, 10 Jun 2026 20:33:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Jun 2026 20:33:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62942753aabfd6992545f04405cbb39eed4237ae5ed4cee184b2f7eb24854ff6`  
		Last Modified: Wed, 10 Jun 2026 20:33:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3789dac8f9c917f9f8a77de757287072987aaa129b4466676d157d16896aac69`  
		Last Modified: Wed, 10 Jun 2026 20:33:31 GMT  
		Size: 366.9 KB (366924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b63f05f064472b2c470b6f8900dd3748f1f7e2c4fed62b87751f6965c956`  
		Last Modified: Wed, 10 Jun 2026 20:33:31 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a08bb8a49a7f5da3876c1243bb2c2adfc6e36414546fec5cf9891a5ea69572`  
		Last Modified: Wed, 10 Jun 2026 20:33:31 GMT  
		Size: 343.9 KB (343880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d3a342c35bf57992160507d034a831b8d650fbecc4928ef4cbad561a328dd3`  
		Last Modified: Wed, 10 Jun 2026 20:33:29 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f7c7203ee1837ca6796925e9c4c7e55c2c1eaf8f555934011a6f036f9b5c1a`  
		Last Modified: Wed, 10 Jun 2026 20:33:29 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4372764e688496bcdc6517ff9be041d13750fb1728600ebc725e2404e4f805`  
		Last Modified: Wed, 10 Jun 2026 20:33:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dbb4a5ec2d34ffa30cc7cc4cdca2c62d41878d6ecaef8fe2784dfe6a685971`  
		Last Modified: Wed, 10 Jun 2026 20:33:43 GMT  
		Size: 223.5 MB (223545651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f1ece0ba7ac763e32f7fbc6626d342c07f4240cc1e9c295bbe708adfd7a12`  
		Last Modified: Wed, 10 Jun 2026 20:33:29 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
