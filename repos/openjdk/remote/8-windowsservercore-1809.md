## `openjdk:8-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:bb60ac11fd828ab845ec713bb127c95805934c8681610d4689149518252cdd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `openjdk:8-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull openjdk@sha256:00c7eb57dc7bb8b378c7324250682f008109584defcf1abf036406ee6c4bbd33
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2375171348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2d2161d4fcf5b47f4787123516edd362bac456cb59d7d23ab9e780c9b7055b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2020 22:03:19 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Apr 2020 22:03:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 14 Apr 2020 22:03:58 GMT
ENV JAVA_VERSION=8u242
# Tue, 14 Apr 2020 22:03:59 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_
# Tue, 14 Apr 2020 22:04:01 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 14 Apr 2020 22:05:12 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:4d2fa2371fb538b0835be954b6708b3e3a1067a5575a0dab42064ba8161b93c3`  
		Last Modified: Tue, 14 Apr 2020 22:27:00 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bfcb120984dc0603767fc1a0d3c080edaf1ae4fd2055fa6ce6f42bf1d1475d`  
		Last Modified: Tue, 14 Apr 2020 22:26:59 GMT  
		Size: 4.7 MB (4669057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2f134d81ce982820bce11d9c4c615d43a97b7c3ffc25fcf3ef9e57623eecb6`  
		Last Modified: Tue, 14 Apr 2020 22:26:57 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71b45e701079db5b5e67e2cea3c9d07c02a72fea3f6fcf7fb4df906b1d233e0`  
		Last Modified: Tue, 14 Apr 2020 22:26:57 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e20f0ffb547521c06a68c7d43930aeb68db3abb45050b112141d28b6bbc1a7b`  
		Last Modified: Tue, 14 Apr 2020 22:26:57 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6f9ac64092cb0f7157d7297fa1af5606690c6d2da6d92555fd4dfd6dad2802`  
		Last Modified: Tue, 14 Apr 2020 22:27:09 GMT  
		Size: 99.8 MB (99789308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
