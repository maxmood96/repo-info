## `openjdk:25-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:af6d891be93dc5d78467bf206c788b0c773ff395f5b846264a4371b3a878ef3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `openjdk:25-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull openjdk@sha256:a8c045e18efdfef509843c78786c9df99d3e985aab677127931b1d37f69449ea
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394141875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7367bdef89c0a64d3c3e1dbb3525e79dd4dba154f5df61af3b7a7d744eea02a7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Fri, 23 May 2025 20:03:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 20:04:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 23 May 2025 20:04:18 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 23 May 2025 20:04:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 May 2025 20:04:26 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 20:04:26 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_windows-x64_bin.zip
# Fri, 23 May 2025 20:04:27 GMT
ENV JAVA_SHA256=2a8b2ea51b3b0b3751867a3117e7fde1235189e6d7601f5ffdb9b9160b270bf2
# Fri, 23 May 2025 20:04:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 May 2025 20:04:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9943b418bf9ba8a51291773118fc42a541e34c1f4fab78a959894cf3d229c79`  
		Last Modified: Fri, 23 May 2025 20:04:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0500c85686b5f06b955c9bf960500d90550d0ae49d9cc7c40529a50b8934f3`  
		Last Modified: Fri, 23 May 2025 20:04:55 GMT  
		Size: 364.8 KB (364752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c6af7931fce13ebf09dd412719b0c8f1cbe3ac08e344e29bb910bb28683282`  
		Last Modified: Fri, 23 May 2025 20:04:55 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6829592eda084943395b0537fade00b78048df09b1d5b7fc4184cb0150a44098`  
		Last Modified: Fri, 23 May 2025 20:04:55 GMT  
		Size: 341.4 KB (341375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382562d7a098abf3220647f7f930d7d1dc1de751a4c9785de53d3b7906c0a682`  
		Last Modified: Fri, 23 May 2025 20:04:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c900365e44f0d2921f75484b6b3da31a3c92936c7edf70837b0dd95c5307c5d`  
		Last Modified: Fri, 23 May 2025 20:04:54 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbb806032cc5270aa321033b0edfe5846a33208ac4b4e5855e70a033974f14e`  
		Last Modified: Fri, 23 May 2025 20:04:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8d090f7b049f0293a4344207801671b9f04d4cf78689b9a45adaf9e9d32b24`  
		Last Modified: Fri, 23 May 2025 20:05:05 GMT  
		Size: 209.7 MB (209710512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881fd87838d847d57f6386bb83cb105696e72ebdd7e1aa83bc3730c43d2473d0`  
		Last Modified: Fri, 23 May 2025 20:04:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
