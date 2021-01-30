## `adoptopenjdk:15-jre-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:94c877b8794e4d7de430e5e7f5b515ca9a86657ec29e111bd4c71c809e3e9f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `adoptopenjdk:15-jre-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull adoptopenjdk@sha256:2a004f52e4fdb5af2618f4c448a23fa1891fe9c7b903ae4f0d8a4779799e1e2d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5895316551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb21f4c2528be0abe97328387a44b35e6ebef4a7e6e59f65a3188e093d368b80`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 13:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 30 Jan 2021 01:35:56 GMT
ENV JAVA_VERSION=jdk-15.0.2+7
# Sat, 30 Jan 2021 01:42:55 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7/OpenJDK15U-jre_x64_windows_hotspot_15.0.2_7.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7/OpenJDK15U-jre_x64_windows_hotspot_15.0.2_7.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (e78fb1b0ccb6413d27dd9ed487f09af3bd0ba204208305c3b20e58607f45a019) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e78fb1b0ccb6413d27dd9ed487f09af3bd0ba204208305c3b20e58607f45a019') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
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
	-	`sha256:3ec2ca503ec4c498611f6b6dcaa9050722abe98059555e1776999190ef53c548`  
		Last Modified: Sat, 30 Jan 2021 02:31:27 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727f118d740f70b9b50b4a0654885bbdcf2e702056f15106156520760e60eb7e`  
		Last Modified: Sat, 30 Jan 2021 02:33:01 GMT  
		Size: 101.4 MB (101420036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
