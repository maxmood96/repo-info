## `adoptopenjdk:8-jdk-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:897ddbc25dc093b79c308d4007b314e1753ac90e6cbf7b5db27fabec5d705f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `adoptopenjdk:8-jdk-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull adoptopenjdk@sha256:42ef9922af471fcd1d1120452f6f273261814709f565f7efa88f95b6a1942984
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6020974563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659746183c4144f00c621b519606201563bb428b1e794779e9c00539cc65162b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 13:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 30 Jan 2021 01:45:13 GMT
ENV JAVA_VERSION=jdk8u282-b08_openj9-0.24.0
# Sat, 30 Jan 2021 01:47:51 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08_openj9-0.24.0/OpenJDK8U-jdk_x64_windows_openj9_8u282b08_openj9-0.24.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08_openj9-0.24.0/OpenJDK8U-jdk_x64_windows_openj9_8u282b08_openj9-0.24.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (079268d9ba232091b81ef9bbf1f001e498ab7823b9def204a6fd1115e2e9d976) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '079268d9ba232091b81ef9bbf1f001e498ab7823b9def204a6fd1115e2e9d976') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 30 Jan 2021 01:47:52 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:51e9c5c519fdcd28aa0ed033a3cc16cf37dd76bea8ec06b2dc4a344415bdd224`  
		Last Modified: Wed, 13 Jan 2021 15:10:27 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93db5c732622afc0821849cd0a725165172a30c4ca01dc6eff3c83b10536c6e5`  
		Last Modified: Sat, 30 Jan 2021 02:33:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b445ae7f27d0845cd4c9c6d8028c4d596af789fd58ab2482a92cc7bb75e800fc`  
		Last Modified: Sat, 30 Jan 2021 02:37:59 GMT  
		Size: 227.1 MB (227076700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c6c959ed43a0e3c8c0426f08e5f08fd849c227c62fa202d932f57d9db91f44`  
		Last Modified: Sat, 30 Jan 2021 02:33:45 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
