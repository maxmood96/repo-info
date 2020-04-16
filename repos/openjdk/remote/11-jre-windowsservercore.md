## `openjdk:11-jre-windowsservercore`

```console
$ docker pull openjdk@sha256:afc7161ffb45fb7708b79d89b9f74e0156172501505b0e8a04e1fad841c020e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64
	-	windows version 10.0.14393.3630; amd64

### `openjdk:11-jre-windowsservercore` - windows version 10.0.17763.1158; amd64

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

### `openjdk:11-jre-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull openjdk@sha256:48c9b70877ace21fc9f910f462c663cd47305a2a9d066f0a05d10aa44c4af4bc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5777976858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5552dac17adb5aec553665924c9e9052ca09438d8ca326d63ca0845b22c42f05`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Apr 2020 21:35:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2020 21:54:17 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 14 Apr 2020 21:55:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 16 Apr 2020 00:54:01 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 00:58:58 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 16 Apr 2020 00:58:59 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 01:00:31 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
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
	-	`sha256:2ca133681cbf3e157b9c44aeddf863455c9cdab7e9ea44f65cf4d66a21f40af5`  
		Last Modified: Tue, 14 Apr 2020 22:21:29 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f52187584f4339cfbee494daedfe654741eb95afba5eddbb3a63fbdf0d43e36`  
		Last Modified: Tue, 14 Apr 2020 22:21:30 GMT  
		Size: 5.4 MB (5383721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467a72c245a28ede1ad962ad683dc54563dac71e9ffee28a62416a102d8f63a1`  
		Last Modified: Thu, 16 Apr 2020 01:11:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166256e76dc35cb06f4cd3dab7a077c57b2061f2a42a4b29e009c7d61c9590a5`  
		Last Modified: Thu, 16 Apr 2020 01:13:52 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2a77c18303cb331f1d3039a1c2e0df59459d0b578993c44d4dc1b4a889b4a2`  
		Last Modified: Thu, 16 Apr 2020 01:13:52 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34d17bbd5f6b19738130704514dd23695deaf8d36a8535a22ba95b55074ef68`  
		Last Modified: Thu, 16 Apr 2020 01:14:00 GMT  
		Size: 44.5 MB (44519869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
