## `python:3-windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:22c4f00e523ea6f3c9f12dc7e8ccb7377f7146a37720f9c080eb0c871644e0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `python:3-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull python@sha256:7a934e27fde39ecc65f1e845290b9df73529e8744e2706cdf5251f73c23be84c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178036428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e5fa4023c45341683062bf7b403418acbaaeb2793f6510e6f8d382ef439871`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Wed, 03 Jul 2024 00:06:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Jul 2024 00:06:17 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 03 Jul 2024 00:06:17 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 03 Jul 2024 00:08:25 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 03 Jul 2024 00:08:26 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 03 Jul 2024 00:08:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 03 Jul 2024 00:08:27 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 03 Jul 2024 00:08:47 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 03 Jul 2024 00:08:47 GMT
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
	-	`sha256:0f5002a3405e62936fc8626acef5b4ec8f64442f5c1f85e5161bf092f31c4bef`  
		Last Modified: Wed, 03 Jul 2024 00:08:51 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44df6ded973864272a4b7aa2ab8f06ec6769be8f029ab5596b87c7422f865b91`  
		Last Modified: Wed, 03 Jul 2024 00:08:50 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd5bfe41a345402f6f4d205d95028c80680c21d4c0bb20ecd669edb2af69c52`  
		Last Modified: Wed, 03 Jul 2024 00:08:50 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166a98dd64e41b478e83d280afedf732a7444961d9badaf4b1b61283ccec88e8`  
		Last Modified: Wed, 03 Jul 2024 00:08:54 GMT  
		Size: 48.6 MB (48602077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238cc31a21c7b3900e2e579e44f15a4cbb30e551ee16c4181fb978257691decf`  
		Last Modified: Wed, 03 Jul 2024 00:08:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6873652a132dd540599e1265fed2bc2c5753358be18eca81a7c0729e86d4e1d8`  
		Last Modified: Wed, 03 Jul 2024 00:08:49 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefc477cc9c3f3e2c6b0deb4bf9d1acbc86e48a79259edeac01022da062dbc4b`  
		Last Modified: Wed, 03 Jul 2024 00:08:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4647aad75f4ad0a9d31525a62f6397bd42f5394e72ac56e66a537c35a7b775`  
		Last Modified: Wed, 03 Jul 2024 00:08:51 GMT  
		Size: 11.2 MB (11235009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57cf6a73a14aed2c3310dcf70c05319054677263e8383d3588b20ee567e7581`  
		Last Modified: Wed, 03 Jul 2024 00:08:49 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
