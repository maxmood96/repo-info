## `adoptopenjdk:11-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:920c746347b75b7d42603db050fac7c289ab4d8bc28d191ae80292033255ad99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `adoptopenjdk:11-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull adoptopenjdk@sha256:dbd7fb136716fa6ecfe66fe07c4c83d94848497fa2abd32f88a372f32665ed83
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6167724035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1079a6dbc0a51e89a0ed9357e7c6090c3dc4d288ff11f5aeac172c27d03e3cbd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 13:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 30 Jan 2021 01:25:50 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:28:57 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.10_9.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.10_9.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (f12011de94a72e1f14c9e68ce63bdd537aab1bf51eb336eba6d6061bc307baeb) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f12011de94a72e1f14c9e68ce63bdd537aab1bf51eb336eba6d6061bc307baeb') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 30 Jan 2021 01:28:59 GMT
CMD ["jshell"]
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
	-	`sha256:bbdc50f926853bb800a12133df45c2968f881964493be64856afa41b31204a55`  
		Last Modified: Sat, 30 Jan 2021 02:27:31 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a388bf65a9d00802b7e3a9b12843f5f1a410e8bbcb89d93cf310a7e14c5805e`  
		Last Modified: Sat, 30 Jan 2021 02:28:00 GMT  
		Size: 373.8 MB (373826132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb907f05ccc014e145fe7aa512c1263db3942d8e76e7e94be1ee9688eb62a11`  
		Last Modified: Sat, 30 Jan 2021 02:27:31 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
