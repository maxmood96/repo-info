## `hylang:windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:5bde602fe1fcd295bb63067211404cdc4ecf54612c9d6e788bddac2a8bb3d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `hylang:windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull hylang@sha256:201ad6c628aa9c45d05f3751ecba599dd27c711a7fc374bd82fa071b00e6ffb9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2192773386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71c637b60cb64a6ee1d656d19f2ea6eb4330525a5d73361bd27651cf167b3be`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:58:09 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:58:10 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 12 May 2026 23:58:11 GMT
ENV PYTHON_SHA256=f9c09f5ed6f796fd1a8bc5ddfa41715a494b453c4781f0e35d5077cf9fa58f6d
# Tue, 12 May 2026 23:58:51 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:58:52 GMT
CMD ["python"]
# Wed, 13 May 2026 00:32:36 GMT
ENV HY_VERSION=1.2.0
# Wed, 13 May 2026 00:32:37 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 13 May 2026 00:33:19 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 13 May 2026 00:33:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7f3cfa06a6dfb39cc22416a3fe6eff4b710bfeeccf05db45d77158ff23cf7b`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91ad01b1d407414ae266c6d5f8d9c0bb0b2689fe371c38a7571438ad85c0e7f`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74178a30e0303c0c21ed95e5ff390e5b58a1a755bd7d53d4167832a08c74400e`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c55dd5cfe2037fd17b90af958774b3cbfbd7147faa9264d71df2de5ca55808f`  
		Last Modified: Tue, 12 May 2026 23:59:02 GMT  
		Size: 61.7 MB (61678797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114d0893892b1275f89469f1046c4d8eb67d669829d0ed2b72970a4b73e53803`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcdeabd4f744e030f044762224448d932632381bf09223bb1940b25ea9f4470`  
		Last Modified: Wed, 13 May 2026 00:33:24 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da8a7ab9885aa10e70a867b36ea938f31bad377ef4b3c74ba22ddb587e4adf7`  
		Last Modified: Wed, 13 May 2026 00:33:24 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c8ba8208ca88101952175c9c517e83a038d1a635b3893697f29b0e43b2d5ab`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 8.7 MB (8663447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03dcefda00dca3ff500774d0c842e6276ffb8c19de3a8cb869c405a18d09eb0`  
		Last Modified: Wed, 13 May 2026 00:33:24 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
