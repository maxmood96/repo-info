## `python:windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:9df72b3ac7f8c1e6b485bce0dbc82dae876629065f3856402f61d0e1a91cef79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `python:windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull python@sha256:dfe37173bc536df83a7234d04b758341956b185c3f756e82cb7a3b44aa64e5e1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178273324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965906f5363c728a77a5183577e9513d84eaf96542797e8dabefcd8a80caea9e`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Thu, 27 Jun 2024 00:11:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Jun 2024 00:11:11 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 27 Jun 2024 00:11:11 GMT
ENV PYTHON_VERSION=3.12.4
# Thu, 27 Jun 2024 00:11:47 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Thu, 27 Jun 2024 00:11:48 GMT
ENV PYTHON_PIP_VERSION=24.0
# Thu, 27 Jun 2024 00:11:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 27 Jun 2024 00:11:49 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 27 Jun 2024 00:12:05 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 27 Jun 2024 00:12:05 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344694d52138a4fe45ba14b1c42eec63de90655517a2d4264f79a24c2f7c319d`  
		Last Modified: Thu, 27 Jun 2024 00:12:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e6b38fc7502259bc41ce7828500cb8ea9190bbb5cbdd2630c2fa744bf12f20`  
		Last Modified: Thu, 27 Jun 2024 00:12:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18483a19e4063625db50066b4e3ad55cf49afc65535bb7e4952a316cc788860b`  
		Last Modified: Thu, 27 Jun 2024 00:12:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20557e6a8361cf9568bc9e14cb6a3eef59762629b4061a765a6cea6f845d9e8`  
		Last Modified: Thu, 27 Jun 2024 00:12:12 GMT  
		Size: 48.6 MB (48579306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc0d0246c3697e6c0ff808b194bb6b2760401e5ed6baa9f6e91b8682224268a`  
		Last Modified: Thu, 27 Jun 2024 00:12:08 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a7622a69242ee332e3af88bdc571712d1360b051d01e56d09a22f3cffd45c5`  
		Last Modified: Thu, 27 Jun 2024 00:12:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd81cc02daec9707cbbac49a409bc0ed24c3e1f66bf6f12aea81f3bc30b5c13`  
		Last Modified: Thu, 27 Jun 2024 00:12:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb9c96ab9671761fb7147a896c45a633858d196dd26a62a5bbfbb8d4669b1f`  
		Last Modified: Thu, 27 Jun 2024 00:12:09 GMT  
		Size: 11.5 MB (11494719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bebb676d364b5f75bb602f057c79a244680080946c6b18451148c4c27a0103`  
		Last Modified: Thu, 27 Jun 2024 00:12:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
