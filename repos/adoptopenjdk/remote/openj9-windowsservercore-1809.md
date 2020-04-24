## `adoptopenjdk:openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:0f1583c05166b5232b05670768fa2b352c82f3882730f5c603c2ebb85e4f2fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `adoptopenjdk:openj9-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull adoptopenjdk@sha256:fdada963a249e05956d703f8df3df251ee67c49a411356ddd0d82361f0db0f78
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2658537666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10c8aed409696caab19ae7f6a4168e87ab8fbe0d7919e02b9264b172e4d7613`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Apr 2020 21:05:22 GMT
ENV JAVA_VERSION=jdk-14.0.1+7.1_openj9-0.20.0
# Fri, 24 Apr 2020 21:08:02 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.1%2B7.1_openj9-0.20.0/OpenJDK14U-jdk_x64_windows_openj9_14.0.1_7_openj9-0.20.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.1%2B7.1_openj9-0.20.0/OpenJDK14U-jdk_x64_windows_openj9_14.0.1_7_openj9-0.20.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (be27624f76ca8cb2e437b6ff383004a143502c6e2de5e64ed4e4c8cd13260bdb) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'be27624f76ca8cb2e437b6ff383004a143502c6e2de5e64ed4e4c8cd13260bdb') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Fri, 24 Apr 2020 21:08:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Fri, 24 Apr 2020 21:08:03 GMT
CMD ["jshell"]
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
	-	`sha256:30b5cb0f5b338f5a46b986ae7af8050dff80eb60e9256dbeb55384d68b1e06cd`  
		Last Modified: Fri, 24 Apr 2020 21:29:47 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3d49d71632d329bbe562c9d0ae27a5e659130990747268409c183fd5693729`  
		Last Modified: Fri, 24 Apr 2020 21:30:17 GMT  
		Size: 387.8 MB (387825846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad1a1f7185aea878da4d33e78ebf5cecd2066392a3903afa6c022750259abc7`  
		Last Modified: Fri, 24 Apr 2020 21:29:47 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539c4452fdfa14b899b6c45015185f226e21080222671de3a4b0f87c3df98879`  
		Last Modified: Fri, 24 Apr 2020 21:29:48 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
