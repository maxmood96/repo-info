## `hylang:1-python3.14-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:bc1e9ebb6885c00a0db90482177e252b542dfdb7318b254ea10b1fc751e2e775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `hylang:1-python3.14-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull hylang@sha256:5e7e2874dd4769cab6a69a60fe5a992304c35233a3e1993fa9634291c811a30f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2051702944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76eac332457113ba7aa6f5ae7dd7ad28c3185b74adf24bea758d209f629d3fa1`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Wed, 08 Apr 2026 17:19:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Apr 2026 17:39:15 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 08 Apr 2026 17:39:16 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 08 Apr 2026 17:39:18 GMT
ENV PYTHON_SHA256=b571567bd11ea98fd7a2cf85791d2c8557a63b1e04e9d1dae665a275cac87f1b
# Wed, 08 Apr 2026 17:40:06 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 08 Apr 2026 17:40:07 GMT
CMD ["python"]
# Wed, 08 Apr 2026 18:20:52 GMT
ENV HY_VERSION=1.2.0
# Wed, 08 Apr 2026 18:20:54 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 08 Apr 2026 18:22:10 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 08 Apr 2026 18:22:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aa4d4919296d1d8685401acc6e97229be39b276efc000646b5f628d584af51`  
		Last Modified: Wed, 08 Apr 2026 17:21:45 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5099a7d88eef52b4ec0b8ae377a225f59b193fd17a33fddf5c33f35674f424f7`  
		Last Modified: Wed, 08 Apr 2026 17:40:12 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e12c50fc7d4bf1c0bc39db543e6cbe506fcaf919fb185dc87d88793d002dc4`  
		Last Modified: Wed, 08 Apr 2026 17:40:12 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfb195495c2a9da00a909ad65e2f97a0a3a0c6acb977d0e91f868fa6a36ce38`  
		Last Modified: Wed, 08 Apr 2026 17:40:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fec5e162c51daeabd27b353a65a161dbb30e2cf513576429ea79031116b50a8`  
		Last Modified: Wed, 08 Apr 2026 17:40:23 GMT  
		Size: 61.1 MB (61124801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ab896369bfc0d36846cc3b88f721f2cbdbaafeffd5dbb50703e3c5e619b20a`  
		Last Modified: Wed, 08 Apr 2026 17:40:12 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f717b6f9b1a37924366b67c61143f175fb19cccc3c5a2b46b744c25e4011f66`  
		Last Modified: Wed, 08 Apr 2026 18:22:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedbef6cf02b5cabdbc5ea4386a41819ce6a50a8f0a6e7977280fa43b27349b`  
		Last Modified: Wed, 08 Apr 2026 18:22:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bf85500d4c8d0b85c82f2fab03c66920dbd08686de3e5a976175be4f64beae`  
		Last Modified: Wed, 08 Apr 2026 18:22:18 GMT  
		Size: 8.3 MB (8286314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cc2c0f80661ef3626ac3b0570db90284344a3d248a1ee0de662aac5d917ffd`  
		Last Modified: Wed, 08 Apr 2026 18:22:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
