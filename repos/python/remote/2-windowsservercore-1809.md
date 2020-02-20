## `python:2-windowsservercore-1809`

```console
$ docker pull python@sha256:af9437c538012ada247df5704ff8c9bd87a426e16f5e712fc6634261674ee14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `python:2-windowsservercore-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull python@sha256:cc7a6f8a70d7170afd3176bd7080df9dd54e7a1ca3c97a8d0766e5d0e7938488
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280381315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dadbca30aa38537d0ae97d0801a6dbeca3b7a1d14fa6080aab4d9c0ff999759`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 04:51:21 GMT
ENV PYTHON_VERSION=2.7.17
# Thu, 20 Feb 2020 04:51:23 GMT
ENV PYTHON_RELEASE=2.7.17
# Thu, 20 Feb 2020 04:53:27 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 04:53:29 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 20 Feb 2020 04:53:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 20 Feb 2020 04:53:31 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 20 Feb 2020 04:54:47 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 04:55:46 GMT
RUN pip install --no-cache-dir virtualenv
# Thu, 20 Feb 2020 04:55:48 GMT
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
	-	`sha256:7cd97be5d47a9eb722fc1c972ddd44b96a15221fb48601ae9fe5721312ce50b6`  
		Last Modified: Thu, 20 Feb 2020 05:05:33 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8caa846f65391c8be14a9692c81631ecb85ade940712090bdc02a660794efcfd`  
		Last Modified: Thu, 20 Feb 2020 05:05:30 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5c8453f60765b82c866a800af37b80bfae166964580f6e8bd2b7bc8a6f7fb5`  
		Last Modified: Thu, 20 Feb 2020 05:05:57 GMT  
		Size: 38.9 MB (38925750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25687fb4e4a27946d3c0b3d6712c8e2eb0d857d6f40c5ee56a52cb3924c88bf`  
		Last Modified: Thu, 20 Feb 2020 05:05:30 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1968ab1428f1fc3d52cb7a9e936cf80643948c42a3a79d8f0ee8b63d3d8c75c3`  
		Last Modified: Thu, 20 Feb 2020 05:05:26 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09479614c031318878b26467c3e0e94b4205f1a2bc699edc8b2637fb4a9ff3ad`  
		Last Modified: Thu, 20 Feb 2020 05:05:27 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2aee9eeaa0ddf406041a8c64726804d58de6310d93b20a352a449910d501de4`  
		Last Modified: Thu, 20 Feb 2020 05:05:45 GMT  
		Size: 5.0 MB (5000177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479de2fea1b301de587e8b7d9663796ce01403f35341388ebff06c2c1e5c5077`  
		Last Modified: Thu, 20 Feb 2020 05:05:35 GMT  
		Size: 5.9 MB (5943102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a58e01c3756110810107dbdd9564efd0f481867a5b5bc5ddbcfba434d6b6b3`  
		Last Modified: Thu, 20 Feb 2020 05:05:27 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
