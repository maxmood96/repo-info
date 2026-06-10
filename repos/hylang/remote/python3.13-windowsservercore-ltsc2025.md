## `hylang:python3.13-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:3fc5c842d99b6a7b0305e6c307bf600106501c72191d9496e74a3fa43c8150d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `hylang:python3.13-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull hylang@sha256:12405950240eb98c6dd805906aa4216e965b5dac529c694654f5c8b886897b69
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346447460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f868e92192782d6d41cb7ce86c7d343f13edaa6d619b22efb717d7d784ee0ee4`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:13:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:25:41 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 09 Jun 2026 22:25:41 GMT
ENV PYTHON_VERSION=3.13.13
# Tue, 09 Jun 2026 22:25:42 GMT
ENV PYTHON_SHA256=3c9c81d80f91c002ced86d645422d81432c68c7d9b6b0e974768ca2e449a4d00
# Tue, 09 Jun 2026 22:26:22 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:26:23 GMT
CMD ["python"]
# Tue, 09 Jun 2026 23:22:35 GMT
ENV HY_VERSION=1.3.0
# Tue, 09 Jun 2026 23:22:35 GMT
ENV HYRULE_VERSION=1.1.0
# Tue, 09 Jun 2026 23:23:17 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 09 Jun 2026 23:23:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac36840d63df762ebfcb782261ddd28db92bf6ffe83aa68028d7c342812ec9a5`  
		Last Modified: Tue, 09 Jun 2026 22:14:25 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af1f2c5398b217edecbf97f74aaad00da05892ce68340a58c7dca51792812a7`  
		Last Modified: Tue, 09 Jun 2026 22:26:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b9886e64946c08db874f2ffeefe536ed451cd34919def1c9c65b34ba2af56a`  
		Last Modified: Tue, 09 Jun 2026 22:26:28 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef70d9db85381254cb0d56f3a3571c05bf32e642ea3ca030a7cdf56b12cecb3c`  
		Last Modified: Tue, 09 Jun 2026 22:26:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74429b1f8218f507401a2c977b17fb033a9d164e98ee96f18cba03bb07e100ec`  
		Last Modified: Tue, 09 Jun 2026 22:26:35 GMT  
		Size: 58.9 MB (58935955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209fb096024886ae2eb5ee47a656f966c8d87444d58370d29604e711a576cdb5`  
		Last Modified: Tue, 09 Jun 2026 22:26:28 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a59689a054e635fb5a75bdc1d375d90ea8c1c8bce82748cb06e6552b9720600`  
		Last Modified: Tue, 09 Jun 2026 23:23:21 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a891ecf98153d26b1fe30828e951a4308fe08cca4f941e6f472def521e8173b7`  
		Last Modified: Tue, 09 Jun 2026 23:23:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187ea974a1d0b0c862f62e314e86e5d76105780c777f9743b0b8e182bbdba2c1`  
		Last Modified: Tue, 09 Jun 2026 23:23:23 GMT  
		Size: 8.4 MB (8358199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d87820ba50eb45ec67b017a79c61740e0595612f56777f1d2c2502397b6edd`  
		Last Modified: Tue, 09 Jun 2026 23:23:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
