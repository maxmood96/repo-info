## `openjdk:24-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:ea78a635dcd173cefcc83e685e0ad794b5a9bfffa4d3876c763cdc08f5fde3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:24-jdk-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:2737b5eb46ab8cc0b62e0faba69b98458bb2d3eee931f51b91a32351c2f192fd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2223816769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d070d76a513b5e15ee4a51d2635ec51015e63e7a0125cc1f4f78ea9378148712`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Sat, 14 Dec 2024 00:29:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 14 Dec 2024 00:31:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 14 Dec 2024 00:31:12 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 14 Dec 2024 00:31:20 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 14 Dec 2024 00:31:21 GMT
ENV JAVA_VERSION=24-ea+28
# Sat, 14 Dec 2024 00:31:21 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_windows-x64_bin.zip
# Sat, 14 Dec 2024 00:31:22 GMT
ENV JAVA_SHA256=ea0199fbcac35f83c9729678556b6d924f9e88b2a0669d982af3dc0cd06c3c84
# Sat, 14 Dec 2024 00:31:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 14 Dec 2024 00:31:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33023972992ef5a52a051cd19be54c9c98412dc74da4e4ad7beaffbc570ebe91`  
		Last Modified: Sat, 14 Dec 2024 00:32:02 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fd8da4cd1e5aec397fa3aea6090911bc72a3c62820c269c27652b2b6c4952a`  
		Size: 475.7 KB (475717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20ef923bbc318a5914c206a2cd0b38b9bfd0d4ab700a2b749d6daa2ff054f1`  
		Last Modified: Sat, 14 Dec 2024 00:32:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3a5f94574e26ac4d18bddd2b0e52b2613c203ff2f0139fc891cc0aa51b9e07`  
		Last Modified: Sat, 14 Dec 2024 00:32:02 GMT  
		Size: 331.5 KB (331531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9722dcb51de3386fa565a6bbbe0f8b0cba2f76bd95c789e3ed47b55a95df56c`  
		Last Modified: Sat, 14 Dec 2024 00:32:01 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925db4ba36f25e02e1813cc7d9a531a567a21a95cbbf20d8fa3452cfcd39bf9f`  
		Last Modified: Sat, 14 Dec 2024 00:32:01 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aecd67b1155df95fb4bdaddb4d35bebab7b9ed347463b89a7b1e9e7b5bd665a`  
		Last Modified: Sat, 14 Dec 2024 00:32:00 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c1b92c000cfe5f9211dc6ea61f70f78f3c1899a21c3a3592bd7c5e00f50692`  
		Last Modified: Sat, 14 Dec 2024 00:32:12 GMT  
		Size: 208.8 MB (208831528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47c3131d69a79b135c63f8e128205ee1d565e98e618692e9a154c1032d6e763`  
		Last Modified: Sat, 14 Dec 2024 00:32:01 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
