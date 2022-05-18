## `openjdk:19-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:7c212ba7315e4b9e8a6c671ff4c3ca6aba8e1c72c3e67ef11a6edecbc3a0bec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.707; amd64

### `openjdk:19-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.707; amd64

```console
$ docker pull openjdk@sha256:41d1ee5436de4a7b3922ee213f8068f20444d1cfc3392b7c8f7949f85ebf587c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2429905498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cafa048b52551658bec7af386d73fb3819940acfd9f7df2a5101e94a7bbbd37`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 15:28:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 May 2022 15:28:56 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 11 May 2022 15:29:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 18 May 2022 01:14:35 GMT
ENV JAVA_VERSION=19-ea+22
# Wed, 18 May 2022 01:14:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/22/GPL/openjdk-19-ea+22_windows-x64_bin.zip
# Wed, 18 May 2022 01:14:37 GMT
ENV JAVA_SHA256=84b71fd73691ab488f8fe238772e16e13563b23351df453e71c9eb34d08cae44
# Wed, 18 May 2022 01:15:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 18 May 2022 01:15:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7320671bb1ef07c493563d61e332d907b7a248c0d182698a877d84e65327b614`  
		Last Modified: Wed, 11 May 2022 15:56:04 GMT  
		Size: 607.9 KB (607907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c59d468f4140dfeb9ca7cccc1a19de4b9dee810da486843372bc823daddb570`  
		Last Modified: Wed, 11 May 2022 15:56:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613b2526877fb3edad53c027ade0fb2feb1ec41cfe4a7bfc4d5d1db891b391e5`  
		Last Modified: Wed, 11 May 2022 15:56:04 GMT  
		Size: 539.4 KB (539446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae2e2227db375917b97104a1e87f1c8db8dfba75cdc5aca40c347499248a7c9`  
		Last Modified: Wed, 18 May 2022 01:21:46 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae54bff88a164a18f0e0c4a123258f891a52d95d0761e7c1679fc142d7ea3ff`  
		Last Modified: Wed, 18 May 2022 01:21:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b5b13c8d88cc71f66eb3d664a9a262cc1c883cdf445b7da64b7ef52a979617`  
		Last Modified: Wed, 18 May 2022 01:21:46 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d8c442a60f5c1bc4b18deb7e376d2dfec328fd77ba5803fda0fdaf02d5ef1f`  
		Last Modified: Wed, 18 May 2022 01:25:04 GMT  
		Size: 191.2 MB (191214391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff90d112cbae829b50d475b8862556802abc0000d87586c3dbe55f104c47873`  
		Last Modified: Wed, 18 May 2022 01:21:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
