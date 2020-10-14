## `openjdk:11-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:adf801aac3abc90749bc8c031ed768c66db0ed27f572178ca182a0f6e07a7dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:11-jdk-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:c7ef08ac85830065e2f65f975ffe4c2a31b36c9e55ecc967cbc06a43d51d7ab7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2578082210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6b1bb1eabd9ef1625033e6b5a8220171a2b697b8743d30ee93b8765dbbf4c9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 18:03:11 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 Oct 2020 18:03:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 14 Oct 2020 18:03:58 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 14 Oct 2020 18:03:59 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_windows_11.0.8_10.zip
# Wed, 14 Oct 2020 18:05:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 Oct 2020 18:05:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f24549ffd67841d2abd5b00ca5ac77dd540ae7fdd1c5015df4b2e75feb1c873`  
		Last Modified: Wed, 14 Oct 2020 18:40:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1117af659dc8efb682205f3b9eeb244de0c062c1c510b5edfe0c1fb95679113f`  
		Last Modified: Wed, 14 Oct 2020 18:40:09 GMT  
		Size: 9.2 MB (9229357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1baa928a68325599e22d6c20e68537f3c208f43de98c387f5a503d6740222fe3`  
		Last Modified: Wed, 14 Oct 2020 18:40:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e0c4d33407917e54d14c0792ab0213db6ed055bbdd2df2328e60cee92ab781`  
		Last Modified: Wed, 14 Oct 2020 18:40:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce7645cd9d7e90d43c749e3f1f4ff2d00f11811f5e4e6f16919b5cbaa740415`  
		Last Modified: Wed, 14 Oct 2020 18:43:54 GMT  
		Size: 194.8 MB (194757025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c478aea9f5ad83adda22a5f73780573660297700b1e9efe18310bc3151c0fa`  
		Last Modified: Wed, 14 Oct 2020 18:40:07 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
