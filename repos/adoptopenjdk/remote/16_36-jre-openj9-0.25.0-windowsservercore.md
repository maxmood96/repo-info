## `adoptopenjdk:16_36-jre-openj9-0.25.0-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:72343588bfa4f7c4522d817926fae387981a935a1b3fc9f3f6c1500090dc38f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64
	-	windows version 10.0.14393.4283; amd64

### `adoptopenjdk:16_36-jre-openj9-0.25.0-windowsservercore` - windows version 10.0.17763.1817; amd64

```console
$ docker pull adoptopenjdk@sha256:3cae9cb345f094aad8450c274a2547fb84abc1c9413479ecc763d45501cc7bbd
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2544648030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cad815325de50a9d046f121bafe84eca4726024ef63e46d3867ad48ad55205d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Fri, 26 Mar 2021 00:31:49 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36_openj9-0.25.0/OpenJDK16-jre_x64_windows_openj9_16_36_openj9-0.25.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36_openj9-0.25.0/OpenJDK16-jre_x64_windows_openj9_16_36_openj9-0.25.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (49e6a468a50b65f7b3839881bca7a7fbea1be81d734f1b52662063a6db563387) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '49e6a468a50b65f7b3839881bca7a7fbea1be81d734f1b52662063a6db563387') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 26 Mar 2021 00:31:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
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
	-	`sha256:d40fe2c172e6cd89da47fa00951de791a26c98efe61cb0d15a7c3129f060b2b6`  
		Last Modified: Fri, 26 Mar 2021 00:44:13 GMT  
		Size: 83.1 MB (83109332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d100415ad8f1ccc2cf71bc1d4cf155e8f506a396c1f448dd34adc93faf9a73`  
		Last Modified: Fri, 26 Mar 2021 00:42:37 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:16_36-jre-openj9-0.25.0-windowsservercore` - windows version 10.0.14393.4283; amd64

```console
$ docker pull adoptopenjdk@sha256:ae441a96f8139f3dcffdb5ce8d5463bf2f8a9cd7e6ff373c78be7adc77feb755
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5880698011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78f28dfd7b33c392e88bf199cdb7b48ae961fd4d65a6c0daf935bc6c2c67158`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Fri, 26 Mar 2021 00:33:42 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36_openj9-0.25.0/OpenJDK16-jre_x64_windows_openj9_16_36_openj9-0.25.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36_openj9-0.25.0/OpenJDK16-jre_x64_windows_openj9_16_36_openj9-0.25.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (49e6a468a50b65f7b3839881bca7a7fbea1be81d734f1b52662063a6db563387) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '49e6a468a50b65f7b3839881bca7a7fbea1be81d734f1b52662063a6db563387') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 26 Mar 2021 00:33:43 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
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
	-	`sha256:1addbedac48e1b01ee77ce12c8f41320b120d7c54e39540e78a81c13bc2577ed`  
		Last Modified: Fri, 26 Mar 2021 00:46:02 GMT  
		Size: 83.8 MB (83783023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625d9f58149eb2c223603bd6bfd38349310a5e5b106df7b849bb3fc5c2523575`  
		Last Modified: Fri, 26 Mar 2021 00:44:24 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
