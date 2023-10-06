## `openjdk:22-ea-18-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:2111c7ac63c5e7b7f8be3535e48b192103ae37e43d8877ad3e61877ce6d9f11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `openjdk:22-ea-18-jdk-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull openjdk@sha256:6c991eef6547d7c9a985262798fa1d4f1578b05a3a004b61e856434b38db8bca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216366855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f9d52f5c7a367373113f14d9f53c7208c8c2a53e1d3ace6dc0420b56acc9f4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 05:16:37 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Sep 2023 05:16:38 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 13 Sep 2023 05:17:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 06 Oct 2023 19:23:42 GMT
ENV JAVA_VERSION=22-ea+18
# Fri, 06 Oct 2023 19:23:42 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_windows-x64_bin.zip
# Fri, 06 Oct 2023 19:23:43 GMT
ENV JAVA_SHA256=9514da1d60086946d1324cfabda5280213d7243eec44e2268bbbf02248d910ff
# Fri, 06 Oct 2023 19:25:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 06 Oct 2023 19:25:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da151b70a7f82a6d6963a3317229ba06177114b9d44cd362e90207d42aa4d828`  
		Last Modified: Wed, 13 Sep 2023 05:26:10 GMT  
		Size: 255.5 KB (255460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f8ba7984984551020a40f5b8881b3c1fb035e9785ba3bdbae07f7c770a4f6d`  
		Last Modified: Wed, 13 Sep 2023 05:26:10 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e0c6f3841f682fcfe5bcc0fb248fac7844337b14dd92db7132434ac8133685`  
		Last Modified: Wed, 13 Sep 2023 05:26:09 GMT  
		Size: 216.8 KB (216765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546e19438720ca5be9cc6f6ca12dd43dbd0ee51e3d956fa050684eea20145129`  
		Last Modified: Fri, 06 Oct 2023 19:27:33 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1df7a8549db58b678cf0dffe7a47dbf7e0cc16219d70b61bd646b668aea8be`  
		Last Modified: Fri, 06 Oct 2023 19:27:33 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0955a80e4c5c94da0b6a3a76fc08e78ae0edd17619653dcac0a5ccbb7b9fbb70`  
		Last Modified: Fri, 06 Oct 2023 19:27:33 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d90a92e8079e54a9e719807c15fc68d3dcd25cb14c07f21234d870e29be38d`  
		Last Modified: Fri, 06 Oct 2023 19:27:53 GMT  
		Size: 199.6 MB (199556397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659ccf3fd0e7f326819a4feeb79c55112e329af41c1d6d004b1dc0039e08827f`  
		Last Modified: Fri, 06 Oct 2023 19:27:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
