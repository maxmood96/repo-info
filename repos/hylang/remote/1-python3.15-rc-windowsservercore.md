## `hylang:1-python3.15-rc-windowsservercore`

```console
$ docker pull hylang@sha256:74eecec9a4c07d227d8f2490c20d43572b82faee13b12c4540f38782f897c68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `hylang:1-python3.15-rc-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull hylang@sha256:3837d9168276f86d513f67620e69cb64957731889847167032ba224b1dee890f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279540117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ca724fb963bfb1a2f23700286219ca2dd2a3874584156278c1b6165afb9251`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:50:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:50:01 GMT
ENV PYTHON_VERSION=3.15.0b1
# Tue, 12 May 2026 23:50:02 GMT
ENV PYTHON_SHA256=de7f62783f765061c7e97ed7b30f780c3d15de5b3154e88b2f9cb92ce1df6957
# Tue, 12 May 2026 23:50:45 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:46 GMT
CMD ["python"]
# Wed, 27 May 2026 00:13:15 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:13:17 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:14:29 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 27 May 2026 00:14:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dab9e350fc730aed7db6c5533fb3137169005dbb3d03e7ec95809aba0cb46c`  
		Last Modified: Tue, 12 May 2026 23:40:03 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7943388fa07ee1de54b31509671e91d9bd87ae0ee43e59ee8143343d59bf6fce`  
		Last Modified: Tue, 12 May 2026 23:50:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5af423f6ebba9483e7961631ccc3cd37a9cae0d9613c8cfe391745bdb69b0`  
		Last Modified: Tue, 12 May 2026 23:50:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4055cebf29157b9781801828fc2178a4fee2bab70a10c89b69ed4d8752cb7328`  
		Last Modified: Tue, 12 May 2026 23:50:50 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f6b0a5a11324ed15cd085378f74242535634187deec757e960d4cfb95bfe83`  
		Last Modified: Tue, 12 May 2026 23:50:57 GMT  
		Size: 65.2 MB (65157996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbf5decb3fbf6f79727af21287c526b118876643dbecfb1023ea039836929a6`  
		Last Modified: Tue, 12 May 2026 23:50:50 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9275d0e27b60392d1b6c84e18c4e52fdd7281ea649852221a01a76367e8f82`  
		Last Modified: Wed, 27 May 2026 00:14:34 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdc0e599ce1d9c994b96197ab8001e01ade07ba10be81d635082c6e0bc6f08d`  
		Last Modified: Wed, 27 May 2026 00:14:34 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ef20cd0ee8bf5473c34f52661e753dc1964c6ffb0e277deb6117dae7c85f1f`  
		Last Modified: Wed, 27 May 2026 00:14:36 GMT  
		Size: 8.4 MB (8429649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17210b3a2c05eb5a0323c289e04ebf7d2e2dff695010c0f4d6c7733a9673fb65`  
		Last Modified: Wed, 27 May 2026 00:14:34 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-python3.15-rc-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull hylang@sha256:e7b72a15737df61aa7955b5617c30ad44da5fff04c144aa08cc93d2a2ebfc613
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2196563267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb924a2b02a490c563650dd8cfaa4e1daf1491b10ef51c3bd135c90e6278f17`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:58:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:58:02 GMT
ENV PYTHON_VERSION=3.15.0b1
# Tue, 12 May 2026 23:58:02 GMT
ENV PYTHON_SHA256=de7f62783f765061c7e97ed7b30f780c3d15de5b3154e88b2f9cb92ce1df6957
# Tue, 12 May 2026 23:58:42 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:58:43 GMT
CMD ["python"]
# Wed, 27 May 2026 00:12:45 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:12:47 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:14:17 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 27 May 2026 00:14:19 GMT
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
	-	`sha256:7e72ddab0326e6089ca74907ae3ac383e56049d5df737a07aea5f46d67a27c95`  
		Last Modified: Tue, 12 May 2026 23:39:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f85c007ea80447f4c9c70381246307e47dc0fa56e1b7ab0acb3e8ed34cb42fa`  
		Last Modified: Tue, 12 May 2026 23:58:47 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b1a76beeb5c68989dc478ad5f31e2a8069647efb386faaed93a09e03b9c61d`  
		Last Modified: Tue, 12 May 2026 23:58:47 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5ebae5f190b89d2d0d39e25abd8f708ef3e3ba1d378f1b4355f014f200bf0f`  
		Last Modified: Tue, 12 May 2026 23:58:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71db24aca82750cb681098d371985ef9ff0311f0d831317e01edbd128c96a48f`  
		Last Modified: Tue, 12 May 2026 23:58:53 GMT  
		Size: 65.5 MB (65503621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b87d4fe1a5cb75e84abfcae675971d95c19bd02839f635b698f7dbfefa444fe`  
		Last Modified: Tue, 12 May 2026 23:58:47 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e946431705d9b7b817e9f5609cfa698b425c2b45fe9226003309117fc5b9dc3c`  
		Last Modified: Wed, 27 May 2026 00:14:23 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a4cb3123664d49bb0cee52a4038bd9b21b5a4c95e5c38b7e5690d8a59b8afc`  
		Last Modified: Wed, 27 May 2026 00:14:23 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f985a8222e7bb1adf9408fb7013976559b9728f02fa5f1a6d8254d9538ee2b48`  
		Last Modified: Wed, 27 May 2026 00:14:25 GMT  
		Size: 8.6 MB (8628491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac38fdccd099e825fc31b84efd27b83a255259b153b10d97b5b5fb99f66d94d`  
		Last Modified: Wed, 27 May 2026 00:14:23 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
