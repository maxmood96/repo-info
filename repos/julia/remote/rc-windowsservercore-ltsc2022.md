## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:c91f597c41598bb33429df948ae62df0c1a503be4ea177e303cef283406f6e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull julia@sha256:fd7b176c905b3ff7816019f4e78c8ea509360e7a4df310abe2ab541e82225d45
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2388416557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a7e53b8a9b63d10902472c693ecef9c1a9ee3b971d8f1aa681e72553ebe5f5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Mon, 29 Jul 2024 21:56:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Jul 2024 21:56:18 GMT
ENV JULIA_VERSION=1.11.0-rc2
# Mon, 29 Jul 2024 21:56:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc2-win64.exe
# Mon, 29 Jul 2024 21:56:19 GMT
ENV JULIA_SHA256=5c9b27f41094a3458973eeede7ace2af4c2fadadbc7f30b700ab8cf089641d15
# Mon, 29 Jul 2024 21:57:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 29 Jul 2024 21:57:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2004ced6f75dfc26548982bc549bdcd35b913eb3a72269dbc399e6d3a182c3f7`  
		Last Modified: Mon, 29 Jul 2024 21:57:47 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877125878edd23f086297cf2fa61fe3826b6e168c9d6c8e4c4338e38bffab560`  
		Last Modified: Mon, 29 Jul 2024 21:57:45 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2236b4bc0c3384cf00f8a5f9365333f4caa8308f8d82a15f1aeb20f90949d73`  
		Last Modified: Mon, 29 Jul 2024 21:57:45 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac19f648370d52d66947cf612f872aa678d5e72a926bbaf9b8c056a1dc71b18`  
		Last Modified: Mon, 29 Jul 2024 21:57:45 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9233490af4b5310655ba6cc4a839ea66d417519ecd03280579dfc784a061b34b`  
		Last Modified: Mon, 29 Jul 2024 21:58:14 GMT  
		Size: 248.8 MB (248809802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43345dca3cbb7b6d74fec0d9781014740fe3d1d430434136a4c8a19dfd8e940`  
		Last Modified: Mon, 29 Jul 2024 21:57:45 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
