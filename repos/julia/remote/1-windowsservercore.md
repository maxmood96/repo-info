## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:c4871d8c13bfc3159fc87406b4a4c3e9f9c4e2fea9cd6c69ca0f412b425f6b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull julia@sha256:1e4b7f5b44aa6558e933498902b86501ba7267ba62adb6f0938c8c4b71aba877
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299825052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2e252caf683ad4b7724e209776f69c1b734015a97c1e2f4f045baae5ca07f3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:51:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:51:17 GMT
ENV JULIA_VERSION=1.10.3
# Wed, 15 May 2024 21:51:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.3-win64.exe
# Wed, 15 May 2024 21:51:18 GMT
ENV JULIA_SHA256=688e746f3d8700ba44a6cbc9ce04ccead4cd921f093af80259e10d0b0c5448c8
# Wed, 15 May 2024 21:52:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 15 May 2024 21:52:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fd7d46b7dbed13742df5e22d2267ea056cdb3f70bc8f9147389bc632163f1b`  
		Last Modified: Wed, 15 May 2024 21:52:30 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0ed11d25d34f3a16d4292fde1a9e6b7da15fea76c4aa3308f487796b6273e2`  
		Last Modified: Wed, 15 May 2024 21:52:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b8ff38bb3d607ec5a47b5be099ab8ff355f2dfe94e0f9f89b8f1618e460a6f`  
		Last Modified: Wed, 15 May 2024 21:52:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0caba2abc5dcf37b39c313426a082246e87ca46087766af4432c54ecee5c6f`  
		Last Modified: Wed, 15 May 2024 21:52:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd124ff2baef897040b4efae42ab088239a99b382bf1a8e825861118af18719`  
		Last Modified: Wed, 15 May 2024 21:52:52 GMT  
		Size: 187.1 MB (187147246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e8b432882aec9f9a09afb6546b7c41c6da75cd8a4531c7f2d0b019fd1f2ca2`  
		Last Modified: Wed, 15 May 2024 21:52:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull julia@sha256:0824a81f2228a9f89ee654725201e60dd26d2aaa87f13fead1b9517945785bab
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2366981500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190274e4a5cc0e7316ca0b3308f72cc73637f9c2a18f529aaff476a77aa02a38`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:51:17 GMT
ENV JULIA_VERSION=1.10.3
# Wed, 15 May 2024 21:51:18 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.3-win64.exe
# Wed, 15 May 2024 21:51:18 GMT
ENV JULIA_SHA256=688e746f3d8700ba44a6cbc9ce04ccead4cd921f093af80259e10d0b0c5448c8
# Wed, 15 May 2024 21:54:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 15 May 2024 21:54:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95f7df4e233b6e548287dfbdf0622b0b4d84cd86154ff0d63e47049392ecdf`  
		Last Modified: Wed, 15 May 2024 21:54:55 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b32820487a45df2280409928ff790e234e6c79f9d3d7235e0495e2df5720712`  
		Last Modified: Wed, 15 May 2024 21:54:54 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccad58740d7837c41c1e0e413a860785eeada06bfb27fe96c451654d39b506a5`  
		Last Modified: Wed, 15 May 2024 21:54:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091220304dc5c00c8cef2c0ca080036b7e423ed795b3a9aa722ff1be599b59`  
		Last Modified: Wed, 15 May 2024 21:54:54 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2e77e63490e0ccc5caece135d676366ebff3aa29b0923fb4532fc767c24bc2`  
		Last Modified: Wed, 15 May 2024 21:55:17 GMT  
		Size: 187.3 MB (187263593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476a090ae4dfda2b9a05f0870b2113b9347e2ba5d0af072a66fe5d8f1464c83d`  
		Last Modified: Wed, 15 May 2024 21:54:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
