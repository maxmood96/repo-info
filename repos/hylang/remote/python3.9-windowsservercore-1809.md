## `hylang:python3.9-windowsservercore-1809`

```console
$ docker pull hylang@sha256:4b6000ab12fac95b463db47eafe8997250970a1c14cada06df3de06af889abea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `hylang:python3.9-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull hylang@sha256:decf753a49dabad65a4689b91a136ffc76f0cbdbd17215ac6eb4a4fe13cb30bf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2768501789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb707830cc5711c3f7e12213dd0845dc017f5b4a7c8ce31eefdabe99af4c3586`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 19:03:16 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 11 Jan 2022 19:22:21 GMT
ENV PYTHON_VERSION=3.9.9
# Tue, 11 Jan 2022 19:22:22 GMT
ENV PYTHON_RELEASE=3.9.9
# Tue, 11 Jan 2022 19:24:42 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Tue, 11 Jan 2022 19:24:43 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 11 Jan 2022 19:24:44 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 11 Jan 2022 19:24:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Tue, 11 Jan 2022 19:24:47 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Tue, 11 Jan 2022 19:26:35 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 11 Jan 2022 19:26:36 GMT
CMD ["python"]
# Wed, 12 Jan 2022 06:37:41 GMT
ENV HY_VERSION=1.0a4
# Wed, 12 Jan 2022 06:37:42 GMT
ENV HYRULE_VERSION=0.1
# Wed, 12 Jan 2022 06:38:54 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 12 Jan 2022 06:38:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1d7d79b7b7fe7eea084017c3aa788ff192ce295331911516ca7ed3fed49efc`  
		Last Modified: Tue, 11 Jan 2022 19:32:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a35a3ac4cf853bd2ac258aa2bfc8d7d7538e437a48a99681fd193af6454bd7`  
		Last Modified: Tue, 11 Jan 2022 19:36:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1962756dfe022be6722b3e107fc6304ddbb16172dde521b0b26de4dbb06ba6db`  
		Last Modified: Tue, 11 Jan 2022 19:36:41 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a90ccfcec3602a61bc6e7350c8293dbee6cde23781dc0f3dcb11a3569b4b75e`  
		Last Modified: Tue, 11 Jan 2022 19:36:49 GMT  
		Size: 49.7 MB (49656301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81ec16001a4d683d3563777b3de3644cb952cc459229eb7217f5acdf6ca07f6`  
		Last Modified: Tue, 11 Jan 2022 19:36:41 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab065bc84f28382e65a24c86f3f174953a7cf1f045d486b7eaaf65834db6f03`  
		Last Modified: Tue, 11 Jan 2022 19:36:39 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595a74a4b485069858fbd223b14b82a8745772ea7b856aa1bbc199eb8420742a`  
		Last Modified: Tue, 11 Jan 2022 19:36:39 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782a4345ebfd14086e10131918dbd5479fd94475095746f7151e2446a3ad731e`  
		Last Modified: Tue, 11 Jan 2022 19:36:39 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285cd5de045fd0bb1e776b7cc77b6c619a909b4993702d32d44acf53a4ec4212`  
		Last Modified: Tue, 11 Jan 2022 19:36:41 GMT  
		Size: 6.3 MB (6304341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947c94b5f1051d02f15e32c0a153c007eba76c100a9ffef4c09d8aa96c73e71d`  
		Last Modified: Tue, 11 Jan 2022 19:36:39 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8939bab7231bd16da693085ea4eb7e273d899b516901d28cf5d3c9f7bb2b277`  
		Last Modified: Wed, 12 Jan 2022 06:44:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0816e0c9781335863b9e45932445def66c431092f07d020c7abeada19f7a73`  
		Last Modified: Wed, 12 Jan 2022 06:44:22 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff52c602251da82a87b055e9a304b214be66d910ffbd379870e50b5a526dbcc`  
		Last Modified: Wed, 12 Jan 2022 06:44:23 GMT  
		Size: 939.7 KB (939665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2abdf2241fef11ed8180e2817ac0800fd32eec6074d960a24adbc777f9490fa`  
		Last Modified: Wed, 12 Jan 2022 06:44:22 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
