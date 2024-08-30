## `openjdk:24-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:fbe8b27bce66c7090d593883400ef15675735d44d524a66293259c31889e3cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `openjdk:24-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull openjdk@sha256:ed82f90dbfbb7ff8c7787e18ae80264f4511394c5b179d933b1b87873c7f5682
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2350529662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea63ec57a55b72655b92ba3d991029e796af44147c2754d4b9924cfcee9aeea`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Thu, 29 Aug 2024 21:49:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 29 Aug 2024 21:50:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 29 Aug 2024 21:50:15 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 29 Aug 2024 21:50:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 29 Aug 2024 21:50:22 GMT
ENV JAVA_VERSION=24-ea+13
# Thu, 29 Aug 2024 21:50:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_windows-x64_bin.zip
# Thu, 29 Aug 2024 21:50:23 GMT
ENV JAVA_SHA256=f872535c7185b35e6509c62f7ed7bec65d8f958dc6742e40211244d6964e7ae6
# Thu, 29 Aug 2024 21:50:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 29 Aug 2024 21:50:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b467e0c02cbbda676c75d98c052e6270ed05ecedc18393646e49b76212a34`  
		Last Modified: Thu, 29 Aug 2024 21:50:53 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fee6a81327ebdec77c652ba8f2dcc9cbd4bb8ccf862a57112bdbd973fc58ef6`  
		Last Modified: Thu, 29 Aug 2024 21:50:54 GMT  
		Size: 374.1 KB (374077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89eada4e4f54fbbb366c7eb141560ff65db57bcb3e79788ec65b26a1c8388e0`  
		Last Modified: Thu, 29 Aug 2024 21:50:53 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85ecbb64d94334810cbff732dd9ca0720547ec26ae9e7a257f0b6a16f8d6527`  
		Last Modified: Thu, 29 Aug 2024 21:50:54 GMT  
		Size: 355.6 KB (355623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5199b0150e456cdaa860589b25723a0411bb5c827fd5be806f8b4fabb01f90ef`  
		Last Modified: Thu, 29 Aug 2024 21:50:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833e52106eefe71a62a99e5ace371a68700c3e3614eeac3d22cbdb5fbce78bde`  
		Last Modified: Thu, 29 Aug 2024 21:50:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23cbc7e785340c742a5e1a6cfaeff14db8cfb0e89cb543cab7a005dff975bfd`  
		Last Modified: Thu, 29 Aug 2024 21:50:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636eb131398685303fa0abfd555aa1ec298c41dd3a5a93d12d325e29cde8a0aa`  
		Last Modified: Thu, 29 Aug 2024 21:51:03 GMT  
		Size: 208.0 MB (208027256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c224d174dba7bdd099fff358a76ce0ccb2dd188dead0c3a71bfefdfc17707bf1`  
		Last Modified: Thu, 29 Aug 2024 21:50:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
