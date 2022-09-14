## `python:windowsservercore`

```console
$ docker pull python@sha256:739732499a2b51c72b6b3e4da98d7bddeaffe1702ea672a3e575649f52f94e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `python:windowsservercore` - windows version 10.0.20348.1006; amd64

```console
$ docker pull python@sha256:b98f208064ad6d4e12f3f90d26e889d1c1e36621cecf9952e4cecd145cfc3027
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2400375193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4edad90126ea0353a8989f15fe7eeec9401ba6dd3b0e72b916c5939aacfb60`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 12:31:43 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 Sep 2022 15:49:17 GMT
ENV PYTHON_VERSION=3.10.7
# Wed, 14 Sep 2022 15:50:36 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:50:37 GMT
ENV PYTHON_PIP_VERSION=22.2.2
# Wed, 14 Sep 2022 15:50:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 14 Sep 2022 15:50:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5eaac1050023df1f5c98b173b248c260023f2278/public/get-pip.py
# Wed, 14 Sep 2022 15:50:40 GMT
ENV PYTHON_GET_PIP_SHA256=5aefe6ade911d997af080b315ebcb7f882212d070465df544e1175ac2be519b4
# Wed, 14 Sep 2022 15:51:24 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:51:25 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cda85049692c403fdc829f8b3166e77cc97a143c264d551b85e33a61d7374a`  
		Last Modified: Wed, 14 Sep 2022 12:44:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dc9b49f4e0a213b17c7394db1c3595aaf53e404b10ac0abb1b677a346b270a`  
		Last Modified: Wed, 14 Sep 2022 15:56:37 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786631e567f12ca6f9c0bbc7e1c210cb4b465e0e02985890993c8816c4e0c891`  
		Last Modified: Wed, 14 Sep 2022 15:56:44 GMT  
		Size: 49.5 MB (49524061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f11038909391cfc0e695374c9900faf0ae38e2f5123417344e19ed9af877b69`  
		Last Modified: Wed, 14 Sep 2022 15:56:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5f37c42a3ddc95cb6cb826ed1753b77874cf51d056e775d3a1aa9bef80bdd2`  
		Last Modified: Wed, 14 Sep 2022 15:56:35 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297ee74c97f0580913b76e24ebe08ec57160a485a8cedf8c5a7be46f1720b7bf`  
		Last Modified: Wed, 14 Sep 2022 15:56:35 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c57cf4c451f745a137552d1629c2a9da8e07daf6db09a75b729014deac5a70`  
		Last Modified: Wed, 14 Sep 2022 15:56:35 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1253a00353810e0ff6378d4e6eb7c923848b69a3685cc6949d12c5ac532ff13`  
		Last Modified: Wed, 14 Sep 2022 15:56:36 GMT  
		Size: 3.9 MB (3890151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6084b92f410cc120d3dde218c72d7387fea90a1bc8ea7c2cd1f22ea6a8060002`  
		Last Modified: Wed, 14 Sep 2022 15:56:35 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull python@sha256:da99082462721d048dc0ef5551f079a390f124509a3a4d3da9f5dda95f854a30
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2756555081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2791066da6a5ec7a4e787b71de4571c0c927a8f7ac123c385e23fe53782dae`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 12:34:41 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 Sep 2022 15:51:45 GMT
ENV PYTHON_VERSION=3.10.7
# Wed, 14 Sep 2022 15:53:39 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:53:40 GMT
ENV PYTHON_PIP_VERSION=22.2.2
# Wed, 14 Sep 2022 15:53:41 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 14 Sep 2022 15:53:42 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5eaac1050023df1f5c98b173b248c260023f2278/public/get-pip.py
# Wed, 14 Sep 2022 15:53:43 GMT
ENV PYTHON_GET_PIP_SHA256=5aefe6ade911d997af080b315ebcb7f882212d070465df544e1175ac2be519b4
# Wed, 14 Sep 2022 15:55:11 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:55:13 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a686acd7e84aaf987dc724048fb8374c8a5e930e3604f400fd8e38bfe1e6aeaf`  
		Last Modified: Wed, 14 Sep 2022 12:44:50 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243e1d5a24940697bc81799c65b88756a4276102687a860e70d21691cab13f02`  
		Last Modified: Wed, 14 Sep 2022 15:57:02 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac8ec813ce16fd48ca23c7a3118edd858a8a999ab28734c7edc502a3d0f9899`  
		Last Modified: Wed, 14 Sep 2022 15:57:10 GMT  
		Size: 49.3 MB (49316910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9640d55472dc675bb50cab0eee0ff095665b323228c2e86450a7ca3d9eb9e9f8`  
		Last Modified: Wed, 14 Sep 2022 15:57:02 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1165cba5df3f59da87cdedd691233976b54fc45999dc781b2da6ba4ebc3441`  
		Last Modified: Wed, 14 Sep 2022 15:57:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf4dd54c66d9824be9da7ba7a1c1bbaa254b02c102a6d66bfbfaa20d489b9a8`  
		Last Modified: Wed, 14 Sep 2022 15:57:00 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa042d28fc0f3d55479146e39b3e5c953441fbecda49992fbfc4ed9788d7488`  
		Last Modified: Wed, 14 Sep 2022 15:57:00 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea9f0ed9d30bc0e370609ea614cc714a82ebfc2fe46c9c4f4d418eeac87a9a1`  
		Last Modified: Wed, 14 Sep 2022 15:57:01 GMT  
		Size: 3.7 MB (3662166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9885397a2e5fdc48ff9584d0946bc7d893f9308596b27ec18fb4e7a5ec7ee0c`  
		Last Modified: Wed, 14 Sep 2022 15:57:00 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
