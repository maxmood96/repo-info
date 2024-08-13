## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:5bdab681915914146b29440430fe5ce61dc78fd04db039b71923eacb8c4eb483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull julia@sha256:2f7b9d7e855a01b053946329b95c1cc8013f3d9f38ff5635890085f5ccf377e9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2432631492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0a9ebd0906f1c10c31b5d7d834e07df5763b423429fb37c495ddd099776842`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:07:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:07:44 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 13 Aug 2024 20:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.4-win64.exe
# Tue, 13 Aug 2024 20:07:47 GMT
ENV JULIA_SHA256=c1b659abc90991dcbdf461f33cae483501da736fc223c11d4c51f337338ccb21
# Tue, 13 Aug 2024 20:09:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:09:02 GMT
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
	-	`sha256:466660ab88f39644bf2424a39259379c6086eb48b2d953dacaf09aaa733b651b`  
		Last Modified: Tue, 13 Aug 2024 20:09:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9a0170b18a1d2902f05f758d754e7fde53b62a0b733a5f2e3871feb0d74416`  
		Last Modified: Tue, 13 Aug 2024 20:09:07 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cc82bf302859215f03f2747b5e3710582e58a8b040fbf54e41cc2a1269e795`  
		Last Modified: Tue, 13 Aug 2024 20:09:07 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7c70c01270ef25ae24ff8b7b09f910de1bd12b9a2079f404f9e081a244e54a`  
		Last Modified: Tue, 13 Aug 2024 20:09:07 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d85cbf1002fb6640e6e56bf81c86b1e3a29c4e0303a79fa707b84b08016126`  
		Last Modified: Tue, 13 Aug 2024 20:09:32 GMT  
		Size: 187.4 MB (187421769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc75a49c3d92e9cb3c5f5d799aecc6d03e5eeeb26bb593f92786869ee28510b`  
		Last Modified: Tue, 13 Aug 2024 20:09:07 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
