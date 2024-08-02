## `python:windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:4f357205c4e8f0bc007cf35f0fc747d23dcc43086bd56a165fab7760b6385468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `python:windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull python@sha256:97f23821b46c6b319c8dc1255b7b2a0b9a045b4f173b3dba263bb39fa55b91dc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2200786941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd500a8573c4ca31221a98fb9e8319144e89159050a38d271fc1f06811e23eb`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Fri, 02 Aug 2024 14:33:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 02 Aug 2024 14:33:37 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 02 Aug 2024 14:33:37 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 02 Aug 2024 14:35:56 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Fri, 02 Aug 2024 14:35:57 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 02 Aug 2024 14:35:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Fri, 02 Aug 2024 14:35:58 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Fri, 02 Aug 2024 14:36:19 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 02 Aug 2024 14:36:20 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4b63dd9d97d3b0684d3fecb21a43575c60735d5e8ee2eafba47479be5ee44b`  
		Last Modified: Fri, 02 Aug 2024 14:36:26 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cffc8318ab95ae814f07dd67ccdf19831fd4b3611dbb8fbf473013380813732`  
		Last Modified: Fri, 02 Aug 2024 14:36:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b3ca145c1deddaf8604b5de5e37ef72581696427442c0f47ebef80708d795`  
		Last Modified: Fri, 02 Aug 2024 14:36:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d987cf1ab25acae7c3fe0196081b148fd384a361a214771451eb89efa54526`  
		Last Modified: Fri, 02 Aug 2024 14:36:30 GMT  
		Size: 48.6 MB (48586703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae36cafd22855a14444d7c1c48f5d6e859b00baa80e0f99c7ed2b14b52c6b4f9`  
		Last Modified: Fri, 02 Aug 2024 14:36:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2458e1fc6969f08c9aefa14cd522fd7953d75fe65efd4684a42b6aa1fa6e141c`  
		Last Modified: Fri, 02 Aug 2024 14:36:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d530fe054584f80727039ecd56d6970ada143fb3638be678d885c9efbdfa8c`  
		Last Modified: Fri, 02 Aug 2024 14:36:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4211a2b55aed3563f5d83a44000f52d1af452b65a85b4915f5da6eeff0bb951`  
		Last Modified: Fri, 02 Aug 2024 14:36:26 GMT  
		Size: 12.6 MB (12590895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6621fa0e025abaff9779343ead7da7b70db6c930768411b22115c676162d2092`  
		Last Modified: Fri, 02 Aug 2024 14:36:24 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
