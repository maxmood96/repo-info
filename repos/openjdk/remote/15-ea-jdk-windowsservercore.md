## `openjdk:15-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:5c8b90da5d097519230c906ce0a2d8e16db044a8abfa862748a0948e0e2b4db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64
	-	windows version 10.0.14393.3630; amd64

### `openjdk:15-ea-jdk-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull openjdk@sha256:fb8a8c9a208f83a5577f74de3f3632e2113bc64553ddeaaa3dc88b6776a8a085
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463595765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534381f54abd9ee5d832c1198de43c69235a220dd04fa76b8aa65497ef89670c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2020 21:33:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 14 Apr 2020 21:33:27 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 14 Apr 2020 21:33:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 07 May 2020 21:15:20 GMT
ENV JAVA_VERSION=15-ea+22
# Thu, 07 May 2020 21:15:21 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/22/GPL/openjdk-15-ea+22_windows-x64_bin.zip
# Thu, 07 May 2020 21:15:22 GMT
ENV JAVA_SHA256=df01fe6b5cfa1ec43cd3754d1e76723ab1c6041283b369d2b4e5b7182e9fbaec
# Thu, 07 May 2020 21:17:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 07 May 2020 21:17:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de6b6e18c57fb613f91d77606e5355771830df52cc6b00e32e74a46a7449d5b`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 4.7 MB (4670665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac510bfbe15bdc6d786e0d3d1e28704fc631e945bcce42fb963d86c2f56d0fd8`  
		Last Modified: Tue, 14 Apr 2020 22:15:54 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0176aea199d3313340042e173fe6b28bc5a463a889d351a42f25db76d678ebf6`  
		Last Modified: Tue, 14 Apr 2020 22:15:55 GMT  
		Size: 295.7 KB (295672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514284b9c18cda501cb27c85bf13fb21bae10a8020de77b55539534a6488d191`  
		Last Modified: Thu, 07 May 2020 21:26:23 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810ca664d07a17d47309349fabced2d13724b8e8f2da20d7d7e71b6b30662078`  
		Last Modified: Thu, 07 May 2020 21:26:23 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040c88cf3e05cf1b90fbaf339c58f3506b917d4d880aee1aa490de36f093df13`  
		Last Modified: Thu, 07 May 2020 21:26:23 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2842abf9b756ce74e70cc84432249eafaa1d6700a4246f91f3bbac8161e0d22`  
		Last Modified: Thu, 07 May 2020 21:26:42 GMT  
		Size: 187.9 MB (187915374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f276c2a33a83ab4d83e652b2453454cfd417aa9d111ca575fafcc7f690605`  
		Last Modified: Thu, 07 May 2020 21:26:23 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-ea-jdk-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull openjdk@sha256:52131ca976fd83ad09e7450b498da4cdce62802db16b9b766304e76c651c415f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5936301056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95e78bd99d1e133863c37c9a3950de0afd9e4c474706234462928b3479038f7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Apr 2020 21:35:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2020 21:37:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 14 Apr 2020 21:37:13 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 14 Apr 2020 21:38:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 07 May 2020 21:18:02 GMT
ENV JAVA_VERSION=15-ea+22
# Thu, 07 May 2020 21:18:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/22/GPL/openjdk-15-ea+22_windows-x64_bin.zip
# Thu, 07 May 2020 21:18:04 GMT
ENV JAVA_SHA256=df01fe6b5cfa1ec43cd3754d1e76723ab1c6041283b369d2b4e5b7182e9fbaec
# Thu, 07 May 2020 21:21:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 07 May 2020 21:21:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ac0134cee91589d04e97f11994235cce86faef5c581d15f2e143ecb90e92572`  
		Last Modified: Tue, 14 Apr 2020 22:16:36 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7792b001970c03ccacbdc7259d0133f320d88e7fdd9394b9c70fe73808fe3ca`  
		Last Modified: Tue, 14 Apr 2020 22:16:39 GMT  
		Size: 5.4 MB (5386185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca3b2979cce17b2f697228c6fc457c3e7099847025fa3aa0cc258fba5a84f6b`  
		Last Modified: Tue, 14 Apr 2020 22:16:37 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99af87d48adcdc7e4a329d2b4d9e50fe2ee23d2596b256f156fc562bb7aba5b1`  
		Last Modified: Tue, 14 Apr 2020 22:16:39 GMT  
		Size: 5.4 MB (5370916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cc536a8386f0842cfe49365e76150bc6f5b403ad831d5c509e93678980cece`  
		Last Modified: Thu, 07 May 2020 21:27:03 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ea231125b18e4dd03946da4a145356078c8ae78a70872a40f573d270b5722c`  
		Last Modified: Thu, 07 May 2020 21:27:02 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3322ce017a8d0174e023e62876fd777be64ae5c7f3428932a32a6948e171c5e5`  
		Last Modified: Thu, 07 May 2020 21:27:02 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f1d142b9cabebc78e04d2d1efa6cfc9a340d39575b35f79a2e18fef73127d4`  
		Last Modified: Thu, 07 May 2020 21:27:24 GMT  
		Size: 197.5 MB (197469507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eb3beee28970aa917f7f9f02f1bd42acf9e2f2d38e44852c4247f72a462ae2`  
		Last Modified: Thu, 07 May 2020 21:27:02 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
