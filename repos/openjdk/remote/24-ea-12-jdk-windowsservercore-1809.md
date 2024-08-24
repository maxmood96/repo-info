## `openjdk:24-ea-12-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:dc1d8ed2b321d7f60c01926dc3a65313975e444cb65f0ba1de3098398df01d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-ea-12-jdk-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:9b0fa610f8586952531cccb7d4e63145523eb08733151d694729c848e5e4c445
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454082538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138870c8073f1cb44e8fe67c97cb1508b66f54b77e26d8e695cad1ad8c068613`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 23 Aug 2024 21:10:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 Aug 2024 21:11:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 23 Aug 2024 21:11:42 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 23 Aug 2024 21:12:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 Aug 2024 21:12:06 GMT
ENV JAVA_VERSION=24-ea+12
# Fri, 23 Aug 2024 21:12:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/12/GPL/openjdk-24-ea+12_windows-x64_bin.zip
# Fri, 23 Aug 2024 21:12:07 GMT
ENV JAVA_SHA256=4e795033e522ad8a7dcff604368b71de74b1481f8d8878b4cda5a7996fec6352
# Fri, 23 Aug 2024 21:12:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 Aug 2024 21:12:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d38875d3b475125af1dd31f647530544339988ce626051c201151eada40ce76`  
		Last Modified: Fri, 23 Aug 2024 21:13:01 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ad13a61d0733650c0a3fd6163c0eee8cec886729317d65179f302712a9ec90`  
		Last Modified: Fri, 23 Aug 2024 21:13:01 GMT  
		Size: 502.7 KB (502736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9fd336ef6f9de138fb232f78ce9e0fdc0c500bdd7d7b5849cc5d702905ab26`  
		Last Modified: Fri, 23 Aug 2024 21:13:01 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ea4fb0a2b177f18f9805b86ed89c85ad6335f3f21f2e58b85410ed7ddea7ca`  
		Last Modified: Fri, 23 Aug 2024 21:13:01 GMT  
		Size: 357.0 KB (356957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7302ac089ca87f42c73eddc05e409c2e8858bf0ad18c728c5065b284c20dd86d`  
		Last Modified: Fri, 23 Aug 2024 21:13:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2687a8b1dca9722b1dcf869fd46816c8b78943a59218d740db779cf181e8f10`  
		Last Modified: Fri, 23 Aug 2024 21:13:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a22226215f3b9b1cdeca70408f715cfc3021ff99e3bc52a3b5e46996d64ffe`  
		Last Modified: Fri, 23 Aug 2024 21:13:00 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8781422c68590818f225d02df93fa7b10fe466f026e7caa80e4edc009182c8a`  
		Last Modified: Fri, 23 Aug 2024 21:13:11 GMT  
		Size: 208.0 MB (208011815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3d7157ac309a20b349f810bfd33f80552bb2f12393c3e614cd307015ee1467`  
		Last Modified: Fri, 23 Aug 2024 21:13:00 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
