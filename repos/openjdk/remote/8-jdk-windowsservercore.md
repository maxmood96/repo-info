## `openjdk:8-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:5b7e4203db519f68ccb6db18fd7e67d0778277c240d844e2e61e0066575234d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64
	-	windows version 10.0.14393.3750; amd64

### `openjdk:8-jdk-windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:6ab4a16326631c9fbcea1d8cf38bc72cbe07525beffd59b063e68940af5c1a89
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2398730535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba05e3b268fc1591e017aecd0bb15f264dea3d831b8f5b594bb96cbab266f058`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2020 23:04:41 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Jun 2020 23:05:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 09 Jun 2020 23:05:23 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 23:05:25 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Tue, 09 Jun 2020 23:05:26 GMT
ENV JAVA_URL_VERSION=8u252b09
# Tue, 09 Jun 2020 23:06:42 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52332a6d13a4eceaf15230fbd96c1f7136ebbb1b447dbee2026fa966d16e5d5`  
		Last Modified: Tue, 09 Jun 2020 23:32:34 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dd3b73be0c8bbdcab3e2ddbd39573c9fa7aa2e25a64801dd873a8d424d12fa`  
		Last Modified: Tue, 09 Jun 2020 23:32:34 GMT  
		Size: 4.8 MB (4762718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfbc99c9dcdf8401e437fd2bada9fbde4f01b912a801ccc7329e710a44dfd1d5`  
		Last Modified: Tue, 09 Jun 2020 23:32:32 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fca1d91d823bc8ce4c6a80d7ce21a9024bfdeb38714b3d6544b6e8b9c244c1`  
		Last Modified: Tue, 09 Jun 2020 23:32:32 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d37e4d3fa43b2bebb523ea4868a22430f12f979fb7b7557027447a792f8a95`  
		Last Modified: Tue, 09 Jun 2020 23:32:32 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127096c246f15f45c68929e870ffe382db31194d37c962ad4cb67a667061ae5b`  
		Last Modified: Tue, 09 Jun 2020 23:32:43 GMT  
		Size: 100.0 MB (100047808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-jdk-windowsservercore` - windows version 10.0.14393.3750; amd64

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
