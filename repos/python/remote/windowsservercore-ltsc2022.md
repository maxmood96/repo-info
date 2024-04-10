## `python:windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:46a8689e99312a7b0ca3539c8ea14c6953c709902a93e66ec4d43b2ee9a0a0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `python:windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull python@sha256:9157060d90585e216c35871ea374dab7ca790c54b4093660f7635cbc62a5194e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2059326254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fe7464c69c01faf5eba34087555e1181e2dc0142d962095f45945dbea254b5`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:18:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 10 Apr 2024 03:26:03 GMT
ENV PYTHON_VERSION=3.12.3
# Wed, 10 Apr 2024 03:27:22 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 10 Apr 2024 03:27:23 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 10 Apr 2024 03:27:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 10 Apr 2024 03:27:25 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 10 Apr 2024 03:28:23 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 10 Apr 2024 03:28:24 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb93bd91ebaca1f8ca1935d71220a97a995164ec557ee8f0c159d1e3a79e0db2`  
		Last Modified: Wed, 10 Apr 2024 03:39:59 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175b67d83ca32d2e1856965a4c502511ebb5a6cb4a2d40138e454285e1d83c2d`  
		Last Modified: Wed, 10 Apr 2024 03:40:33 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9e4d910d24bd0e8d60986ee9bc3d81a4cb1bc838d6894dcc2facdb1a2bbd15`  
		Last Modified: Wed, 10 Apr 2024 03:40:40 GMT  
		Size: 48.6 MB (48621079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5e3151b9cd395324c57c423b425e14e356cd748869def74b27836051f5ce21`  
		Last Modified: Wed, 10 Apr 2024 03:40:31 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e188e23c2c1b0877eb526f4f1525b1a0fcede90afd293b55c799ace69cc7f688`  
		Last Modified: Wed, 10 Apr 2024 03:40:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37490d1a4419d22bdd09b400301584aa4e70791735ee6b8646db3a0dd7a7468`  
		Last Modified: Wed, 10 Apr 2024 03:40:31 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e436775cb090408d1c7c598f88936137d805a704950399e80a62afb901347f`  
		Last Modified: Wed, 10 Apr 2024 03:40:34 GMT  
		Size: 11.3 MB (11321556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7225df3f6d2e03ad7c6db9a613628d10ec4de6a5bfa7132e54c07f7368ad044`  
		Last Modified: Wed, 10 Apr 2024 03:40:31 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
