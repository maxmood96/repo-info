## `hylang:python3.9-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:db4311306b578b1a5fd124bc712548a158e59f9621f41b7cff01074c940ccf67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `hylang:python3.9-windowsservercore-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull hylang@sha256:cb5f260a367eed2a07ea8c29221fdd6bf62aa987eafa6019f96a28136f069618
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2265181839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c0669aa3f1b8925a1f6d1c3e679dd90ea3c9eb678b9a4d49bb100a57901837`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Jan 2022 00:18:26 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 20 Jan 2022 00:32:20 GMT
ENV PYTHON_VERSION=3.9.10
# Sat, 29 Jan 2022 00:32:31 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Sat, 29 Jan 2022 00:32:32 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Sat, 29 Jan 2022 00:32:33 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Sat, 29 Jan 2022 00:32:35 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Sat, 29 Jan 2022 00:32:36 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Sat, 29 Jan 2022 00:33:47 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Sat, 29 Jan 2022 00:33:49 GMT
CMD ["python"]
# Sat, 29 Jan 2022 00:59:08 GMT
ENV HY_VERSION=1.0a4
# Sat, 29 Jan 2022 00:59:09 GMT
ENV HYRULE_VERSION=0.1
# Sat, 29 Jan 2022 00:59:44 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Sat, 29 Jan 2022 00:59:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12065e818a142b555fc680a1b49a6821fbe7e8cc183fcb2210bfb689cb21ac99`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56d8cf17ed6e3db2d6ef7b8c37801c7644e2dbb511361f88cf8fa42510d666e`  
		Last Modified: Thu, 20 Jan 2022 00:42:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7737d7eb329a45fb9a5d5e8dd5e66547780a455c45b69d7e28474f526cc01b33`  
		Last Modified: Sat, 29 Jan 2022 00:41:32 GMT  
		Size: 50.0 MB (50018156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1239cbccd98a4719026fff92e296780f0f266c4de05fcf75ac70260a02a24bbc`  
		Last Modified: Sat, 29 Jan 2022 00:41:24 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820ec755faa6072767e77ae5525298e3dce7876a5a2950811cae32037561bfa6`  
		Last Modified: Sat, 29 Jan 2022 00:41:22 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6246e380772cd7c453a61379012b39e0d226b10101011ebbc349d63ae55b1d80`  
		Last Modified: Sat, 29 Jan 2022 00:41:23 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce28e4cfdadcbb983b05e555c94e0e9338e0127bbdd51946aebfbf402e4ba33e`  
		Last Modified: Sat, 29 Jan 2022 00:41:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e495f3d669ae16c84e91b78cf26f52aeb56bd30ba9d7152dc6a8baa137f7088`  
		Last Modified: Sat, 29 Jan 2022 00:41:25 GMT  
		Size: 6.5 MB (6502081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d79c1cdb301aa0c4f4817a98121391e0f66f3d9898e42e9146d68bb633b1a6`  
		Last Modified: Sat, 29 Jan 2022 00:41:22 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af5fb9a406c193bbeeb9a86dfc954507d7ea87302dcdedcc29be4a7ab39ea5b`  
		Last Modified: Sat, 29 Jan 2022 01:01:54 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4201ae8603abd6ae16f739a73176d6a1c5c0e06755c406295301d6915b7d5e28`  
		Last Modified: Sat, 29 Jan 2022 01:01:54 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5449d68efc8b10e03834fe41bead6b185cd2b3a3a124ebff7064bbfa697ea28e`  
		Last Modified: Sat, 29 Jan 2022 01:01:55 GMT  
		Size: 1.1 MB (1146185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfd6a6966834b53340b848e4b500a19003905e350188754fbfd9ef976f7b67c`  
		Last Modified: Sat, 29 Jan 2022 01:01:54 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
