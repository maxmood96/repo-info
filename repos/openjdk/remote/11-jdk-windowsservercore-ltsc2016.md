## `openjdk:11-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:78a06300d7e6a8fc29d1b01c00739e8a6e691faa0a4ded021076cc4f6c44f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `openjdk:11-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull openjdk@sha256:d8480fcd3fc5657e5ee9347a73c116c70f8560e8960251743b48b9c7bfe73b9b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5934757139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6330ced3863bec12874359db7572da7bc32b2d2e31e3e080c693cae2e84a89e0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Jun 2020 22:36:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2020 22:54:43 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 09 Jun 2020 22:56:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 09 Jun 2020 22:56:07 GMT
ENV JAVA_VERSION=11.0.7
# Tue, 09 Jun 2020 22:56:08 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Tue, 09 Jun 2020 22:56:09 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Tue, 09 Jun 2020 22:58:43 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2020 22:58:46 GMT
CMD ["jshell"]
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
	-	`sha256:ac85d43745a7efcbde867bfdd7056538ab0ab4b41bb0e329cb0c696e429a1229`  
		Last Modified: Tue, 09 Jun 2020 23:26:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67916dbbf47158f61e0bd7f82d338dabd49e85b6ef0e0dc07a3fd186498fbc55`  
		Last Modified: Tue, 09 Jun 2020 23:26:05 GMT  
		Size: 5.4 MB (5384868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef538ce36975bf2ce2c73b320c719fceac565a4a02d26b84567438f558affb94`  
		Last Modified: Tue, 09 Jun 2020 23:26:01 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9fd49805a004ef5e2d26010725dbfe77aa61f599677c805e44403952ba5923`  
		Last Modified: Tue, 09 Jun 2020 23:26:01 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd9f1510d6f662e41337039452220b3b02ea66047f94bacc7baded2f82d9e0f`  
		Last Modified: Tue, 09 Jun 2020 23:26:01 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dc4f9542fc51c536d289c4070e363c4afd738abbd75c63e69ccc29ea65e45e`  
		Last Modified: Tue, 09 Jun 2020 23:29:28 GMT  
		Size: 195.4 MB (195367719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234db9f62f8bc68f2eb9acc221cec6781c2d06307d9bcc8ab16e1f2ccf498c12`  
		Last Modified: Tue, 09 Jun 2020 23:26:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
