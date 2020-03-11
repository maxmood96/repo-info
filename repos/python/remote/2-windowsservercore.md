## `python:2-windowsservercore`

```console
$ docker pull python@sha256:92a9ec35e889d08025afb04410f057088aaca13efdcf76ea07f7cd34b004868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `python:2-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull python@sha256:e78cc617dc4c6c60646e0136a6b3fc8d1946710f75c74b4d9d4c1b0267fd9de3
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5787698884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5571f5f358acb8fa03321b8471e8ae0cef4cdde9def6521f4519715b2be2399b`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 04:44:15 GMT
ENV PYTHON_VERSION=2.7.17
# Thu, 20 Feb 2020 04:44:17 GMT
ENV PYTHON_RELEASE=2.7.17
# Thu, 20 Feb 2020 04:46:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 04:47:01 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 20 Feb 2020 04:47:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 20 Feb 2020 04:47:04 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 20 Feb 2020 04:49:16 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 04:50:55 GMT
RUN pip install --no-cache-dir virtualenv
# Thu, 20 Feb 2020 04:50:56 GMT
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
	-	`sha256:672ae8f5a9c349cb12c1fdd88856b9d2bf7ee44e12a2daa845c2bf13b204ffa2`  
		Last Modified: Thu, 20 Feb 2020 05:04:25 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f514fded7e8b5a1fdfa272ca8a4535a8b2ab69be9889338485e5630e3853e8e`  
		Last Modified: Thu, 20 Feb 2020 05:04:23 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f82a192f2de1894bf3a83325786700236078d2a9f7116c8ccefd5ac1dfc1fb`  
		Last Modified: Thu, 20 Feb 2020 05:04:51 GMT  
		Size: 39.7 MB (39662066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9362ab8c1826ca90a0bb4469d3022da7a180d59acab2afac3e4f49efb5af07d5`  
		Last Modified: Thu, 20 Feb 2020 05:04:21 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e56aa3e89f735d51cc7f6d6da90256fd0c3531ee51d034868121a0086064a9`  
		Last Modified: Thu, 20 Feb 2020 05:04:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fdbc65ab8c8c628ae351b857ca2e9e71d1ea3df9d843012f6cc8aeac40faed`  
		Last Modified: Thu, 20 Feb 2020 05:04:19 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490539fb3bccd5ea31d7a3d536ac32a394ed10b4287c9f3f229cf514ce202703`  
		Last Modified: Thu, 20 Feb 2020 05:04:40 GMT  
		Size: 10.0 MB (10022262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe853e25654529599d0627dad1bc2b1ca45f9278256ceb7af0ac44d45b2d433`  
		Last Modified: Thu, 20 Feb 2020 05:04:29 GMT  
		Size: 10.9 MB (10941172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33b6ff905419ce2798764bfeb0eb1718200e128f7ee24e7ea64b68adf495c4c`  
		Last Modified: Thu, 20 Feb 2020 05:04:19 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:2-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull python@sha256:d23e9d954d06623da9ddc6dcb4f2c84e8068be52529501884947ed0d324c4d51
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2315330848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9692cd49bb00f84c9cf7589f3081a71368f8ca8f987b2c0087f46fa2035bb6a6`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Mar 2020 01:10:35 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 11 Mar 2020 01:10:36 GMT
ENV PYTHON_RELEASE=2.7.17
# Wed, 11 Mar 2020 01:12:41 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Wed, 11 Mar 2020 01:12:42 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 11 Mar 2020 01:12:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 11 Mar 2020 01:12:45 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 11 Mar 2020 01:13:59 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Mar 2020 01:14:49 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 11 Mar 2020 01:14:50 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be3f6a22e2eff170b790e610e001e272785ac22eb8f2e608204080097ddb44c`  
		Last Modified: Wed, 11 Mar 2020 01:20:00 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4517726fc5b1a00a25e996df30b165335003b87e15b4eece8aebb561eaf5009e`  
		Last Modified: Wed, 11 Mar 2020 01:19:57 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ed6bd47591326662d52ce2108afa144dd2daefee8cda1747dd52e9b72499b7`  
		Last Modified: Wed, 11 Mar 2020 01:20:25 GMT  
		Size: 39.0 MB (39013698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08300665d8cf39290938cf9112d290a13d3570de9ee456d9ba7b38671476824`  
		Last Modified: Wed, 11 Mar 2020 01:19:56 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6c6d59522bdf5c0b355201341250efd2658e33efc3e87174367e6302c68862`  
		Last Modified: Wed, 11 Mar 2020 01:19:53 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8708b29656f4db33761ef9c60ad6cbf6f4cd1e0f9b57f6a9931cf001d20c96e`  
		Last Modified: Wed, 11 Mar 2020 01:19:53 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d83b4b5d7c9fd585eb109ccb641192ddb9f415c45976e3c427997a69510bafd`  
		Last Modified: Wed, 11 Mar 2020 01:20:13 GMT  
		Size: 5.0 MB (4998981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8a78ffefcb1dd1697356a4b5c5410b6bee31de323f903065e6a63c3657056f`  
		Last Modified: Wed, 11 Mar 2020 01:20:01 GMT  
		Size: 6.0 MB (5973465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ae6173aa7c239d93308c44263335b25e14e6cb2fc65c5649239927c47e87c2`  
		Last Modified: Wed, 11 Mar 2020 01:19:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
