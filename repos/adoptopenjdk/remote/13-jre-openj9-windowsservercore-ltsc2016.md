## `adoptopenjdk:13-jre-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:d866f1316459083e63957a600159427dd363b0bd90460d7a5c9e05e5e4612966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `adoptopenjdk:13-jre-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull adoptopenjdk@sha256:64ad1501faafaa2438bf56269fca5f94713e7623c6fe660510372d36a626152c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5805402858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffbae5af660f29b2695ce101f112cfc05db240815b316a86d42a6bc2c8e9070`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 18 Mar 2020 14:44:45 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_x64_windows_openj9_13.0.2_8_openj9-0.18.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_x64_windows_openj9_13.0.2_8_openj9-0.18.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (c27a5f69d41058773e4ccf8bfd5b247b50f57cab0a65a540fcc25984b5eafadc) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c27a5f69d41058773e4ccf8bfd5b247b50f57cab0a65a540fcc25984b5eafadc') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 18 Mar 2020 14:44:46 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
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
	-	`sha256:8019a9258f0747078c77404f6505d11bec44a91cf8009f88512bfc047d9786ca`  
		Last Modified: Wed, 18 Mar 2020 14:54:58 GMT  
		Size: 76.6 MB (76638414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c5893f3a1c5c51dc047672e9e3578222c78344e02492e1858d30557a55b8f8`  
		Last Modified: Wed, 18 Mar 2020 14:54:48 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
