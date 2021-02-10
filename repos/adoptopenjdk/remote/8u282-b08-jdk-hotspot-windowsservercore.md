## `adoptopenjdk:8u282-b08-jdk-hotspot-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:b4428db4d42b61f343fb08f21b2d753337ffeb9ebc8e13215792fd537b124ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64
	-	windows version 10.0.14393.4225; amd64

### `adoptopenjdk:8u282-b08-jdk-hotspot-windowsservercore` - windows version 10.0.17763.1757; amd64

```console
$ docker pull adoptopenjdk@sha256:df95eb1a720ccd9617854cfdcfe2b78bf6b51d45c50d2866d832d1a34dc10047
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2641264657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bce05d43794a0cff39e68bc4c42bedb69a75723b29f245caa9e5bec28b58019`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Wed, 10 Feb 2021 13:14:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Feb 2021 17:51:02 GMT
ENV JAVA_VERSION=jdk8u282-b08
# Wed, 10 Feb 2021 17:52:09 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u282b08.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u282b08.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (fe137353ffa9f5b02c7783737e73ddf7668a3222b02c5d91abb8b8a2e55871ff) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fe137353ffa9f5b02c7783737e73ddf7668a3222b02c5d91abb8b8a2e55871ff') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:433d24156d44dde3b3c6c0094ba5824a315286ae537c68f272e464fc426510f6`  
		Last Modified: Wed, 10 Feb 2021 13:40:44 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b3247b5009581c51d85b36549cbf342c943291be77b761d1261d6ff96bebc8`  
		Last Modified: Wed, 10 Feb 2021 18:47:42 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07bc990379b5e74fc19cf0b81aacd449f2cb446ef7659b745d8015a6001f9bc`  
		Last Modified: Wed, 10 Feb 2021 18:48:01 GMT  
		Size: 202.0 MB (201995137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u282-b08-jdk-hotspot-windowsservercore` - windows version 10.0.14393.4225; amd64

```console
$ docker pull adoptopenjdk@sha256:4a3eabb54073ebf2a16cd4f238a18bd1a11b3bbe578f23ce420cc95728013ca7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5997710229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f53ace4bca3f134996a0a50092c61ae21279588d69ad57a74269606a0c903`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Jan 2021 18:11:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Feb 2021 13:17:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Feb 2021 17:52:15 GMT
ENV JAVA_VERSION=jdk8u282-b08
# Wed, 10 Feb 2021 17:54:02 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u282b08.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u282b08.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (fe137353ffa9f5b02c7783737e73ddf7668a3222b02c5d91abb8b8a2e55871ff) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fe137353ffa9f5b02c7783737e73ddf7668a3222b02c5d91abb8b8a2e55871ff') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:62c48323ed8ac695b8cbe0ecedcc28ba185a234673ad9241df2b151dd00f9181`  
		Size: 1.7 GB (1725027107 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c03f1c41641d4a4cf6906dee9a590ee67135d926dddab80cfef993cae745a38a`  
		Last Modified: Wed, 10 Feb 2021 13:41:36 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4126d68e2e6fb0c6bf47c53cf1c679441cdbc967eb03257aecb7005b2ae8c914`  
		Last Modified: Wed, 10 Feb 2021 18:48:15 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d75306c887f48448e89e7d8c7d369c59fa4747e511c0222ec1b2cf011b74d3`  
		Last Modified: Wed, 10 Feb 2021 18:52:20 GMT  
		Size: 202.7 MB (202694482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
