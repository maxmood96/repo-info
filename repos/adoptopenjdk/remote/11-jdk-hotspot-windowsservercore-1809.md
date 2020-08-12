## `adoptopenjdk:11-jdk-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:125628c448a9c5b4e75a48d17825bd53932f9886838fb5385124f493c35b90ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `adoptopenjdk:11-jdk-hotspot-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull adoptopenjdk@sha256:d358d57829daa6e3591c79331be3092acebd48d4d1eca1aea4158a7a665dd505
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2705449994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8ed6851993d54666027cfd9e25100726549dacf3dfc2822e9d2a06ba19b3c6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 16:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.8+10
# Wed, 12 Aug 2020 16:41:23 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.8_10.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.8_10.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (148b487e0dde39ec5c0f32aa2397c17968b6cf6818822cea2b2394dfd0157396) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '148b487e0dde39ec5c0f32aa2397c17968b6cf6818822cea2b2394dfd0157396') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Aug 2020 16:41:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43065500f09f35124a5d71517aa493fd23ad75660682600f7f6b40aa7629ac78`  
		Last Modified: Tue, 11 Aug 2020 20:54:54 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c94a78c8dcda649933adffcf00105e47b979ec6b724eee07b3250136185957`  
		Last Modified: Wed, 12 Aug 2020 17:50:23 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbc2abb61683c4057166db82accf87a003b3f51f56901fe7161000122ab6913`  
		Last Modified: Wed, 12 Aug 2020 17:51:25 GMT  
		Size: 369.6 MB (369579572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ef1342d4963e591f0e80eb402410e2df4dec80de5d749d7f01a5aaa38ba76c`  
		Last Modified: Wed, 12 Aug 2020 17:50:23 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
