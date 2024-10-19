## `hylang:python3.12-windowsservercore-1809`

```console
$ docker pull hylang@sha256:951bf23ed08678cfc02f73b4895f62f58f44d2d5f5627887db15a8f0cb48df3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `hylang:python3.12-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull hylang@sha256:9447052b3101bf1a1c490c2fc2714f6b9216b364bb05afa09f84db6f1ec121e3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1967431352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c090d8c63d4165c13900554f53bb59cebe02fed1f78106b85bf49b4a41e602e0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Sat, 19 Oct 2024 00:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 19 Oct 2024 00:55:29 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 19 Oct 2024 00:55:29 GMT
ENV PYTHON_VERSION=3.12.7
# Sat, 19 Oct 2024 00:55:30 GMT
ENV PYTHON_SHA256=1206721601a62c925d4e4a0dcfc371e88f2ddbe8c0c07962ebb2be9b5bde4570
# Sat, 19 Oct 2024 00:57:32 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Sat, 19 Oct 2024 00:57:33 GMT
CMD ["python"]
# Sat, 19 Oct 2024 02:10:21 GMT
ENV HY_VERSION=1.0.0
# Sat, 19 Oct 2024 02:10:23 GMT
ENV HYRULE_VERSION=0.7.0
# Sat, 19 Oct 2024 02:12:10 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Sat, 19 Oct 2024 02:12:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b35f0e0ca9afbf7af8ca04e1d174a4eb00b2fd2b058ce0db51a4f92a2e4e4e`  
		Last Modified: Sat, 19 Oct 2024 00:57:38 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1f01ac08dada2d930822ee929d7c0b4ace4a56ea9179be02439de0b6555f2d`  
		Last Modified: Sat, 19 Oct 2024 00:57:37 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a24e3b848801f63b45bd7ded4ac828977bd7d0c12011e09dc44e8df8933e570`  
		Last Modified: Sat, 19 Oct 2024 00:57:37 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f940227e9a54cd3801612acfea467250d6c9ae3583a4b1e65df7126d4d192502`  
		Last Modified: Sat, 19 Oct 2024 00:57:37 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecec472c88a2410bf9d724d3421ea9f5357257fcfd015e29b41d3fa4b14acef1`  
		Last Modified: Sat, 19 Oct 2024 00:57:41 GMT  
		Size: 58.5 MB (58454821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa0030ff8562f26181cb3a3e1f88e7ad0e8f92632387493e42234fb8f7b6af6`  
		Last Modified: Sat, 19 Oct 2024 00:57:37 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14d091e3d14a122be538907576c762ec1387c286a22cc46d2db9774ed56b71d`  
		Last Modified: Sat, 19 Oct 2024 02:12:15 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021cd53b2b68080aee51bcfc0185a747c3ec2ecea0b5a3d5b5b14eb2f19d7a7`  
		Last Modified: Sat, 19 Oct 2024 02:12:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccd8c0e620012f6c6420d5ae3de0bd90233d4ef8d03a0390f6036dbe53d9cc5`  
		Last Modified: Sat, 19 Oct 2024 02:12:17 GMT  
		Size: 7.1 MB (7140450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed452f810abde06bc24ed5b49edc13ae5d0b235bae91929b1f18e8a869a1833f`  
		Last Modified: Sat, 19 Oct 2024 02:12:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
