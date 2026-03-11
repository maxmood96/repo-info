## `hylang:pypy-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:c7438dc134990d26a9560045676c4b9c73fa461f3b5487e43bc4e7912c64fd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `hylang:pypy-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull hylang@sha256:3eb6928ff1cd6d1e3b9373b150038613148605616edd19579daf7653d38c01c3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136367332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc729a2807d3f3918c1987011d23b88af80e08f5f7c93110f97d9413e58c05fb`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 21:58:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:08:22 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:08:31 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:08:31 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 10 Mar 2026 22:09:04 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:09:05 GMT
CMD ["pypy"]
# Tue, 10 Mar 2026 22:45:33 GMT
ENV HY_VERSION=1.2.0
# Tue, 10 Mar 2026 22:45:34 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 10 Mar 2026 22:46:15 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 10 Mar 2026 22:46:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81554eae26db4c1974c22c8ad6c1f1d41dab3672c63880fb71e3821a8288fe2b`  
		Last Modified: Tue, 10 Mar 2026 21:58:52 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d1f0204c8e29ea0299f6fb22fd91a3fffc3468121d8f8b5923e58d8a0ec63`  
		Last Modified: Tue, 10 Mar 2026 22:09:09 GMT  
		Size: 346.5 KB (346464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6fca2f5d4863c7e444fa5e52d5b5c4ed971a5b522dbdc6a306e2b75f2fc934`  
		Last Modified: Tue, 10 Mar 2026 22:09:13 GMT  
		Size: 15.5 MB (15527831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94542ab02e4573ceba22e3858865eab76982ef74a6ef22e6cacb1a3bab06316`  
		Last Modified: Tue, 10 Mar 2026 22:09:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea0ffc4fc899d3612252f739e174fdb14d9a065d89c0fd82b882e95e0f79d0a`  
		Last Modified: Tue, 10 Mar 2026 22:09:13 GMT  
		Size: 30.7 MB (30664379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e32a224a56f4a048ba721bf0b172029e4b0788dd54e4f9e765d146064693ab9`  
		Last Modified: Tue, 10 Mar 2026 22:09:09 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509be946ece288d9ff6f63a4e1f548ca5a53288460b20f746f889149889a40c0`  
		Last Modified: Tue, 10 Mar 2026 22:46:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984d0b860e6d2a68044eb8fedf736044ea8bb6235062ac17fca864a6eec0da55`  
		Last Modified: Tue, 10 Mar 2026 22:46:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56913f2af3e47c413930fa6597dd915c8c881d288c3b50a0a29a349378b8abb`  
		Last Modified: Tue, 10 Mar 2026 22:46:22 GMT  
		Size: 8.6 MB (8624708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94dfa415d51a8d7f35ce239fdcc011a91197d6d88c3a0130d29a80f76f6e850`  
		Last Modified: Tue, 10 Mar 2026 22:46:20 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
