## `python:3-windowsservercore-1809`

```console
$ docker pull python@sha256:1e52597db2d0b86f0130a42b2b1bc105f66a8c5da736a168f0aa7cade1ce95e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `python:3-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull python@sha256:28e411a4a9c6a52d2726525bbe7123def7bb303cd2961ae67ef2a48f415ce17f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2766351489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109506ba07fa696d4073eece7fb746704e1d207d2308dd8cf4fdab41194c3306`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Jan 2022 00:21:23 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 20 Jan 2022 00:28:22 GMT
ENV PYTHON_VERSION=3.10.2
# Sat, 29 Jan 2022 00:28:51 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Sat, 29 Jan 2022 00:28:52 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 29 Jan 2022 00:28:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Sat, 29 Jan 2022 00:28:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 29 Jan 2022 00:28:56 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 29 Jan 2022 00:30:43 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Sat, 29 Jan 2022 00:30:45 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3b1920413d4106671928a45f37c4a14069c2cc7b710839baa300bc22b5be3a`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86198cb30a26133b5d3817993914528c192ac08a7a3c9c8284904910404f8a28`  
		Last Modified: Thu, 20 Jan 2022 00:42:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104df3e296a628c12ee22ad11fd4963b0da84381deab11060cbf6e91483077fe`  
		Last Modified: Sat, 29 Jan 2022 00:41:08 GMT  
		Size: 46.5 MB (46547190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c335378507abdd522fa405b6993dabee5ea6faf31c2ec7161d461c2df825af24`  
		Last Modified: Sat, 29 Jan 2022 00:40:17 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d4e2613ffdeba677f907f7b34c9c6182407aac728d59e47972e9822fa5d02d`  
		Last Modified: Sat, 29 Jan 2022 00:40:15 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1c47890e212478319f4f39d6f85cb2fd9b48228bada4f4f3257ada7a06e4`  
		Last Modified: Sat, 29 Jan 2022 00:40:15 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67ca3915cf57a6249103f7025c1c4718b6a9142c4d52121107b2a4ab69118ef`  
		Last Modified: Sat, 29 Jan 2022 00:40:15 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0ade7d9003e119f6f655429893964be2bc869d667c00311dbaf73d1d1bf7fc`  
		Last Modified: Sat, 29 Jan 2022 00:40:17 GMT  
		Size: 6.5 MB (6471435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8ee8b222d9a19fa54cd8ed484452708556f4007c25039f78341826954861e1`  
		Last Modified: Sat, 29 Jan 2022 00:40:15 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
