## `openjdk:24-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:e043abd50865536986630fe7ec914011e138fb23e9f39150492d7f7d200437f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-jdk-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:2cb2f938d9f6136ac2e76baa4346b576c9ba326cd68d66e9c34848d57b8a68e6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331793980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48505aa8ce416eeafc0d920a46473bdf6d750fbb1cfd7f0420f56a19e6c7c78`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 11 Feb 2025 01:27:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Feb 2025 01:28:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 01:28:44 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 11 Feb 2025 01:28:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 11 Feb 2025 01:28:53 GMT
ENV JAVA_VERSION=24
# Tue, 11 Feb 2025 01:28:53 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_windows-x64_bin.zip
# Tue, 11 Feb 2025 01:28:54 GMT
ENV JAVA_SHA256=11d1d9f6ac272d5361c8a0bef01894364081c7fb1a6914c2ad2fc312ae83d63b
# Tue, 11 Feb 2025 01:29:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 11 Feb 2025 01:29:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 20:54:32 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e234e6069560f159ad18cc39139f458f581239319eea40597f2911373a9eaf`  
		Last Modified: Wed, 12 Feb 2025 00:09:42 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2140653f9fb175a607f063c88779f5242b16471cf76cb60e6f513820a5221186`  
		Last Modified: Wed, 12 Feb 2025 00:09:42 GMT  
		Size: 341.8 KB (341843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc622ca2797c3c6aad46ee02bb7ce468475c098d9d6942ef9e6e59ba67b8b3a9`  
		Last Modified: Wed, 12 Feb 2025 00:10:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5268ec88d568b0d8a6f11b42b70c591c6183262e30239679ea83d9d7a625409`  
		Last Modified: Wed, 12 Feb 2025 21:01:14 GMT  
		Size: 332.9 KB (332860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e658a8d2f5b66fc17c6e6f7e9847ce162633273aeb13bc6cca8bda0e47ae6a56`  
		Last Modified: Wed, 12 Feb 2025 00:10:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09f8ac2bd7c4e3cc62e6975cbef316afdba7a2056c2713ced314cc7ec8660e5`  
		Last Modified: Wed, 12 Feb 2025 21:53:41 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a995f2596a6a384dbbb1b6db39e9bcb5923d8bbd446fabc52f4d49aca6ac9b`  
		Last Modified: Wed, 12 Feb 2025 21:53:44 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da33fcb981601d6961850ed0130205428b31024e16ab45698808d4f39436ab6`  
		Last Modified: Wed, 12 Feb 2025 21:54:03 GMT  
		Size: 208.9 MB (208899320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6ce2a4d253adf4b3b018a4e70b5d7facdc4e4af8bdcadef2d962b293499111`  
		Last Modified: Wed, 12 Feb 2025 21:54:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
