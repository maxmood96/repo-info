## `python:rc-windowsservercore-ltsc2016`

```console
$ docker pull python@sha256:8507361110edf3fa5aadaaba8b140f70abbb6cf6257317f1bcff180a5aac0cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `python:rc-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull python@sha256:1f3fd2bcaeb646e5182857363188d92d1b0edd310bc3d22de1c88f074c1a579c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5794634511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc6ef03924f18fdb00f683f9429800477941378cb0f217e557f03c306b4572a`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 04:14:25 GMT
ENV PYTHON_VERSION=3.9.0a3
# Thu, 20 Feb 2020 04:14:26 GMT
ENV PYTHON_RELEASE=3.9.0
# Thu, 20 Feb 2020 04:17:41 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 04:17:44 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 20 Feb 2020 04:17:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 20 Feb 2020 04:17:46 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 20 Feb 2020 04:19:54 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 04:19:56 GMT
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
	-	`sha256:81e08c105973abf69665a3b7d1eeec6826585c7bbfaea8a8812a68e9d40309c7`  
		Last Modified: Thu, 20 Feb 2020 04:57:06 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6deac3b3cd09d92e9deaab0799e3be9d590f17c13475c244294fd52ffd209d21`  
		Last Modified: Thu, 20 Feb 2020 04:57:06 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66a3f0f435f339439ff8328f2c6426e8b9393379b249f6ed869794d6b233d13`  
		Last Modified: Thu, 20 Feb 2020 04:57:37 GMT  
		Size: 57.2 MB (57176262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b98565fff716bbcb5e854c917688dfcef57a1cb528e53e785f58fb8708489ee`  
		Last Modified: Thu, 20 Feb 2020 04:57:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a37f396927fdeb66a92abf807f9c59efdbd4a37f944eb96d19f6d2afa23d66`  
		Last Modified: Thu, 20 Feb 2020 04:57:02 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5428accbe0bdbc791e749024f04a47c64bb519746bbb232b0aa93b9c6ca431`  
		Last Modified: Thu, 20 Feb 2020 04:57:03 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a11b5f465adf56e744526d263ea9071e3bc499120651172b5c539d7f7b184e`  
		Last Modified: Thu, 20 Feb 2020 04:57:17 GMT  
		Size: 10.4 MB (10384862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9d0fa97fe9612805a81007c5a4246ce2086355aa82f90a94cdeb88f07c8327`  
		Last Modified: Thu, 20 Feb 2020 04:57:02 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
