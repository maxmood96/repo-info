## `hylang:python3.13-windowsservercore-1809`

```console
$ docker pull hylang@sha256:75efc68cc8a8b43a8418255b9a82206ce2744e25983de20795f673e6fb79b104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `hylang:python3.13-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull hylang@sha256:df96a42b20f7b4e38f0d257150f571e4bb9cfac50949a3320aa9f4df32699ef3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2079197684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b88a5855bee282e690ea886a7d3e4efe89aff7b30669c5879e90154170a6d09`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:48:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:48:52 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 11 Dec 2024 20:48:53 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 11 Dec 2024 20:48:53 GMT
ENV PYTHON_SHA256=6b33fa9a439a86f553f9f60e538ccabc857d2f308bc77c477c04a46552ade81f
# Wed, 11 Dec 2024 20:51:03 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:51:03 GMT
CMD ["python"]
# Wed, 11 Dec 2024 21:45:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 21:45:45 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 21:46:53 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 11 Dec 2024 21:46:54 GMT
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
	-	`sha256:423c7669108167f8baa807e0bb78ef040fe68c5036e8e9d0d0e7a06dc61aad3d`  
		Last Modified: Wed, 11 Dec 2024 20:51:07 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0366976a769d834e0b9a1bb4f4bf289b3d8ce27900408161fae4797ab74bd246`  
		Last Modified: Wed, 11 Dec 2024 20:51:06 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643dfe8e4149091507083b0f448a6a113e085c1a645a77d5f2c56f1cdbd30d6e`  
		Last Modified: Wed, 11 Dec 2024 20:51:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d024e102fa3431d027ca055778d02c7f2c5cb325655c8bf121495c32edd4a`  
		Last Modified: Wed, 11 Dec 2024 20:51:06 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1887d08bb6bd5a7af1e5d7066ff48049111f5b6a7decd3c1a9cc4accc4fed`  
		Last Modified: Wed, 11 Dec 2024 20:51:11 GMT  
		Size: 57.9 MB (57882243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde5c805afadbb910417ec0b6c89754f9c1b019ba7931b103a69a8592980dc63`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9418fd6f250d5c1c6bf4accf46444e0f9f3b9b2452350b72bb58a642dd64406c`  
		Last Modified: Wed, 11 Dec 2024 21:46:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a91225254be230adf98a7c672bf07a4047c7ea1d0f67409f40a0b1b2391f5d`  
		Last Modified: Wed, 11 Dec 2024 21:46:58 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ef713cfb7120f5d6379782bfdaed858f31bc4956f3436d29b29a306b484124`  
		Last Modified: Wed, 11 Dec 2024 21:46:59 GMT  
		Size: 7.1 MB (7134814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3d280c6c3c000cb266137deca827c5bf7aba4c552ebf554679c62880d08f21`  
		Last Modified: Wed, 11 Dec 2024 21:46:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
