## `adoptopenjdk:8-jdk-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:775f694515acbf2d2ab1349cb8937364afcaf094c5767c206c777b427a452e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `adoptopenjdk:8-jdk-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull adoptopenjdk@sha256:6cfa88b6022319471ca30b667e96357b869f1a5af98a1e46c7ceb1f88362d697
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5928202342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f4570c365adf18efc007ea3c986696df7847f19f8e1f2ac168921f7587db4c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Fri, 13 Mar 2020 21:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Mar 2020 14:10:21 GMT
ENV JAVA_VERSION=jdk8u242-b08
# Wed, 18 Mar 2020 14:12:51 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u242b08.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u242b08.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (10478f65692b86bfff4fc029db119d6eac2a48f23c1bc542e5443ce6f2547573) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '10478f65692b86bfff4fc029db119d6eac2a48f23c1bc542e5443ce6f2547573') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
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
	-	`sha256:c383ed6765cf597a8d53b8a7f30df1a6cc75eeb3219457f6c318cba46dbadbdb`  
		Last Modified: Wed, 18 Mar 2020 14:47:40 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fea40b5f30fcbb3aea70db990db8ddfdf78416c39c8606b46c8d10ab41061f3`  
		Last Modified: Wed, 18 Mar 2020 14:47:59 GMT  
		Size: 199.4 MB (199438966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
