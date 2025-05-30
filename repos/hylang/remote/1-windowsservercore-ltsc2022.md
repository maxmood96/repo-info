## `hylang:1-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:86f93e53ce83ddd5e01e46c91b8659ecd766a2f840b2e40a3241932cf5a0b665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `hylang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull hylang@sha256:3b41e5e156c9f0141e72146fdfdd9fb7b4c28eb345ad7ca228f04170ee16cbd9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2341307380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89be3510cc8b7d3628a10550502e7a108bd30f5b5f3edd6fc6351f30dda84481`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 21:07:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:07:36 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 May 2025 21:07:37 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 14 May 2025 21:07:37 GMT
ENV PYTHON_SHA256=698f2df46e1a3dd92f393458eea77bd94ef5ff21f0d5bf5cf676f3d28a9b4b6c
# Wed, 14 May 2025 21:08:17 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:08:18 GMT
CMD ["python"]
# Fri, 30 May 2025 18:03:05 GMT
ENV HY_VERSION=1.1.0
# Fri, 30 May 2025 18:03:06 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 30 May 2025 18:04:23 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 30 May 2025 18:04:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff0e4dd7efa5989e8bc4bafdbae8281cfe3b6c6e1fb0ace7c967f6875197e87`  
		Last Modified: Wed, 14 May 2025 21:08:24 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8439e54412a351baecd7ee30786516c6f5036f5b96608f42509eac909a0f390`  
		Last Modified: Wed, 14 May 2025 21:08:22 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b713148db48039f3c25322ba75c80b23161d10cd5c7e302ebfc4e702adadda`  
		Last Modified: Wed, 14 May 2025 21:08:22 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f054dc4466e7987629a9722e60275374536c2c3b29703e2b2d07192cd059fe13`  
		Last Modified: Wed, 14 May 2025 21:08:22 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74235f4593ddfb2baac17bcb20948f042e338a4f0f37d56bf9925093b3b088e0`  
		Last Modified: Wed, 14 May 2025 21:08:28 GMT  
		Size: 59.2 MB (59175874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6268e252e5779b0bc804c98ddc3a45ab90d41933b87b6b7dfc90e071f972fd6`  
		Last Modified: Wed, 14 May 2025 21:08:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bb0a8463e4e83f65c766406d3067a9c37a620a0a85cfb5bca2cbef1db385d2`  
		Last Modified: Fri, 30 May 2025 18:04:27 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bb5a494e1d5b1b710874c47ec881c92712d992024948ee84035d09c9ad16b3`  
		Last Modified: Fri, 30 May 2025 18:04:27 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295532bbc252d968dc24cea6466fa5aa87abd6b387973a057625119fd99a9b13`  
		Last Modified: Fri, 30 May 2025 18:04:28 GMT  
		Size: 8.5 MB (8493040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbfc3a9820d243fc28b940ab102dc419a24d26a0bf54c72ea67fc99ce2a0956`  
		Last Modified: Fri, 30 May 2025 18:04:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
