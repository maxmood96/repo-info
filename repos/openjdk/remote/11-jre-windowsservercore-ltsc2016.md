## `openjdk:11-jre-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:1edf790799924ee5fc6140465a323099fa22f03f02ce029abf85fd27a5e18f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `openjdk:11-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

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
