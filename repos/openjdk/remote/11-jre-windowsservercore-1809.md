## `openjdk:11-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:fb6f5717c63d7f13cbad1bb7fa2d7bc367e82764c6812237cb680edc5893197b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `openjdk:11-jre-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull openjdk@sha256:b1117335cc8a0e72046cf08a57ec2f055901d0dcc0c05e8aa7e5e68ed0033429
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2314818002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58aeed022ddc1562f9ef15aaa227e4eeff90983d2f06cb4149df4a087a43862a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2020 21:51:51 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 14 Apr 2020 21:52:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 16 Apr 2020 00:52:20 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 00:57:58 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 16 Apr 2020 00:57:58 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 00:58:47 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76226cfc56487958b0dd09e402ad764ebe45c0d60a9f371b313f464139d53067`  
		Last Modified: Tue, 14 Apr 2020 22:20:19 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0881d2c023f862a62321635e36b1908f2cd044ddf41621a6b369b072550b481f`  
		Last Modified: Tue, 14 Apr 2020 22:20:20 GMT  
		Size: 4.7 MB (4669064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db0f414ea98c4b23c121c16eb3ce24e395e5d3777653d722ee0fdc4d680bb32`  
		Last Modified: Thu, 16 Apr 2020 01:10:22 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4ea4965699d530a4c03c686f7a38454ce8f3698b3f2648ff1fe2889f0a3f1`  
		Last Modified: Thu, 16 Apr 2020 01:13:30 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a653b292ca72d21ae321967fb6c72d47d3df109ccfaa4764af98308e188d8b3c`  
		Last Modified: Thu, 16 Apr 2020 01:13:30 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1336317f54f7d997a223973eeec3fba24e6a60460f5d050f2156d977322ad`  
		Last Modified: Thu, 16 Apr 2020 01:13:39 GMT  
		Size: 39.4 MB (39436049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
