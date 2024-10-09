## `hylang:1-python3.13-windowsservercore-1809`

```console
$ docker pull hylang@sha256:fb7fe7631cf91547b0a354020880a04265f666272d012ec32135e3d1eb5e6b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `hylang:1-python3.13-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull hylang@sha256:cc54b38579571505bfb826c14ef892ece14aaa183449c8e0a34a46e2fe0ec982
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1785066828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5eb02eb87bd4211eb2f832f35ef49b1557568aed2b4e629f2fa92a8f28bbb0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Mon, 07 Oct 2024 23:58:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Oct 2024 23:58:28 GMT
ENV PYTHONIOENCODING=UTF-8
# Mon, 07 Oct 2024 23:58:28 GMT
ENV PYTHON_VERSION=3.13.0
# Tue, 08 Oct 2024 00:00:58 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 08 Oct 2024 00:00:59 GMT
CMD ["python"]
# Wed, 09 Oct 2024 00:04:53 GMT
ENV HY_VERSION=1.0.0
# Wed, 09 Oct 2024 00:04:54 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 09 Oct 2024 00:05:34 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 09 Oct 2024 00:05:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4f5beaab8987474694d050e9b59d3bdae365f75b6adbef41facc9bff75a8f5`  
		Last Modified: Tue, 08 Oct 2024 00:01:03 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c60cb593aaa6c27c51614d217c437c6b922458e9dad94660aef27e8bdd09439`  
		Last Modified: Tue, 08 Oct 2024 00:01:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fa69649489797663455e246f6a56d96feac0a1524425724256b7e02e6443fd`  
		Last Modified: Tue, 08 Oct 2024 00:01:03 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d395d3501186ed36ca3bf7c76049197f4714af17c23355e1d9f96e44c0018455`  
		Last Modified: Tue, 08 Oct 2024 00:01:08 GMT  
		Size: 57.5 MB (57479386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c241c217fc02e13f43b2f304701cef3106e3c578b5539270c9a5467d9b4c8a84`  
		Last Modified: Tue, 08 Oct 2024 00:01:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02975168587ac577a11467580f7111d726cdb6fd78cd87e78572f1301858a643`  
		Last Modified: Wed, 09 Oct 2024 00:05:39 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc6f0513a351e5d08f5242e10adfc08e4b32bbb418b27ee890c3a266ffdf4ef`  
		Last Modified: Wed, 09 Oct 2024 00:05:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fe48b47aeb2570e6a8f7352306e7ea053beeae923a290a65221293498aa9bd`  
		Last Modified: Wed, 09 Oct 2024 00:05:40 GMT  
		Size: 7.3 MB (7309985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefa7940bb19c0f9453542f8fb7ea93e472219facf06c0cc8497a8bba308a234`  
		Last Modified: Wed, 09 Oct 2024 00:05:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
