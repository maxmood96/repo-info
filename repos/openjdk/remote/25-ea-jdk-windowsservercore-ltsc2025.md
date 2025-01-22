## `openjdk:25-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:623b030e813bc9591933f192399af21db4d4f75761497838fd6eedbc044e8bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:25-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:5f40f071db47b76263e032cd76429532f10566dfb4aec073504829d21e327365
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708805018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466937dc19bcf9f62699d4be4d0f69e647a1f8d65d6097a15c0c94466260f444`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:35:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:35:48 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:49 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 22 Jan 2025 20:35:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:35:57 GMT
ENV JAVA_VERSION=25-ea+6
# Wed, 22 Jan 2025 20:35:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_windows-x64_bin.zip
# Wed, 22 Jan 2025 20:35:59 GMT
ENV JAVA_SHA256=291c57a76ce4ef742a0402b2af6ae2b2eab2614738b9bc0e335ab9d06f105d33
# Wed, 22 Jan 2025 20:36:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:36:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56afbaf5be45e7507490636cd18263219edc7e9cb73565c9c694b852317f17f4`  
		Last Modified: Wed, 22 Jan 2025 20:36:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a4ee573a63f0f5f9c6d7fe32e8b07170b0c7ac306140695d552ba4b9bbbd0a`  
		Last Modified: Wed, 22 Jan 2025 20:36:28 GMT  
		Size: 360.1 KB (360132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2b43ceb41a88ac6395607fe935fada9b9c49d77c8d0586bf1014ebfea3871b`  
		Last Modified: Wed, 22 Jan 2025 20:36:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5d9146e6fb8589506f7d26be1b18f8b949f3ee9a804748cda6c717415fa152`  
		Last Modified: Wed, 22 Jan 2025 20:36:28 GMT  
		Size: 371.1 KB (371125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469074ed00b2a658e733653410f1df20f6443c770cb62b53341e92765616ee0a`  
		Last Modified: Wed, 22 Jan 2025 20:36:26 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec9e88c3ad6f499f3ce418f5ccf2e94e2b32b1b8135c0761fb2328a5dd76b54`  
		Last Modified: Wed, 22 Jan 2025 20:36:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74119d549af5c60266d807dc5a7450ec09aebcdcaa75d40228bee22ff39b23b3`  
		Last Modified: Wed, 22 Jan 2025 20:36:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7caca01e8efce1a580a38b18721cce6328af3e1470345e66773ccf8d8e5c25f8`  
		Last Modified: Wed, 22 Jan 2025 20:36:38 GMT  
		Size: 207.8 MB (207788398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecf26106fa37f3861cfb32d493d7ea79a05d3b05369cc1fb1065989100b443f`  
		Last Modified: Wed, 22 Jan 2025 20:36:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
