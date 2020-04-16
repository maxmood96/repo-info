## `openjdk:8-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:f71dfb16857ee6ba28d38a86936c7d444b82520da9b9556f13b15a70fa5fb51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `openjdk:8-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull openjdk@sha256:ee1a9db96788ee5f8474700b16c2f77e8418d9bc59be08e524613f74df8f4243
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5838611521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c672581f83ce848e5f03aa5f3ff2eab7ee1fc8778c5b0b159d1c2176906eccf8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Apr 2020 21:35:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2020 22:05:30 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Apr 2020 22:06:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 16 Apr 2020 01:02:22 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 01:02:23 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 16 Apr 2020 01:02:24 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 01:04:26 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:59e0cf4292e83257e5609e02da1f800e8823e26a3c2e8d7032002e6ae2a7de39`  
		Last Modified: Tue, 14 Apr 2020 22:27:28 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24c3037c3266b54d877359067da7914c2001bc5180c81a37a2a6d03b44dd100`  
		Last Modified: Tue, 14 Apr 2020 22:27:28 GMT  
		Size: 5.4 MB (5385208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff88c189da0a650b8a5398942c5d6cffdb179e37f7048c0f746492cf882c7be6`  
		Last Modified: Thu, 16 Apr 2020 01:14:55 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d8d42864dd76e4e129d40ba3ddbfad7e0f66f8a769469cec3fff34b5eed0c6`  
		Last Modified: Thu, 16 Apr 2020 01:14:56 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca44c0e48b537d57e81059af16bd77d94d7071b01070f4eac6772dc8989ebaeb`  
		Last Modified: Thu, 16 Apr 2020 01:14:55 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e88b0b84a22b40c3261ceb53c6c4175a02622576106ffcb9592357e68eae42`  
		Last Modified: Thu, 16 Apr 2020 01:15:10 GMT  
		Size: 105.2 MB (105153167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
