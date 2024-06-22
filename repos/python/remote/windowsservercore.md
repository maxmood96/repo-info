## `python:windowsservercore`

```console
$ docker pull python@sha256:d7be6044fd2becf02b03f435520cd16925e42d67ea9b356938caf652271da3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `python:windowsservercore` - windows version 10.0.20348.2529; amd64

```console
$ docker pull python@sha256:1ca20cf4a486d1d7d765cce28b7126b2fb759aceee3cf3f8698a857e8cc0187a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178134857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d232003f146ce00229d428705f9ca203f21a4ff6b1fc946327a5f091a27db3cd`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 00:33:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 01:45:32 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 22 Jun 2024 01:48:07 GMT
ENV PYTHON_VERSION=3.12.4
# Sat, 22 Jun 2024 01:49:25 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:49:26 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 22 Jun 2024 01:49:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 22 Jun 2024 01:49:28 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 22 Jun 2024 01:50:21 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Sat, 22 Jun 2024 01:50:21 GMT
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
	-	`sha256:8b4326efd24d64d6a2efa78c581696b3d528dfcf784a3d6605e621e343b62e16`  
		Last Modified: Sat, 22 Jun 2024 00:59:51 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69f7b2aa7a1e1ac771664da199b076a028b454982a5ec44e7e7d5df49b7421d`  
		Last Modified: Sat, 22 Jun 2024 01:54:25 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea2e525655bc336b757a3205db9484f86c5daa728a9315145d64077f8de3867`  
		Last Modified: Sat, 22 Jun 2024 01:54:43 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fce98902999f36a1f1c0288ad8946dff6a028d84fa13ae1c6568f0b2a23e4ce`  
		Last Modified: Sat, 22 Jun 2024 01:54:49 GMT  
		Size: 48.5 MB (48527341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf410a9eb7c13023b8714067377d19d2725d54e679fe4ea0838f028752216e76`  
		Last Modified: Sat, 22 Jun 2024 01:54:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03891f92dba4ab914a9d67adc1aa5bca51cb052a9ceea05d7d64be0fb9c60cd8`  
		Last Modified: Sat, 22 Jun 2024 01:54:41 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7627f8f0e7c55b52fa98325578f77f9cb5f106eae29314155cda16eb2981cb`  
		Last Modified: Sat, 22 Jun 2024 01:54:41 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da654bef7aa9743af192886daed729d368537fed8edb06221a9cd5a3ed2fd94c`  
		Last Modified: Sat, 22 Jun 2024 01:54:43 GMT  
		Size: 11.4 MB (11407274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79ee014a0f0bd25e6f493945b5ec81bf9950025e860b3f39bd162083bf43077`  
		Last Modified: Sat, 22 Jun 2024 01:54:41 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull python@sha256:0e3c22cf393fe56b5dcb76bef7714c18a18883b8e49766d6d7f6fd11e7f0df05
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279077188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b534324ecdc22ab95b0ba1011a494014f628c1860f366993c755d7a83c6a5601`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 17:37:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 20:33:48 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Jun 2024 20:40:00 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 12 Jun 2024 20:42:02 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 12 Jun 2024 20:42:03 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 12 Jun 2024 20:42:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 12 Jun 2024 20:42:05 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 12 Jun 2024 20:43:50 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Jun 2024 20:43:51 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04390472505d81fa325a5cfd00620c5caa18dd222dd0a98f7a089b8c65b438b`  
		Last Modified: Wed, 12 Jun 2024 18:39:01 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fa54baa51cdfd73a44d61bfdf6270ca0795a58cc06217f856065041c5c4bf2`  
		Last Modified: Wed, 12 Jun 2024 20:51:06 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39483533fb02980c616b94941516c76dff4d07f4d453d1dcaf6a9b6a9476055c`  
		Last Modified: Wed, 12 Jun 2024 20:51:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64e6d3b601d0da055b29035042b1cabb9cfd7635e2a9e383ce99a6be8a2732e`  
		Last Modified: Wed, 12 Jun 2024 20:51:49 GMT  
		Size: 48.7 MB (48698034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ebfa314e9d81d487d5ef1ff28b632d2660f38f5b6cb1ac44133402847e13d`  
		Last Modified: Wed, 12 Jun 2024 20:51:40 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f4f7cd3f981c3f9376ca84d27d2240d878da064ebece9fa87334e3a72933d2`  
		Last Modified: Wed, 12 Jun 2024 20:51:40 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bf905d1999d3cebd0df04148050455aacc35022425ff116a55b2c5e43a056b`  
		Last Modified: Wed, 12 Jun 2024 20:51:40 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980ce66eeea4cf2619f4f6caf273bc1ee9c731402552ed304c7817230c32c726`  
		Last Modified: Wed, 12 Jun 2024 20:51:43 GMT  
		Size: 9.7 MB (9688130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a1b90a2ca4c04cf90e5a79a3b838efdc74f9b5780f32666c2ebcc656274702`  
		Last Modified: Wed, 12 Jun 2024 20:51:40 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
