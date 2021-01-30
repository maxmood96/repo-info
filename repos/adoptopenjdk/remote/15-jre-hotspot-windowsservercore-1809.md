## `adoptopenjdk:15-jre-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:ea4936165155185cb25d127f2fda6322d3db08636d4d65a3652b7ffb6c623837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `adoptopenjdk:15-jre-hotspot-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull adoptopenjdk@sha256:03537507d4b88adcb138a4fb0965e37d39e592b8390604972225f90f5b645a5e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2536507060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4e89169535cb4811590945d1c5834fbfaf9590ac8e452d8d1afa5ea13a8002`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 30 Jan 2021 01:33:14 GMT
ENV JAVA_VERSION=jdk-15.0.2+7
# Sat, 30 Jan 2021 01:40:44 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7/OpenJDK15U-jre_x64_windows_hotspot_15.0.2_7.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7/OpenJDK15U-jre_x64_windows_hotspot_15.0.2_7.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (e78fb1b0ccb6413d27dd9ed487f09af3bd0ba204208305c3b20e58607f45a019) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e78fb1b0ccb6413d27dd9ed487f09af3bd0ba204208305c3b20e58607f45a019') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ebcff80f114376ff2a39691ab49e4044d6d8813161ac60c53c8c87347a3d4e`  
		Last Modified: Sat, 30 Jan 2021 02:30:42 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6d00eb9cd8fc7f0df859a2cf733a9fc4449f53334d5f183d725dd021996fed`  
		Last Modified: Sat, 30 Jan 2021 02:32:34 GMT  
		Size: 100.7 MB (100732452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
