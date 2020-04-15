## `adoptopenjdk:14-openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:9c17a30dd64e5d7d390f957c5ab078f5884ee43d2a4cbf471301c02643c6f5ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `adoptopenjdk:14-openj9-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull adoptopenjdk@sha256:6063e2ceeb61c9653ef18c8a17538f2f1c34e179dff0928e756d33c1f904fd9d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2659620670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f39fe86015f44a0b211a4b36affc81a4df27e0684cb565968bea9a407e6bd2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 18:43:49 GMT
ENV JAVA_VERSION=jdk-14+36.1_openj9-0.19.0
# Wed, 15 Apr 2020 18:46:21 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36.1_openj9-0.19.0/OpenJDK14U-jdk_x64_windows_openj9_14_36_openj9-0.19.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14%2B36.1_openj9-0.19.0/OpenJDK14U-jdk_x64_windows_openj9_14_36_openj9-0.19.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (b245cca34f2bb6e063b19aed44efb7e22ae57d1c832554ef9deb7a7f521c3b20) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b245cca34f2bb6e063b19aed44efb7e22ae57d1c832554ef9deb7a7f521c3b20') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 15 Apr 2020 18:46:22 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 15 Apr 2020 18:46:24 GMT
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
	-	`sha256:d75fead29fd92346386224517920b3fa11875b02e04800a499cd71322669c826`  
		Last Modified: Wed, 15 Apr 2020 19:29:24 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afca93e23047b2bdc3f0207df5314f4ced73ea3a15a82db31cbd4aea18c1faf2`  
		Last Modified: Wed, 15 Apr 2020 19:30:03 GMT  
		Size: 388.9 MB (388908894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80545c8435f9bf598478b33d6ca670305a0e7eb9de5e1230f7f2cb27576c19f6`  
		Last Modified: Wed, 15 Apr 2020 19:29:25 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860a743a5db366a68da7f101af594ab54eaa6558e26ef6bc7e7d21b9fdab8878`  
		Last Modified: Wed, 15 Apr 2020 19:29:24 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
