## `python:windowsservercore-ltsc2016`

```console
$ docker pull python@sha256:9bc6f1b6f5d79883133510fbfd5ad8405596cd7d19115be3bbcbc1ee215af1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `python:windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

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
