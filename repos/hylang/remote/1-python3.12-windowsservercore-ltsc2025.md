## `hylang:1-python3.12-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:2193856bf63091293ed51f39a449d4900a26b4461082876541bff3d660af4fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `hylang:1-python3.12-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull hylang@sha256:0c0e27605fd4d431e8444d92d10a584fcfc4c5f7c895f4e8da5d113b53e4e1ac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2977381983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04150da862cb0595d844a8f68cb01c6a94bcaa5491f0c2bde2cb7b2507dbad82`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:48:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:48:19 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 18:48:20 GMT
ENV PYTHON_VERSION=3.12.9
# Wed, 12 Mar 2025 18:48:21 GMT
ENV PYTHON_SHA256=2a52993092a19cfdffe126e2eeac46a4265e25705614546604ad44988e040c0f
# Wed, 12 Mar 2025 18:48:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:59 GMT
CMD ["python"]
# Wed, 12 Mar 2025 19:18:05 GMT
ENV HY_VERSION=1.0.0
# Wed, 12 Mar 2025 19:18:07 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 12 Mar 2025 19:18:46 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 12 Mar 2025 19:18:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6ab578ec8491b47ec39e11a79eeac738d23b741f5f2d9480e6f8f35366e9c8`  
		Last Modified: Wed, 12 Mar 2025 18:49:05 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095ddf14630b8b7dcff9dbdf09047657aa0f426431be631646cf7a5f04d5b3cc`  
		Last Modified: Wed, 12 Mar 2025 18:49:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6732778a9d15b5ceedc87d2fd5974a16ecc0f3f3aba789df74feeb38c278b2`  
		Last Modified: Wed, 12 Mar 2025 18:49:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab72a92e0ac0561e7ecf182a29d3bd6a8fb17976e172558e51a5fd99ac666fe`  
		Last Modified: Wed, 12 Mar 2025 18:49:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48feb201ade569bac5347a5e18f93cb3c2392d976e9a90a2fdbf31fec8f5557e`  
		Last Modified: Wed, 12 Mar 2025 18:49:09 GMT  
		Size: 60.1 MB (60096959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512c0c087e203eae3cbd53618793e3bc1ce757df8be0d04c962dc392579b9e55`  
		Last Modified: Wed, 12 Mar 2025 18:49:03 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeca3573ec84a86a77d32b065a5d32e36c14b12ae030e12954d26ff43a52b5c1`  
		Last Modified: Wed, 12 Mar 2025 19:18:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f2a351fafab1b4603d39c849c98b6aa554fd90158515c11f09c28c6bf3f201`  
		Last Modified: Wed, 12 Mar 2025 19:18:51 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3080e4e47ee475bef9b5373c4f3d0226eb0bce71e440ab888dca839bd190ec13`  
		Last Modified: Wed, 12 Mar 2025 19:18:52 GMT  
		Size: 8.6 MB (8626886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3662e365c0d1d4d52b9f72fed72f7f1f8a8fb27aef68aee13a4d136e683f2d8`  
		Last Modified: Wed, 12 Mar 2025 19:18:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
