## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:d8d991f04dba32b3d345911d416543416f0936db90cf1483a18e0b4c0e5b8c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull julia@sha256:59930ae7595b5fdc16c9a293f0abc122d8fc364e7d8ce3e5c2a5f7e6756cc1b5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186661998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13e44a2fb7920601877a5f2970aba1300712c4c313e9758624323a0d3ada1b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 30 Apr 2024 21:49:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 30 Apr 2024 21:49:51 GMT
ENV JULIA_VERSION=1.10.3
# Tue, 30 Apr 2024 21:49:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.3-win64.exe
# Tue, 30 Apr 2024 21:49:52 GMT
ENV JULIA_SHA256=688e746f3d8700ba44a6cbc9ce04ccead4cd921f093af80259e10d0b0c5448c8
# Tue, 30 Apr 2024 21:51:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 30 Apr 2024 21:51:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0162462ac8e21912c4dc6bc583bc0aa396ff310924c75020c1dd5d84b9444a`  
		Last Modified: Tue, 30 Apr 2024 21:51:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a01808be12ea6d8e666ac4e0ba27b4ed29bc28a6d6b79db67a1334deed40c4d`  
		Last Modified: Tue, 30 Apr 2024 21:51:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727834c38ea41d07307df22346e629e1225460d20dc9c0644572832e69a5146b`  
		Last Modified: Tue, 30 Apr 2024 21:51:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbea072db9d21283d89d47d81f570013db417eeb9bc2fb2b7c70b901b43eeb4a`  
		Last Modified: Tue, 30 Apr 2024 21:51:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc8af169f1f4f0df080fe9e7c20110e16b37fc0e9e41064126570dd27140799`  
		Last Modified: Tue, 30 Apr 2024 21:51:55 GMT  
		Size: 187.3 MB (187281919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e494cdbacd2fb13126efb6e606c12c63a3c4c9995b6808dae3ecb156fc7715`  
		Last Modified: Tue, 30 Apr 2024 21:51:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull julia@sha256:1fd5d053f986cc4e16156eae0bcc873db52486d330621c454076bda83b426743
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2351712007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff815d1ebdd8b310ca35adac6da729cd9ed3fdd07216b6002724c818ab44bf51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 30 Apr 2024 21:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 30 Apr 2024 21:49:53 GMT
ENV JULIA_VERSION=1.10.3
# Tue, 30 Apr 2024 21:49:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.3-win64.exe
# Tue, 30 Apr 2024 21:49:54 GMT
ENV JULIA_SHA256=688e746f3d8700ba44a6cbc9ce04ccead4cd921f093af80259e10d0b0c5448c8
# Tue, 30 Apr 2024 21:53:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 30 Apr 2024 21:53:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7937ff6a70c7c1f270975873f4ffedbbf0f439123ad2798f0a541e5a9418916`  
		Last Modified: Tue, 30 Apr 2024 21:53:07 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849f8d4299df67a3ac9b7d00ee4f6677213eb5a2043d808a3d04cabb65936921`  
		Last Modified: Tue, 30 Apr 2024 21:53:05 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c305cac823cae094f060731eeb9516e95fc5085ce60320b5a028602968c14a91`  
		Last Modified: Tue, 30 Apr 2024 21:53:06 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48219fa751cb975067bfc46d789ae470beaf0dc93541b59bea6fd6a6031d27c`  
		Last Modified: Tue, 30 Apr 2024 21:53:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02ca3c3645c1e6c43cc6cfa0c23df8956dbbae606775687bf89915ec7f3e273`  
		Last Modified: Tue, 30 Apr 2024 21:53:28 GMT  
		Size: 187.3 MB (187277506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74546cae5aa02d84606fc9021bdd9095dfc4b88f6b4a4dd1bcecafc8b4b39f9e`  
		Last Modified: Tue, 30 Apr 2024 21:53:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
