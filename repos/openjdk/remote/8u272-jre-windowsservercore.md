## `openjdk:8u272-jre-windowsservercore`

```console
$ docker pull openjdk@sha256:9aeb1eb729d888e64b440a6d68c806b0cd026cd0857cb07e89d52b727dd3272e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `openjdk:8u272-jre-windowsservercore` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:98cb824fd0d4bd25785cc94705706f0dbc0a85ef71937f315d453ea8162af844
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2426241416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f73ba9807992494c743c418de7b50a20ae1720b58c37ae64e0ba9a26e6ba668`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 18:14:23 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Oct 2020 18:15:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Mon, 26 Oct 2020 23:16:39 GMT
ENV JAVA_VERSION=8u272
# Mon, 26 Oct 2020 23:20:55 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u272-b10/OpenJDK8U-jre_x64_windows_8u272b10.zip
# Mon, 26 Oct 2020 23:21:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:423e6d8e8bc166e44e75a7429a9d4337b7f187f5087a11a1ffa628b9d5c9fa3f`  
		Last Modified: Wed, 14 Oct 2020 18:50:47 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955986b14a9eba01fe3b415706ff08c9b8d356c2c46b6100a3bc762273d0ecb7`  
		Last Modified: Wed, 14 Oct 2020 18:50:50 GMT  
		Size: 9.2 MB (9229481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319edd33d3771a9750d94fe0e08598e37754eec20662b6dbcab8c3c4af9977d4`  
		Last Modified: Mon, 26 Oct 2020 23:28:13 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479658d9550d2631afdf167ec6338c3079607863a9b5ee337018922cf2ca6b39`  
		Last Modified: Mon, 26 Oct 2020 23:31:34 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb29499eee7a1223d65e65d1c0aa8a823ff922127309cb1df03eeec9ca3efb8`  
		Last Modified: Mon, 26 Oct 2020 23:31:41 GMT  
		Size: 42.9 MB (42917238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8u272-jre-windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull openjdk@sha256:421a7f7159881ac1fc8ebf7f63d86ed65a742f181a75098b5493b09cb12e3881
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5799364925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73afb78606e1c0301933e3ba1220c2b5b5ed7e48270d9e5ecd73d4a90ea25af`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 18:16:20 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Oct 2020 18:17:35 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Mon, 26 Oct 2020 23:17:52 GMT
ENV JAVA_VERSION=8u272
# Mon, 26 Oct 2020 23:21:46 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u272-b10/OpenJDK8U-jre_x64_windows_8u272b10.zip
# Mon, 26 Oct 2020 23:23:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:cffa1e768304d56e30305c9ac557468df987effb01142b8bffef4c43698d8707`  
		Last Modified: Wed, 14 Oct 2020 18:51:23 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5135402b2d35127448acb3ec865346d17536f47e5ed865a0b400e6d93d0a9b7e`  
		Last Modified: Wed, 14 Oct 2020 18:51:26 GMT  
		Size: 9.9 MB (9915365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6412d2f8042f71e4b27766034d224753f249ed5972a2a602888e2cbed8895760`  
		Last Modified: Mon, 26 Oct 2020 23:30:34 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac4d63453f7f4e112f6d8325aed7f17941f6ed32a6984eec1d0d84988226e7`  
		Last Modified: Mon, 26 Oct 2020 23:31:53 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d83951ce2c28582bdfef229163e3ee2cd373fb8bfa5481d2efcaa8b4543e2ae`  
		Last Modified: Mon, 26 Oct 2020 23:32:02 GMT  
		Size: 48.1 MB (48093332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
