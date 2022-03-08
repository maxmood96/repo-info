## `python:3-windowsservercore`

```console
$ docker pull python@sha256:412ecf36fec9872877669f3208fab53e91b01dff3fd7eabaeff60fd12c870dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.524; amd64
	-	windows version 10.0.17763.2565; amd64

### `python:3-windowsservercore` - windows version 10.0.20348.524; amd64

```console
$ docker pull python@sha256:1e65bed07a96b5fc914df8c30a9a3508ebc93be4b38ca108340fce42364442c6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2264871531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879c544e89673b0133f0708376112743067b3da320e9826e482a0f5307178560`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Tue, 01 Feb 2022 02:49:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 09 Feb 2022 13:37:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 20:25:10 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Feb 2022 20:31:35 GMT
ENV PYTHON_VERSION=3.10.2
# Wed, 09 Feb 2022 20:32:51 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 09 Feb 2022 20:32:53 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 09 Feb 2022 20:32:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 08 Mar 2022 01:23:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Tue, 08 Mar 2022 01:23:12 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Tue, 08 Mar 2022 01:23:54 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 08 Mar 2022 01:23:55 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:898469748ff68223ab87b654b29fb366c1f4f2b7cfad7a37426346ea16db8dfa`  
		Size: 963.2 MB (963225591 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7062696b7aef1ca33afdf32084a532f7e3151a844eb7cb2455bcc907e0f42a58`  
		Last Modified: Wed, 09 Feb 2022 14:28:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e372b4996c8441162dd2ab7b7fc70276cf746df4b5e4d2d8c724b3b69b0099`  
		Last Modified: Wed, 09 Feb 2022 20:44:23 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e41a66f00eba96b62a4c237fe9a6f7a0b2c93bbe7afdc724b7366cc94a7a461`  
		Last Modified: Wed, 09 Feb 2022 20:45:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61884a4640bbd000f3c98f226bd37da6c508b798bdbaf408f15009821a522553`  
		Last Modified: Wed, 09 Feb 2022 20:45:54 GMT  
		Size: 46.8 MB (46761599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8440c4bd22e8a6b52ea8f7c0d8a685c45de0c4e125858cb5f541076c2ed3b9f7`  
		Last Modified: Wed, 09 Feb 2022 20:45:47 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d629dfadf0f75ed53504d6bb50683de3f9def2005682fbd23cb0a89a0dff5fe`  
		Last Modified: Wed, 09 Feb 2022 20:45:45 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75785a3906a3b4ee6372a38ffe72ec64f61ce3c6b02cde848ca5cd4a11ee4739`  
		Last Modified: Tue, 08 Mar 2022 01:29:18 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16b313b5968d5995217a80495afe0a595ace5b67a6372d8c5db72729bbb5999`  
		Last Modified: Tue, 08 Mar 2022 01:29:18 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85e3190a5abeb266b7c717d3ddc4945c942f5a5772da4657f09d4ba062dd377`  
		Last Modified: Tue, 08 Mar 2022 01:29:19 GMT  
		Size: 3.2 MB (3174252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327e36c9ef167159f6f51683dd52ad57e28943f8afbe883dad6dd7959f20d846`  
		Last Modified: Tue, 08 Mar 2022 01:29:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-windowsservercore` - windows version 10.0.17763.2565; amd64

```console
$ docker pull python@sha256:a4aaa45bef7943a633402c7aaefb933e6fa01c8108e2d076524150e4c6d67867
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2763241508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878e08f85a816f898d429d60cd1c504c504ae7aa7aec3ea6862660f9c85f6dca`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 13:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 13:19:44 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Feb 2022 20:33:49 GMT
ENV PYTHON_VERSION=3.10.2
# Wed, 09 Feb 2022 20:35:49 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 09 Feb 2022 20:35:51 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 09 Feb 2022 20:35:52 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 08 Mar 2022 01:24:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Tue, 08 Mar 2022 01:24:04 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Tue, 08 Mar 2022 01:25:26 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 08 Mar 2022 01:25:27 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f0c1566a9285d9465334dc923e9d6fd93a51b3ef6cb8497efcacbcf64e3b93fc`  
		Last Modified: Wed, 09 Feb 2022 13:26:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a7c52a40ee1a3e8513436661e94eab0212813dc541bb3fdec3e396a986d673`  
		Last Modified: Wed, 09 Feb 2022 13:27:20 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa304a4f34e2e051cd97fedd65599e9fb5d39a0d18dc01a6937c5206b16c1203`  
		Last Modified: Wed, 09 Feb 2022 20:46:11 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9591bb7b6d98832c1f583580d4270340a2791f6c6e145b1784e1f5d42e20df25`  
		Last Modified: Wed, 09 Feb 2022 20:46:17 GMT  
		Size: 46.5 MB (46544066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d8c1bf45de3997fe38cf3ef27cb91ed40919a7b13c6234f6074e784808be5f`  
		Last Modified: Wed, 09 Feb 2022 20:46:11 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177364207a5e525c7c1f66b8ad4682fd7b1699def51e982b9eb98cc954b10ff8`  
		Last Modified: Wed, 09 Feb 2022 20:46:08 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257eef3893b38bd692c4c1083b7b704c7a7d42ccba767c914699a2ea311545d2`  
		Last Modified: Tue, 08 Mar 2022 01:29:34 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ad5e3769e350fef9e1982eefc72004480de6ccd398f370aad49ee88c959b1d`  
		Last Modified: Tue, 08 Mar 2022 01:29:35 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5947b19d2df23097892446c6b358a47c3494d17cb9ee90abe0cbc53057fd96e`  
		Last Modified: Tue, 08 Mar 2022 01:29:36 GMT  
		Size: 3.0 MB (2971442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546e1fa143ec21fbf2239a02d6c2ebce141c2235f92dfd22f2730afa63aa7c3a`  
		Last Modified: Tue, 08 Mar 2022 01:29:34 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
