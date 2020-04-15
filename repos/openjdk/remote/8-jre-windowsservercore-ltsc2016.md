## `openjdk:8-jre-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:f35394733c4fdf4264e0d578b17bf1dbc236acb751a85e2d4d7b39515dbe34ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `openjdk:8-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull openjdk@sha256:1b3725c43fc6bb1aa06281ccf43467d7e18bd5678bdc3d434039810959212393
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5776146281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58849173a0ac375b7c995d9b499b62682c0a7efdfc3479cd1ae0646f610540a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Apr 2020 21:35:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2020 22:05:30 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Apr 2020 22:06:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 14 Apr 2020 22:06:45 GMT
ENV JAVA_VERSION=8u242
# Tue, 14 Apr 2020 22:11:25 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 14 Apr 2020 22:11:26 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 14 Apr 2020 22:13:08 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ac0134cee91589d04e97f11994235cce86faef5c581d15f2e143ecb90e92572`  
		Last Modified: Tue, 14 Apr 2020 22:16:36 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e0cf4292e83257e5609e02da1f800e8823e26a3c2e8d7032002e6ae2a7de39`  
		Last Modified: Tue, 14 Apr 2020 22:27:28 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24c3037c3266b54d877359067da7914c2001bc5180c81a37a2a6d03b44dd100`  
		Last Modified: Tue, 14 Apr 2020 22:27:28 GMT  
		Size: 5.4 MB (5385208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8ed35ed097774fd157d137dfb053145170648377c65f34be5cf3bba9eaa1ce`  
		Last Modified: Tue, 14 Apr 2020 22:27:25 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beadc4e122d72af35b4635e3cf335594b0bc4a22c75010263e9f93191e4c633e`  
		Last Modified: Tue, 14 Apr 2020 22:28:46 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c23bc3d9a8f20ece798a77feafed45a322597cbe9fa2623f559902adabd0dc3`  
		Last Modified: Tue, 14 Apr 2020 22:28:47 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8e6d86336ebfb176c452546b612d5ebfff103ef93ed357d7c6e9a47b67a2e2`  
		Last Modified: Tue, 14 Apr 2020 22:29:30 GMT  
		Size: 42.7 MB (42687828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
