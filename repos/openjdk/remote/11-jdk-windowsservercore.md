## `openjdk:11-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:4238f4d05c7850565e7609efda4f732ebee09fe70d534b0e91d50bedb113e984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64
	-	windows version 10.0.14393.3443; amd64

### `openjdk:11-jdk-windowsservercore` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:f823041570e6c98ac5e86fa2097384e7e2f14eb1518cf34fe6d6b55f61200d76
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2412174902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cc8eb420d0c598e1504b7d5e087236b6a1be81c7489ef05946e79b0ef2f5d1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 01:17:38 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Jan 2020 01:18:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 15 Jan 2020 23:56:31 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 15 Jan 2020 23:56:32 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_
# Wed, 15 Jan 2020 23:56:34 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 15 Jan 2020 23:58:23 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 15 Jan 2020 23:58:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1361e3321e08ed3279942f89e1e0c8e55b80c3557476fbb5f7d09dc69b7e3228`  
		Last Modified: Wed, 15 Jan 2020 02:04:53 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cb5c1399aeffc808a1e0e308439d9cc57968bbd344f0108a94ae421c200ad7`  
		Last Modified: Wed, 15 Jan 2020 02:04:54 GMT  
		Size: 4.5 MB (4546435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117a2905b79606e799609f8d736990ac7004da1dee2a6a3a2d0114bdb244a449`  
		Last Modified: Thu, 16 Jan 2020 00:23:20 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0fb83322a8bc3dcbf8da18048d1d217821bcb6793727ef6b2c7cf8e937072c`  
		Last Modified: Thu, 16 Jan 2020 00:23:20 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b4f8b685f2556a565fa8bd69597855285b056c29da72a37b83447018dd2d87`  
		Last Modified: Thu, 16 Jan 2020 00:23:20 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8fcc7d22592d88b5850019f3b6556aa1c0a35502c5b65b8ba448c63aefb0be`  
		Last Modified: Thu, 16 Jan 2020 00:23:44 GMT  
		Size: 190.2 MB (190210138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b310810289c2ec61f1f03957263e780aeb975a72c03fe7b4edc180794a4db3`  
		Last Modified: Thu, 16 Jan 2020 00:23:20 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:11-jdk-windowsservercore` - windows version 10.0.14393.3443; amd64

```console
$ docker pull openjdk@sha256:5d5a7f833b3bb5b4bd0884d0f7ae67a8c77fdafa768f778f1fa460e9e1102892
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5925378733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0128a0c802d88b6d5985424c22478d9231e634805c1428c62b6d76c132d5c23e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 01:20:42 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Jan 2020 01:21:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 15 Jan 2020 23:58:50 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 15 Jan 2020 23:58:51 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_
# Wed, 15 Jan 2020 23:58:52 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Thu, 16 Jan 2020 00:01:44 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 16 Jan 2020 00:01:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8eda3425549320b6a36c0e2db12648d558a344a9da357393d801d01e306dbf`  
		Last Modified: Wed, 15 Jan 2020 02:09:08 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29348091d9ce947f1938356b82630d7ca42472ba69b25d92567aff11f1ab394f`  
		Last Modified: Wed, 15 Jan 2020 02:09:10 GMT  
		Size: 5.4 MB (5386894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b81e9d57f23ad0b9b849aaee9894cf27057b1d84910595910e6c6ba4af4ed1a`  
		Last Modified: Thu, 16 Jan 2020 00:24:44 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a65d204997043324f2031e1d12061698893310a85b98aae5f115d171717de56`  
		Last Modified: Thu, 16 Jan 2020 00:24:45 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1266cb2343e9b01f936ad299b743dc4adb1ecfa5921d3131d9567876fb4bee42`  
		Last Modified: Thu, 16 Jan 2020 00:24:44 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9152ab12b47f960089df71009cb361d5726ced6af13e577f51dc3e195f1275`  
		Last Modified: Thu, 16 Jan 2020 00:25:09 GMT  
		Size: 195.4 MB (195385374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd118cc89b36a66a9c48bf7c362ceca3c753eaa5c541258062b87c7fd5d8ac4`  
		Last Modified: Thu, 16 Jan 2020 00:24:44 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
