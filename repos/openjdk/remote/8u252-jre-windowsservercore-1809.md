## `openjdk:8u252-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:77c1239d5d05c92016bd82fe899e2c3f146284d73dc0d1c834532cfaee7900b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `openjdk:8u252-jre-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull openjdk@sha256:053040a57b18dec553fbe1d8d945f2f19c041b41734b4ffa52ab3bd6c18e352c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313122476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284ef1c97775df3630c08c2778b9fac5d699cfad2b9895f869647c37b35db914`
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
# Thu, 16 Apr 2020 01:00:55 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 01:05:26 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 01:05:27 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 01:06:09 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:fa6236287bbd5cfd4d436cdce20de85b1808ee4420d6ba293192224ba0d4d705`  
		Last Modified: Thu, 16 Apr 2020 01:14:25 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdb3789d730b49076705c35b4decdca7b656c18c8d6375baf594342185abf50`  
		Last Modified: Thu, 16 Apr 2020 01:15:53 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca92024a0a05d90980046ad226de335e2368569a01f9c7559e6b23830a0ef58b`  
		Last Modified: Thu, 16 Apr 2020 01:15:53 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f89a5d9635c74a6cbc2923e3a0c5f2b602edb9f3138199accf18f15d21a46eb`  
		Last Modified: Thu, 16 Apr 2020 01:15:59 GMT  
		Size: 37.7 MB (37740588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
