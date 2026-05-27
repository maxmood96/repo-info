## `hylang:python3.15-rc-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:bad921fff3cb419f5bd9d3e9b70d5cf48d344230b87ac5e80e3d74ec26b35a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `hylang:python3.15-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

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
