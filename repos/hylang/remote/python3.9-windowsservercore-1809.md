## `hylang:python3.9-windowsservercore-1809`

```console
$ docker pull hylang@sha256:01d745c987d023a99af20527674245318c43d588c63d1d24f4e6acb8779d1650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `hylang:python3.9-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull hylang@sha256:5a94d98e0300d0c6f087b3091acb6e42c73554586f2f4a9509172c57f41341aa
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2770412883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a032a5b72586e4c846647600a7785a6875bdc35ab1fc2c79b44a52ce075301`
-	Default Command: `["hy"]`
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
# Thu, 20 Jan 2022 00:35:18 GMT
ENV PYTHON_VERSION=3.9.10
# Sat, 29 Jan 2022 00:36:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Sat, 29 Jan 2022 00:36:22 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 29 Jan 2022 00:36:24 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Sat, 29 Jan 2022 00:36:25 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 29 Jan 2022 00:36:26 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 29 Jan 2022 00:38:14 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Sat, 29 Jan 2022 00:38:15 GMT
CMD ["python"]
# Sat, 29 Jan 2022 00:59:53 GMT
ENV HY_VERSION=1.0a4
# Sat, 29 Jan 2022 00:59:54 GMT
ENV HYRULE_VERSION=0.1
# Sat, 29 Jan 2022 01:01:07 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Sat, 29 Jan 2022 01:01:08 GMT
CMD ["hy"]
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
	-	`sha256:efc5d9a2a231f83c2265bc66899b66853b5da86b5b0ece8354cc9a7709312e8e`  
		Last Modified: Thu, 20 Jan 2022 00:42:57 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d54bbee06ab94a79e55046c5f5adadd36fd34f34c94e30f2d1f4c1ab49e6b5`  
		Last Modified: Sat, 29 Jan 2022 00:41:52 GMT  
		Size: 49.8 MB (49813032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09aebfb388b23748c1df2627a49480b966f0e9f43354ce46eda27bd5a7a86f77`  
		Last Modified: Sat, 29 Jan 2022 00:41:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5dfefb7587a7a2e41691ac784e2134be64146a67affd4bb9846a7c29f89b0d`  
		Last Modified: Sat, 29 Jan 2022 00:41:42 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c22d27d8b1dc8ee6a1551a4959b42370b103fe3faacf55880a0f4873d53853`  
		Last Modified: Sat, 29 Jan 2022 00:41:42 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643a54edec900e17f2bf981945a1d92f74be58cccdded48ca2359c6f49bc4d24`  
		Last Modified: Sat, 29 Jan 2022 00:41:42 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48efd9a4b7d7b181246bce01720255e896ad0cc1e3f5cdf21a7dba4ba19921cd`  
		Last Modified: Sat, 29 Jan 2022 00:41:48 GMT  
		Size: 6.3 MB (6306476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fd31861e309de6da537cd6dc8d2ffa2b3a1fc9be02ae94386063f35cc02bd6`  
		Last Modified: Sat, 29 Jan 2022 00:41:42 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f093d8db9fb7c9e2aff029d267d6aebf41155453b14464bdc7454480599ab852`  
		Last Modified: Sat, 29 Jan 2022 01:02:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2735e9baeab16020086c92c94126e6cee75958bb77c20e2714ef8295f6dabbcd`  
		Last Modified: Sat, 29 Jan 2022 01:02:07 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0e21e2287765999085ca37b48a0d52bf1126c6d350140b2187ba0f64236cfb`  
		Last Modified: Sat, 29 Jan 2022 01:02:08 GMT  
		Size: 956.2 KB (956231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd04c3a472aedef9d5e665836eb69e2ec14cf0bfdcf070bad8ad903fdf747792`  
		Last Modified: Sat, 29 Jan 2022 01:02:07 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
