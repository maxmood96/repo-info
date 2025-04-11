## `hylang:pypy3.10-windowsservercore-1809`

```console
$ docker pull hylang@sha256:e42fab6282ca150cf1ed78549ddea1b5289f03fff7b70bbe2b74fe977208bfa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `hylang:pypy3.10-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull hylang@sha256:f45b3241ef9984869f99d3c51490a9cad3f9461c54b03082da168da205ecc59f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216080121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b96139596de5b202ee940158582a52b76b0c191f5e73f07a2cbbce15effc29f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Thu, 10 Apr 2025 21:49:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Apr 2025 21:49:46 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Thu, 10 Apr 2025 21:50:01 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Thu, 10 Apr 2025 21:50:02 GMT
ENV PYPY_VERSION=7.3.19
# Thu, 10 Apr 2025 21:50:37 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'c0d07bba6c8fb4e5804f4a8b3f8ef07cc3d89f6ad1db42a45ffb9be60bbb7cc2'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Thu, 10 Apr 2025 21:50:38 GMT
CMD ["pypy"]
# Thu, 10 Apr 2025 22:14:19 GMT
ENV HY_VERSION=1.0.0
# Thu, 10 Apr 2025 22:14:21 GMT
ENV HYRULE_VERSION=1.0.0
# Thu, 10 Apr 2025 22:15:40 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 10 Apr 2025 22:15:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe01f61f68fc05dbf54215b67ce05c18fa436819f4bb43b75b19382b8513ebc`  
		Last Modified: Thu, 10 Apr 2025 21:50:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8393983ee26b938a29105baf1999cefdf70ae0c249544efc67b78539c11ffa`  
		Last Modified: Thu, 10 Apr 2025 21:50:43 GMT  
		Size: 329.6 KB (329593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5969cc41a95c0e09943995489f6877abfc47728f32f75023317747042f4d9c3e`  
		Last Modified: Thu, 10 Apr 2025 21:50:45 GMT  
		Size: 15.5 MB (15496407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e84a935ab0ba96f39442ace1509443e42666ca69ea0f03183a45411a0d129cb`  
		Last Modified: Thu, 10 Apr 2025 21:50:43 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe11e284db2b1ccb021a3f8c0e6a3a8f36ed59538e7dbd09fa39f00e7c0e0d2`  
		Last Modified: Thu, 10 Apr 2025 21:50:47 GMT  
		Size: 30.3 MB (30254406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9929f12dcecbcee630508ded70c008e2a2d5e98b2b1567659406f20cb89fd61a`  
		Last Modified: Thu, 10 Apr 2025 21:50:43 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd3c15811fb277d263c57e5fcd50a9901e3e792de88341cdc9ce4bc491873a2`  
		Last Modified: Thu, 10 Apr 2025 22:15:45 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbf3fec2836aa1ef12813bd260399853a7392c1c9142d6733a527d62d3176ae`  
		Last Modified: Thu, 10 Apr 2025 22:15:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7eda4133decd3fa3c0a2decb5e57f913c1da85fa1d18c569accd26c23f1f10`  
		Last Modified: Thu, 10 Apr 2025 22:15:46 GMT  
		Size: 7.3 MB (7266137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569a9cc1869005c4c0f55b1a80ae8806cc7a09e87b36e78215dc69db884650f5`  
		Last Modified: Thu, 10 Apr 2025 22:15:45 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
