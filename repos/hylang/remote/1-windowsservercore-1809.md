## `hylang:1-windowsservercore-1809`

```console
$ docker pull hylang@sha256:472980f5de77436713d2c247b773cd7062e3c93003eb8413688ee5ceb9b77a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `hylang:1-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull hylang@sha256:edcd603cb84f0fc5d27f5121ae355b1838d6b79e8c5a90929daf847cb8f48191
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075407082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0df8fee57532535c0482b33a338388f11d9ba66c69b75faccdd8a07087e8de`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:18:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:18:32 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 14 Nov 2024 20:18:33 GMT
ENV PYTHON_VERSION=3.13.0
# Thu, 14 Nov 2024 20:18:33 GMT
ENV PYTHON_SHA256=78156ad0cf0ec4123bfb5333b40f078596ebf15f2d062a10144863680afbdefc
# Thu, 14 Nov 2024 20:20:18 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:20:19 GMT
CMD ["python"]
# Thu, 14 Nov 2024 21:21:42 GMT
ENV HY_VERSION=1.0.0
# Thu, 14 Nov 2024 21:21:44 GMT
ENV HYRULE_VERSION=0.7.0
# Thu, 14 Nov 2024 21:23:08 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 14 Nov 2024 21:23:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33faaaa342cf5ea879707bfd0ec7e1bbf9e55acf595859c29002cda9715d0759`  
		Last Modified: Thu, 14 Nov 2024 20:20:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9e048993d10b503629950c8739bcaa886395e07d4c2d631243230cd9aba76e`  
		Last Modified: Thu, 14 Nov 2024 20:20:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e911286c397244c6526ae07c7a27e450803cfb341fcdd0cbb78d3cfae16e84a`  
		Last Modified: Thu, 14 Nov 2024 20:20:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeaacbff3cb119c2d8df7a9b839be99cdd3a84a917fa164f9bdaa059c6205565`  
		Last Modified: Thu, 14 Nov 2024 20:20:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9c8be745b040cec06d795882cf237a5a0e125713165574534a245acb33b41c`  
		Last Modified: Thu, 14 Nov 2024 20:20:27 GMT  
		Size: 57.6 MB (57595680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f20e1b3af557ac4be54eab69100ce39ba15cc0c1650fe5c0261caf2a4ee292b`  
		Last Modified: Thu, 14 Nov 2024 20:20:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b5b684c8cd7c0fd9cbc0dac4db677b299a73f9a06c8253a8cc2c48b83218ef`  
		Last Modified: Thu, 14 Nov 2024 21:23:12 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b7f8c98afb324ca1c0b23f80e111856cf86887b993f8d0ab7573f86d5c0520`  
		Last Modified: Thu, 14 Nov 2024 21:23:12 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc729ec1d74c0871da42a2ce0dd9d7618daaaf42c49b85eeeaae82a438f08ee`  
		Last Modified: Thu, 14 Nov 2024 21:23:12 GMT  
		Size: 7.1 MB (7147124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fb684e7eb92905544262646dd35b40a5cd4bb6f5b831b64b216241680cb715`  
		Last Modified: Thu, 14 Nov 2024 21:23:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
