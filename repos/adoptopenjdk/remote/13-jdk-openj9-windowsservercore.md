## `adoptopenjdk:13-jdk-openj9-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:e1faf266050777e8f33874dea3f9217da729c32cb4042dd2a5fe7ff375170201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64
	-	windows version 10.0.17763.1098; amd64

### `adoptopenjdk:13-jdk-openj9-windowsservercore` - windows version 10.0.14393.3568; amd64

```console
$ docker pull adoptopenjdk@sha256:aec3ac649bf6a2fce32e25897c0276c743341cc247da0eadf743b6d547751365
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6129131351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a5a4854c8c37633b785266949abbfa8596cc06dff0c0c0b24313fe58717abc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Fri, 13 Mar 2020 21:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Mar 2020 14:38:58 GMT
ENV JAVA_VERSION=jdk-13.0.2+8_openj9-0.18.0
# Wed, 18 Mar 2020 14:42:25 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jdk_x64_windows_openj9_13.0.2_8_openj9-0.18.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jdk_x64_windows_openj9_13.0.2_8_openj9-0.18.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (b96fdec7f69ff3a36ed3b03774d7ad3fc9385c80de7d8df9c4e6b4fbec70dcd9) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b96fdec7f69ff3a36ed3b03774d7ad3fc9385c80de7d8df9c4e6b4fbec70dcd9') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 18 Mar 2020 14:42:27 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 18 Mar 2020 14:42:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f08cc5bf7287bc1d8f72edfe2439c99210e433230a22fc73264fcf1685850ed2`  
		Last Modified: Fri, 13 Mar 2020 22:09:47 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ab0c0e750b074fa7a2b973e8294e83259593d5925670f16d4e899276ee81bd`  
		Last Modified: Wed, 18 Mar 2020 14:53:38 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f374011457059d9e7015c1b2672a6d03058efbc27c8c03012f241bdbdcca0c7`  
		Last Modified: Wed, 18 Mar 2020 14:54:33 GMT  
		Size: 400.4 MB (400365783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be68c1fe6faa0f538202875985ca1531ed51a10fdf51a6ecd45d7ae88b2337d`  
		Last Modified: Wed, 18 Mar 2020 14:53:38 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39dd31c88fcb0516133d4e5c52b7b8ca6ae1196c765f98e990598c335bc11e7c`  
		Last Modified: Wed, 18 Mar 2020 14:53:39 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jdk-openj9-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull adoptopenjdk@sha256:47cdb15dfb030adfcd44d78ffbbede45f607cf2721092bb475a2643c145accca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2660522540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60faadd26a246796bdb8d528a547cfe0ad16f2e35dd34fc72ff323809d8c44f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Mar 2020 16:05:18 GMT
ENV JAVA_VERSION=jdk-13.0.2+8_openj9-0.18.0
# Wed, 11 Mar 2020 16:08:18 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jdk_x64_windows_openj9_13.0.2_8_openj9-0.18.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jdk_x64_windows_openj9_13.0.2_8_openj9-0.18.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (b96fdec7f69ff3a36ed3b03774d7ad3fc9385c80de7d8df9c4e6b4fbec70dcd9) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b96fdec7f69ff3a36ed3b03774d7ad3fc9385c80de7d8df9c4e6b4fbec70dcd9') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Mar 2020 16:08:20 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 11 Mar 2020 16:08:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584a2e40e039a572fb351d45223c6bc4d35b148b422802fdf7195dad802e5b14`  
		Last Modified: Wed, 11 Mar 2020 16:21:05 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ddfabbf77aa1c302f4b24a9b5699d69bc343720e1007216151385d8c4dd881`  
		Last Modified: Wed, 11 Mar 2020 16:22:06 GMT  
		Size: 395.2 MB (395181424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34b3a13fbac03e57c0eaf0a6c68531597d21768590033703c32910415b2342e`  
		Last Modified: Wed, 11 Mar 2020 16:21:06 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e5a7999ffe85760efdd6197fc065202f8fd1b3d6476306ce257520076d639`  
		Last Modified: Wed, 11 Mar 2020 16:21:05 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
