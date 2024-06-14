## `openjdk:23-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:91798065a043d490c9f16264607aa2469fd1a818787e99858a419333a103a2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:23-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:3763a6c9285b445efdc36021e8ad82060280baf2bbc7a0ea2e4039623c57b039
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2427879216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84964c53d95d3224e6cec3483c18fca9c19681abeb4d72cf1797f8fceeca3fb5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Fri, 14 Jun 2024 01:10:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jun 2024 01:10:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:10:59 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 14 Jun 2024 01:11:17 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:11:18 GMT
ENV JAVA_VERSION=23-ea+27
# Fri, 14 Jun 2024 01:11:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_windows-x64_bin.zip
# Fri, 14 Jun 2024 01:11:19 GMT
ENV JAVA_SHA256=32824da64e6c9cf88cd5a05fe443afcbbc809ef6d31125581adb03c42574a650
# Fri, 14 Jun 2024 01:11:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 14 Jun 2024 01:11:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c7652107e157e4107eec38016399214072b42e76e0fe157b2d85af4dedc827`  
		Last Modified: Fri, 14 Jun 2024 01:12:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21efae21de8ade2039b5a09d51a3dda4f9e2367e120140f3ac207589e78480`  
		Last Modified: Fri, 14 Jun 2024 01:12:02 GMT  
		Size: 473.2 KB (473243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16e2d3367af132dea745e0e930ecb8b20a5824294e38b8978b7901c2f988528`  
		Last Modified: Fri, 14 Jun 2024 01:12:02 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006f5e414a248976f9b1f6969d1f0788def63ec00e55fb81d28bd97d58c57ee4`  
		Last Modified: Fri, 14 Jun 2024 01:12:02 GMT  
		Size: 321.1 KB (321107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0398062330db499c87f9310d404322593c8b45c277b8357097d9260ee7e295`  
		Last Modified: Fri, 14 Jun 2024 01:12:00 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d771f56c9406509f1f0175060772b172e5964589c3f645b5ccc7f87adc3fb`  
		Last Modified: Fri, 14 Jun 2024 01:12:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fcd5c442c08de28ef5a898cbd208258420c2730cab1512777cfb2d26beb01f`  
		Last Modified: Fri, 14 Jun 2024 01:12:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c267bccf70c87c8d6c94cff80e7c2466e9964dd6aec0adda1bd819f515b2c3`  
		Last Modified: Fri, 14 Jun 2024 01:12:13 GMT  
		Size: 206.4 MB (206395910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d885024750fb722fd19afbe1f2a1b502e2e874da59139e8fdf19ba1f2c6819`  
		Last Modified: Fri, 14 Jun 2024 01:12:00 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
