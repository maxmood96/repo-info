## `hylang:python3.9-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:842a2277e547b2b279d72b259ab4a6724d6f777e50ba442f7425042bb5b4f4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `hylang:python3.9-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull hylang@sha256:521a4e5fb0e750378008108d3c6eb2ed3503c23f017d9c7931b85fd7817ec76b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6330619651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db71831345b0b3cce61f5b94e2ba2cf15f39372b639bfbb70558988f5a00b38`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 01:53:27 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 10 Nov 2021 02:03:21 GMT
ENV PYTHON_VERSION=3.9.8
# Wed, 10 Nov 2021 02:03:22 GMT
ENV PYTHON_RELEASE=3.9.8
# Wed, 10 Nov 2021 02:05:09 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 10 Nov 2021 02:05:10 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 10 Nov 2021 02:05:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 10 Nov 2021 02:05:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Wed, 10 Nov 2021 02:05:14 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Wed, 10 Nov 2021 02:06:41 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 10 Nov 2021 02:06:42 GMT
CMD ["python"]
# Wed, 10 Nov 2021 02:32:09 GMT
ENV HY_VERSION=1.0a3
# Wed, 10 Nov 2021 02:33:20 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 10 Nov 2021 02:33:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee32b722eae60843ab69b9a429e222c325d19f4554fc09616632500513b4739`  
		Last Modified: Wed, 10 Nov 2021 02:10:38 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c07784a637abcce734b2e665db17560147cee3520834ad783afd332d0e89af`  
		Last Modified: Wed, 10 Nov 2021 02:12:23 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd64bcd5712bdeb138c852efea6597c0ca7c6c7c3ffa450b26f844ee2d97d1e`  
		Last Modified: Wed, 10 Nov 2021 02:12:23 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8a1f401b9a387faa6ae7bc541d9dc6e1a7d60db2eb0c88eb13e7de8f7b8836`  
		Last Modified: Wed, 10 Nov 2021 02:12:30 GMT  
		Size: 49.9 MB (49929125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb7b104bf9b3a7c40f1c581f3337bef20fcef05799e89174d7f11b1de8c5234`  
		Last Modified: Wed, 10 Nov 2021 02:12:23 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46a7adefd686e8e22d5b609debb3b8e38997c43b355339c72d61be3c56e6a76`  
		Last Modified: Wed, 10 Nov 2021 02:12:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec83debfc6bbe249a512d38f1431d7b962eb7080a3538c47cefebe2cdb0843b`  
		Last Modified: Wed, 10 Nov 2021 02:12:21 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0696e49f1dfd9dc407f4a55e4f5d9f26a2948294eb9d756700a57fad282e76b7`  
		Last Modified: Wed, 10 Nov 2021 02:12:21 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fee665c8d83aa51d5740d80174fb5c5e38ec66f1429ae2e2b16094df2e524d`  
		Last Modified: Wed, 10 Nov 2021 02:12:23 GMT  
		Size: 6.3 MB (6285904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fb513a3f1af474b10be04710ef3404b0a615f4bbf1df6f17462d7f778d2615`  
		Last Modified: Wed, 10 Nov 2021 02:12:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef74b80efc36177ad535e2b15108223735c81b41230ae18cc9d6b37360cae624`  
		Last Modified: Wed, 10 Nov 2021 02:34:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39210dacb09d36e2f1c4c1b50bdde9887fe7707588bee5152c6ea3a36369cdec`  
		Last Modified: Wed, 10 Nov 2021 02:34:22 GMT  
		Size: 1.3 MB (1298218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d067892924f4a1fc3c6fe8d4be9bcdc62e5bac4b029351e0ae9b6068ae917a85`  
		Last Modified: Wed, 10 Nov 2021 02:34:21 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
