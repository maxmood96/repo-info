## `python:3-windowsservercore`

```console
$ docker pull python@sha256:8fcdb53ef64613b22459c9d4cb70d99a48d90e49693f2a3c2a2d3a43223f9673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1040; amd64

### `python:3-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull python@sha256:ffcbf0bac7397e98bf3effe53575201e59752683aa52959bead1ce86ee00ccae
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5794478050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e74b9685baf346e5a215bfadbba6dc5295052fa3675f5acbff3e8a31a51f12`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 04:24:21 GMT
ENV PYTHON_VERSION=3.8.1
# Thu, 20 Feb 2020 04:24:22 GMT
ENV PYTHON_RELEASE=3.8.1
# Thu, 20 Feb 2020 04:27:39 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 04:27:41 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 20 Feb 2020 04:27:42 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 20 Feb 2020 04:27:43 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 20 Feb 2020 04:29:53 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 04:29:54 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72c4471958f7f0f07260f0f430bcffb0bc07811088c24cffba1439d250ea1ae3`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf9770f3f9263e9d5164c0ba2826d8b7fca31da730f3d592cf8e1beea4b14db`  
		Last Modified: Thu, 20 Feb 2020 04:59:19 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085578fb400289069b2632dbb9237fba7589cd2c662a13e300bd3107480b49fe`  
		Last Modified: Thu, 20 Feb 2020 04:59:19 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b648d754a949c31a4db3ff9c73f42d3e6cf127fb543ede47fac88d9722ff2c`  
		Last Modified: Thu, 20 Feb 2020 05:00:25 GMT  
		Size: 57.0 MB (57027635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee93b5613cb05b9495cfbaf20d545bb74cf4e0f4d6ea4b65250b15d59329707`  
		Last Modified: Thu, 20 Feb 2020 04:59:16 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62abc61e11fc3aa7427cdfe7418c220c4cd0d0bf7d2b3c5b2334809dc5803adb`  
		Last Modified: Thu, 20 Feb 2020 04:59:16 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2550f86eeff51d60a42bad1636d42391dd4b4755ba1cb5bb8d8311c1a0f111b9`  
		Last Modified: Thu, 20 Feb 2020 04:59:16 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08b719083b3ad47c6b7aa48fdc35100e9c4d40d79cf2d1a11250fe1bab3a740`  
		Last Modified: Thu, 20 Feb 2020 04:59:27 GMT  
		Size: 10.4 MB (10377072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75af9ac1e85fc700e1eb5d371c9d2c7ca0eb421dc3f67092383aaaabac55864`  
		Last Modified: Thu, 20 Feb 2020 04:59:16 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-windowsservercore` - windows version 10.0.17763.1040; amd64

```console
$ docker pull python@sha256:a7e0b39673ca6fe5930facc8c5c190fa67670a20f9cd4545946b5556f095b8f1
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287663544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d0bd2ccb2d667dad8789112ef01e4d56e0cc309682f205bcdd2867a339d292`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 04:30:13 GMT
ENV PYTHON_VERSION=3.8.1
# Thu, 20 Feb 2020 04:30:14 GMT
ENV PYTHON_RELEASE=3.8.1
# Thu, 20 Feb 2020 04:32:43 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 04:32:44 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 20 Feb 2020 04:32:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 20 Feb 2020 04:32:48 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 20 Feb 2020 04:34:00 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 04:34:01 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2061e035d6ba931d9f00238104b970d3410f4ef0d9603b4f074c7052858e01e3`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad5b1dadd8f1d34572164108247a6b0aed8204bdeabad478da2440e6f2a3594`  
		Last Modified: Thu, 20 Feb 2020 05:01:12 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12034dc899cd0d9525919179c7d4774d31bba521e402587f369ca6e124a5fbc5`  
		Last Modified: Thu, 20 Feb 2020 05:01:12 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7187e4fdde9a32cd20c923b9bbcac50938f9d6a39555a80005e68d1ab98260`  
		Last Modified: Thu, 20 Feb 2020 05:01:41 GMT  
		Size: 51.8 MB (51790375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff34cb16a8d271052e8525b4292671ebc16ed1b9e0e4b60b65dc53b9306d3f28`  
		Last Modified: Thu, 20 Feb 2020 05:01:09 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14938abc2b9a071b475021803817888f36d65c70ae009b8f6d4c571cab5a0fb5`  
		Last Modified: Thu, 20 Feb 2020 05:01:09 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5349c96ead504b69b2d4c769c934d0466bcb450d012d5be896f42e7ae1f3073`  
		Last Modified: Thu, 20 Feb 2020 05:01:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e4f4389f84d0850e15ba3390114596a0e5cfdf8e268034d3c58c07ae903ef4`  
		Last Modified: Thu, 20 Feb 2020 05:01:21 GMT  
		Size: 5.4 MB (5360873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbda978e3cd99b1c9cf7839f830ba2345e4b8935b14b905130e55e4032b34fab`  
		Last Modified: Thu, 20 Feb 2020 05:01:09 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
