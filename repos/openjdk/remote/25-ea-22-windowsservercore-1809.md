## `openjdk:25-ea-22-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:964058e006d7ab27d265ec60f58e6160d458dcf55c91e5fc94fe9d5c0016cf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-ea-22-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:54090a5ef369c7d42a77a1fedad0cb9147c2f3bac8b233fb1b71856bca79f43c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2375005139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4228a207bf21cc8502ebd19424f0879d342b2d3038aed09f79f9a2f25e4227e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Mon, 12 May 2025 19:12:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 May 2025 19:12:29 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 May 2025 19:12:29 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 12 May 2025 19:12:36 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 May 2025 19:12:37 GMT
ENV JAVA_VERSION=25-ea+22
# Mon, 12 May 2025 19:12:38 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_windows-x64_bin.zip
# Mon, 12 May 2025 19:12:38 GMT
ENV JAVA_SHA256=8b16ab02467967b98cf7d8743da9c9688d3ff39b4a693b66b6d9fe84cc0bb55a
# Mon, 12 May 2025 19:13:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 May 2025 19:13:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f5267256fed79be05b2ef46ceaf13a089dd34bb61f4089dca6b316a4397661`  
		Last Modified: Mon, 12 May 2025 19:13:11 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e9a85db0ce624d463535a0953cbe1d35ff4ab69d6a845bb14ad713db4f95bd`  
		Last Modified: Mon, 12 May 2025 19:13:11 GMT  
		Size: 367.8 KB (367841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1a14251df0a7ade3cb63071c848fef6e4e1d4dd011b63237493599157a7ac0`  
		Last Modified: Mon, 12 May 2025 19:13:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd79b955cae5c8c598ae988e0ce0f715fc5f6af58f965d7bceaf6c87c9f9e46`  
		Last Modified: Mon, 12 May 2025 19:13:11 GMT  
		Size: 348.2 KB (348244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c4b485942ecc306d6f19dfbb24e7326850201de420a30b19e84fde604dc6eb`  
		Last Modified: Mon, 12 May 2025 19:13:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6815cc2d9d11384351d45521e0de357c46fdf69b9d6402922ce7e78ad6fbd3`  
		Last Modified: Mon, 12 May 2025 19:13:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0045d82500993210d43df888cecf2ce3d395be377c1469e99af50f504bf903d1`  
		Last Modified: Mon, 12 May 2025 19:13:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ef18d48e3701e589cc59c573a1f96639c3d5b214ffa35032b85a92d605ac6f`  
		Last Modified: Mon, 12 May 2025 19:13:20 GMT  
		Size: 208.8 MB (208755511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c6dc09d151f3c310a77916774614b8e0793bdff641956dfa0ae08844fc2389`  
		Last Modified: Mon, 12 May 2025 19:13:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
