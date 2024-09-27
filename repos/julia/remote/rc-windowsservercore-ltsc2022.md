## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:2e2c2ae67255f61b1a6783e55ff151a494554f4384dc3a7d6246dcfcab571589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:35a86c812bf628fb0d57b23f41577f4128481313c59bb13424c059d0b803ebd6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714813472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8f677d649794ca9bd0b54895cc4d5a76f671ca0a4c318e5f410914d42e8447`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 26 Sep 2024 23:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 26 Sep 2024 23:58:06 GMT
ENV JULIA_VERSION=1.11.0-rc4
# Thu, 26 Sep 2024 23:58:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc4-win64.exe
# Thu, 26 Sep 2024 23:58:07 GMT
ENV JULIA_SHA256=8db57de418602e300e8332b7140498cd3f72ce841bbd16135b20bf1f0cada689
# Fri, 27 Sep 2024 00:00:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 27 Sep 2024 00:00:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f903642668f734897abc460d44dd08deec9dc38623b685d8d09eb8cf630bc94`  
		Last Modified: Fri, 27 Sep 2024 00:00:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d275bd801bfda68beede2930292c5a969e388ba326f13308ac15a03a9bdba0`  
		Last Modified: Fri, 27 Sep 2024 00:00:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0933520c1d651ad54fa7b6a5a0e8985c0f38cdeee95fa4e98a361db392d2da13`  
		Last Modified: Fri, 27 Sep 2024 00:00:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87140fa53f4ce1594a5e3fb9f18a10085109783ffc8a7a6eb5b47dbb7ebbaba0`  
		Last Modified: Fri, 27 Sep 2024 00:00:17 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932d9916e7a519cc1fe7703f62666821d0a161b18ee6f4505a5b58d827ff0b7a`  
		Last Modified: Fri, 27 Sep 2024 00:00:47 GMT  
		Size: 252.6 MB (252614573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cac0016497e277302fec19b617390d469467c3904225f04591157be3ddf269`  
		Last Modified: Fri, 27 Sep 2024 00:00:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
