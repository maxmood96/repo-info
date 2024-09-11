## `hylang:pypy-windowsservercore-1809`

```console
$ docker pull hylang@sha256:f31ea9cd1dc1d8aecdc00217546eac465ecf22f0f582f1a54a3dfaa745e1327c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `hylang:pypy-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull hylang@sha256:167684116c5db496ef52df7e9509f662aac51a49d8118fb292e8d3a038d448a3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1773700207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630159007b05a67ad97ad61ef5a18c3d1778ca0b85dceea890d6c5fdb602aa37`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:05:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:05:22 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:54 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:05:55 GMT
ENV PYPY_VERSION=7.3.17
# Wed, 11 Sep 2024 00:07:45 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.17-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'cab794a03ddda26238c72942ea6f225612e0dc17c76cac6652da83a95024e6e8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.17-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:07:47 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 11 Sep 2024 00:07:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 11 Sep 2024 00:08:24 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:08:24 GMT
CMD ["pypy"]
# Wed, 11 Sep 2024 02:08:18 GMT
ENV HY_VERSION=0.29.0
# Wed, 11 Sep 2024 02:08:20 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 11 Sep 2024 02:09:23 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 11 Sep 2024 02:09:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f50f0a6841306396beedd592c8c805f7bd62c11fb8f64b1d26c65abc72f7a6`  
		Last Modified: Wed, 11 Sep 2024 00:08:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f6633fe81d423773822716e6ea3d812d325f81038b9324b70939a94c5ea33`  
		Last Modified: Wed, 11 Sep 2024 00:08:28 GMT  
		Size: 333.2 KB (333231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4079cda8af652a86f6b8d6ebb4077cf61e6b9568af3aeea8567039714e9f5a`  
		Last Modified: Wed, 11 Sep 2024 00:08:30 GMT  
		Size: 15.5 MB (15502992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac8c68b232cfee63cb42b709a1ad052b52eeaba022e1611b842c40f4583a12f`  
		Last Modified: Wed, 11 Sep 2024 00:08:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f425305633bb6742974da66a8810042de75a72562000926437bd87e4fcda8a`  
		Last Modified: Wed, 11 Sep 2024 00:08:31 GMT  
		Size: 26.4 MB (26430019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513661c61e6e23f066ee7653148cae24ed1853a12ab13f8ea282fff1e59539f7`  
		Last Modified: Wed, 11 Sep 2024 00:08:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43efd8ea8e68ca6760bc2ed90a158806cf507171076867979c4279837579a42`  
		Last Modified: Wed, 11 Sep 2024 00:08:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60051a8e84cc9aaa70d6e144bdb56ab3e64655ef6f1a3b63051a9a5efa87cd6c`  
		Last Modified: Wed, 11 Sep 2024 00:08:28 GMT  
		Size: 3.9 MB (3900788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc20928c89ccc11f0e9bb7c1e1d769fa4c05807222945c3636c8b189927c4d`  
		Last Modified: Wed, 11 Sep 2024 00:08:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716b5d0c7f632cd43431b680c8e04043df8dc1964402ea37a04fba1a13447e64`  
		Last Modified: Wed, 11 Sep 2024 02:09:26 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162cb50c158d13b6909e6822017f9808f2879d7e70d09db6b17f0bf55f313d7d`  
		Last Modified: Wed, 11 Sep 2024 02:09:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0be10925822ae24f04e39db715913493f9cb6efecbbca97374d4835f2fb89dd`  
		Last Modified: Wed, 11 Sep 2024 02:09:27 GMT  
		Size: 7.3 MB (7254434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e11c322a8703440cac414c3ade6883c0ddf3c77b54deae29cf053e7f0468c51`  
		Last Modified: Wed, 11 Sep 2024 02:09:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
