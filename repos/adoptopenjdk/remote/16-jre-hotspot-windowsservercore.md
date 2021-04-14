## `adoptopenjdk:16-jre-hotspot-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:89b0aa9729b9e9ad703f0e626495b8976b0a73eef4e87b5cccc60935789d1429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `adoptopenjdk:16-jre-hotspot-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull adoptopenjdk@sha256:bf293f4199584ee1bdea062fa2398298704b12fa3daedc352e5874a0a6f92483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2553098854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9299e93bf6cf39f3d5c67ab1723007a582223b7e7cb4cb5217cbd9ae2e39046`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 18:25:11 GMT
ENV JAVA_VERSION=jdk-16+36
# Wed, 14 Apr 2021 18:31:30 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36/OpenJDK16-jre_x64_windows_hotspot_16_36.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36/OpenJDK16-jre_x64_windows_hotspot_16_36.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (8871544e7e2a5a4ad7ec1d8b976a1fb19b312ab77fcd4681014669341691cc44) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8871544e7e2a5a4ad7ec1d8b976a1fb19b312ab77fcd4681014669341691cc44') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53fc385dc9efa1e7b61ba503d543de9ed12cb2bdcea828d2125a31847e3611`  
		Last Modified: Wed, 14 Apr 2021 19:25:42 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793c66499abef8eb420c8e4c676e8f4002b51ee6efe609ebd056a157ce0d1dc6`  
		Last Modified: Wed, 14 Apr 2021 19:29:26 GMT  
		Size: 83.3 MB (83342129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:16-jre-hotspot-windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull adoptopenjdk@sha256:8cf79c4c3e27c2e0b1b2de219c66c17dd84105791ca4026717e3b0271e7baf1f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5878729768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2411e95e9a26bdf2146c072fc7e2993b19f658f422075dec2fe3690f09ab9f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 18:27:12 GMT
ENV JAVA_VERSION=jdk-16+36
# Wed, 14 Apr 2021 18:33:50 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36/OpenJDK16-jre_x64_windows_hotspot_16_36.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36/OpenJDK16-jre_x64_windows_hotspot_16_36.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (8871544e7e2a5a4ad7ec1d8b976a1fb19b312ab77fcd4681014669341691cc44) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8871544e7e2a5a4ad7ec1d8b976a1fb19b312ab77fcd4681014669341691cc44') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
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
	-	`sha256:d4e2098c9001f006062dde31a1c289c88aff8f8dfb5890f62457cd30a1fbb2df`  
		Last Modified: Wed, 14 Apr 2021 19:27:01 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313437c2165c71a01a864892b42602a9394c975379660afe6c9af47a3cf515ad`  
		Last Modified: Wed, 14 Apr 2021 19:29:50 GMT  
		Size: 83.8 MB (83843088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
