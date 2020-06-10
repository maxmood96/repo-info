## `openjdk:11-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:aac6b4b7931a616fff87adf70a8d1ae7ca37e00982ab21fb26e0c323465a1006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `openjdk:11-jre-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:6f4306a022b13e02368bac4d2476392ae558aca2b372a3a0afb84cbf8b8422fd
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338099657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc5ef8514b5355d730ce8f39ae0928247214aafca3ec3d572dc554b1ccfe6f2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2020 22:52:17 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 09 Jun 2020 22:53:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 09 Jun 2020 22:53:01 GMT
ENV JAVA_VERSION=11.0.7
# Tue, 09 Jun 2020 23:00:52 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Tue, 09 Jun 2020 23:00:53 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Tue, 09 Jun 2020 23:01:43 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
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
	-	`sha256:3f5b33153431bbe5c072f154c35123d6a1853452f73140098fbeb1b0763c5a56`  
		Last Modified: Tue, 09 Jun 2020 23:25:24 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390d4fd09797398fc8daf46bf72ea55fe19268f7fe185eb4cea2cc8ba8aabc23`  
		Last Modified: Tue, 09 Jun 2020 23:25:30 GMT  
		Size: 4.8 MB (4762523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc1ad9af33077efc5916609a569fd69b97166b518e69d545a5887f4812558e0`  
		Last Modified: Tue, 09 Jun 2020 23:25:22 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec7f9bdbfa84ebfbf1ee4a506f7caa8a9934d638b45256460aeac698c44c39a`  
		Last Modified: Tue, 09 Jun 2020 23:30:30 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df8fe892525b84ced645e579c48db15d6fc68b927a04ea5b82e491f00f42657`  
		Last Modified: Tue, 09 Jun 2020 23:30:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6561bf3fea4b874c5468cdbe45dff4b1bd1d37746c92adcf09eb82103983ae7d`  
		Last Modified: Tue, 09 Jun 2020 23:30:38 GMT  
		Size: 39.4 MB (39417199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
