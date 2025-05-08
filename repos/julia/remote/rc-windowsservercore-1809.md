## `julia:rc-windowsservercore-1809`

```console
$ docker pull julia@sha256:ffce673ebd53eb140b524b7889e185b1f20a2bea9533f3eac67e85f679183234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `julia:rc-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull julia@sha256:90887a42840477af7b42ae1941c700ea81847e9ea413e7556a3fc06c7a633d92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454506616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80bb0a9c700b8b6b827f024cb9ede930537021503749da187479aba71ba801a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Mon, 28 Apr 2025 18:16:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 28 Apr 2025 18:16:11 GMT
ENV JULIA_VERSION=1.12.0-beta2
# Mon, 28 Apr 2025 18:16:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta2-win64.exe
# Mon, 28 Apr 2025 18:16:18 GMT
ENV JULIA_SHA256=92421914379d45e328f4d7e531c26cc7c4504675b25f5d79872f41fdd98e5bed
# Mon, 28 Apr 2025 18:18:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 28 Apr 2025 18:18:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Thu, 08 May 2025 17:14:51 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139daca1231c3dc6c386d14ef757302c18a7287c04e6d802c87e44c947149134`  
		Last Modified: Mon, 28 Apr 2025 18:18:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1bf971f69786e98e28e5c243d4b549bd6fcacf21db2c4f0516e7b25e65c927`  
		Last Modified: Mon, 28 Apr 2025 18:18:54 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e7a8ad1b9c05731b73aa382c432bf22158c92e669c9ba4ec03dcfdfb76261a`  
		Last Modified: Mon, 28 Apr 2025 18:18:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b7c0ced206a15942175711ed4fe1dcd17b1ecca73beec002b4bcb8109cd75a`  
		Last Modified: Mon, 28 Apr 2025 18:18:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633a017d89b1a58b46f2549215fcfbcfc7318cd39d00a983a4771a5e5e7fc08e`  
		Last Modified: Mon, 28 Apr 2025 18:19:32 GMT  
		Size: 289.0 MB (288974358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534319338f74f12d33ae69a6a8987cf98bdfcaab457d1502f74f32e3975f46a8`  
		Last Modified: Mon, 28 Apr 2025 18:18:54 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
