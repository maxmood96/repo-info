## `openjdk:24-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:c16be882fd7ebef02b091b95308a0457dfb2884470bc3edb3524a6dd455caaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:a00dfee83acbfc93ecc4649c89628ec0627eacda6aa0563e8856ecfedb1bbfa8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2427962910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503f0d557140ecab09bb5db3bbfe48df6266b2073a070c6a853f39d13fb0bed9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:15:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:16:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:16:53 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Jun 2024 18:17:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:17:13 GMT
ENV JAVA_VERSION=24-ea+1
# Wed, 12 Jun 2024 18:17:14 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_windows-x64_bin.zip
# Wed, 12 Jun 2024 18:17:14 GMT
ENV JAVA_SHA256=84640da466dc6c7af5dbd523e321f5cfef6b81a434c1558b43633e7485da95f7
# Wed, 12 Jun 2024 18:17:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:17:50 GMT
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
	-	`sha256:559b7a7993ffd5e1b96aba469916c6d8fabc5ef877eaaba5ba7c3c976f1c42cb`  
		Last Modified: Wed, 12 Jun 2024 18:17:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a4b9104dad18aa6b339c045a214e7337c24343be05fadaff0b8783393e3c5c`  
		Last Modified: Wed, 12 Jun 2024 18:17:55 GMT  
		Size: 475.0 KB (475014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b88b81a77ecb7a8822734017801f1bef0d60eceae01bd8e536f6268c7af7b36`  
		Last Modified: Wed, 12 Jun 2024 18:17:54 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653f4b54e17863fe7d174fb00c45be7f75d07cfb1c73fc4406c1a029b845da52`  
		Last Modified: Wed, 12 Jun 2024 18:17:55 GMT  
		Size: 322.8 KB (322784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc109fce1e7d6d1c7aff0e9598b5497afd5368ffda2a1f28fbd2acfcfeeff509`  
		Last Modified: Wed, 12 Jun 2024 18:17:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9b4a3d65aee8778712b23d5d19e4e16e3c9e0ca21aff1bb9ac6d3501ddc9c`  
		Last Modified: Wed, 12 Jun 2024 18:17:53 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfdefd97289f13704e3fc93f2c87137d5a604cbb4f999fe1fd6b299fd233a45`  
		Last Modified: Wed, 12 Jun 2024 18:17:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7397b9b8e070bc9ad6133b761b3e26a01f2a8a46c763fd5718ce7e148b89b948`  
		Last Modified: Wed, 12 Jun 2024 18:18:04 GMT  
		Size: 206.5 MB (206475972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0dc625f5db20c918bf5322be2af99a668d6084b18a4b3dfc9fb14851a8c218`  
		Last Modified: Wed, 12 Jun 2024 18:17:53 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
