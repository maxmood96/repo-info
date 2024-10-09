## `hylang:python3.12-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:89286042e16e8cdd9f05e3b885ca28efd0a37305fecb6e6018b79041250f8c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `hylang:python3.12-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull hylang@sha256:a480af6eede0fccdf8928730447dd273e5bb031c42cdee6f2c106f19df0e860b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1530955976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2a485edb2bee635d0023cd611ccda4d459c492025bde7f358ef88fd30c9b67`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Tue, 01 Oct 2024 22:20:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 01 Oct 2024 22:20:58 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 01 Oct 2024 22:20:58 GMT
ENV PYTHON_VERSION=3.12.7
# Tue, 01 Oct 2024 22:21:52 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 01 Oct 2024 22:21:53 GMT
CMD ["python"]
# Wed, 09 Oct 2024 00:04:46 GMT
ENV HY_VERSION=1.0.0
# Wed, 09 Oct 2024 00:04:47 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 09 Oct 2024 00:06:04 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 09 Oct 2024 00:06:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f1de96038f21e50e44827ed7cb17f3a51a5b70ae9f0394596ed0337a3580b6`  
		Last Modified: Tue, 01 Oct 2024 22:21:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c6feef198d91217a38f719d7bddb46384411f6c315c0c31bd043b64c9031a`  
		Last Modified: Tue, 01 Oct 2024 22:21:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b808279a4a37c63ddbe872ba40b09988db4b1b95443cb3112f8db9a8b36ff2a4`  
		Last Modified: Tue, 01 Oct 2024 22:21:57 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2956cc242fba49fa3b67649b91474e916efcf78476fe939345114b9bca9206d`  
		Last Modified: Tue, 01 Oct 2024 22:22:02 GMT  
		Size: 59.9 MB (59911656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea2a654e1a0f976bc273a861f10e31063518e237ed2207adce0a404c6bdca23`  
		Last Modified: Tue, 01 Oct 2024 22:21:57 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e2f3b8315623159cb52082b3a0fd9feaa3906d1931dd068c312edfdea53e4c`  
		Last Modified: Wed, 09 Oct 2024 00:06:07 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1995d493a52b6256ca5bbf05f524460c1b599e50a02a9c65ad1a868b4624117`  
		Last Modified: Wed, 09 Oct 2024 00:06:07 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1e136c3ba33171bf903d2988188b3e1db710ee68f53785e9a99555a5bbb072`  
		Last Modified: Wed, 09 Oct 2024 00:06:09 GMT  
		Size: 8.8 MB (8842884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d04e11bd7784496f92530b145e9ab9b4a565e4b4b0eff30055775c11794baf`  
		Last Modified: Wed, 09 Oct 2024 00:06:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
