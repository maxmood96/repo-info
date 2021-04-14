## `adoptopenjdk:16-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:62e65ca8f2738d3907b59f3023eee1affd93891f4c49d0626fdc97c8095fdb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `adoptopenjdk:16-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull adoptopenjdk@sha256:de2cb2df5a6e0323247492a4154b091f6070e88e8e630811e6e934cd8f16e9c6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6182524073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24892f76764339bd01a7fe3d1d3f0f849e14b804cd86046d4415395b04b461e`
-	Default Command: `["jshell"]`
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
# Wed, 14 Apr 2021 18:29:49 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36/OpenJDK16-jdk_x64_windows_hotspot_16_36.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36/OpenJDK16-jdk_x64_windows_hotspot_16_36.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (7e10ec7e61baad6293c8b2812eee7d049450602c9493f658f5476c48f0c450b1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '7e10ec7e61baad6293c8b2812eee7d049450602c9493f658f5476c48f0c450b1') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Apr 2021 18:29:51 GMT
CMD ["jshell"]
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
	-	`sha256:de7b723bdedf8b8d5e17885a1f54017aae11caf154fd45bb90fd897a28e0920e`  
		Last Modified: Wed, 14 Apr 2021 19:27:36 GMT  
		Size: 387.6 MB (387635959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b2cbb5f0b4708e468726a1d297008069432a834d18651ef95180e243be3552`  
		Last Modified: Wed, 14 Apr 2021 19:26:59 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
