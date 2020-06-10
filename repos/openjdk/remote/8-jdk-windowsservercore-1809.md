## `openjdk:8-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:640d2bfacd14236df87129d6c2e7ac643eee18c63018b4d3e9cd3b11ce7ccfa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `openjdk:8-jdk-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

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
