## `openjdk:25-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:7bf972d507a25350c7d3d839f6b4663bf22a0454cdfe8994428022f71aa7963c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-ea-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:3995bae6863f529980d80559465051a18c29f26e2393248d7d3286e3a458845f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2360193389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139dcda29592b699634068860908758abd9ea7a5b2ff752c81142755ed1923f6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Fri, 21 Mar 2025 17:16:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Mar 2025 17:17:20 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:17:20 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 21 Mar 2025 17:17:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:17:27 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 17:17:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_windows-x64_bin.zip
# Fri, 21 Mar 2025 17:17:28 GMT
ENV JAVA_SHA256=a095e71a2552995360224643760900b2c44fc91dad10cab9d289bed71fa936dc
# Fri, 21 Mar 2025 17:17:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 21 Mar 2025 17:17:51 GMT
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
	-	`sha256:79207f2177d6845797b0817847078d4d6dd5ea90aab1efeff99a81659263c7e6`  
		Last Modified: Fri, 21 Mar 2025 17:17:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fe4fedb6c8705826bee29c3d281dcbe969a91c6ff312f3d9c56723e19518d0`  
		Last Modified: Fri, 21 Mar 2025 17:17:57 GMT  
		Size: 341.5 KB (341476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6865af3755eadda1958e1e828851c76e29d85609846870f331a044c4e767c2e3`  
		Last Modified: Fri, 21 Mar 2025 17:17:57 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7afc79c6049e83f64448aa2fbcd652435d5bdc7d5b0886c8a9139f90cb800a`  
		Last Modified: Fri, 21 Mar 2025 17:17:57 GMT  
		Size: 332.1 KB (332126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c25587320e34c7c0c2c501042ce24bc5c995d4046d2d297342a9b3eab6508a0`  
		Last Modified: Fri, 21 Mar 2025 17:17:55 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a14a51d5c9dcb38a3e7a985f2757a764a27eadaebb9f9feb198974f71099f9e`  
		Last Modified: Fri, 21 Mar 2025 17:17:55 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb74eb8d91dcd2aa7a44ca646dddf87c181c56b911b795a18fe422c97bd28a`  
		Last Modified: Fri, 21 Mar 2025 17:17:55 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad5da8215fb889f89ff018e86c90b2e160359f111373a6092349f752abf6e0`  
		Last Modified: Fri, 21 Mar 2025 17:18:06 GMT  
		Size: 207.9 MB (207877359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747ebe89f34874a9758188d8399c52b866c267c0a0e2cdb090ff45fc1862e3d8`  
		Last Modified: Fri, 21 Mar 2025 17:17:55 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
