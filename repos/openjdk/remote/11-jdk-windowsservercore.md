## `openjdk:11-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:af7114d3a2cff81360d45f3fe53408d577394e93f5d5db3c34b4274c64ee491f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64
	-	windows version 10.0.14393.3808; amd64

### `openjdk:11-jdk-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:fb3ed3fff9d0255b96370be93d23237d996757e6a9016ec5fdef793e1608b4a1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2514084765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ec9ec7dd7e95b846a9c632f90794e017cdcd301eaf6b2b1ce53b9025c5805b`
-	Default Command: `["jshell"]`
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
# Thu, 16 Jul 2020 23:18:00 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_
# Thu, 16 Jul 2020 23:18:01 GMT
ENV JAVA_URL_VERSION=11.0.8_10
# Thu, 16 Jul 2020 23:19:45 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 16 Jul 2020 23:19:47 GMT
CMD ["jshell"]
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
	-	`sha256:50553b418a7a23a6d4c19c73333409e2dd5d1e133026c049515c301ed56a5980`  
		Last Modified: Fri, 17 Jul 2020 00:22:27 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26d2c6ab6461a47ba87c62c60bbe939ab5d00c05f997b64a54899c3d6790bd8`  
		Last Modified: Fri, 17 Jul 2020 00:22:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32ba1d906cd0d22b7be26e03b0253bef39d7dc0133e88e3f9d4e04e3dcc2669`  
		Last Modified: Fri, 17 Jul 2020 00:22:46 GMT  
		Size: 194.8 MB (194750440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bddc192c9dd1dec714184459fdf5609cacef5def1077e576e26c3e762df970`  
		Last Modified: Fri, 17 Jul 2020 00:22:26 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:11-jdk-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull openjdk@sha256:ea6bbcd9e7f359ef27246eba853b752fb71cbc997860e1a40e7fb076c2fba694
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5947208698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4146516c474c0a51e8eafbe5b61ffc9cefda7feed0b3ac7dbca650a4339030`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 02:16:53 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 21 Jul 2020 17:22:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 21 Jul 2020 17:22:36 GMT
ENV JAVA_VERSION=11.0.8
# Tue, 21 Jul 2020 17:22:38 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_
# Tue, 21 Jul 2020 17:22:39 GMT
ENV JAVA_URL_VERSION=11.0.8_10
# Tue, 21 Jul 2020 17:25:20 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 21 Jul 2020 17:25:22 GMT
CMD ["jshell"]
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
	-	`sha256:47f6d4495790b9ffe933ed4c10a93a72ea2e73c78561ec63e187ec5e21165b51`  
		Last Modified: Wed, 15 Jul 2020 02:50:38 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6a9c03c0cb5a12f909fc8d9c26fcef63f8cffd16a05b66514faafe7c8d4203`  
		Last Modified: Tue, 21 Jul 2020 17:42:15 GMT  
		Size: 9.9 MB (9860240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e265cf04cbaa24514fde0b7e9b932f81d0f424e68121917f621c07ca5f5b933`  
		Last Modified: Tue, 21 Jul 2020 17:42:09 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458aeaa8ceac19b0185619ba0b90727b78126df5e87909a6ab7eba91bcffb4a5`  
		Last Modified: Tue, 21 Jul 2020 17:42:09 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16961162f205a9b648b320e0883e271596a60ebc913d2d96005377c51a3fb60a`  
		Last Modified: Tue, 21 Jul 2020 17:42:09 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ace538ecbeb7dfc4e6ff4d85c49b393c687a44338cba4d88683d137f6d99e5f`  
		Last Modified: Tue, 21 Jul 2020 17:42:32 GMT  
		Size: 199.9 MB (199879559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e1d02037781960ca426cdc3ce018928e39207527377d81b432928f89db16a1`  
		Last Modified: Tue, 21 Jul 2020 17:42:09 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
