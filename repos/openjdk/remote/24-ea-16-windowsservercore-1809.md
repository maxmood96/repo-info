## `openjdk:24-ea-16-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:1f40f3bb6a7a93b4ecfc963cf8a225588543b42c827743a93181270ed1254b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `openjdk:24-ea-16-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull openjdk@sha256:5272bca9b2b488e059b3c4be361d2f48c74ec33ca82fee69944573d0151c589a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1928904789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1736ffa87c50a303e6ef4d022486f6c473a358923f0ad9320bea5d02d4e319e9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 20 Sep 2024 17:57:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 20 Sep 2024 17:59:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 20 Sep 2024 17:59:20 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 20 Sep 2024 17:59:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 20 Sep 2024 17:59:31 GMT
ENV JAVA_VERSION=24-ea+16
# Fri, 20 Sep 2024 17:59:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_windows-x64_bin.zip
# Fri, 20 Sep 2024 17:59:32 GMT
ENV JAVA_SHA256=842becbcc452ec5681e3bdc32d3aaa18634d97d24b9e5c3b49b221f30e9ceb0f
# Fri, 20 Sep 2024 18:00:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 20 Sep 2024 18:00:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d716ebc255dc8a277e218b3228b5ba7dd6ea0588720eaab89d252b55f13ae9f9`  
		Last Modified: Fri, 20 Sep 2024 18:00:16 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb385430d7387d6f6a3aea2ac118424af5c69073120dfd5c4114521b214a420c`  
		Last Modified: Fri, 20 Sep 2024 18:00:16 GMT  
		Size: 330.1 KB (330107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f377b85172b5fef6052e2ae3457904c46d21c0fb4ae6478aae7fbd70fa5a43e`  
		Last Modified: Fri, 20 Sep 2024 18:00:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b8bf9d48d88d50c42351c3c16f854ef0ee56cdc667a897f9bc76c0f7bd80b1`  
		Last Modified: Fri, 20 Sep 2024 18:00:16 GMT  
		Size: 290.5 KB (290538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f998ab64da78607508c97a0615894d4e1372f7e56b0d9a1fb57d25d47ac93c92`  
		Last Modified: Fri, 20 Sep 2024 18:00:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84c982c2c3f0b681aafb046538fcbd0ce1058cdada710d092477e589aca1394`  
		Last Modified: Fri, 20 Sep 2024 18:00:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a8eb707275aabe9be794bc0ffa585446403779562b16acb601a489fc55752`  
		Last Modified: Fri, 20 Sep 2024 18:00:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d29119f6baa95f8f69e392135922c8f77fc484559a510af39a12e19ccb899e8`  
		Last Modified: Fri, 20 Sep 2024 18:00:25 GMT  
		Size: 208.0 MB (208008037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc16aa62d37f76a3fe2f8c91bd6909582a3c16bd249931e53c1c717b73b2a11`  
		Last Modified: Fri, 20 Sep 2024 18:00:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
