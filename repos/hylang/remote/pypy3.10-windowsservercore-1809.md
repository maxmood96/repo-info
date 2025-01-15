## `hylang:pypy3.10-windowsservercore-1809`

```console
$ docker pull hylang@sha256:5c572ba49f423388e85cd411918480add3165825bbbd635fb9b3ee9a3b98bf37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `hylang:pypy3.10-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull hylang@sha256:be9cb9dce778196b86db6f9193ba99ff7d50d26b16e6e1f1b80283f25b26a881
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2175696202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48869b7050afa42c647188508a21b03dab51db0b158ec7e397802e471057be35`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:38:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:38:28 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:38:44 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:38:45 GMT
ENV PYPY_VERSION=7.3.17
# Tue, 14 Jan 2025 23:39:09 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.17-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'cab794a03ddda26238c72942ea6f225612e0dc17c76cac6652da83a95024e6e8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.17-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:39:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 14 Jan 2025 23:39:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 14 Jan 2025 23:39:37 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:39:38 GMT
CMD ["pypy"]
# Wed, 15 Jan 2025 18:05:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 15 Jan 2025 18:05:45 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 15 Jan 2025 18:07:13 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 15 Jan 2025 18:07:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47674fbe80c93a961e8e1d2f35f76651483d189585aeb0a65fc64996acbe40e`  
		Last Modified: Tue, 14 Jan 2025 23:39:46 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11f809650e94b8c103ce484af82006f02f1bb305627fa02e72afdc1cd0f03d7`  
		Last Modified: Tue, 14 Jan 2025 23:39:45 GMT  
		Size: 329.8 KB (329819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f1c97b06fa9a5cd8ab1d315e8457823ab44adbf0eb5a628cacb1564c831ad`  
		Last Modified: Tue, 14 Jan 2025 23:39:46 GMT  
		Size: 15.5 MB (15501473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7ce9a980ebfec3b0d491d63d775866c2fbbc405e1850834d570fccbcf3bd69`  
		Last Modified: Tue, 14 Jan 2025 23:39:45 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea57ee5984f5cc3c820dc1f86618d20509644ab16385c0f229fe217f255935b3`  
		Last Modified: Tue, 14 Jan 2025 23:39:47 GMT  
		Size: 26.4 MB (26445001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9901c9effc5b81fec33bc56e5f3d1b06c9dc3c9856953a35cb2ec7b0d961e7a`  
		Last Modified: Tue, 14 Jan 2025 23:39:43 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854543b220a5509cd5fc412356a3502c85cfa27a0e07169ccf82a9dca6c82e43`  
		Last Modified: Tue, 14 Jan 2025 23:39:43 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf234c0b58c9ab751b844ea52ce5d96f928f2d2cb837e21cfaa4f7812b408e3e`  
		Last Modified: Tue, 14 Jan 2025 23:39:44 GMT  
		Size: 3.9 MB (3918471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a92bf9524b5ec6a7fd5a14cfaac2d3e4803c1216dd1a0e67c5560deb83066b`  
		Last Modified: Tue, 14 Jan 2025 23:39:43 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b88f43a05e799fa7925223cf61fd859b9030b95b4867bd4037764fc754237a`  
		Last Modified: Wed, 15 Jan 2025 18:07:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24f939e28b160f5521820020301a640f832802ef2b20f790c9cc8922216750b`  
		Last Modified: Wed, 15 Jan 2025 18:07:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c425a31617555f344ca4525a1ddd2383eaf525d096f3136dc868be0b60c6898`  
		Last Modified: Wed, 15 Jan 2025 18:07:17 GMT  
		Size: 7.3 MB (7278500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851ac1dd24ffa381c55d9c61830e34e6135053f162b0868cc7d8e5c3cbd35dc9`  
		Last Modified: Wed, 15 Jan 2025 18:07:16 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
