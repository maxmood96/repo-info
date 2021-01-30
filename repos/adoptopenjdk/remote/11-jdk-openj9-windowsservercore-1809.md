## `adoptopenjdk:11-jdk-openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:65d48e6aaac203e9c4dd95ab15b38e118400a87d323b354aaa03527b7e2119b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `adoptopenjdk:11-jdk-openj9-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull adoptopenjdk@sha256:eb90d3205e5de3efd7ed18fa89df4028ebe90f9654fa0c67aaa112745ed1ea89
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2815472223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b58e1572aef7796c6124893b4f4736f73b863b727b1434c12ba50f0d3d955a`
-	Default Command: `["jshell"]`
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
# Sat, 30 Jan 2021 01:54:09 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.10_9_openj9-0.24.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.10_9_openj9-0.24.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (f0abd0ad0fcecb0afee310d19655db680b2758f015d26bbb28ca50eaf263b09c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f0abd0ad0fcecb0afee310d19655db680b2758f015d26bbb28ca50eaf263b09c') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 30 Jan 2021 01:54:11 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
# Sat, 30 Jan 2021 01:54:13 GMT
CMD ["jshell"]
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
	-	`sha256:47d71259006607c93a42bc244c53a91d6f25693bcf8286648c09c33adef2b899`  
		Last Modified: Sat, 30 Jan 2021 02:47:49 GMT  
		Size: 379.7 MB (379694977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f229b4460d849fa5ed4961e9ef26cf7af5cf3eeb753a51c0e42cd028792eaf`  
		Last Modified: Sat, 30 Jan 2021 02:40:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65306cd20c28f8911fd1350f4e9a95cff5f390309c87fddc1976524ec37391de`  
		Last Modified: Sat, 30 Jan 2021 02:40:50 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
