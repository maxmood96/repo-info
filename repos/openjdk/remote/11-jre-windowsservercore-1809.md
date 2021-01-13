## `openjdk:11-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:0c3d2313f4f5878311499864ef9951094d31fe132edcaad0c4337ae33d4f7be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:11-jre-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:70a99f91f82b1495ffb6b2719f796af5ab46e122db41ec2434c288760fc22f7d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2489127208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b25faec4b9aa1aab5a933fe5d9e5038e4e02d6bc65732229129e5e8078c2492`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 20:44:21 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Jan 2021 20:45:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 13 Jan 2021 20:45:06 GMT
ENV JAVA_VERSION=11.0.9.1
# Wed, 13 Jan 2021 20:52:29 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_x64_windows_11.0.9.1_1.zip
# Wed, 13 Jan 2021 20:53:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
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
	-	`sha256:971349fa4cc521df2fdf5b01ee402b4753cd032fa00f4571fea0acfd4d0d5fdf`  
		Last Modified: Wed, 13 Jan 2021 21:26:41 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f0b6dc5ad26e757655f988b268c27fc1ae614a2b3f21efe68d1b3921d169d1`  
		Last Modified: Wed, 13 Jan 2021 21:26:40 GMT  
		Size: 9.4 MB (9361866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b52eaa48c571dad47066158bee7bad2f6d9c28bc4b3b2c735dff851c5167c9`  
		Last Modified: Wed, 13 Jan 2021 21:26:39 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6a6f16eaa42cf696f602044261ef28210a069f083c4c096aab00760f76857`  
		Last Modified: Wed, 13 Jan 2021 21:36:12 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09204513a439471c40b59cca8d82c70eec930af37e773f30ec5a6c70c272a841`  
		Last Modified: Wed, 13 Jan 2021 21:36:26 GMT  
		Size: 44.0 MB (43988664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
