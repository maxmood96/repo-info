## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:01fe914f4006ed1e78101eb08e3324d2543f8d194312f5bba28ea45e7f9c1da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.4652; amd64

```console
$ docker pull julia@sha256:6cf6e5ecbeee13d32d72c81aa7b7819219bdaf34b8a31490bc8dc63cf2ad690d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3776720762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321017c9c9cef89c3c74075b49605d12dbf2a4afef9e8fda889a4388f1e1a0ab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:09:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:47 GMT
ENV JULIA_VERSION=1.11.5
# Wed, 09 Jul 2025 18:09:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Wed, 09 Jul 2025 18:09:52 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Wed, 09 Jul 2025 18:11:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:11:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc2722fd5deff120f9d9394364399fe735fcf97df486389025afef39919a581`  
		Last Modified: Wed, 09 Jul 2025 20:02:31 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a3bec0451b9a6ea3fbd83f2ec0a66dad989bea2ccc534b55531e73bb498932`  
		Last Modified: Wed, 09 Jul 2025 20:02:31 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a58ceb0d30cb71fec73207f1566a08638d127b1f6cbfd18c633c6e6e77516f7`  
		Last Modified: Wed, 09 Jul 2025 20:02:31 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26924396c896f1291c0d2e9a6788038903e861146f2ff0444a1954e4cf23ed4`  
		Last Modified: Wed, 09 Jul 2025 20:02:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc630654b377065bef7799f429ef29159ce19d9e3b247834af34290137a550a`  
		Last Modified: Wed, 09 Jul 2025 20:02:48 GMT  
		Size: 285.5 MB (285540819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ca702f1646e803e90514cd5cdeeffc0dd54123efc2fa084922d94984e1a9a6`  
		Last Modified: Wed, 09 Jul 2025 20:02:32 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.20348.3932; amd64

```console
$ docker pull julia@sha256:33c7ea7f1899c7988bd66ab55b15039695d6515e78306b464d59701fbafcbcd9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2566074422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5373554de82728c9892fb652a562ca80f6e65dc5a7f4ee2733089b6c8e2e548a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:08:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:08:04 GMT
ENV JULIA_VERSION=1.11.5
# Wed, 09 Jul 2025 18:08:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Wed, 09 Jul 2025 18:08:07 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Wed, 09 Jul 2025 18:09:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:09:45 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead664d42713c9d4b86ccb9d68c158ca48567d382409d9b6506b3a708b8fea4d`  
		Last Modified: Wed, 09 Jul 2025 20:02:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ffc3d3e05d296ab01b07dee15ffd2538e48462923f337af5c9079adc3132f1`  
		Last Modified: Wed, 09 Jul 2025 20:02:30 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a1eaa9d6d69239f4248f3822b5e01fa6b868a00b651461d12193f2387e0e85`  
		Last Modified: Wed, 09 Jul 2025 20:02:30 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61fdeed15f00013d11533e4727658bdfe894a9a5bd92bd569ace5293b925ba7`  
		Last Modified: Wed, 09 Jul 2025 20:02:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d975f3fd6bbd3097c2d9ef28fdc49f18ff77e341d2d5dce3dd1e50eaec20c7c0`  
		Last Modified: Wed, 09 Jul 2025 20:02:38 GMT  
		Size: 285.5 MB (285464469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c47749bfeee45459941d7ac292a135fd99cf884953b90576b5fcd2301acc60`  
		Last Modified: Wed, 09 Jul 2025 20:02:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
