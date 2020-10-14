## `openjdk:11-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:4b0e5df5dedc82f433becde3710887fce93c54ed7766a66b23033ed801bfddf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `openjdk:11-jdk-windowsservercore` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:c7ef08ac85830065e2f65f975ffe4c2a31b36c9e55ecc967cbc06a43d51d7ab7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2578082210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6b1bb1eabd9ef1625033e6b5a8220171a2b697b8743d30ee93b8765dbbf4c9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 18:03:11 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 Oct 2020 18:03:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 14 Oct 2020 18:03:58 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 14 Oct 2020 18:03:59 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_windows_11.0.8_10.zip
# Wed, 14 Oct 2020 18:05:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Oct 2020 18:05:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f24549ffd67841d2abd5b00ca5ac77dd540ae7fdd1c5015df4b2e75feb1c873`  
		Last Modified: Wed, 14 Oct 2020 18:40:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1117af659dc8efb682205f3b9eeb244de0c062c1c510b5edfe0c1fb95679113f`  
		Last Modified: Wed, 14 Oct 2020 18:40:09 GMT  
		Size: 9.2 MB (9229357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1baa928a68325599e22d6c20e68537f3c208f43de98c387f5a503d6740222fe3`  
		Last Modified: Wed, 14 Oct 2020 18:40:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e0c4d33407917e54d14c0792ab0213db6ed055bbdd2df2328e60cee92ab781`  
		Last Modified: Wed, 14 Oct 2020 18:40:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce7645cd9d7e90d43c749e3f1f4ff2d00f11811f5e4e6f16919b5cbaa740415`  
		Last Modified: Wed, 14 Oct 2020 18:43:54 GMT  
		Size: 194.8 MB (194757025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c478aea9f5ad83adda22a5f73780573660297700b1e9efe18310bc3151c0fa`  
		Last Modified: Wed, 14 Oct 2020 18:40:07 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:11-jdk-windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull openjdk@sha256:a989ff23a1260c182194a30454c9b9f2453e19a057cced8d4be12c06a142a324
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5951212726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf0a4e311f5d5b1b7919ffb91bbc42d3f96dcca7f28e17b0b8eb66dd9206162`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 18:05:40 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 Oct 2020 18:06:59 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 14 Oct 2020 18:07:00 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 14 Oct 2020 18:07:01 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_windows_11.0.8_10.zip
# Wed, 14 Oct 2020 18:09:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Oct 2020 18:09:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268572cf853e5b33ed53392bbc6e62b1e762b24c14e02c14f668989d10278072`  
		Last Modified: Wed, 14 Oct 2020 18:44:28 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3d8ff91d4c7e5d649f483f3fb3c7e2fdcc0f92af4d0de4baa1d52f9ec225ca`  
		Last Modified: Wed, 14 Oct 2020 18:44:26 GMT  
		Size: 9.9 MB (9921487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c960dab8931b205ef056318e8d24326b5607a98e721ca8b7c25f17e3902890`  
		Last Modified: Wed, 14 Oct 2020 18:44:23 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b12a8eb832065b8bf776a1cf3436e25b6bdd22f0f447e294a1b077677e1416e`  
		Last Modified: Wed, 14 Oct 2020 18:44:23 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a26641dde55448543763047d8082c26b07b78ef1951bcb4fa591c4ce3fa5b65`  
		Last Modified: Wed, 14 Oct 2020 18:44:45 GMT  
		Size: 199.9 MB (199933887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949f33f9f73e300564d5b9609b929c61aedd1a00c769fe3b099e8aefc529dbe9`  
		Last Modified: Wed, 14 Oct 2020 18:44:23 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
