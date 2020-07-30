## `openjdk:8-jre-windowsservercore`

```console
$ docker pull openjdk@sha256:fb7d8f77965b56b0daf50122746361d0913379fa1c5619c79978888ca07c0ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64
	-	windows version 10.0.14393.3808; amd64

### `openjdk:8-jre-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:428901eef07a899d28da59b723138dee37aebb6667361e2413bbb0c8beb2b3c7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2361468972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d5d379e8ba521ea5bffccd33c2e13b4cbccca5b2a4bc84e3ea9c75dcf6c0d0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 02:27:30 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 29 Jul 2020 01:34:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 30 Jul 2020 22:15:58 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:20:52 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_windows_8u265b01.zip
# Thu, 30 Jul 2020 22:21:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:9df9d9d4f1a50ee68e53390188a27d433831832a28f411a3139d70477d10675d`  
		Last Modified: Wed, 15 Jul 2020 02:53:31 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b3d7034be591a9d090e50c29e82c24fab7c18bfcca00ed67cdb92fa16b819e`  
		Last Modified: Wed, 29 Jul 2020 01:54:56 GMT  
		Size: 9.2 MB (9158120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e1a5c991cbf6c27388f85277556e3cd12c4994b2a3818ddd36a50ea98f5f39`  
		Last Modified: Thu, 30 Jul 2020 22:27:15 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb35349a9c20e03a5a733b16b54b918547b6b18d48597d2046a6abff69b60a63`  
		Last Modified: Thu, 30 Jul 2020 22:28:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0201e03e05415384642ed4745e12a826d2bae97a51287786312ab5d54db590a3`  
		Last Modified: Thu, 30 Jul 2020 22:28:50 GMT  
		Size: 42.1 MB (42113992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-jre-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull openjdk@sha256:88829cde8a4af8bf7d29e725ad91cfb0904f8c3de97e3d7b56f879015f3f552f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5794572006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7475b1dfc3e6192ce957cc57293874752e4a6cbb0df53b3f813fe957a31696b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 02:29:56 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 21 Jul 2020 17:29:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 30 Jul 2020 22:17:24 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:21:43 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jre_x64_windows_8u265b01.zip
# Thu, 30 Jul 2020 22:23:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a507ee4c5f1710265ef802239c6b751e4038de0880d1199939f60e9a55b852`  
		Last Modified: Wed, 15 Jul 2020 02:54:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b0899d9cbfdc8ef5b7419fd7d8f190d7b9957f1c89fe3d9e4958a99f059352`  
		Last Modified: Tue, 21 Jul 2020 17:43:33 GMT  
		Size: 9.9 MB (9863224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a9d7deb47074f873005657e1bf1c8d2655bbe22a4e592813cabb086d448c2f`  
		Last Modified: Thu, 30 Jul 2020 22:27:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0affa7a5d9fc6dd3f980491d666e0224ada9ae6e38d8ed748ad31197456058`  
		Last Modified: Thu, 30 Jul 2020 22:29:01 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3532976e6c51c8b82a929dc68f8369621be87c505e7b9e8aa28a5f2bc525d7a9`  
		Last Modified: Thu, 30 Jul 2020 22:29:09 GMT  
		Size: 47.2 MB (47242170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
