## `hylang:python3.7-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:246086b1547a8e2e33dd531f5e1e1232744cbe1bb7ea187ae159c5055a95dd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `hylang:python3.7-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull hylang@sha256:cfe7642942e7472d46585339cb84afca91079974c79b0aff59b49c51733921de
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5797278807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9302db81294774c473b062783d0baff10ded9018653867440f4fde0c2f1483de`
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
# Sat, 25 Jan 2020 02:30:50 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 06 Feb 2020 02:09:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 06 Feb 2020 02:09:31 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 06 Feb 2020 02:11:20 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 06 Feb 2020 02:11:21 GMT
CMD ["python"]
# Thu, 06 Feb 2020 02:30:41 GMT
ENV HY_VERSION=0.18.0
# Thu, 06 Feb 2020 02:31:53 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Thu, 06 Feb 2020 02:31:55 GMT
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
	-	`sha256:4a1e551f40b29cc9febe7710ec872cc14345e63e6aebc6f466826b95716eaae4`  
		Last Modified: Sat, 25 Jan 2020 03:13:25 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288aecc50d56a21fc941ff3d690776094743b7268901eed3ca0f88a787e4171d`  
		Last Modified: Thu, 06 Feb 2020 02:21:52 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ebcdcf9f6ac0df08974c0895e82eb91d524e0c5f389a9c2993b717bf309432`  
		Last Modified: Thu, 06 Feb 2020 02:21:52 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e749975da6ab813856ea43c45671d6a907243cd90377cf6a65ad5d1fc36b0b0c`  
		Last Modified: Thu, 06 Feb 2020 02:22:06 GMT  
		Size: 10.4 MB (10383257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a0f5acdccfc587368ee5278f15b61d307976e89004657ec4ecc0a51e32fb55`  
		Last Modified: Thu, 06 Feb 2020 02:21:52 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8201a1a8f05db56d80012b7270293ad0185a0a7f70d9c91481aa5c6e0f1df287`  
		Last Modified: Thu, 06 Feb 2020 02:36:51 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477c6266040e99791d1f00224b4e05f918aea349aec615d024e1a94eaa598baa`  
		Last Modified: Thu, 06 Feb 2020 02:37:04 GMT  
		Size: 6.1 MB (6136075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f712656421629b2f7acae51fb1dd88ecad967c2f4692050bf4bd9522b5e6fc`  
		Last Modified: Thu, 06 Feb 2020 02:36:51 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
