## `pypy:windowsservercore-1809`

```console
$ docker pull pypy@sha256:f28d3af03cd1c84a7fdd1c847b630f607178dfd1de32c63dbb917e4747ae3f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `pypy:windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull pypy@sha256:0f218b80d0d1bfaedeaec3055ee08fb571f1c98a3a8a22cd9ebdb57359a08f2e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2106156872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a653afa93c93d5808a7795f50809fa6bf4a8fb1131b6e917b670ad6233a1c04`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 04:55:16 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 13 Dec 2023 04:56:32 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 27 Dec 2023 22:17:37 GMT
ENV PYPY_VERSION=7.3.14
# Wed, 27 Dec 2023 22:19:40 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.14-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '1713edd310f400935fe9a9f8fa0fd9da1a405eaf7b69564d00f437fb498327f8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.14-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 27 Dec 2023 22:19:42 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 27 Dec 2023 22:19:43 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 27 Dec 2023 22:21:49 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 27 Dec 2023 22:21:50 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e50cb20293f79a406b32eaa263b4f5f669651268c1a0e3df487e71861dc6de5`  
		Last Modified: Wed, 13 Dec 2023 05:16:30 GMT  
		Size: 448.7 KB (448728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb29b611573a92510c58084bc2cea8b24b1a036c9164a58ed86f8a5723226b2`  
		Last Modified: Wed, 13 Dec 2023 05:16:32 GMT  
		Size: 15.4 MB (15449062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d4454fb2841127291b80e273491284b3c23b7d40ed0b554ab7111c1e2a5111`  
		Last Modified: Wed, 27 Dec 2023 23:17:14 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00840fa573575b5174acc9a0f550a237e2d782ec4f9839cb96959984c3fee4ba`  
		Last Modified: Wed, 27 Dec 2023 23:17:19 GMT  
		Size: 26.7 MB (26702688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bc6c798945ab7137696c06bc19d1eda241a4c2e24715403a32b6cceb94c3e0`  
		Last Modified: Wed, 27 Dec 2023 23:17:12 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacf2bb9aa0a7af096fc42952508d7cf7e2fe20b95b558fad95116b0abb090a0`  
		Last Modified: Wed, 27 Dec 2023 23:17:12 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4a3a91cb92a50a164f2b5674480cdbe4d7ddee888d853ae2471b683c1b3b7c`  
		Last Modified: Wed, 27 Dec 2023 23:17:14 GMT  
		Size: 3.8 MB (3840485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40eb8830c907974f0fabae1a0081addca4e57be500c789feee7709dd93a8e4bf`  
		Last Modified: Wed, 27 Dec 2023 23:17:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
