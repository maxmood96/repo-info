## `adoptopenjdk:8u282-b08-jre-openj9-0.24.0-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:f0c118c08c3610964b53dce860367ada7e1e2e804b3d1d989bdf87020aa2017e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `adoptopenjdk:8u282-b08-jre-openj9-0.24.0-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull adoptopenjdk@sha256:abff06eb196cedf96b21d712c121e8849d4245c230a7f69d17c35924c6144fd8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5892583666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66092d4d2852e7fb0f3d9137182f3181c903cb9e72f92db14d26d6fb711e4d51`
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
# Sat, 30 Jan 2021 01:51:35 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08_openj9-0.24.0/OpenJDK8U-jre_x64_windows_openj9_8u282b08_openj9-0.24.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08_openj9-0.24.0/OpenJDK8U-jre_x64_windows_openj9_8u282b08_openj9-0.24.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (cb1ba5f2d086ac3fb6a875ac7749837c1b0a7493d988d0b2360a0f2b392255c3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'cb1ba5f2d086ac3fb6a875ac7749837c1b0a7493d988d0b2360a0f2b392255c3') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 30 Jan 2021 01:51:37 GMT
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
	-	`sha256:c61658089c1e95efb965d7c4441a568204356d886aee9e0105202a548e953448`  
		Last Modified: Sat, 30 Jan 2021 02:40:40 GMT  
		Size: 98.7 MB (98685791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0f19b71a4a47ff3c9c3c816d20588992c25180ce6b68edc375af8dba73665`  
		Last Modified: Sat, 30 Jan 2021 02:40:27 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
