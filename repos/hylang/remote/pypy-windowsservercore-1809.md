## `hylang:pypy-windowsservercore-1809`

```console
$ docker pull hylang@sha256:45985e8cc5ff7f86e07c1d0a59b5d26e7b7100205f04e1703a88ca3389035cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `hylang:pypy-windowsservercore-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull hylang@sha256:568bb3e7b49e4ba96a66e95bf860649c316910efc6cc35ea23aadae930916e2d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2761479280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efe262317218b4c8b92257168ee3f8ac8e1b1d6f51453a14d0af87b08a2668d`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 05:11:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 06:05:18 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 06:06:26 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 12 Jan 2022 06:06:27 GMT
ENV PYPY_VERSION=7.3.7
# Wed, 12 Jan 2022 06:08:08 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.8-v7.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '8ceb03d2f7b73c6ce0758290bc42ba366a45c46e033eda36f1779d957a905735'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.8-v7.3.7-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy3 --version") ...'; 	pypy3 --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Jan 2022 06:08:09 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 Jan 2022 06:08:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 Jan 2022 06:09:48 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Jan 2022 06:09:49 GMT
CMD ["pypy3"]
# Wed, 12 Jan 2022 06:40:21 GMT
ENV HY_VERSION=1.0a4
# Wed, 12 Jan 2022 06:40:22 GMT
ENV HYRULE_VERSION=0.1
# Wed, 12 Jan 2022 06:41:45 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 12 Jan 2022 06:41:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3a70d5fd54e2005efbf590b48700ed40509210354a0d8f3f18c3b444a5325896`  
		Last Modified: Wed, 12 Jan 2022 06:20:33 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588c2f13f9e5198f186b49f0a89b7fe43976588aa49eef301e3b122b8e359d70`  
		Last Modified: Wed, 12 Jan 2022 06:20:30 GMT  
		Size: 342.7 KB (342693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ad434722057555cb6f58a610ece746ab594b3557e5725a1bd190ad09087dfb`  
		Last Modified: Wed, 12 Jan 2022 06:20:33 GMT  
		Size: 15.5 MB (15479273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fff006c7f9539d6d8b14c0ec2c37a93414936a2bcec0fddce5f2eb77d8fc9d9`  
		Last Modified: Wed, 12 Jan 2022 06:20:30 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65bc7e83a76ef5f5aa64b977de8ff493c1eb34cb57858f8aae2b008f0ff70b1`  
		Last Modified: Wed, 12 Jan 2022 06:20:36 GMT  
		Size: 27.0 MB (26977887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f860d81274a083523e76a9c5d63c4739922b4e96d501feda27327bdabdfe1f`  
		Last Modified: Wed, 12 Jan 2022 06:20:27 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04225d0aeb99fd52f0bce3bb3e5ea0df433dfedbc21b6f38d0c4bb3fb8d063c`  
		Last Modified: Wed, 12 Jan 2022 06:20:27 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50489fccd7578d6e6033cebdc27597e57b39258e440766a6393c5766bdd094a`  
		Last Modified: Wed, 12 Jan 2022 06:20:31 GMT  
		Size: 2.9 MB (2926189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d64d9bf524853a617ced356c1e9898510fdfbcb4b0b00dfcb13dff7329b29c2`  
		Last Modified: Wed, 12 Jan 2022 06:20:27 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd55993be400e24b6ca3dc4750cbe9a747c319e9b6f185b03f42ae21a270b14`  
		Last Modified: Wed, 12 Jan 2022 06:44:50 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c26ed045dbfd43f165a83d07c0f46ee884f486865a742680c9e615a310b38c9`  
		Last Modified: Wed, 12 Jan 2022 06:44:51 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc690253a07c6ac4bedcb06af5ef25318133153e722c567afa0456012401087`  
		Last Modified: Wed, 12 Jan 2022 06:44:55 GMT  
		Size: 3.5 MB (3510964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26789f8b8251590e082c49a221efc1ae5724f6a63586f4aaa82286b00dec8eb`  
		Last Modified: Wed, 12 Jan 2022 06:44:51 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
