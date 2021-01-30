## `adoptopenjdk:8u282-b08-jdk-openj9-0.24.0-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:722380839bccc6b0d5d508f5378406a0551ea09c920f7aacb521770ac601ab43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `adoptopenjdk:8u282-b08-jdk-openj9-0.24.0-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull adoptopenjdk@sha256:7177594c779b496ac2efe51fa885d0a09c8d779bf42f76db0d3f73ee9c26ab3c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2662163339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd53e6afc4f2ec8dc83dd25931eaa5922d62240e5ee11d4ace62aa8f4dcfe641`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 30 Jan 2021 01:43:01 GMT
ENV JAVA_VERSION=jdk8u282-b08_openj9-0.24.0
# Sat, 30 Jan 2021 01:44:53 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08_openj9-0.24.0/OpenJDK8U-jdk_x64_windows_openj9_8u282b08_openj9-0.24.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08_openj9-0.24.0/OpenJDK8U-jdk_x64_windows_openj9_8u282b08_openj9-0.24.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (079268d9ba232091b81ef9bbf1f001e498ab7823b9def204a6fd1115e2e9d976) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '079268d9ba232091b81ef9bbf1f001e498ab7823b9def204a6fd1115e2e9d976') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 30 Jan 2021 01:44:55 GMT
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
	-	`sha256:77b9ad82c411569ef55c3e753efa20ead4aa05c5884ae7395c95c1d1da654d90`  
		Last Modified: Sat, 30 Jan 2021 02:33:12 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e14f55afe5db02d76e0cb908b180252736370ac193db8744aa1009fdfbfbef`  
		Last Modified: Sat, 30 Jan 2021 02:33:32 GMT  
		Size: 226.4 MB (226387420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509b6bc11b12f72b2e8e0f8db4f92ea7557377b7dd9a9fcd6d2f1e832c8214b2`  
		Last Modified: Sat, 30 Jan 2021 02:33:12 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
