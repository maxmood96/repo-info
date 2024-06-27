## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1916ecc55beb7ddb264f6b83f70a01ebab5a6eaec37d2a97209538044089608a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull julia@sha256:76e1fec23c897c4030593fb74385851688cdb64ce113508ae20a1b720722b772
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2367837368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a2e16489a9100acf9e1017583fd1e7d56cf46502ae189ce32ccd715ed325ea`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Thu, 27 Jun 2024 00:05:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Jun 2024 00:05:46 GMT
ENV JULIA_VERSION=1.11.0-rc1
# Thu, 27 Jun 2024 00:05:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc1-win64.exe
# Thu, 27 Jun 2024 00:05:47 GMT
ENV JULIA_SHA256=77c6c17a940cd95c0e1bcc4ac3b6b2012cee2a7909dfd7f4494478f6b5742363
# Thu, 27 Jun 2024 00:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Jun 2024 00:06:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f00ae8774ac94d68683b3184c3b46c178e7fe672f822cecc86dafad12dcadd4`  
		Last Modified: Thu, 27 Jun 2024 00:06:46 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d63d3e7ef5fd5ac608de72ece734fd15fa806b140b959cc0f19be5ad74aba5f`  
		Last Modified: Thu, 27 Jun 2024 00:06:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0b415d2aaf45139b8e1fc2e8289105ac8190234147481cb9162976dcb4ec72`  
		Last Modified: Thu, 27 Jun 2024 00:06:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6640899c2625b28758cfec8359bc4456239debb33d1ca9d23eb8a63917268b26`  
		Last Modified: Thu, 27 Jun 2024 00:06:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b992bfa90c3d62abb21ea78c7ec8e78fdfb07e149fbd2916f6e59ca4b53939ef`  
		Last Modified: Thu, 27 Jun 2024 00:07:15 GMT  
		Size: 249.6 MB (249640643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0588192cee5545d46252be254b400168d8746e669e1a0131784881eb950577`  
		Last Modified: Thu, 27 Jun 2024 00:06:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
