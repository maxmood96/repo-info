## `hylang:0-pypy3.9-windowsservercore-1809`

```console
$ docker pull hylang@sha256:4913eae8727c37f8fb5a445ce88906a9387950fe0f9aa9d9f03dc62d68937a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `hylang:0-pypy3.9-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull hylang@sha256:1c8d36421f2de7c9d1f2def25439dc37457c6929d10b0f6fd70c2b25cbcc31ac
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2122340127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafa1d85ddbb21efb968f204950eb41f11c4f8c1a4d62517bd0243bf0727652e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 17 Jan 2024 00:18:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Jan 2024 00:20:29 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 17 Jan 2024 00:21:03 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 17 Jan 2024 00:21:04 GMT
ENV PYPY_VERSION=7.3.15
# Wed, 17 Jan 2024 00:21:44 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.15-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a156dad8b58570597eaaabe05663f00f80c60bc11df4a9c46d0953b6c5eb9209'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.15-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 17 Jan 2024 00:21:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 17 Jan 2024 00:21:46 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 17 Jan 2024 00:22:25 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 17 Jan 2024 00:22:26 GMT
CMD ["pypy"]
# Wed, 17 Jan 2024 00:56:21 GMT
ENV HY_VERSION=0.28.0
# Wed, 17 Jan 2024 00:56:23 GMT
ENV HYRULE_VERSION=0.5.0
# Wed, 17 Jan 2024 00:57:58 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 17 Jan 2024 00:57:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0392cf644bf5d4e63b9d2d7fd94df9f0a8a49ce69c277eeee3eee89199a3603`  
		Last Modified: Wed, 17 Jan 2024 00:22:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72e853e0f55db9c7c0d13571981b2b79197f3884322a3902726da6535967eaf`  
		Last Modified: Wed, 17 Jan 2024 00:22:30 GMT  
		Size: 493.6 KB (493619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4153db4b7b6edbe0e906c46fa6278aa361cbdd1d7871a559025091a2ab9163`  
		Last Modified: Wed, 17 Jan 2024 00:22:31 GMT  
		Size: 15.5 MB (15522902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e393f1bf90954fcc5cf96f4fb93a7cd1043eb72a2bbfc48a207a71146a81c0c`  
		Last Modified: Wed, 17 Jan 2024 00:22:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e197778f307375a523c988848f35d122221e4a6a56a999031831b07e8fcb35`  
		Last Modified: Wed, 17 Jan 2024 00:22:33 GMT  
		Size: 27.6 MB (27576958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc18a5899caf6fbf9bd254b94eb7d22a813accd9dea719cb79d042b9515c2492`  
		Last Modified: Wed, 17 Jan 2024 00:22:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50bc2cd79bc24841db6d3e00645aadc2f3e525c44064ac9e8e08b07929f8b20`  
		Last Modified: Wed, 17 Jan 2024 00:22:29 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1959bdff94d59a0f731cddba8887d5449433a9cdbd14cdb111d71b83521572`  
		Last Modified: Wed, 17 Jan 2024 00:22:30 GMT  
		Size: 3.9 MB (3916896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2425a6940a1592bc6497a101c69be666b495c6ae7966c20b407d703a67bf17`  
		Last Modified: Wed, 17 Jan 2024 00:22:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd611c331385fd4e121ed33022d28ee079155cbf7ee3b654ce2c023346a88419`  
		Last Modified: Wed, 17 Jan 2024 00:58:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474e91fe787aace25e1dbbb010009300b996b2fd756153e69a9dda9d385dd38`  
		Last Modified: Wed, 17 Jan 2024 00:58:03 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a5f5a2dfa64abfdc275f26d5e3e1be6248cf20313c94656af0ba44475f873`  
		Last Modified: Wed, 17 Jan 2024 00:58:04 GMT  
		Size: 5.1 MB (5096819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d84ea02a1af2d5bcd107d7a905c0f81a21e282496d7381ad61c7b610df0eb1`  
		Last Modified: Wed, 17 Jan 2024 00:58:03 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
