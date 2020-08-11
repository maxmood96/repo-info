## `hylang:python3.7-windowsservercore-1809`

```console
$ docker pull hylang@sha256:8ea894116e0485d91ab7a26070841413812ae56e8462a9f8d73f5c246773709d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `hylang:python3.7-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull hylang@sha256:2f09d4d4ecd72a78dd8cd7fab3eebc5d5f1d667d01e419aabed9ea8c56f2f73e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2407470715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f08037209802664a11274d29e71f604b61afac8c78b4c0a17831481810b0a4e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Aug 2020 20:50:51 GMT
ENV PYTHON_VERSION=3.7.8
# Tue, 11 Aug 2020 20:50:52 GMT
ENV PYTHON_RELEASE=3.7.8
# Tue, 11 Aug 2020 20:52:37 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 11 Aug 2020 20:52:39 GMT
ENV PYTHON_PIP_VERSION=20.2.2
# Tue, 11 Aug 2020 20:52:40 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5578af97f8b2b466f4cdbebe18a3ba2d48ad1434/get-pip.py
# Tue, 11 Aug 2020 20:52:41 GMT
ENV PYTHON_GET_PIP_SHA256=d4d62a0850fe0c2e6325b2cc20d818c580563de5a2038f917e3cb0e25280b4d1
# Tue, 11 Aug 2020 20:53:34 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 11 Aug 2020 20:53:34 GMT
CMD ["python"]
# Tue, 11 Aug 2020 21:16:10 GMT
ENV HY_VERSION=0.19.0
# Tue, 11 Aug 2020 21:16:52 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Tue, 11 Aug 2020 21:16:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43065500f09f35124a5d71517aa493fd23ad75660682600f7f6b40aa7629ac78`  
		Last Modified: Tue, 11 Aug 2020 20:54:54 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bde7bc8517ef99d9997c1d31021dccf97f3fa7fae033385ba83df2191ff59f`  
		Last Modified: Tue, 11 Aug 2020 20:56:39 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f943b28901995b3c8cad70f525c4fad99ed8612aae250c0d3e6082d09f029ac`  
		Last Modified: Tue, 11 Aug 2020 20:56:39 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304785766c7e16d487d58e630249be0ce724bafeae60ec29584a2b36ed51b05f`  
		Last Modified: Tue, 11 Aug 2020 20:56:47 GMT  
		Size: 55.9 MB (55894015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3735027967443df3985a44fb14a1be29d1d0276fc58ccb56bbdafd3b3fb95396`  
		Last Modified: Tue, 11 Aug 2020 20:56:36 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb358b8243912b1321907ee017e4b5a1f84df1af8d93cf387b202a6e1e19fbc`  
		Last Modified: Tue, 11 Aug 2020 20:56:36 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbb2a424641a8f52feb9f1516aedcc2b0b6c1a3f39eb934ee5ffa4929485154`  
		Last Modified: Tue, 11 Aug 2020 20:56:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c427fb9c2e71bcefac46d412b48241e04ed5f7fa662713da06dd5b9749bebe`  
		Last Modified: Tue, 11 Aug 2020 20:56:39 GMT  
		Size: 10.2 MB (10201369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15acc3a4f0d7665a24ed4c5a88b1fdc372ab0a2e083a3af35703c060dcb8a27b`  
		Last Modified: Tue, 11 Aug 2020 20:56:36 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921ccea172d9623f2029b662d3559d3889ffd4c8e3579c2c901f91d731411fda`  
		Last Modified: Tue, 11 Aug 2020 21:20:43 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab05177fb3ccd7662a7f594bc017210a60cb10c6981b25253850708a8f5b12a9`  
		Last Modified: Tue, 11 Aug 2020 21:20:44 GMT  
		Size: 5.5 MB (5498108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da407f301771d070f527e987ab818f0a3f1dcad9400e7213c919221d46027fd8`  
		Last Modified: Tue, 11 Aug 2020 21:20:43 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
