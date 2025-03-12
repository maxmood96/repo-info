## `hylang:python3.12-windowsservercore-1809`

```console
$ docker pull hylang@sha256:8aed5502b8bcd8465f5a4e77fa7117b53cfe52e3b587f7ec1644f115cba1d325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `hylang:python3.12-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull hylang@sha256:b1c88ee6bd6d27516512aa987c5ae7464fef7f30862931f66de5ef35eb59e432
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2217364553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4785d2e9421a2c7c5d85923552b8969dcaa8b489acccbcc2d37f6047a781b11d`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:49:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:49:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 18:49:45 GMT
ENV PYTHON_VERSION=3.12.9
# Wed, 12 Mar 2025 18:49:46 GMT
ENV PYTHON_SHA256=2a52993092a19cfdffe126e2eeac46a4265e25705614546604ad44988e040c0f
# Wed, 12 Mar 2025 18:50:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:51:00 GMT
CMD ["python"]
# Wed, 12 Mar 2025 19:17:49 GMT
ENV HY_VERSION=1.0.0
# Wed, 12 Mar 2025 19:17:51 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 12 Mar 2025 19:18:48 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 12 Mar 2025 19:18:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc182e7cf13f9e22000cba27deb4457ea1d5d2f34837430884a4792580ec3c56`  
		Last Modified: Wed, 12 Mar 2025 18:51:04 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55898bef7227dc9e811a2ce352d54904c26c465ca3c8e168ab1c4d4bf9eb1923`  
		Last Modified: Wed, 12 Mar 2025 18:51:03 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3900e17be4fadf995bac023c1a2a187794c72ba719a24b98dc7e716da02954`  
		Last Modified: Wed, 12 Mar 2025 18:51:03 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e938bb4969cb839486b1b3ef95e92d3069f16e27e4b701ec9fbf89dfdf908e67`  
		Last Modified: Wed, 12 Mar 2025 18:51:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3297900c2bc8f782af2ef806eb969009c1b54e97da62d46e9c59895bd366b2`  
		Last Modified: Wed, 12 Mar 2025 18:51:08 GMT  
		Size: 58.6 MB (58607213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625a88776fd655768154e0d14b390368d6c1d4fbc6ddbfcde9d96220ddf23b1c`  
		Last Modified: Wed, 12 Mar 2025 18:51:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa83d096775d192af508439771ffd48e565eeec47ebfdd5f600755416c81549`  
		Last Modified: Wed, 12 Mar 2025 19:18:53 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a40fa4e2f44031abad4125aeed6484529721fe7a857b4cc444137b92d80a85d`  
		Last Modified: Wed, 12 Mar 2025 19:18:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c15ffae0329e7a8e1fb79405433f470f65ea0782495a0f05c2ed32d09aedff`  
		Last Modified: Wed, 12 Mar 2025 19:18:54 GMT  
		Size: 7.1 MB (7112324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10465a5f2c133bea92fed8c0775cea6f06e189bc74943dbb6a3b2cd185ef8b1f`  
		Last Modified: Wed, 12 Mar 2025 19:18:53 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
