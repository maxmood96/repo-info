## `openjdk:11-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:3805414ca5986d5717a0b73ac8e7c9ac9fb7560fb6defb6eff4a780002ffb8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:11-jre-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:0785292cf26c3945617e1c834d00f07d99fc0e83d9c3645e6c8e8168b6428c2d
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261357820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aac0d3287624c696c415ef72d5154e75d01ceaaddc9012e95c67cba649bda06`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 01:17:38 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Jan 2020 01:18:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 15 Jan 2020 23:56:31 GMT
ENV JAVA_VERSION=11.0.6
# Thu, 16 Jan 2020 00:04:00 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Thu, 16 Jan 2020 00:04:01 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Thu, 16 Jan 2020 00:04:56 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1361e3321e08ed3279942f89e1e0c8e55b80c3557476fbb5f7d09dc69b7e3228`  
		Last Modified: Wed, 15 Jan 2020 02:04:53 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cb5c1399aeffc808a1e0e308439d9cc57968bbd344f0108a94ae421c200ad7`  
		Last Modified: Wed, 15 Jan 2020 02:04:54 GMT  
		Size: 4.5 MB (4546435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117a2905b79606e799609f8d736990ac7004da1dee2a6a3a2d0114bdb244a449`  
		Last Modified: Thu, 16 Jan 2020 00:23:20 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9168bba158a4ce7fa0b07d33bd9192506cac0ae6cf0cdf11cae3441d6a3d606`  
		Last Modified: Thu, 16 Jan 2020 00:27:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b94233c77f5a704a7c4df9280b7bdd7c3113e747eb155f144feef520328c84`  
		Last Modified: Thu, 16 Jan 2020 00:27:37 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820bcc7f00c3757b87201047735e0b4b4fee93edb57dcf917fec0d8093596642`  
		Last Modified: Thu, 16 Jan 2020 00:27:47 GMT  
		Size: 39.4 MB (39394237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
