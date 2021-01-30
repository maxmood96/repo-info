## `adoptopenjdk:15-jdk-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:9e904ba6fe9154d83849b3982827756a0df5f5973f1fdfcb6bc7001e4c14d3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `adoptopenjdk:15-jdk-hotspot-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull adoptopenjdk@sha256:55f92c27a059985979fe78f8b20f93362ed3ecf7f033d97639cee535616bfdcc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2813696751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d688503442246acc27624120300deeb0fd3e9cb48b2a24bf80fcf5c91fc2f34c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 30 Jan 2021 01:33:14 GMT
ENV JAVA_VERSION=jdk-15.0.2+7
# Sat, 30 Jan 2021 01:35:41 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7/OpenJDK15U-jdk_x64_windows_hotspot_15.0.2_7.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7/OpenJDK15U-jdk_x64_windows_hotspot_15.0.2_7.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (bff27f4c7b8b562e5ab11b43b1fd257be89fab5779a68fb5cbef1d42a95ff449) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'bff27f4c7b8b562e5ab11b43b1fd257be89fab5779a68fb5cbef1d42a95ff449') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 30 Jan 2021 01:35:43 GMT
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
	-	`sha256:50ebcff80f114376ff2a39691ab49e4044d6d8813161ac60c53c8c87347a3d4e`  
		Last Modified: Sat, 30 Jan 2021 02:30:42 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23b84f079bd9be051cb9dbd4b7e48dbcf1709742c4278c915ea68ade5cd2d55`  
		Last Modified: Sat, 30 Jan 2021 02:31:12 GMT  
		Size: 377.9 MB (377920858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b94358a152a847c56dacd0786393a195dfd6293ef073e7ff2bfde183e60674b`  
		Last Modified: Sat, 30 Jan 2021 02:30:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
