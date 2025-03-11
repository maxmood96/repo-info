## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:f6329f6ba2acb70fa9e6ebbc91d4d536d0672c1f7305a02fbbef863042afb5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
