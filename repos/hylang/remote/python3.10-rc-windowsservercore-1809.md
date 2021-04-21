## `hylang:python3.10-rc-windowsservercore-1809`

```console
$ docker pull hylang@sha256:24574b84dc7a285b56315562b88e1b7e259c4b690c65c58a30009cd423d56d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `hylang:python3.10-rc-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull hylang@sha256:171eabdd7b76cad0c11257a1674fe929bd1c27efe9e76067b4bda5e9685b2722
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528204809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bb442d29f2aa856f296b464d51178f38c42af42abf59aa5b75d75407546480`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:14:23 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 Apr 2021 16:12:03 GMT
ENV PYTHON_VERSION=3.10.0a7
# Wed, 14 Apr 2021 16:12:05 GMT
ENV PYTHON_RELEASE=3.10.0
# Wed, 14 Apr 2021 16:14:03 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 14 Apr 2021 16:14:04 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Wed, 14 Apr 2021 16:14:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/29f37dbe6b3842ccd52d61816a3044173962ebeb/public/get-pip.py
# Wed, 14 Apr 2021 16:14:07 GMT
ENV PYTHON_GET_PIP_SHA256=e03eb8a33d3b441ff484c56a436ff10680479d4bd14e59268e67977ed40904de
# Wed, 14 Apr 2021 16:15:08 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 14 Apr 2021 16:15:09 GMT
CMD ["python"]
# Tue, 20 Apr 2021 01:20:01 GMT
ENV HY_VERSION=1.0a1
# Wed, 21 Apr 2021 01:00:47 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 21 Apr 2021 01:00:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc61c4265bfe314fb772d57da4c3023d46cacdbdab9bb6fd5c475f11696dbab`  
		Last Modified: Wed, 14 Apr 2021 16:38:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26dd937ed415aed6d7b55658d64c0e64b6c00fabc9149cdcf5f46807a0badf6`  
		Last Modified: Wed, 14 Apr 2021 16:38:18 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30c610741e32638ad88b3a931d9dba27429d342f46764e0c15547f009758783`  
		Last Modified: Wed, 14 Apr 2021 16:38:18 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eb0760941830a6e773c8ee0bbbe78705e8c0996304aad223f690e8772ff4f8`  
		Last Modified: Wed, 14 Apr 2021 16:39:21 GMT  
		Size: 51.3 MB (51252865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c59c546c010a19125a37fe8378f84a336e83e07ecf4a7e732f31d740248fe7`  
		Last Modified: Wed, 14 Apr 2021 16:38:16 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e941ef4878ac3688fbef8fe0daa5018a66db59f837f17af7d2f13468ca332afc`  
		Last Modified: Wed, 14 Apr 2021 16:38:15 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0eefbd8808ba84a7895e9499f98eecadb23ed7b46a93559e52b23639c8aa66`  
		Last Modified: Wed, 14 Apr 2021 16:38:15 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cd6386ecba0d504884b37e900280442e1bbc2ef943cea8fb8aa061e5fbb3fc`  
		Last Modified: Wed, 14 Apr 2021 16:38:17 GMT  
		Size: 6.0 MB (5956818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0133349afea57102c91f46c1cb8b2df4d44c7411de09e0ea87de38fd54604b43`  
		Last Modified: Wed, 14 Apr 2021 16:38:15 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca88637e9effd106bfd29aff266e92800c6538d30e3143744dbe4884a607ecc2`  
		Last Modified: Wed, 21 Apr 2021 01:16:21 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859f48f8d7387ec2b5acbbd2cb1c435c71815e8b7306a85a5acd27dff614b7e2`  
		Last Modified: Wed, 21 Apr 2021 01:16:22 GMT  
		Size: 1.2 MB (1227006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e135682c215afaf2e1c2f637d63d8430dd6eda703a38b3c399a776d8278015`  
		Last Modified: Wed, 21 Apr 2021 01:16:21 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
