## `python:windowsservercore-1809`

```console
$ docker pull python@sha256:713ad154d2b6a2df354905c29ff1dff40e2ec4e251527094054db4b02a40018c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `python:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull python@sha256:35702297be9bd0944fb283d918f0e29664ca90d8a90769b97ee42ad63f9b7494
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2127976514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e05f00424401348bfb7ae974a8b0ff838bacd2387e5cd985e7850d5ba0218dd`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 02:35:23 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 11 Jan 2024 02:41:21 GMT
ENV PYTHON_VERSION=3.12.1
# Thu, 11 Jan 2024 02:43:22 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 02:43:23 GMT
ENV PYTHON_PIP_VERSION=23.2.1
# Thu, 18 Jan 2024 23:23:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Thu, 18 Jan 2024 23:23:59 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Thu, 18 Jan 2024 23:25:33 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 18 Jan 2024 23:25:35 GMT
CMD ["python"]
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
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a491646982432d4312b04d714667aa0b0b0cfbf9d62f2d5508036a058e351d`  
		Last Modified: Thu, 11 Jan 2024 02:52:29 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8e4bed9b454791284f7d7388432c3d03d585106ad726c0a592af96c75ea950`  
		Last Modified: Thu, 11 Jan 2024 02:53:07 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90856a008ace3e356cdbba2237dbb7041aaf50f504e4af16289d54632c439ee`  
		Last Modified: Thu, 11 Jan 2024 02:53:13 GMT  
		Size: 48.6 MB (48584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b17f995e1b4fce6518d2bfc74d6d21bc1b81c199dfcff3e197eaf12966777`  
		Last Modified: Thu, 11 Jan 2024 02:53:05 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29ea0c6acf0971211aac54680a069026f67e9faddcb5182d9f51cb7a3af75b4`  
		Last Modified: Thu, 18 Jan 2024 23:29:45 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5593731bc3d4a5a8f9500501fa6940506e0025c52a0c41793a9348d164ad6c`  
		Last Modified: Thu, 18 Jan 2024 23:29:45 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9c1e4ab96adddf7f6f13360d721db1600654d29ccb4e3420538fbfb843acf6`  
		Last Modified: Thu, 18 Jan 2024 23:29:48 GMT  
		Size: 9.7 MB (9660080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8883277267d096511abdc166aaa53dd927e0b450f063f19eaa21d5fc5a5d74a7`  
		Last Modified: Thu, 18 Jan 2024 23:29:45 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
