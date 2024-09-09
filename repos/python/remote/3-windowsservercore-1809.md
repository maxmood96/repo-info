## `python:3-windowsservercore-1809`

```console
$ docker pull python@sha256:db3f13d0df519bd5de14586c6c18ed8e0c40b1839e7aef1bf082a988c1bef243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `python:3-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull python@sha256:715e9827280bace3be1436165fa37623723311ea64b9da168d0abac9f1c017a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2301521194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d2ed2366bd12456fddbe63fe77502c17e5f4565bf3e3fed6df36c606a4c66b`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Mon, 09 Sep 2024 19:06:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 19:06:37 GMT
ENV PYTHONIOENCODING=UTF-8
# Mon, 09 Sep 2024 19:06:38 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 19:08:40 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Mon, 09 Sep 2024 19:08:41 GMT
ENV PYTHON_PIP_VERSION=24.2
# Mon, 09 Sep 2024 19:08:42 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Mon, 09 Sep 2024 19:08:43 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Mon, 09 Sep 2024 19:09:12 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		--no-setuptools 		--no-wheel 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Mon, 09 Sep 2024 19:09:12 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195c57fadf074ae4b05cdcd4d3155ee71045e3367019ed0682ccce2cfb1c11b5`  
		Last Modified: Mon, 09 Sep 2024 19:09:19 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce7b4b1118c143bed4e5c31785d7462e51eacfa9213ca9d63ebe445e75161ce`  
		Last Modified: Mon, 09 Sep 2024 19:09:19 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e10e36d098224d57c43af514fe1dbeb6449fb16caea417a14e723e6447ae626`  
		Last Modified: Mon, 09 Sep 2024 19:09:19 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba8b6a0d0eba35ce74664720b764b278823c6494b60147b140d1bd8118cb5ad`  
		Last Modified: Mon, 09 Sep 2024 19:09:22 GMT  
		Size: 47.9 MB (47935068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e325445e8d816c585735a8c7c742bcd1b0dd83af4bc728468a875ab5753ca38`  
		Last Modified: Mon, 09 Sep 2024 19:09:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fabb392bc6487d212317776c4caa548e8d20e3d811dfd7fc08b7ba0a5be21c6`  
		Last Modified: Mon, 09 Sep 2024 19:09:17 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fffb66c983cb999c6620630cfef1a97e5bc9a6c03df6e36155452ef96a1c8ad`  
		Last Modified: Mon, 09 Sep 2024 19:09:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8546d2213b2d18effea79f1d14acf527d54f2f4fd7f35e5e8f9fc9e0bc86260`  
		Last Modified: Mon, 09 Sep 2024 19:09:18 GMT  
		Size: 8.4 MB (8373798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb1a24265a9bb4181d2854d5c38fa7f53450ffe57ad82288907659a29ec8f97`  
		Last Modified: Mon, 09 Sep 2024 19:09:17 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
