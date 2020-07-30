## `openjdk:8-windowsservercore`

```console
$ docker pull openjdk@sha256:6a7119cebddd73a0b54c47865523ed73b7c3c60f8f30d83915a2a1d1bc31d49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64
	-	windows version 10.0.14393.3808; amd64

### `openjdk:8-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:d99607ef0d6f5e17986545159aaf56eb6b0bdc519929898c5a2ed8a233429b26
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2424175150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c3f9f624cc905d60c9a0d01ce6e5dd772096c98d4520466663574d9dc3a0e0`
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
# Thu, 30 Jul 2020 22:15:59 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jdk_x64_windows_8u265b01.zip
# Thu, 30 Jul 2020 22:17:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:9017a5345410bddbfaab10cb6c45fc1191d0c726fac526953a380f9fef689ed0`  
		Last Modified: Thu, 30 Jul 2020 22:27:16 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54831cfeaaa1224017afd33402f0d03d38616b237f20f169bf85c7fc1fee67d2`  
		Last Modified: Thu, 30 Jul 2020 22:27:29 GMT  
		Size: 104.8 MB (104820173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull openjdk@sha256:c311e5c06e49a63299fc09af13611e3e101681db740fe7a710b7e59a906e7cc0
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5857280238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba73e2a444f8a960b02c91f87eca6423ac3d021f6bc8f1984af3aaf434f121ff`
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
# Thu, 30 Jul 2020 22:17:25 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jdk_x64_windows_8u265b01.zip
# Thu, 30 Jul 2020 22:19:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:fff51672568b9096b5e314ec9d18984a143865fa8aa7bbd470f9cf61ed6c6cac`  
		Last Modified: Thu, 30 Jul 2020 22:27:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697a74caca78ff6a56297543303bc982238ba2d9c1c489d2a36948b78a14c5d8`  
		Last Modified: Thu, 30 Jul 2020 22:27:58 GMT  
		Size: 110.0 MB (109950413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
