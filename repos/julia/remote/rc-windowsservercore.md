## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:029962ce0d4743cdfe6c00ae92079400d0b6f3b0dab768325614d7ad58c98be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `julia:rc-windowsservercore` - windows version 10.0.20348.2582; amd64

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

### `julia:rc-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull julia@sha256:df41cbbde846b48ef7db04e4b048b80243ebf91e41b40344663e12e585cde77a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487392949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7de11f94587fecdf9ee8a162c0a9c6bcc9f9c99486c1dda918f2871ee303188`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Mon, 29 Jul 2024 21:56:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Jul 2024 21:56:28 GMT
ENV JULIA_VERSION=1.11.0-rc2
# Mon, 29 Jul 2024 21:56:29 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc2-win64.exe
# Mon, 29 Jul 2024 21:56:30 GMT
ENV JULIA_SHA256=5c9b27f41094a3458973eeede7ace2af4c2fadadbc7f30b700ab8cf089641d15
# Mon, 29 Jul 2024 21:59:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 29 Jul 2024 21:59:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b226d28a4c3c7b2adf7b2156592bc0013505332e7317f38ec6e96216bf2ddf25`  
		Last Modified: Mon, 29 Jul 2024 21:59:11 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a54de42a766aa5313e1f0225d706523851a214aa3a0edb7619204f18717e3c`  
		Last Modified: Mon, 29 Jul 2024 21:59:10 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a03076090e4a95b1e0640669bba1d3b2c3ba76605aaff41ad3e5699a3e8d6d`  
		Last Modified: Mon, 29 Jul 2024 21:59:10 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ffea93ceff2538e493bf437c8124b747631cde1063bfef59c0698f07a9ffe6`  
		Last Modified: Mon, 29 Jul 2024 21:59:10 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bd8f08ff3f7a1d556c58273900c8f2d624c96570f980f39a36e3e27aca2bd3`  
		Last Modified: Mon, 29 Jul 2024 21:59:40 GMT  
		Size: 249.0 MB (248956997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3d9e77010013f6d9f5e87e2be82a377b0f4edd2833bf9708bcc44d43512fce`  
		Last Modified: Mon, 29 Jul 2024 21:59:10 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
