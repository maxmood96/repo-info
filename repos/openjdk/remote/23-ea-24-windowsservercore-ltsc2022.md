## `openjdk:23-ea-24-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:bce043f348f6113c3632a9a4dd6689d6d3be9d2265e316d1de35ee1698681464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `openjdk:23-ea-24-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull openjdk@sha256:cd5a6e78593feb64d508e55f17826c163104b018173feddc429c8c42c562c6fd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318969321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0bf987e88bea298eef72356515c1fef7cff168bb168aa00f2094233db55676`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:00:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:01:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 29 May 2024 23:01:59 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 29 May 2024 23:02:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 29 May 2024 23:02:06 GMT
ENV JAVA_VERSION=23-ea+24
# Wed, 29 May 2024 23:02:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_windows-x64_bin.zip
# Wed, 29 May 2024 23:02:07 GMT
ENV JAVA_SHA256=d1ca7c4de58322ccecc8598cbfb62a4585ee958e91b66562923df1eac562e816
# Wed, 29 May 2024 23:02:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 29 May 2024 23:02:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413bcf516c2ec3d5fe089c371d9d5c93ff914a027199b94709100a88d5bc016a`  
		Last Modified: Wed, 29 May 2024 23:02:42 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1584f9981234827c702a93f94d35579780bc4e7b3cb3437a20a49bf6d68ca7`  
		Last Modified: Wed, 29 May 2024 23:02:43 GMT  
		Size: 350.5 KB (350512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c07b90d1a62dff46346c8f4be762bf79a031472b9ce03d6837cc880c071a44`  
		Last Modified: Wed, 29 May 2024 23:02:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96922538905ab925e2dc24c4c60c88f5afb2cd228e1847fd9e7c3e8a3dace89`  
		Last Modified: Wed, 29 May 2024 23:02:43 GMT  
		Size: 300.6 KB (300612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4489f9cfc262ad3d0371530b8dc8bf712dcd8374e6e5a5826e3c8038c95c5c4a`  
		Last Modified: Wed, 29 May 2024 23:02:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adaaa63d0aef27f3830c45ae4989c2e800966925b75ce9a7e63f7dbfbb001d2`  
		Last Modified: Wed, 29 May 2024 23:02:40 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3b6d7df801e1b192b45ff9d057d259a6d3005aadb9f8bdb6117f1bc5db7057`  
		Last Modified: Wed, 29 May 2024 23:02:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320c9cd30d8c1b6e3e58c513adf00d6936165af12f9ff617e95e5839880f3c76`  
		Last Modified: Wed, 29 May 2024 23:02:52 GMT  
		Size: 205.6 MB (205639057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a444a778f7d9c2fed47ddbf5aeaaa216a03359cfd943892afc0230ea8fb8b5c`  
		Last Modified: Wed, 29 May 2024 23:02:40 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
