## `hylang:0-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:ff22036cced3453d460961d2a40bf34b160100b9f0e9336cbde92e93d9fb06e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `hylang:0-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull hylang@sha256:7a807b0d1418f3f0cf11b2276dde5a9ceed8528dd847972f965d518ea54b9104
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5797445572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd95e45bbabc6aa2e07d411c7aab9936d82089f98c3031ad4f6fc25978adf014`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 18:15:45 GMT
ENV PYTHON_VERSION=3.7.6
# Wed, 15 Jan 2020 18:15:46 GMT
ENV PYTHON_RELEASE=3.7.6
# Wed, 15 Jan 2020 18:18:51 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Thu, 23 Jan 2020 22:28:37 GMT
ENV PYTHON_PIP_VERSION=20.0.1
# Thu, 23 Jan 2020 22:28:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Thu, 23 Jan 2020 22:28:39 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Thu, 23 Jan 2020 22:30:33 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2020 22:30:35 GMT
CMD ["python"]
# Thu, 23 Jan 2020 23:05:43 GMT
ENV HY_VERSION=0.17.0
# Thu, 23 Jan 2020 23:06:58 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Thu, 23 Jan 2020 23:07:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231d068bc7d6ef0d45f3e7928dd8b7316314a79ba961211f403ff4e6af443363`  
		Last Modified: Wed, 15 Jan 2020 18:41:29 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e6bbf0d2465c626c795a3b859649cabcb07f76f3615f1c6357318a4d51b7e0`  
		Last Modified: Wed, 15 Jan 2020 18:41:28 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eced260e8a270d4df19d1b0e46006c2bd30aa312ff93f9c5e8c9870d92a88b5`  
		Last Modified: Wed, 15 Jan 2020 18:41:59 GMT  
		Size: 56.1 MB (56149516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3eb2ba67c5732a607bb89b45f9a7f651209cfb9a1b6ec98438d7dd6d4a7fc2`  
		Last Modified: Thu, 23 Jan 2020 22:41:52 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c5e5d36c112a8953d5478c026acc31f551d2d99eb3fd00a41908a94458d2d7`  
		Last Modified: Thu, 23 Jan 2020 22:41:51 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77827153a916cd3d04c994d797875eba832b62dc566815aa5416931c1d2b628`  
		Last Modified: Thu, 23 Jan 2020 22:41:51 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0801e1cb53fe6d622ce367ffe1f3efb61df56e3a2189bf6ed627078fee4564c`  
		Last Modified: Thu, 23 Jan 2020 22:42:01 GMT  
		Size: 10.5 MB (10493934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890645c9c72ff2ef196054cae86773e11ebcb30be4b3f39c1694848943b41378`  
		Last Modified: Thu, 23 Jan 2020 22:41:51 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84af40ccec51cba10087fe243dcf4a6ee728f18c80cc86b8aba7a784219c6b4`  
		Last Modified: Thu, 23 Jan 2020 23:11:32 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def516a8af2c6d25c7a67ec97c76c0a121bc91dfb1529217440a499016d3b584`  
		Last Modified: Thu, 23 Jan 2020 23:11:40 GMT  
		Size: 6.2 MB (6192070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c78579f8e6cbd742b41b34c52244ee3380791cd1f749b5158bb80ef9732086`  
		Last Modified: Thu, 23 Jan 2020 23:11:33 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
