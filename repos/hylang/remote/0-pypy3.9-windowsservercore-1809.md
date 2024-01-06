## `hylang:0-pypy3.9-windowsservercore-1809`

```console
$ docker pull hylang@sha256:ea7d492584bca434b6c5f9f0b0938edc09a2e960c1a67702d27fd16b04dc3d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `hylang:0-pypy3.9-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull hylang@sha256:75c376b8b8333122bc80810f721e5ad917f4fa9433288b5922d14b0734d9e632
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2112274665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04e35e23ac5e121d4872a8ba499367824f50d08c51edf724fb21a4b896c6965`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Fri, 05 Jan 2024 18:54:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 05 Jan 2024 18:55:49 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 05 Jan 2024 18:56:30 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 05 Jan 2024 18:56:31 GMT
ENV PYPY_VERSION=7.3.14
# Fri, 05 Jan 2024 18:57:15 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.14-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '9b3d8496f2a4729fdf20d9f835299902048950baad3a42019b67da75ca5b38b7'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.14-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 05 Jan 2024 18:57:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Jan 2024 18:57:16 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Jan 2024 18:57:56 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 05 Jan 2024 18:57:56 GMT
CMD ["pypy"]
# Fri, 05 Jan 2024 19:48:31 GMT
ENV HY_VERSION=0.27.0
# Fri, 05 Jan 2024 19:48:33 GMT
ENV HYRULE_VERSION=0.4.0
# Fri, 05 Jan 2024 19:50:53 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 05 Jan 2024 19:50:53 GMT
CMD ["hy"]
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
	-	`sha256:343b2dd58f2966c80eb4fdb9b3f78212c0fc137e757fad9d1d50b0b7870a6070`  
		Last Modified: Fri, 05 Jan 2024 18:58:04 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837c83195671dfc3b90b1a7d2cce80844b693326efb1a3fd8733fc6aedd99ee8`  
		Last Modified: Fri, 05 Jan 2024 18:58:04 GMT  
		Size: 502.6 KB (502559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e73bbd0762908b1f149ecc8fd70d2d92c74c3de6485133f5492e9ddabc2d115`  
		Last Modified: Fri, 05 Jan 2024 18:58:05 GMT  
		Size: 15.5 MB (15532370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3492fa8574aaca897a08991087e3d8bc3a75e093276998ff979a8ef895eaba`  
		Last Modified: Fri, 05 Jan 2024 18:58:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90548dae65c1b214a49d03095add22a938b4f3d1edaf01798183e693fdab86e8`  
		Last Modified: Fri, 05 Jan 2024 18:58:05 GMT  
		Size: 27.5 MB (27547953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6465bac6de0e3fcf8f19431a2bdaff844e7d6268f88bf8d865bcdb71f0b8c38`  
		Last Modified: Fri, 05 Jan 2024 18:58:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04aefd4405dcbeff4e838388e387b6b02823288443f47be3412f25e17151f44`  
		Last Modified: Fri, 05 Jan 2024 18:58:01 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24f5c9ac0e0447abd8ba65df321eb5443a50ddcbfd8943758a57483b994fde`  
		Last Modified: Fri, 05 Jan 2024 18:58:02 GMT  
		Size: 3.9 MB (3887612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ddaba5df4a2abf4caf5fede45849b5f72a113a00a3cc7b009bca8acec4dc84`  
		Last Modified: Fri, 05 Jan 2024 18:58:01 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61de2828d0565addcb0e52c6b3b2ebd127add6c3afc204aba219ec81db8b150f`  
		Last Modified: Fri, 05 Jan 2024 19:50:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd76c9abfc0f5011a810f9f53add0828536e0929e40ec0ffa3a5f3ee7c34d3c`  
		Last Modified: Fri, 05 Jan 2024 19:50:56 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5b34ee3e44346d3911e5a2fe95f3f17432b3100e16113433367373b895b7c7`  
		Last Modified: Fri, 05 Jan 2024 19:50:57 GMT  
		Size: 5.1 MB (5084680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ac853540e2f2531bc05a817c259650ee353e73b91a229cff1584b7897949b`  
		Last Modified: Fri, 05 Jan 2024 19:50:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
