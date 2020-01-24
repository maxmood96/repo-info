## `hylang:0-python2.7-windowsservercore-1809`

```console
$ docker pull hylang@sha256:8529ec6bc52fa8e6c21d15a0db5b340c43c03b8212c197fc7fcb4809161cd8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `hylang:0-python2.7-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull hylang@sha256:78d497e7048cc0a15fece723440be59d67db35772e75e045ee0cf585e4fbb8e2
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2266335608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d53d95e792ef8f06f5c8a7139b610c1c1b13dbb78205f6a7de1025f20539024`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 18:31:45 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 15 Jan 2020 18:31:46 GMT
ENV PYTHON_RELEASE=2.7.17
# Wed, 15 Jan 2020 18:33:53 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Thu, 23 Jan 2020 22:35:49 GMT
ENV PYTHON_PIP_VERSION=20.0.1
# Thu, 23 Jan 2020 22:35:50 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Thu, 23 Jan 2020 22:35:52 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Thu, 23 Jan 2020 22:37:00 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2020 22:37:27 GMT
RUN pip install --no-cache-dir virtualenv
# Thu, 23 Jan 2020 22:37:28 GMT
CMD ["python"]
# Thu, 23 Jan 2020 23:07:16 GMT
ENV HY_VERSION=0.17.0
# Thu, 23 Jan 2020 23:07:54 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Thu, 23 Jan 2020 23:07:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991e8bf1fe43fb6d1b926596157fec820f98e6bf95f7d87c5037c6a9d454ee94`  
		Last Modified: Wed, 15 Jan 2020 18:44:46 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3061269fafccc2b8dbc758f49ebd8556e388f724ca6c14b7274e2c96eeb5b9`  
		Last Modified: Wed, 15 Jan 2020 18:44:44 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8b29109525c4a2b28a2790a4cf8dcf3e323f9aabee0ae266fe15eef2b42f3`  
		Last Modified: Wed, 15 Jan 2020 18:45:09 GMT  
		Size: 38.9 MB (38905595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6911f9f33335b178e3749845aad68618a2f7054decf6d5e443c8197cbb625906`  
		Last Modified: Thu, 23 Jan 2020 22:43:37 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f87a0c647e396990b9cfee3233cb3b2736bb13dcaa8b03f9af08cd963c782b`  
		Last Modified: Thu, 23 Jan 2020 22:43:35 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df4877f0e39feb521c11e3303829f3706f7db6b410216001473db7673149662`  
		Last Modified: Thu, 23 Jan 2020 22:43:35 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591f333898a85f27eab93dcb103e5aaa8684d2bf2c91b6512faebf950ac269db`  
		Last Modified: Thu, 23 Jan 2020 22:43:44 GMT  
		Size: 5.2 MB (5150424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a363fe4a819dbf72abdbe95846a0acf17de06011eaffe52c09a3caa9876071e1`  
		Last Modified: Thu, 23 Jan 2020 22:43:39 GMT  
		Size: 3.8 MB (3776968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ab38359abb0d9543fae0e8d228d9089dc692cf562c0e0856ea534ec5e4e0a9`  
		Last Modified: Thu, 23 Jan 2020 22:43:35 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10893b8decd414a33251644214309f118f1d2131086a1e909385a2aaa737db84`  
		Last Modified: Thu, 23 Jan 2020 23:12:56 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e1144d546fc51abc5c4aca55add809277d0c7165f707ca3813b7dcb21aa00f`  
		Last Modified: Thu, 23 Jan 2020 23:12:58 GMT  
		Size: 1.1 MB (1080813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9005bb24c8f1e1f9811d90f2f4e1582104512f88b9d370fa3e8b93b3495bb`  
		Last Modified: Thu, 23 Jan 2020 23:12:56 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
