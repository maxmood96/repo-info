## `openjdk:25-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:d2755a8b4c93947f3e93437695948eaa378e5d684a59d7de5ebd235d1b5c7123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-ea-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:251e254dfb9f9a47ec2d7e2c1abedf807c80e05dba9e65dc53a1568e936943a1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2360638175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e311523818ebfce1a8b0ae76be9df1a1336f6fe7dac54b35e65f1ceea52f1dc5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 07 Apr 2025 22:44:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Apr 2025 22:44:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 07 Apr 2025 22:44:58 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Apr 2025 22:45:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 07 Apr 2025 22:45:06 GMT
ENV JAVA_VERSION=25-ea+17
# Mon, 07 Apr 2025 22:45:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_windows-x64_bin.zip
# Mon, 07 Apr 2025 22:45:08 GMT
ENV JAVA_SHA256=46c47281310039b4e8d7e583a1629bfb2ca08a102794c3a68d1f2051101e9f5b
# Mon, 07 Apr 2025 22:45:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 07 Apr 2025 22:45:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f3048ecc78a120590d0dccb41347640d5531608b4d36c7b3d455ef08bc29f8`  
		Last Modified: Mon, 07 Apr 2025 22:45:39 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca03e99a81db423c7d54364b75617d87e5d727d71fb16690ae57d5838fcd91`  
		Last Modified: Mon, 07 Apr 2025 22:45:39 GMT  
		Size: 341.8 KB (341806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cece7347752574d1b62393a40b84e8aa7822efe5a9fee5faf4a43a665e58a97f`  
		Last Modified: Mon, 07 Apr 2025 22:45:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363211d549b6c95ae4168fe1b547472b9f213a63636076e94825152ed653a8e5`  
		Last Modified: Mon, 07 Apr 2025 22:45:39 GMT  
		Size: 332.5 KB (332482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfd5a2e310f8e43fa6a7b87396fd239d2b090111b956f066aaf332ac2b5464c`  
		Last Modified: Mon, 07 Apr 2025 22:45:37 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd9fca6c1f2738ea464a52c498b2a51ae5f84b76a7d865307d1fea122965c90`  
		Last Modified: Mon, 07 Apr 2025 22:45:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e509470d32734352787bcf06d8efae84b3090064e76897c007f6f005f21982`  
		Last Modified: Mon, 07 Apr 2025 22:45:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b125128f74b4bd69deb8bbe829b1933842771faac8c1a3e6598b57b400afe999`  
		Last Modified: Mon, 07 Apr 2025 22:50:19 GMT  
		Size: 208.3 MB (208321416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ae0817d3ae49ef4b81681d2ba90353be4dc790c6d1b3f215cb71cc7c38db35`  
		Last Modified: Mon, 07 Apr 2025 22:45:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
