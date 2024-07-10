## `openjdk:23-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:4807bc2827646308f2cbb606029d15847da9e0aa84e2b4790b03fa8011f0c7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-ea-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:4e1e842f450ce0eef4b8c800295097eb478d8d395ef11a649952280142dbb1e4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2445734929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a942a9ceb649375aa173c48a213e3c61be466529e511835a315692069f34df5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:06:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:07:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:07:15 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 10 Jul 2024 17:07:35 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:07:36 GMT
ENV JAVA_VERSION=23-ea+30
# Wed, 10 Jul 2024 17:07:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_windows-x64_bin.zip
# Wed, 10 Jul 2024 17:07:36 GMT
ENV JAVA_SHA256=bbefe5300370b3a67927c127a1e24a08b8cb1dd37d41b428ed931836e092652b
# Wed, 10 Jul 2024 17:08:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:08:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6647603b5c7f0d572320fc36ef2f501213c8065d16f038cd1c1fe5ad73fcb599`  
		Last Modified: Wed, 10 Jul 2024 17:08:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be80ea146e3e32ca53c09c77fc02170bb45f092a774f30c0c3a295e14b78e86`  
		Last Modified: Wed, 10 Jul 2024 17:08:20 GMT  
		Size: 501.0 KB (500990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162bd6dd44d805fc4feebb72a9bd32782e42d65573e4f668db794bb26a1f0c1f`  
		Last Modified: Wed, 10 Jul 2024 17:08:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f0ca540f7acdc2fb13a88ddfc7ee5d9dabbabb43b8959fdc4418fa3e4c00a7`  
		Last Modified: Wed, 10 Jul 2024 17:08:20 GMT  
		Size: 352.8 KB (352840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f6b869b6e8ad447e0d184c87a31cc3a5ccb1e5b0ca1f0faaeff8144dedff5f`  
		Last Modified: Wed, 10 Jul 2024 17:08:18 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbfb2ea0b86a5e8fd25df3f00bcf2a30cc9117e27b8fa35a4709de8f89d8d6`  
		Last Modified: Wed, 10 Jul 2024 17:08:18 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15b8939054c21402a474cf36cb467e09a74aa36ab8a5668c61bb3b971551521`  
		Last Modified: Wed, 10 Jul 2024 17:08:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61853e6f6949f56a1bee9c49d18d75bb3c4f6fab7ea75c53164f7d17912f3bc3`  
		Last Modified: Wed, 10 Jul 2024 17:08:30 GMT  
		Size: 206.4 MB (206443943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b7f2b6adc91d413d91409c38b081606caf3529c0f70439305cff18f3ad4f9e`  
		Last Modified: Wed, 10 Jul 2024 17:08:18 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
