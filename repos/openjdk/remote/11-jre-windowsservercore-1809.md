## `openjdk:11-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:5aaa625c47a228dc88e831303583b45a4066f14e35c543efcbd79ca90a217bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:11-jre-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:9c8a9da47b99d6ae00ded9bd65440f0748c334f5c0013e8c653b80da5ba79b63
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363177904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf27f2c434de93967f4a9371ff0161505dd837b8d733602373a2a8abf8b5aec`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 02:14:08 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 29 Jul 2020 01:24:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 29 Jul 2020 01:24:11 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:30:09 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jre_x64_windows_11.0.8_10.zip
# Wed, 29 Jul 2020 01:31:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe72f810946627936fb3059295f72a1745bfc735925259534b9cee6d7543ae4`  
		Last Modified: Wed, 15 Jul 2020 02:49:46 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520d3705c7856f755f25379021a94d32e6a41a4f254476a27dbecff51a0c5de`  
		Last Modified: Wed, 29 Jul 2020 01:51:48 GMT  
		Size: 9.2 MB (9158226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc4deb39488c6c0ce9389a9952c320ac191c4476e5327ba2bbb4e88082a9ce`  
		Last Modified: Wed, 29 Jul 2020 01:51:45 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03300be21be934f2b4335ebd26708d99da7744eab76601a2f13a612c0151331b`  
		Last Modified: Wed, 29 Jul 2020 01:53:48 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b82bf8afdd795fd6e7b7edb0548f982efa9efc238926550fe1d0051afe4a17`  
		Last Modified: Wed, 29 Jul 2020 01:53:57 GMT  
		Size: 43.8 MB (43822933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
