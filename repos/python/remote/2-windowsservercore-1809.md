## `python:2-windowsservercore-1809`

```console
$ docker pull python@sha256:8480abec04402fa785b0525f4dc36418a66387630abea08979ae6099e35f6f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `python:2-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull python@sha256:65eb401ccd15a2ef3b5108f6d3d1aefbdd4f19c67e01998cb2363426b0e0789a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320848698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f4cfc0190166d0aa42e3d19e0451b3bea07273bf6555dbe663fb2bb1f9904d`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Apr 2020 00:21:09 GMT
ENV PYTHON_VERSION=2.7.18
# Tue, 21 Apr 2020 00:21:09 GMT
ENV PYTHON_RELEASE=2.7.18
# Tue, 21 Apr 2020 00:22:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Tue, 21 Apr 2020 00:22:22 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Tue, 21 Apr 2020 00:22:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Tue, 21 Apr 2020 00:22:25 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Tue, 21 Apr 2020 00:23:06 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 21 Apr 2020 00:23:43 GMT
RUN pip install --no-cache-dir virtualenv
# Tue, 21 Apr 2020 00:23:44 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa75be16f1858cd341c379ba7e54d9b24eeeeb6741b6cfc38f622b9403435632`  
		Last Modified: Tue, 21 Apr 2020 00:25:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ba24c3e36acdedc41dc020359701b5ef51e0585ba8e4419eb399b203c6b5d5`  
		Last Modified: Tue, 21 Apr 2020 00:25:07 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332bab4ee60328c9fcc309d21340cd1c6c2d757f323b8aadcab0302818e4447`  
		Last Modified: Tue, 21 Apr 2020 00:25:14 GMT  
		Size: 39.1 MB (39109444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36595d215ac4669d877eb8c79f9a29e20d1aec124cb3636a783126d93fe32356`  
		Last Modified: Tue, 21 Apr 2020 00:25:07 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bb6d81892be22e61a8392b2994440f93ce3a49c2f64b10d107565a36165797`  
		Last Modified: Tue, 21 Apr 2020 00:25:04 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da01429e7fbe7ed7ab9ba0105b09fd0f44f68dbc04216eff7da46dafa2e49f7`  
		Last Modified: Tue, 21 Apr 2020 00:25:04 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e1ba8bba570c9590a601f59f6ab64c809f5dcce8d89d1473e15961d97698f1`  
		Last Modified: Tue, 21 Apr 2020 00:25:10 GMT  
		Size: 5.0 MB (5026407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ca08f07b32309701f9c462fd3cbee5d02ab403a0d4b412fc3c0561eb34a8ed`  
		Last Modified: Tue, 21 Apr 2020 00:25:05 GMT  
		Size: 6.0 MB (5997910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1f16c2d88a1a36411583696aea92b174c4131f8b866c61bb9bb1f96ea19774`  
		Last Modified: Tue, 21 Apr 2020 00:25:04 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
