## `adoptopenjdk:8-jdk-hotspot-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:1c94fdad48d19ce28472fa43008ef52f0ea0968fb60289deadb63a715e3e8863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64
	-	windows version 10.0.14393.4169; amd64

### `adoptopenjdk:8-jdk-hotspot-windowsservercore` - windows version 10.0.17763.1697; amd64

```console
$ docker pull adoptopenjdk@sha256:669e255b5d19a0a1025e13674527db5fdcf290776acea4c144e148009a3402b4
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2637762684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe2ceaa5e2859ec85420a830e6da68b099b9e39ba55ae0ea286cb64d4302e7f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 30 Jan 2021 01:15:18 GMT
ENV JAVA_VERSION=jdk8u282-b08
# Sat, 30 Jan 2021 01:17:04 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u282b08.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u282b08.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (fe137353ffa9f5b02c7783737e73ddf7668a3222b02c5d91abb8b8a2e55871ff) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fe137353ffa9f5b02c7783737e73ddf7668a3222b02c5d91abb8b8a2e55871ff') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
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
	-	`sha256:50705780f99d97bf5a59d6164cd80726ef9865688c2092fb65adae83c8a9db25`  
		Last Modified: Sat, 30 Jan 2021 02:14:49 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b56c270dbfa430aee4ade25303913ba21cffc363bd6f1f234adc6ac99cef70e`  
		Last Modified: Sat, 30 Jan 2021 02:18:28 GMT  
		Size: 202.0 MB (201988100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8-jdk-hotspot-windowsservercore` - windows version 10.0.14393.4169; amd64

```console
$ docker pull adoptopenjdk@sha256:d4e200a160025293a05210387613babeb58554d23c40a0b2283258e3375233b2
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5996577151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56212538a28122d87c7f812ac923cfe37fb8adc0c37264eac23cfe609aef820f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 13:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 30 Jan 2021 01:17:15 GMT
ENV JAVA_VERSION=jdk8u282-b08
# Sat, 30 Jan 2021 01:19:48 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u282b08.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u282b08.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (fe137353ffa9f5b02c7783737e73ddf7668a3222b02c5d91abb8b8a2e55871ff) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fe137353ffa9f5b02c7783737e73ddf7668a3222b02c5d91abb8b8a2e55871ff') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:51e9c5c519fdcd28aa0ed033a3cc16cf37dd76bea8ec06b2dc4a344415bdd224`  
		Last Modified: Wed, 13 Jan 2021 15:10:27 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15544b88c12686f9f5ebfaf15f1d635d2ac72fef9507874335c420ec2bd2057`  
		Last Modified: Sat, 30 Jan 2021 02:18:42 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc76b7940e95b0b8a39772c809a2437acd8b3db0a336491cdea1e0c8481e2cf`  
		Last Modified: Sat, 30 Jan 2021 02:19:00 GMT  
		Size: 202.7 MB (202680561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
