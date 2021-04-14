## `adoptopenjdk:8-jre-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:6c116153cffec760d5ee0fdf33fc4ebe0b91151b75c9bdd75fdd9a4c8954229c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `adoptopenjdk:8-jre-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull adoptopenjdk@sha256:1923a0ccc22596604ea3f5606d11bd57f9a20d9dc25a65439f01b895ef6f84b2
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5889067919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15486c13ba42fae5a54df9e772adfe3440cc0dce90c411ec0fc1eb9f6dd73f36`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 18:35:54 GMT
ENV JAVA_VERSION=jdk8u282-b08_openj9-0.24.0
# Wed, 14 Apr 2021 18:42:07 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08_openj9-0.24.0/OpenJDK8U-jre_x64_windows_openj9_8u282b08_openj9-0.24.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08_openj9-0.24.0/OpenJDK8U-jre_x64_windows_openj9_8u282b08_openj9-0.24.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (cb1ba5f2d086ac3fb6a875ac7749837c1b0a7493d988d0b2360a0f2b392255c3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'cb1ba5f2d086ac3fb6a875ac7749837c1b0a7493d988d0b2360a0f2b392255c3') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Apr 2021 18:42:09 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf50aa2d11b972a16121530c3a42b314c5ef879b9018d0f5e556b50b18f37a9`  
		Last Modified: Wed, 14 Apr 2021 19:34:21 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52119b619c1bd90ab37122de3f55f201cf4c963a4d10c03a99e43839214388ef`  
		Last Modified: Wed, 14 Apr 2021 19:35:52 GMT  
		Size: 94.2 MB (94179794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5015cf2fee0857f3932dd43819397dc21b6b279b882271d2d45d97e472b6c279`  
		Last Modified: Wed, 14 Apr 2021 19:35:41 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
