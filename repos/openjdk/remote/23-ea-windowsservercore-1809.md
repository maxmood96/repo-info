## `openjdk:23-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:14ad2d1e2bbd3dbe8a8ae80cb525e62152c21dd2190867c91d79710754f88c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:23-ea-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:d792210fa8ee46d3236504a9b0edf3caa3ce1432b45ee232ed11b35ada253872
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279199367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050a4538564fcbafcef21b86e4cee36002b4b566a3fefff5cdca63f189dec929`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 29 Feb 2024 22:50:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 Feb 2024 22:52:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 29 Feb 2024 22:52:06 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 29 Feb 2024 22:52:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 29 Feb 2024 22:52:30 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 22:52:30 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_windows-x64_bin.zip
# Thu, 29 Feb 2024 22:52:31 GMT
ENV JAVA_SHA256=71a4b8ffa972cd355bf10024250c8f28d6992b430cd294744705cb5ebd2a5a41
# Thu, 29 Feb 2024 22:53:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 29 Feb 2024 22:53:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc08baf1ed8216ca802d7feaad1a6dd6eb25e90df01381e5f9b7af0e92381739`  
		Last Modified: Thu, 29 Feb 2024 22:53:20 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a97d980c6e57e84281601c69cb6a7b97fe86259f65833f72861a311b99f3739`  
		Last Modified: Thu, 29 Feb 2024 22:53:20 GMT  
		Size: 491.3 KB (491252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e0f618abbb34a478a3aadc0b1d05a682eb48a53ea7fa9267453a79810b3eda`  
		Last Modified: Thu, 29 Feb 2024 22:53:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1758018a2f540b6929c679aac245eff91cc26f2d97c2c355873e8d2e67aaff7b`  
		Last Modified: Thu, 29 Feb 2024 22:53:20 GMT  
		Size: 337.9 KB (337932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd17a45e23065742a441bda645d72b26e7e9620f996a2c0338b09f9bc91fab`  
		Last Modified: Thu, 29 Feb 2024 22:53:19 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4399a4b81cc29c5f72ede9afb4feaa4cd16852f42428ec1c7ea44e9da62747`  
		Last Modified: Thu, 29 Feb 2024 22:53:18 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0ee2db1babf7f4eb9e51f7041111928248355eab917cd5302fbc64a407e24f`  
		Last Modified: Thu, 29 Feb 2024 22:53:18 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7416c01d840e96933f93c5165d826696360ab3952c379280bd06dec7df522448`  
		Last Modified: Thu, 29 Feb 2024 22:53:29 GMT  
		Size: 197.9 MB (197913600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3932dc0ae92856a7e8bc5b4c542101ac12e232b7db0efcb06d273688f7fa20`  
		Last Modified: Thu, 29 Feb 2024 22:53:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
