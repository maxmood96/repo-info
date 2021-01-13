## `openjdk:8-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:9eca35ac633b43e761352cb3addd7d6011b13e5e74a1b4aacd111afcf75af83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:8-jre-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:2c5dfaac23eabb5c15b5cfa87c313dbb358d682128455e52f59fddf269661c08
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2488019373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8088f447b81e21df9476e224865760e6799d066e8712c3b3cc8d346f43952747`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 20:55:59 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Jan 2021 20:56:41 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 13 Jan 2021 20:56:42 GMT
ENV JAVA_VERSION=8u275
# Wed, 13 Jan 2021 21:02:56 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jre_x64_windows_8u275b01.zip
# Wed, 13 Jan 2021 21:03:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1014559aa8330920e2a61da1c7cc26b15e9fe552eb1d26ec9bbb38f190014347`  
		Last Modified: Wed, 13 Jan 2021 21:37:46 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055aa085f13458ec1beb7302362f1caac423112886af03fcdc8814f1984e00bb`  
		Last Modified: Wed, 13 Jan 2021 21:37:50 GMT  
		Size: 9.4 MB (9361116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614136f2bedbd56fcecfe9965f262341245de10ab56cd1e2f9b7f41d17c04f04`  
		Last Modified: Wed, 13 Jan 2021 21:37:46 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805d57a7455b7e7423404a3618d9ded67825c86c1bd5658cebc4cc51d3b27a87`  
		Last Modified: Wed, 13 Jan 2021 21:41:19 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcb1970b206ccaeea56da6b49b048001332e1c623026ea7f2d03c06fb0b4a54`  
		Last Modified: Wed, 13 Jan 2021 21:41:26 GMT  
		Size: 42.9 MB (42881583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
