## `openjdk:25-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:115eb27b3ab04e552eeeb3f05c1269a4786ce1821c3b2812f257a89a8387ff08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:25-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:688ab0752617388c50755343a9af66f9f118cda56ad25bceece7c5b6d03fa1a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2708971131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ff67e6157fefe5aab235549319056de6d26f2702170fd34cf956e39cf77873`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Tue, 11 Feb 2025 00:31:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 00:31:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:12 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 00:31:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:18 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 00:31:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_windows-x64_bin.zip
# Tue, 11 Feb 2025 00:31:20 GMT
ENV JAVA_SHA256=422ffa84afebca61d5ff96e0459231633ad47f082eb11fbecdb64c76e37b35ea
# Tue, 11 Feb 2025 00:31:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 00:31:48 GMT
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
	-	`sha256:01d888f48b270b91ba422532bc2e36ee2c9009a235d31b933572c98fb2a11778`  
		Last Modified: Tue, 11 Feb 2025 00:31:54 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6d45a22f500395beb47e2cb7a4dc7f29a1e447ce85797c4159a693df9d9770`  
		Last Modified: Tue, 11 Feb 2025 00:31:55 GMT  
		Size: 394.2 KB (394200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2eb7def73c0a1a86fddb80a5f0af8612df3ca386325278d00fe8f140af191a`  
		Last Modified: Tue, 11 Feb 2025 00:31:54 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a82330af6585f3125be7439bbfa9509bed31588eab7be0e643bc314eec2739`  
		Last Modified: Tue, 11 Feb 2025 00:31:55 GMT  
		Size: 378.8 KB (378773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbda2a06236f1cefae22bfd35cc52b9fd2b3088850004b86e5b73a42f9fd26`  
		Last Modified: Tue, 11 Feb 2025 00:31:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fa0e475cfce3739a734760a24ab96600b94fb059c433743b787dceec2c25b5`  
		Last Modified: Tue, 11 Feb 2025 00:31:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f516a9976d165910d1d4701490e8f1c8b33267600c632a4af5e9359875cc1c`  
		Last Modified: Tue, 11 Feb 2025 00:31:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e32b4aee8d383ee361871904507d36d3c1a5640b2ea482a9649b5ceed66f8e0`  
		Last Modified: Tue, 11 Feb 2025 00:32:05 GMT  
		Size: 207.9 MB (207912795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14af3433982f0f9353873d19a6be00dbcd17b1b09c03cf9a35f516e89134ddcb`  
		Last Modified: Tue, 11 Feb 2025 00:31:53 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
