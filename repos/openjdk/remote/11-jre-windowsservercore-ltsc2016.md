## `openjdk:11-jre-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:b9d75adb577f8f41bffa5fad200df4430fa73eb5c231b5d70e10738a93244b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `openjdk:11-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull openjdk@sha256:6d547c37dd7f1df015c0161f2f25781642866e8049c91deeb95d306a2aaeff43
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5796303471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e652dd2fc68796dc1cd246d144db5a0ce71f9acc6629ae112059073dc8acfd67`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 02:16:53 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 21 Jul 2020 17:22:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 21 Jul 2020 17:22:36 GMT
ENV JAVA_VERSION=11.0.8
# Tue, 21 Jul 2020 17:25:40 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jre_
# Tue, 21 Jul 2020 17:25:42 GMT
ENV JAVA_URL_VERSION=11.0.8_10
# Tue, 21 Jul 2020 17:27:32 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6d4495790b9ffe933ed4c10a93a72ea2e73c78561ec63e187ec5e21165b51`  
		Last Modified: Wed, 15 Jul 2020 02:50:38 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6a9c03c0cb5a12f909fc8d9c26fcef63f8cffd16a05b66514faafe7c8d4203`  
		Last Modified: Tue, 21 Jul 2020 17:42:15 GMT  
		Size: 9.9 MB (9860240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e265cf04cbaa24514fde0b7e9b932f81d0f424e68121917f621c07ca5f5b933`  
		Last Modified: Tue, 21 Jul 2020 17:42:09 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d052c39fd38b6eff9a66e05eb776dd89f51a482770d3370402102737b6821dc2`  
		Last Modified: Tue, 21 Jul 2020 17:42:56 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d251dfe16b82109dcd55d650c5c360cf5d0bda238642a1405841f6513fb15ae`  
		Last Modified: Tue, 21 Jul 2020 17:42:57 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7ed71726f7c135689276301d0115c701ffade981e8ba7bac1425a790f1f70f`  
		Last Modified: Tue, 21 Jul 2020 17:43:06 GMT  
		Size: 49.0 MB (48975463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
