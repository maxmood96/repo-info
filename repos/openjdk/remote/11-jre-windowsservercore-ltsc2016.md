## `openjdk:11-jre-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:36e261e524a54bf8a78bfaf014387dcffb789e64eb5809b9f5c0997d7159bcb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `openjdk:11-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull openjdk@sha256:d77df21569a7431aa74d0cd27ecc45b56e2fc483d1e811bb8ae1e210aea5549d
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5774420534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4a32baa380c4bb02799e6e0a85b9d317ded1f1b7ef5904d46dd827b43e8f92`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 01:20:42 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Jan 2020 01:21:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 15 Jan 2020 01:21:52 GMT
ENV JAVA_VERSION=11.0.5
# Wed, 15 Jan 2020 01:28:15 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_
# Wed, 15 Jan 2020 01:28:16 GMT
ENV JAVA_URL_VERSION=11.0.5_10
# Wed, 15 Jan 2020 01:30:04 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8eda3425549320b6a36c0e2db12648d558a344a9da357393d801d01e306dbf`  
		Last Modified: Wed, 15 Jan 2020 02:09:08 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29348091d9ce947f1938356b82630d7ca42472ba69b25d92567aff11f1ab394f`  
		Last Modified: Wed, 15 Jan 2020 02:09:10 GMT  
		Size: 5.4 MB (5386894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1057760b4ea8a5b6d9e4c235921b7d8ba44cce56826b51adf4138136c49c3e55`  
		Last Modified: Wed, 15 Jan 2020 02:09:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09099d8a301d21e48675102362a0d2d798941bc9be9f8442aef925ce7adf872`  
		Last Modified: Wed, 15 Jan 2020 02:13:03 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6500b78715a4494f190de92bda45f032701d480e7466c65aca76b6767bba3f80`  
		Last Modified: Wed, 15 Jan 2020 02:13:03 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ef6225f8572a1f558a27255d6dc867921f4fdc86fbe02d7765acddb15bc80e`  
		Last Modified: Wed, 15 Jan 2020 02:13:14 GMT  
		Size: 44.4 MB (44428424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
