## `hylang:windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:6c26093868b9b3e897bf0ee2930dff62b799f9233fa5a4755f3608b0dfc1303c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `hylang:windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull hylang@sha256:cbe8bbab9c77e4497a0c2624447126051b6a8bbfc5ec613e74dca8d37b9ac6c8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2150877539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b0ca68edb7d7bae8b47b82914aa61e612b2b65462b926c2b3efc66b6624211`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Wed, 08 Apr 2026 17:19:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Apr 2026 17:39:07 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 08 Apr 2026 17:39:08 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 08 Apr 2026 17:39:09 GMT
ENV PYTHON_SHA256=b571567bd11ea98fd7a2cf85791d2c8557a63b1e04e9d1dae665a275cac87f1b
# Wed, 08 Apr 2026 17:39:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 08 Apr 2026 17:39:59 GMT
CMD ["python"]
# Wed, 08 Apr 2026 18:19:06 GMT
ENV HY_VERSION=1.2.0
# Wed, 08 Apr 2026 18:19:08 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 08 Apr 2026 18:20:39 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 08 Apr 2026 18:20:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b706869c752ba28bcb159891eada3b5f478cd2aa0d7d2ff972a1f0146e43f9`  
		Last Modified: Wed, 08 Apr 2026 17:21:35 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54485d6156054e716eb09b630a88bba3692108c3e9a7f3950edb236e4938266`  
		Last Modified: Wed, 08 Apr 2026 17:40:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c054b2269fa73b2f58d55faad76aff83e788f3eff141678dd5d210fc1a649c5`  
		Last Modified: Wed, 08 Apr 2026 17:40:10 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8a503cb14547dd0cadfc4afe4f38520949a72bbfeb6ae7623548e9ad068d3c`  
		Last Modified: Wed, 08 Apr 2026 17:40:10 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6079c1b5da4ed55e2f60235ee1f3de3651cfbc4f7c4843e5108b8b3cbb10d4`  
		Last Modified: Wed, 08 Apr 2026 17:40:21 GMT  
		Size: 61.2 MB (61248429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ca609ffd10a0c894031c39d4d91ac5fb2950f52db2f1edcc8f76819d17bf6`  
		Last Modified: Wed, 08 Apr 2026 17:40:10 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8f7b70d4815493386358f5e67df5e1b817491f97bac40f323aa42443b065bb`  
		Last Modified: Wed, 08 Apr 2026 18:20:44 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b469b6f2845a18e2ff74b458316a8797ec1ad07e82cb7880276f104c8b0f120`  
		Last Modified: Wed, 08 Apr 2026 18:20:45 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88586a1506bca708c383c6b08d78335daa26f4a0cf39582946cea0b052340f85`  
		Last Modified: Wed, 08 Apr 2026 18:20:46 GMT  
		Size: 8.4 MB (8422606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c9d276f5ab972d7d33b54ecb3779aefcc08db70b21ba7f701881e01906de0e`  
		Last Modified: Wed, 08 Apr 2026 18:20:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
