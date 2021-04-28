## `hylang:python3.8-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:db989a5c977f1aec3d2d6280c9d15e21c4a1c79e8308b081e4c7ac3375bd64c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `hylang:python3.8-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull hylang@sha256:97430e2098f1be76d8dfeb6186a9a1aaa3b8a425a0988bf6e744d4fe44d19d7c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5871427942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f97ab9f89bbfa4181b0cb9fb60852ea0eafe5be0703d04db56909d2c68629e4`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 16:15:18 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 Apr 2021 16:32:16 GMT
ENV PYTHON_VERSION=3.8.9
# Wed, 14 Apr 2021 16:32:17 GMT
ENV PYTHON_RELEASE=3.8.9
# Wed, 14 Apr 2021 16:34:56 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Tue, 27 Apr 2021 22:21:38 GMT
ENV PYTHON_PIP_VERSION=21.1
# Tue, 27 Apr 2021 22:21:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ab9dde151f662745c13461f00c453dcf32a51ea9/public/get-pip.py
# Tue, 27 Apr 2021 22:21:40 GMT
ENV PYTHON_GET_PIP_SHA256=0ed17e859b835ad5bf00851f4dc8bbc3520c13dfff6c131d410cdb3a92ff0af9
# Tue, 27 Apr 2021 22:23:20 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 27 Apr 2021 22:23:21 GMT
CMD ["python"]
# Tue, 27 Apr 2021 22:47:24 GMT
ENV HY_VERSION=1.0a1
# Tue, 27 Apr 2021 22:48:52 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Tue, 27 Apr 2021 22:48:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b4598ab88dab64b25b4257872564af9825cc6cd41fc8cc1ad11c32958d0da9`  
		Last Modified: Wed, 14 Apr 2021 16:39:38 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2ba2f82f3eddbacdc29cc778a55d06ae05a67ecde117b71217e52591dab5f2`  
		Last Modified: Wed, 14 Apr 2021 16:42:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9327741bb35a9e94c5d9774ebf204c6256a8f84fa6fa63112bcb14e5fb3580`  
		Last Modified: Wed, 14 Apr 2021 16:42:34 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b761757c76a5489a33afa548887814f66f6d6414128957a48a9511cb178d1109`  
		Last Modified: Wed, 14 Apr 2021 16:42:44 GMT  
		Size: 58.6 MB (58623548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b65c55d02062d357f28569cf5629dc0dc21f57144719f552ee0c495c01e0dc`  
		Last Modified: Tue, 27 Apr 2021 22:26:27 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54bfc76d4fd036324e594d632e1129a1e2eb9abb6b6e0d66ea2a794a8a96475`  
		Last Modified: Tue, 27 Apr 2021 22:26:27 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bf02051d3de003fc00925b0e00b1e063aa8ad962077586a0e3d32e8c6d88db`  
		Last Modified: Tue, 27 Apr 2021 22:26:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee2dc08fed8d8ff7aac37dac864bac499652e077ccc35bfde61f8080b70b60f`  
		Last Modified: Tue, 27 Apr 2021 22:26:39 GMT  
		Size: 11.4 MB (11444503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c7f43dcebe057b7926da56cc84714ee215d2b24bd7311024e347ed2a061863`  
		Last Modified: Tue, 27 Apr 2021 22:26:27 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b432211768c8e871feb1191b01481e2fbe9007f92319d268083f96f275f205`  
		Last Modified: Wed, 28 Apr 2021 12:05:27 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09350e48ee2b491dde3ea6c3d409c677d53264f5d9b08c4256a17a8bab48bbac`  
		Last Modified: Wed, 28 Apr 2021 12:05:29 GMT  
		Size: 6.5 MB (6462037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918c00f939f4249e2dcab7bb0ab9a404ecb8a3f4118150df0029dc1d10b0291`  
		Last Modified: Wed, 28 Apr 2021 12:05:28 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
