## `python:windowsservercore-1809`

```console
$ docker pull python@sha256:806eacd24141213c5448588954a47e3ffc0b2a7b122383055ae35cee37048954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `python:windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull python@sha256:7abc64560691c0428e24a58f48bfa9c3159e9d2f41ea47570a389f20fe8e3b08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298326330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8a85d8ba707a84d92344b36ac2baa9e10a5d541cba47ad499d00d69e4f9dba`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Fri, 02 Aug 2024 14:34:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 02 Aug 2024 14:34:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 02 Aug 2024 14:34:50 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 02 Aug 2024 14:39:55 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Fri, 02 Aug 2024 14:39:56 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 02 Aug 2024 14:39:56 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Fri, 02 Aug 2024 14:39:57 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Fri, 02 Aug 2024 14:40:38 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 02 Aug 2024 14:40:39 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1367d384888610faccbb8f525001a77c9cc3c5b07134a45b86d6f989056902`  
		Last Modified: Fri, 02 Aug 2024 14:40:45 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6229040263263579e7ffe84a05f1f35a5002854d65ba5080449b4ce9be334bcc`  
		Last Modified: Fri, 02 Aug 2024 14:40:45 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae9b4fde544fc1e6cf7693b7fbb4b5fbb1be028c82bd8386fecfc9e60fc8442`  
		Last Modified: Fri, 02 Aug 2024 14:40:45 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6e16aa3cc88ce9285353288dde07f7205bb48d52e8a44b8f51bc2677e31c72`  
		Last Modified: Fri, 02 Aug 2024 14:40:49 GMT  
		Size: 48.8 MB (48787967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601f82c2ada8e4a87e8e1b380e708f8af4ea23f5677368a4ac50f8bfc16ec06c`  
		Last Modified: Fri, 02 Aug 2024 14:40:43 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e60837a2e0fe54aa061aa1eb58f2368832ed064ccfa447bb0857bf599d7992`  
		Last Modified: Fri, 02 Aug 2024 14:40:43 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74eda95f84d14eed47ffba8fb4f5e52c4147f0f95969280bdba22a9e2bde43d`  
		Last Modified: Fri, 02 Aug 2024 14:40:43 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c6e45ad30e9438918a3d9e9ccfbc60dd4b461c29186c25d77b4d4e31e1a122`  
		Last Modified: Fri, 02 Aug 2024 14:40:45 GMT  
		Size: 11.1 MB (11099441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980f33a0b5d4438c0a1ec6fba9c53262db84d639f0d28e40896b2b9fed31e003`  
		Last Modified: Fri, 02 Aug 2024 14:40:43 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
