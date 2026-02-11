## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:063f81d0b492f69d91b44610a595bb09c15d260e49aca9d4493573e51f3ba850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull julia@sha256:26fed03bf77315768437da7da712a2f328c8b1b8cac8051c598773a246a7c5ae
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251070899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5459db51f755279bcda92a316020302155ef6308bcc9b9097f803dc6200d5efe`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Wed, 11 Feb 2026 01:13:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 01:13:42 GMT
ENV JULIA_VERSION=1.12.5
# Wed, 11 Feb 2026 01:13:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.5-win64.exe
# Wed, 11 Feb 2026 01:13:43 GMT
ENV JULIA_SHA256=97c0cff9770baa823d40eb6f4f47fdfdcc3c48c609882354c01734f8abcd14f8
# Wed, 11 Feb 2026 01:14:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Feb 2026 01:14:59 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ebd08ecafce1c314a35f93321236af74ba2d89445873606cbf6cde8bd3a26c`  
		Last Modified: Wed, 11 Feb 2026 01:15:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1a0fcb121f9dab830587148600c6c4deb87fe294485c75bf250458e3737dc1`  
		Last Modified: Wed, 11 Feb 2026 01:15:07 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac78364a3a60882997b569d917c39824c76786078c56c98f217a383313edc08`  
		Last Modified: Wed, 11 Feb 2026 01:15:07 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ef5db1d7661d7aaf4e9b0df0a716bc21ab2229d1a373a3418c6bee0947ca0b`  
		Last Modified: Wed, 11 Feb 2026 01:15:07 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df0205b12d9ac3914654323c88534f6960ced5ac66adc8f6c5555fbd0faec99`  
		Last Modified: Wed, 11 Feb 2026 01:15:51 GMT  
		Size: 286.3 MB (286304404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82407043b8355a557b4f4f6e426d4cc8b9ac13a7346dd2f989142e3529dae81`  
		Last Modified: Wed, 11 Feb 2026 01:15:07 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
