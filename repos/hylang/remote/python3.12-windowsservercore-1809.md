## `hylang:python3.12-windowsservercore-1809`

```console
$ docker pull hylang@sha256:2f3f585e13393ec0a76b8553b30012083c64260e897f25f666de8a6680baa2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `hylang:python3.12-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull hylang@sha256:d324805179b89128b84333f01394fe526cc0e1febcdc1cd22bb28998d5771d06
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2080033483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba682b0ba4d26bec8e64afd32faa4bd963e4a91c6b2d64c5504e79b606948353`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:41:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 11 Dec 2024 20:41:50 GMT
ENV PYTHON_VERSION=3.12.8
# Wed, 11 Dec 2024 20:41:50 GMT
ENV PYTHON_SHA256=71bd44e6b0e91c17558963557e4cdb80b483de9b0a0a9717f06cf896f95ab598
# Wed, 11 Dec 2024 20:42:46 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:42:47 GMT
CMD ["python"]
# Wed, 11 Dec 2024 21:42:15 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 21:42:16 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 21:43:00 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 11 Dec 2024 21:43:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c69b30de0bb94495a01d2ffa3cbe2160d47354a632fa558a9a28bb1f5586a26`  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3f4905dceffd459d14fbfb30b842c645d5d62e6248061cb2b78399fe229df9`  
		Last Modified: Wed, 11 Dec 2024 20:42:51 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61eb8d3c795404a9cce5e17b329a1d1d8f7e3403af85c201eee41fbf81d3d14`  
		Last Modified: Wed, 11 Dec 2024 20:42:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf845fe8780bfa8b4a27751991a0bc5196b903cf3c58ac13e37e1cf1d0ee557`  
		Last Modified: Wed, 11 Dec 2024 20:42:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb2a1b246e83da13677def7201662292fbef830339c769b762c341cc1c5e043`  
		Size: 58.7 MB (58732455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf5cf7377be1465e2468dce6ac41ac1f30018149d8eca84eb04e1723195c16f`  
		Last Modified: Wed, 11 Dec 2024 20:42:51 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd45c9de024c14b50839877fe61a7ec0dad686afe0832186bdb98b17c94737ff`  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66440333fec0da771f09e768aeba1e8bc568afcd7ab31760e3f81e3ebd8a39c`  
		Last Modified: Wed, 11 Dec 2024 21:43:05 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9eedae6d81c3ac2fc8f4cc7f7f2953cbd10fa6bfed3029af2710cc833959cc`  
		Size: 7.1 MB (7120328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638cddf4563cde2905140f158bbef89081c438bd1e80d8e445abc38aec3c3978`  
		Last Modified: Wed, 11 Dec 2024 21:43:05 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
