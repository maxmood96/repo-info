## `hylang:python3.13-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:644cadc2dd3adcf52a5fe700eb5e01886f1345f20e8e74c87865273ce3fe5ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `hylang:python3.13-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull hylang@sha256:c48867b1cafcb2e9dd8173cd3ad000b9ddff28d4b4728a61e9a4650692f6ac7e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2567949023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e69374ad1ce6a89b20e03ec898c55c3563375778a38d2355b34b8ac333f3f0e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:35:33 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 22 Jan 2025 20:35:34 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 22 Jan 2025 20:35:34 GMT
ENV PYTHON_SHA256=6b33fa9a439a86f553f9f60e538ccabc857d2f308bc77c477c04a46552ade81f
# Wed, 22 Jan 2025 20:36:14 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:36:15 GMT
CMD ["python"]
# Thu, 23 Jan 2025 01:31:31 GMT
ENV HY_VERSION=1.0.0
# Thu, 23 Jan 2025 01:31:31 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 23 Jan 2025 01:32:04 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 23 Jan 2025 01:32:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19237d199862601a98531e9b8bfda6501ab27c1f30eb6a4abbeb22c52f6916a`  
		Last Modified: Wed, 22 Jan 2025 20:36:20 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130efb27f2a57cab4bfa2dc4a52f549e4643ff63c2b35e7ba2da8db8bd0dd3ce`  
		Last Modified: Wed, 22 Jan 2025 20:36:19 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dd8a5b956b01088ab04c71d167c383aa836ad3da3fa19350a2f50aab38c498`  
		Last Modified: Wed, 22 Jan 2025 20:36:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78f598b5bbfd8426db2abb3783b51ad8767c4c2b1a3e0f92acf8e60fe3c0676`  
		Last Modified: Wed, 22 Jan 2025 20:36:19 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713940dd6a6fe43204145a02a404d436530759cf49bb2612d05adcf2e202dc36`  
		Last Modified: Wed, 22 Jan 2025 20:36:24 GMT  
		Size: 59.1 MB (59126015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953707e6644d3ec25aa83b610ec6b7b2af6bfeb4caa072858a9552c05e18935c`  
		Last Modified: Wed, 22 Jan 2025 20:36:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bc5da18bb41d30db50519d239a34f50883f97cbb8137db3edb4f11f94c6d4b`  
		Last Modified: Thu, 23 Jan 2025 01:32:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49e528022936eda4df16b3c13be9a85731ec061948f41b6172b51f8b31386ed`  
		Last Modified: Thu, 23 Jan 2025 01:32:07 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59a740169286cd93a78fadcc087de5e53fb87098ad268768bdbb16eb89d81bd`  
		Last Modified: Thu, 23 Jan 2025 01:32:08 GMT  
		Size: 8.5 MB (8535013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba7705b695d089cf044138d2a8768bb455375861649a924e41b7e5ff2a2542f`  
		Last Modified: Thu, 23 Jan 2025 01:32:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
