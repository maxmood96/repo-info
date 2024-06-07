## `python:3-windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:9860ce7be1831afa3c14331dd414fa2212211327b764c990a22bd3f8fa0cf5c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `python:3-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull python@sha256:35367ac9e936ad94c728eaa861034cc422d0775ae317df6826cf0c9fb68d8722
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172655888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebd52956a42c947c814aea09feaf10ba9142c72d8702ad0c329dfce734af84e`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 19:36:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:44:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 07 Jun 2024 19:23:48 GMT
ENV PYTHON_VERSION=3.12.4
# Fri, 07 Jun 2024 19:25:04 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Fri, 07 Jun 2024 19:25:05 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 07 Jun 2024 19:25:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 07 Jun 2024 19:25:07 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 07 Jun 2024 19:25:58 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 07 Jun 2024 19:25:59 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241bde7d4f3acae2008c131651582fc2bb7b130e1f5b90583702d17cad8acd2f`  
		Last Modified: Wed, 15 May 2024 20:42:14 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9095658bb6bac54f714159ea4048684ba7f19e08f8955fc7c75a0f9bc8ee8da2`  
		Last Modified: Wed, 15 May 2024 23:05:21 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fcbf32b0aed4a9a788d95f5fa7876e42e8f1c2f7d5b59603a874b1aebf2720`  
		Last Modified: Fri, 07 Jun 2024 20:16:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49cf805ffb75ce1ec0010fd7860cedb03c773ff2f70db34c9c2ab33c07ad71e`  
		Last Modified: Fri, 07 Jun 2024 20:16:19 GMT  
		Size: 48.6 MB (48552236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9da1a900cf9d8520c13f6ea23819ecb1cf1021243d0679c388aa4dfd2044aee`  
		Last Modified: Fri, 07 Jun 2024 20:16:11 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58da5a54170312af607bce4f45d16506a8df11d3476815e9bb55ec6bf29b2d53`  
		Last Modified: Fri, 07 Jun 2024 20:16:11 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c9f1600fab608df53c86373eb1cc470ad87b97f7e380d3a16874b85bed927c`  
		Last Modified: Fri, 07 Jun 2024 20:16:11 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ba9bad223df075e6f4d11ab20da629a2dac7eb321b4da1c4b1c1bee35d9f99`  
		Last Modified: Fri, 07 Jun 2024 20:16:14 GMT  
		Size: 11.4 MB (11422417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ec3b52459acb754bcd94d3ce75b1043e85761be03e6c2f8d40e34f53ec27a`  
		Last Modified: Fri, 07 Jun 2024 20:16:11 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
