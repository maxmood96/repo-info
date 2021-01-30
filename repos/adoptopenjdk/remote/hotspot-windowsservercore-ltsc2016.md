## `adoptopenjdk:hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:ac4e53935cbf93146841e8634942700680aaef974a9792b51f72d1edb8daaec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `adoptopenjdk:hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull adoptopenjdk@sha256:5b19e8bf46bd5a2b9ddfe4b1a1d664cf697997ce37a8cb2bf6eed5e33b094a25
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6172525120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733dd4648d13484bb2119bcff1ea0020f2fe4cf8edc7e75cb75b9ba7e7edeca3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 13:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 30 Jan 2021 01:35:56 GMT
ENV JAVA_VERSION=jdk-15.0.2+7
# Sat, 30 Jan 2021 01:39:04 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7/OpenJDK15U-jdk_x64_windows_hotspot_15.0.2_7.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7/OpenJDK15U-jdk_x64_windows_hotspot_15.0.2_7.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (bff27f4c7b8b562e5ab11b43b1fd257be89fab5779a68fb5cbef1d42a95ff449) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'bff27f4c7b8b562e5ab11b43b1fd257be89fab5779a68fb5cbef1d42a95ff449') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 30 Jan 2021 01:39:06 GMT
CMD ["jshell"]
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
	-	`sha256:3ec2ca503ec4c498611f6b6dcaa9050722abe98059555e1776999190ef53c548`  
		Last Modified: Sat, 30 Jan 2021 02:31:27 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f211ae4bf0c0d2b96078f6e188b44b04ebe270d15fe545e8e20fb56700fb97`  
		Last Modified: Sat, 30 Jan 2021 02:32:04 GMT  
		Size: 378.6 MB (378627322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25138d445aa6e119394a81c0e6cd22d6c1b8fca7b2eefe68877cc0b353bb4a74`  
		Last Modified: Sat, 30 Jan 2021 02:31:27 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
