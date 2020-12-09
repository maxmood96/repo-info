## `openjdk:15-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:2a7c041613f3cb38e3bc0a8869e154b26f54543797b175ec4b8f3a442654dc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `openjdk:15-jdk-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull openjdk@sha256:d2468598629140cb30edf61eedd304c755deb7d4bd982077090819e97cff29d6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2596492998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f37ab6461dcc58344f708e17cafe67983977172a0b7688358e65cb19dc2f70`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 13:30:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 18:50:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 09 Dec 2020 18:59:49 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 09 Dec 2020 19:00:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 09 Dec 2020 19:00:10 GMT
ENV JAVA_VERSION=15.0.1
# Wed, 09 Dec 2020 19:00:11 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_windows-x64_bin.zip
# Wed, 09 Dec 2020 19:00:12 GMT
ENV JAVA_SHA256=0a27c733fc7ceaaae3856a9c03f5e2304af30a32de6b454b8762ec02447c5464
# Wed, 09 Dec 2020 19:02:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Dec 2020 19:02:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a4372d14958dc8a7eaaace9e4774e7f1db524da5eb4474b5e46738848a3a61a5`  
		Last Modified: Wed, 09 Dec 2020 13:54:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935e3005fe76a11e222d9322d452d314edc4ba767499cc7c7e9f7cff154513fc`  
		Last Modified: Wed, 09 Dec 2020 19:32:28 GMT  
		Size: 9.2 MB (9236222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bf3750bea96f7ea8b6aa19ff70ed12a705d91d16dcc1fb5a3c85f5730f5344`  
		Last Modified: Wed, 09 Dec 2020 19:34:46 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90942bd8683cbd3eef336f8314d215359de32f896e8e2efbeb1f697e0ff9c44`  
		Last Modified: Wed, 09 Dec 2020 19:34:46 GMT  
		Size: 288.8 KB (288801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff7b63af5b94beea5760459ffac1b1967daa2c9780e5eb2eb77b8d8aa15ba67`  
		Last Modified: Wed, 09 Dec 2020 19:34:43 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915603362ace290ac140d8453a67924acb5ac93097c101c4344c37ee9af7adfa`  
		Last Modified: Wed, 09 Dec 2020 19:34:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e2a285389d2f3c56f58a06b3ebf54c6bc94c1673186494b25aca1802fa3ab4`  
		Last Modified: Wed, 09 Dec 2020 19:34:43 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b0bcfd3149e1d06b243441dcaaf06c6a28b2159c8b1e06cd03a19aee888f5a`  
		Last Modified: Wed, 09 Dec 2020 19:35:04 GMT  
		Size: 196.1 MB (196086698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5467d9ebf6c327b0799032c39ffe0264afde65a86c4fa0fd9aa2501acf2fcb`  
		Last Modified: Wed, 09 Dec 2020 19:34:43 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
