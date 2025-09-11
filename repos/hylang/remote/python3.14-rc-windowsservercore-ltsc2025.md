## `hylang:python3.14-rc-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:3fa28118b4ea508e9b25418956e7763c469462bfa201530404d22b5324bc12eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `hylang:python3.14-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull hylang@sha256:1cdd3e6416c8e9e1748e483c3980e54fa237ffbc9fa5b4e4ff52eb10bf6a9d3c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3640778010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216da418aa16d8f25f6ab14954636938edeb13a49337d9d52698fd26b94ce3fd`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:49:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 22:01:02 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 10 Sep 2025 22:01:03 GMT
ENV PYTHON_VERSION=3.14.0rc2
# Wed, 10 Sep 2025 22:01:04 GMT
ENV PYTHON_SHA256=cf4732baba457a6d444f4c084e0bcf9eab4302730b5cab6031e5767bab3a2a7f
# Wed, 10 Sep 2025 22:01:50 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 22:01:51 GMT
CMD ["python"]
# Wed, 10 Sep 2025 22:21:04 GMT
ENV HY_VERSION=1.1.0
# Wed, 10 Sep 2025 22:21:05 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 10 Sep 2025 22:21:33 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 10 Sep 2025 22:21:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fd427e102cbe35deefe716d425d4fb43161e3bb67a6a5fb81d622845645d2e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1741415ee1d7f916c1982f96574f5d7c49d3ead6abed0dd9928bdff6ef093763`  
		Last Modified: Wed, 10 Sep 2025 22:02:35 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c49f4f4e0d8027042342d8a63cf4346644e4dd16feb1c79c18b13d6d4bea303`  
		Last Modified: Wed, 10 Sep 2025 22:02:35 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5713b80fae71ec5c648c16e075e2d68d0c3a06efee6371b34cd90be52723cf9`  
		Last Modified: Wed, 10 Sep 2025 22:02:35 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ca808ea95a9bfec8c73e0bdec282596be11843b88299ecb4648879f175d361`  
		Last Modified: Wed, 10 Sep 2025 22:02:42 GMT  
		Size: 60.8 MB (60755304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9926145c6234bd769834c079c6a902ddaafa1dc59b0c66f3e452e06bf3e9147b`  
		Last Modified: Wed, 10 Sep 2025 22:02:35 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f6745645233a5d6f09047f316b87e864de49731765374001385bd11bb8a91d`  
		Last Modified: Wed, 10 Sep 2025 22:21:50 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32193ea577481e0a7697cbcd5d31e5fbf83921b35087a5fda2cef5144a402dcc`  
		Last Modified: Wed, 10 Sep 2025 22:21:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0dfb3b6126b21c37af2e1829fa3387cb3e9630e1c859c1c27ba54898a88609`  
		Last Modified: Wed, 10 Sep 2025 22:21:51 GMT  
		Size: 8.6 MB (8572476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6539bea670b420c13f74b4e378e7c20d527818311746c2b9b83688884f813b8c`  
		Last Modified: Wed, 10 Sep 2025 22:21:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
