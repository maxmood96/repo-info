## `openjdk:11-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:eea54da76bbff5a87b43ccc8d5a91941095b0fb121539422644e03ec38d034b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:11-jre-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:621f7ee230aef1f1fd2f74c1df2ae29f1aa59d2eef436aa59f7cc6afa25ad183
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363178953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05009f1dbb8e0f638d9c8b06bd1281e3fcc2d446ca1db85c19aa9d404cb3b091`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 02:14:08 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Jul 2020 02:14:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 16 Jul 2020 23:17:59 GMT
ENV JAVA_VERSION=11.0.8
# Thu, 16 Jul 2020 23:33:58 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jre_
# Thu, 16 Jul 2020 23:33:58 GMT
ENV JAVA_URL_VERSION=11.0.8_10
# Thu, 16 Jul 2020 23:34:50 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe72f810946627936fb3059295f72a1745bfc735925259534b9cee6d7543ae4`  
		Last Modified: Wed, 15 Jul 2020 02:49:46 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f857dc923b786b18ab0918e8a0e201ca958973606bc4e94358acc5f3c1ee1d7`  
		Last Modified: Wed, 15 Jul 2020 02:49:49 GMT  
		Size: 9.1 MB (9135283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77e52531a28ad80246272644f3018501be1a8598ecd4ba2b8c828c8cf54345d`  
		Last Modified: Fri, 17 Jul 2020 00:22:26 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86df6d99fbb9bbfa681b81941f5abedef15ba6fc5d00b9a60c52b725ba0dc6f0`  
		Last Modified: Fri, 17 Jul 2020 00:23:49 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df76ae5e8a276747fe7f2bb651627f8ac75fec6e8d48597b899250388ddca76`  
		Last Modified: Fri, 17 Jul 2020 00:23:49 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5487b316a793ccd15d27d231c50888e3a62a54da61fbdb796e241f6cc5362dab`  
		Last Modified: Fri, 17 Jul 2020 00:23:58 GMT  
		Size: 43.8 MB (43845741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
