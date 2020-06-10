## `openjdk:8-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:24b6fcdfbf251b0ef37ab90235e9e6f707d7a17cf5cefd568f394da171496861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `openjdk:8-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull openjdk@sha256:fee6f71e0d178d63d271d77e6a6cd812129294c20e3fbd8e6969c1a277b9aea1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5844523923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022d5796fcbae3fa5ad363d6ffa57838fa6e2f1f7a587f1f38bd73398e3e4ea0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Jun 2020 22:36:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2020 23:06:53 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Jun 2020 23:08:17 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 09 Jun 2020 23:08:18 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 23:08:19 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 23:08:20 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 23:10:37 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c938241e0507e1ada5f864325483d86fd08533a5a31e7cb6ec1357db9891b245`  
		Last Modified: Tue, 09 Jun 2020 23:18:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6efeab943acb379b8bd4d0dc4f19a541b7538946603e0267a1dab8dc1528783`  
		Last Modified: Tue, 09 Jun 2020 23:33:02 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5ac5751f3659ba87911bad898574099b553cd1ce9b816ff347f04e6cee8c58`  
		Last Modified: Tue, 09 Jun 2020 23:33:01 GMT  
		Size: 5.4 MB (5386119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a117a4a0f0bd8cd0a3f93efe8ee96d4e1756e36d81c8294318a861f6d5042644`  
		Last Modified: Tue, 09 Jun 2020 23:32:59 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb93eea2579f21055e1d5a46c78a7ce6918cefe31d6d317353ec491c14dc9b7`  
		Last Modified: Tue, 09 Jun 2020 23:33:00 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40774fd9a1e35d0f14879e6487eab2cee82e82496acf122a7b178134ff1a95c1`  
		Last Modified: Tue, 09 Jun 2020 23:32:59 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876cc5cc0ce1e3bb806fda045c1cd1715aed963d2507ac4ea774cf029f403a62`  
		Last Modified: Tue, 09 Jun 2020 23:33:13 GMT  
		Size: 105.1 MB (105134325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
