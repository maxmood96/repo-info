## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:672a80d760ad72eb415544019fe7aedcd081bab81d82a9fd079a0170f46d0d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull julia@sha256:fb90544c49ef8c1d7695ad1f455b48d966f28bce85ec839ba7a176e10262ddd5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2564423219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd47e84da26a8dcec6afdda9ae46a79e8deb2ce0aabe290140ff3c44b022e50`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Fri, 04 Apr 2025 20:43:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 04 Apr 2025 20:43:11 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 04 Apr 2025 20:43:12 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta1-win64.exe
# Fri, 04 Apr 2025 20:43:12 GMT
ENV JULIA_SHA256=b9ec290ab3f5262553d30ebf852e9acf4f9c96ef415b9ef8005f1eadde807ca1
# Fri, 04 Apr 2025 20:44:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 04 Apr 2025 20:44:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e06107763bc2290d4e94ccee22231ac6bddea0ecd685169280ff02b9b09561`  
		Last Modified: Fri, 04 Apr 2025 20:44:32 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aae33e2b9aebc7e7b967f0c99c96dadb34a3bdbe1bce40616a92266067529ef`  
		Last Modified: Fri, 04 Apr 2025 20:44:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a371c4fa34b3029df098afc1a95b80a7451075374738d30714b50a1a53b08b`  
		Last Modified: Fri, 04 Apr 2025 20:44:31 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd49d602335383b40b273b53627e9c31995ed9f42a7c729b099c061d6325ee0`  
		Last Modified: Fri, 04 Apr 2025 20:44:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36827157ef23c44073bd4dc4839dec392e9a9bd47544616b2ed03e63d5bcc007`  
		Last Modified: Fri, 04 Apr 2025 20:45:11 GMT  
		Size: 294.5 MB (294475598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fe588f5fd435da161ec4daafbfddd02e5708dac543a2f572ce51c7a5bb749e`  
		Last Modified: Fri, 04 Apr 2025 20:44:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
