## `adoptopenjdk:8-jdk-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:36d90b471f01d2a296a54455c116274569e6dd0b370d084553d29630034daf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `adoptopenjdk:8-jdk-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull adoptopenjdk@sha256:dc0816db567c83dd6f433d7493dea4259377fab75bd6a0f6354b68f622a61e82
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6017465081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72d9f799c125228cbf1e9586299287f8e2af3ab7b89d6cd8e9daf579a3eff7`
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
# Wed, 14 Apr 2021 18:38:16 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08_openj9-0.24.0/OpenJDK8U-jdk_x64_windows_openj9_8u282b08_openj9-0.24.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08_openj9-0.24.0/OpenJDK8U-jdk_x64_windows_openj9_8u282b08_openj9-0.24.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (079268d9ba232091b81ef9bbf1f001e498ab7823b9def204a6fd1115e2e9d976) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '079268d9ba232091b81ef9bbf1f001e498ab7823b9def204a6fd1115e2e9d976') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Apr 2021 18:38:18 GMT
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
	-	`sha256:605772b6b515505cc402296e95a498f497068e35563c13bae7be5a9735725e33`  
		Last Modified: Wed, 14 Apr 2021 19:34:43 GMT  
		Size: 222.6 MB (222576997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ffb5749c8c69a206dfbea56536ef547991f0e4466cc019a24adcf1e2bb44ea`  
		Last Modified: Wed, 14 Apr 2021 19:34:22 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
