## `adoptopenjdk:16_36-jdk-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:3a3f8e8de3558c0d1cec21c59131f5fc9adbfb8970f248ef53ed07b263d62496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `adoptopenjdk:16_36-jdk-hotspot-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull adoptopenjdk@sha256:1c540d5cb25e952f683cc838836b6bd574abaf0424f61968e60df574c1752504
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2852411363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3b4b0214b1daf8e8611bbf946c72b2d4d9ba613f916a1e2ab6bdaf9815493`
-	Default Command: `["jshell"]`
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
# Mon, 19 Apr 2021 19:41:34 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36/OpenJDK16-jdk_x64_windows_hotspot_16_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16%2B36/OpenJDK16-jdk_x64_windows_hotspot_16_36.msi ;     Write-Host ('Verifying sha256 (7e10ec7e61baad6293c8b2812eee7d049450602c9493f658f5476c48f0c450b1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '7e10ec7e61baad6293c8b2812eee7d049450602c9493f658f5476c48f0c450b1') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Mon, 19 Apr 2021 19:41:35 GMT
CMD ["jshell"]
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
	-	`sha256:223260ac584538f11dd65badfb1f6d9558032ccdb25fdebed3a40b00f4d6a0be`  
		Last Modified: Mon, 19 Apr 2021 20:51:11 GMT  
		Size: 382.7 MB (382653209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea0b71d0afa976198428e9d6a9d14ca55d7fac6fd4cd354a352cf1d296fb4b9`  
		Last Modified: Mon, 19 Apr 2021 20:43:59 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
