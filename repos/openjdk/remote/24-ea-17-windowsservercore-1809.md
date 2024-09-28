## `openjdk:24-ea-17-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:05ce6cc7d2bc6d6eedf6302747fa649da91570af5f13547ebe56eb4b4ba60707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `openjdk:24-ea-17-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull openjdk@sha256:a1abcd7ac8fee1bc4fc2f22a46792136564a5afa0eb573baf0a35f7121ac11b5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1929304862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29bbf05690f025e76a4ceec4b3e72d5d329d3f34aea043511581fc434ac2a462`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 28 Sep 2024 01:00:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 28 Sep 2024 01:01:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 28 Sep 2024 01:01:27 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 28 Sep 2024 01:01:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 28 Sep 2024 01:01:34 GMT
ENV JAVA_VERSION=24-ea+17
# Sat, 28 Sep 2024 01:01:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_windows-x64_bin.zip
# Sat, 28 Sep 2024 01:01:35 GMT
ENV JAVA_SHA256=bf219cde78b52efb95b3b6fc5e4204bfdaeaaabfac61261ef44b662f774f44a9
# Sat, 28 Sep 2024 01:02:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 28 Sep 2024 01:02:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af1060f2294623cea7608c3c89316d72c5087467a9f2b92a4cfc91f574aa95`  
		Last Modified: Sat, 28 Sep 2024 01:02:11 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e3ea2621ad0eeac60806eacb9d0315cebe14a35ab053f6351a503bb871b2e9`  
		Last Modified: Sat, 28 Sep 2024 01:02:12 GMT  
		Size: 356.5 KB (356520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56916cf9d90b207e2d8bf324d862648bfeb4a9ee7b6c53e4ec145e999f40ac9e`  
		Last Modified: Sat, 28 Sep 2024 01:02:11 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019683ddf3f3c2ddd8c16faebd16acc8fa21bae204dcb4200fa236b8eeee7a79`  
		Last Modified: Sat, 28 Sep 2024 01:02:12 GMT  
		Size: 349.6 KB (349556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3163071c326f0759290635843bb7187478dc1a2edbb6e4771010f52e2420af1c`  
		Last Modified: Sat, 28 Sep 2024 01:02:09 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9154185126530ed4d31a8a48d02cc56d11f899f97948fc6a41f14e43c8403e4`  
		Last Modified: Sat, 28 Sep 2024 01:02:09 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b345a48ca459bcc55db6722f6500b786aec437e35501c458d6611818863db0cb`  
		Last Modified: Sat, 28 Sep 2024 01:02:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8deacdfd9ae78d8e1f10bc459834f7610d432974fba84dac59d8499210b253fe`  
		Last Modified: Sat, 28 Sep 2024 01:02:20 GMT  
		Size: 208.3 MB (208322604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be1e7d3d3dfc44064233726e09b47070646faa9d8ee0f34945de71ed7764d2b`  
		Last Modified: Sat, 28 Sep 2024 01:02:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
