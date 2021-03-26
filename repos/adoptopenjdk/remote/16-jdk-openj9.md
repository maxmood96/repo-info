## `adoptopenjdk:16-jdk-openj9`

```console
$ docker pull adoptopenjdk@sha256:1625753ce4fc1aea13304e7e38451f5cd60ac39f079be2539ea05bb11368878c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64
	-	windows version 10.0.14393.4283; amd64

### `adoptopenjdk:16-jdk-openj9` - windows version 10.0.17763.1817; amd64

```console
$ docker pull adoptopenjdk@sha256:1dac1d4ffc59776b653b8eb79b78253cf3b1f5a2e6ca0911c612c217b1ac0d92
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2862047247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1927a2a6cc305c94ed86ad2e402793fe390313532baf723654e6d05788d67723`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Mar 2021 00:26:35 GMT
ENV JAVA_VERSION=jdk-16+36_openj9-0.25.0
# Fri, 26 Mar 2021 00:28:06 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36_openj9-0.25.0/OpenJDK16-jdk_x64_windows_openj9_16_36_openj9-0.25.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36_openj9-0.25.0/OpenJDK16-jdk_x64_windows_openj9_16_36_openj9-0.25.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (5d5a2dd21567b376185076c4fcba42caf9e5c35565bbc2c416140514c8622460) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5d5a2dd21567b376185076c4fcba42caf9e5c35565bbc2c416140514c8622460') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 26 Mar 2021 00:28:09 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
# Fri, 26 Mar 2021 00:28:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e972ecb87b4a5ab636b1fb6ca4b3b32c81264cb6e52953719faf08a000bc28de`  
		Last Modified: Fri, 26 Mar 2021 00:40:55 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba46be6d71fb6ce383f30db61456ca70afde7d810230f8387ae5ed5458646196`  
		Last Modified: Fri, 26 Mar 2021 00:41:27 GMT  
		Size: 400.5 MB (400507107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c7646456caf0f5f7f986845ee0619425ac7dfef15377d4827c05fc9b526a15`  
		Last Modified: Fri, 26 Mar 2021 00:40:55 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c917ba6fd0bae5961173c41760ceda28dad6ced5abe2e98937875ee8074e3e`  
		Last Modified: Fri, 26 Mar 2021 00:40:55 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:16-jdk-openj9` - windows version 10.0.14393.4283; amd64

```console
$ docker pull adoptopenjdk@sha256:d5d157ac1495a36ddef667ba8a32783da4e5b17441f7df115435310f0a211c6e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6198101619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63728970e1aa7bccb838d5d30007bf49f7a740db355219ca2daf63edef8fbaf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Mar 2021 18:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Mar 2021 13:42:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Mar 2021 00:28:20 GMT
ENV JAVA_VERSION=jdk-16+36_openj9-0.25.0
# Fri, 26 Mar 2021 00:30:39 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36_openj9-0.25.0/OpenJDK16-jdk_x64_windows_openj9_16_36_openj9-0.25.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36_openj9-0.25.0/OpenJDK16-jdk_x64_windows_openj9_16_36_openj9-0.25.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (5d5a2dd21567b376185076c4fcba42caf9e5c35565bbc2c416140514c8622460) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5d5a2dd21567b376185076c4fcba42caf9e5c35565bbc2c416140514c8622460') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 26 Mar 2021 00:30:41 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
# Fri, 26 Mar 2021 00:30:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30bda99601c5cbd3b2118409f401852ea648e2319bd81518723e476b28d764c5`  
		Size: 1.7 GB (1726924885 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76680da9dc6db108ddf2e353c494b45e8486a6751619a13ed8fb3ad64b9a16e9`  
		Last Modified: Wed, 10 Mar 2021 14:06:08 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e41728ea40a7f7166fbec97a7e642d142df4b341bf918404307e12dd5ffcaa6`  
		Last Modified: Fri, 26 Mar 2021 00:41:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d259a75169762db7ebb2e248a9cde2aee92038d56058906edb7e61197c82a57e`  
		Last Modified: Fri, 26 Mar 2021 00:42:16 GMT  
		Size: 401.2 MB (401185183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edac28a873af7d64437a7e8fc4619fd32082926f4b0c5d058d50f0bbfe9c9973`  
		Last Modified: Fri, 26 Mar 2021 00:41:44 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f4c053de4e1e736909c5b06ed2be77d482fa8c7438c974c0a5e040d3e1593b`  
		Last Modified: Fri, 26 Mar 2021 00:41:44 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
