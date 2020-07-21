## `python:windowsservercore-ltsc2016`

```console
$ docker pull python@sha256:81c346e5d8d3114fb4c09acd57c51f128ad8dade495ed9c2969029ec6a6d0303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `python:windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull python@sha256:b43bbbf15b6753c957f3d3328b15ac03b257d780ee093371f8659ee2b1ffe704
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5810717568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc0fe343f102bde0d1f0ba09d3065bb954845bde7c55aba99f94bb3b90dbc32`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Jul 2020 17:54:36 GMT
ENV PYTHON_VERSION=3.8.5
# Tue, 21 Jul 2020 17:54:37 GMT
ENV PYTHON_RELEASE=3.8.5
# Tue, 21 Jul 2020 17:57:08 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 21 Jul 2020 17:57:10 GMT
ENV PYTHON_PIP_VERSION=20.1.1
# Tue, 21 Jul 2020 17:57:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/eff16c878c7fd6b688b9b4c4267695cf1a0bf01b/get-pip.py
# Tue, 21 Jul 2020 17:57:13 GMT
ENV PYTHON_GET_PIP_SHA256=b3153ec0cf7b7bbf9556932aa37e4981c35dc2a2c501d70d91d2795aa532be79
# Tue, 21 Jul 2020 17:59:05 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 21 Jul 2020 17:59:06 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d7ec3f9f2d24e997d93fb18f7ee2d26be25a890248396d7734e959a270a174`  
		Last Modified: Tue, 21 Jul 2020 18:05:09 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e8e910e5f34358935ec3a4c3ce99d111dbecca77ab2cb178fca2cce4237d2c`  
		Last Modified: Tue, 21 Jul 2020 18:05:09 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0cf46a9c2c98cffd335ca954926a0aa9f2b0cbcff6547e82a9c32ff1f28c3f`  
		Last Modified: Tue, 21 Jul 2020 18:05:19 GMT  
		Size: 57.9 MB (57874585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e877f1ba23f4b54461b1dd66aa41cdb756514b64087534b30177328a6657d257`  
		Last Modified: Tue, 21 Jul 2020 18:05:06 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db61f44d3c14d1a1afbcb86184b79121ce05742bb58b5740d5a4a69b9f8e8de`  
		Last Modified: Tue, 21 Jul 2020 18:05:06 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4514ee44c195cfbf6a1fdf630c8ae3c07e0a861efbba576f3d4cdd8fafa2e818`  
		Last Modified: Tue, 21 Jul 2020 18:05:06 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73283bd237496b84163796dc54a28373e54c40d1ea63f5c9ba91b7705e06d935`  
		Last Modified: Tue, 21 Jul 2020 18:05:11 GMT  
		Size: 15.4 MB (15372891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9832e00979b61174faa0b234422abb819279668a953f7c3ebb84b19c6a1222f`  
		Last Modified: Tue, 21 Jul 2020 18:05:06 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
