## `python:windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:49f7da65cdaaf1d0e343e2682f3d16658163769d74f04ac8b40e49fb86c4f05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `python:windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull python@sha256:e334239bcd50c675dddd5efb62764d064d0e74db51e574717af646df85a3efda
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199515092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ea176b956534597e75ed8ac59e7dec9c58f318517743772ef6ed5588e40b45`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Mon, 09 Sep 2024 17:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Sep 2024 17:58:24 GMT
ENV PYTHONIOENCODING=UTF-8
# Mon, 09 Sep 2024 17:58:25 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 17:59:50 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Mon, 09 Sep 2024 17:59:51 GMT
ENV PYTHON_PIP_VERSION=24.2
# Mon, 09 Sep 2024 17:59:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Mon, 09 Sep 2024 17:59:52 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Mon, 09 Sep 2024 18:00:10 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		--no-setuptools 		--no-wheel 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Mon, 09 Sep 2024 18:00:10 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3a7ce06a5527d3150853a87e747fc118a136f5ba23099a1c33e64efb4c649d`  
		Last Modified: Mon, 09 Sep 2024 18:00:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bda5bac3a840d05a912244303ec39bf7ecdd1a89935062700350627d70abaaf`  
		Last Modified: Mon, 09 Sep 2024 18:00:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4af161cd2ea35beb321b1de2c414c35dd9b8bf118f7738fc53c2e039f20644`  
		Last Modified: Mon, 09 Sep 2024 18:00:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c666080c71e95276aec8fd76d55ba48f945e4ea501a062504e47af44c5b05f69`  
		Last Modified: Mon, 09 Sep 2024 18:00:21 GMT  
		Size: 47.8 MB (47766057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19acd01e980911aee174d18ece7f4b56bce976692c790c3bb696964f613b3728`  
		Last Modified: Mon, 09 Sep 2024 18:00:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ed4bb6c83d694819fa009c945b776e9dc2eb72ff96eb7b99e0da4dc69f7643`  
		Last Modified: Mon, 09 Sep 2024 18:00:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2194327725a18de516a52942f2acf5f3d71fdd5ba77823ab10076e0f1dc373e8`  
		Last Modified: Mon, 09 Sep 2024 18:00:15 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d966db2215620afcb4b8db63012b6b0d5750f266626abb9cc2e3cb305f5b27cd`  
		Last Modified: Mon, 09 Sep 2024 18:00:17 GMT  
		Size: 10.0 MB (9975068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62b1751064b982aee764e7b26bd4d9f6ee11362141082d10289627c2a5458e3`  
		Last Modified: Mon, 09 Sep 2024 18:00:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
