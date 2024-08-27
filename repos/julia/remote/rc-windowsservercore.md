## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:e3328aa33ab766b06571b18fac3fad4555c2ebe8ea582a668556447151c53fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `julia:rc-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull julia@sha256:e0d4f45b321751c09c6c88c51f09e70583b6de82ea3f532909984c377554d15a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2393920065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82309e195a465d7f44b29ced1b57fc0fbef25db259e8b0a8da42af49d2909d9b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 27 Aug 2024 20:04:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 Aug 2024 20:04:40 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 20:04:41 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc3-win64.exe
# Tue, 27 Aug 2024 20:04:42 GMT
ENV JULIA_SHA256=c8cf68a67216205306760cf5c0adbbaa281a859a61483409e9320b0e8c8ce605
# Tue, 27 Aug 2024 20:05:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 27 Aug 2024 20:05:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1ec36eed7919deb97704658849dfc031f34d2369f05b10e9b9d3b63dd89dc0`  
		Last Modified: Tue, 27 Aug 2024 20:06:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e88df49064c34265f709d07ffae1b96143fd8f6e00f6916386785b838155ad`  
		Last Modified: Tue, 27 Aug 2024 20:05:59 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd37384f48b942098e55f5d2fcb3232783393a4bdd92eddfee327fd6ec8bf11`  
		Last Modified: Tue, 27 Aug 2024 20:05:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e730dad64bf037b7a7f0a3ae8692c551860ccb8b971e7cadff3204eb3fc50b`  
		Last Modified: Tue, 27 Aug 2024 20:05:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b37702a0f31e4e1096e8f384cff63773ea93abbfbffc2c3dbfdc2a44e1bb71`  
		Last Modified: Tue, 27 Aug 2024 20:06:31 GMT  
		Size: 252.1 MB (252148644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee05a32a382dbae44aec3a5d8a883f81403eba80e9396c99cdf9f834fa75d2a1`  
		Last Modified: Tue, 27 Aug 2024 20:05:59 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull julia@sha256:e87f65e4ae843949fdb7b111836aa61baa9be549855b5547b89f0f6b6b96df80
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2497474476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bdbbfce3254360fb6216ee173a0d386973e6452a5ffa9546aacfaa06549c97`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 27 Aug 2024 19:56:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 Aug 2024 19:56:03 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 19:56:04 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc3-win64.exe
# Tue, 27 Aug 2024 19:56:04 GMT
ENV JULIA_SHA256=c8cf68a67216205306760cf5c0adbbaa281a859a61483409e9320b0e8c8ce605
# Tue, 27 Aug 2024 19:58:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 27 Aug 2024 19:58:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e41993097840a6f84ef1f126e6db081e1a8ad55f7f89d4b157382cde7a180fc`  
		Last Modified: Tue, 27 Aug 2024 19:58:52 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0115fd5fa2c2d05059d08ecaabb6269d74d6d2c4b5860f85c7c8e5481f29be6`  
		Last Modified: Tue, 27 Aug 2024 19:58:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c12cc15a7f0bb45833f020c942e01d783cee0547462f94ad360e05e96e79c2b`  
		Last Modified: Tue, 27 Aug 2024 19:58:50 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5d1e2c8d818160dd29c0e37dabc52855165e6d35c6732f5a686adefaeda787`  
		Last Modified: Tue, 27 Aug 2024 19:58:50 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76898a9dd96fe3582db7c090ba6f3eadd4f8198f89a681311600dc65a6cdfd60`  
		Last Modified: Tue, 27 Aug 2024 19:59:20 GMT  
		Size: 252.3 MB (252264784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c691d0511554e576cfad409beeff1511f20ad67e774025923ff6b2d3752c46e2`  
		Last Modified: Tue, 27 Aug 2024 19:58:50 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
