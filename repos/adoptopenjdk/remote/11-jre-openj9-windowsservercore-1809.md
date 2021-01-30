## `adoptopenjdk:11-jre-openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:735b17cb85086b1fc3fda45d8c787685d7f428494c4cc39a222d5d62d50fa4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `adoptopenjdk:11-jre-openj9-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull adoptopenjdk@sha256:6a5fd6f81d311b2e543000a5173980b5c5e7943635492bb208426ff263888662
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2516354062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a36768044c583a1f6610431e49d17934a035d1276a06880c6bf834162669b3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 30 Jan 2021 01:51:46 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Sat, 30 Jan 2021 01:58:55 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_windows_openj9_11.0.10_9_openj9-0.24.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_windows_openj9_11.0.10_9_openj9-0.24.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (66bf50f000c1803a66ccd00ccb24dbfd18a69a14731e6eb8be48f9813a6cd841) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '66bf50f000c1803a66ccd00ccb24dbfd18a69a14731e6eb8be48f9813a6cd841') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 30 Jan 2021 01:58:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
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
	-	`sha256:b13b91e20ec3ce05db37dd2629a45c36cad0297a8789704b2aef7ce97554139f`  
		Last Modified: Sat, 30 Jan 2021 02:40:50 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e1c715bc8cd30091f0f2758efc2dea0ad98db5d1bd326fb1c81e6cd4cc0dae`  
		Last Modified: Sat, 30 Jan 2021 02:50:24 GMT  
		Size: 80.6 MB (80578066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a946d785373a63fb344e48a64ec164838d04b20dd6bebed6e27337172ea8fa`  
		Last Modified: Sat, 30 Jan 2021 02:48:51 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
