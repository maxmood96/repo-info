## `hylang:python3.12-windowsservercore-1809`

```console
$ docker pull hylang@sha256:5f004905b05d33a4f38927e80d8073cbcef9568cf23c9f9a6891f7027fe6e8ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `hylang:python3.12-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull hylang@sha256:836c6254b9aeb273f893318c2d7db61fb406282d9b7d446820583d3d6330e8d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2249663543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50fa05d55053725b79c41c51a3e3e5299b788d5b0eb5772754593be3b11d236c`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:01:47 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 May 2025 21:01:48 GMT
ENV PYTHON_VERSION=3.12.10
# Wed, 14 May 2025 21:01:48 GMT
ENV PYTHON_SHA256=67b5635e80ea51072b87941312d00ec8927c4db9ba18938f7ad2d27b328b95fb
# Wed, 14 May 2025 21:02:40 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:02:41 GMT
CMD ["python"]
# Wed, 14 May 2025 21:11:12 GMT
ENV HY_VERSION=1.1.0
# Wed, 14 May 2025 21:11:13 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 14 May 2025 21:11:55 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 May 2025 21:11:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8223cfc55541f2c8fe083bb4ab6e3fb60bdaf483d8bbb133de4abade089cc21`  
		Last Modified: Wed, 14 May 2025 21:02:47 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0feafd314dbe2c54629d5ab05e755a69e599f5376d89d037ecdeaf0ab0f5c17c`  
		Last Modified: Wed, 14 May 2025 21:02:45 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2673a5986e4c9b584f69a34a3848ba077e9036e78713af82e47b3f6f332912e9`  
		Last Modified: Wed, 14 May 2025 21:02:45 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54460b2f5ec458eb0266282e48f310f51470906521f8d24ebc775f34e56b786c`  
		Last Modified: Wed, 14 May 2025 21:02:45 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a899b710bb575dc9daf02743f7e656cecae43ef738a2656555c4b7063123ecf`  
		Last Modified: Wed, 14 May 2025 21:02:51 GMT  
		Size: 58.8 MB (58798702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bc3300376edee630648fe5977f2cccf643219214240662b231f0379515a133`  
		Last Modified: Wed, 14 May 2025 21:02:45 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34374542819aa0665536ad0ca2cfb52a1e9f3a48941aebd9380ecac4d5742107`  
		Last Modified: Wed, 14 May 2025 21:11:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fac2154bc242095e2e18c7941806147664ff252e19b26ab5ad131d159f378eb`  
		Last Modified: Wed, 14 May 2025 21:12:00 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c52c2fc776fb1315889337e79d9a8b9df7bd6e760debc14eca880f2bcb8147`  
		Last Modified: Wed, 14 May 2025 21:12:01 GMT  
		Size: 7.1 MB (7136656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d6eb97cae1d6f81e8fd1c4b941d3ef344a82cff8e203358567f66fe710912d`  
		Last Modified: Wed, 14 May 2025 21:12:00 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
