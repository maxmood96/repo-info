## `python:windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:bb5aba737033fd49355ad8a745fd5f4ee361a990e1a7afabc029d988284d16c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.524; amd64

### `python:windowsservercore-ltsc2022` - windows version 10.0.20348.524; amd64

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
