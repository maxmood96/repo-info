## `hylang:1-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:ace1b0b47ea46e76c2b124655167d577475cd2562f7fae2a1bad679d52fbad14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `hylang:1-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull hylang@sha256:95230709096bf3ee5fbe4f332286bcbbd163949d95d450ce3f848f18119343fb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3543939539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c7448fa4fa58c021a8defb0d0f5cb5e6e7583b8c33b4cdc8baa420f5e8d237`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 12 Jun 2025 22:41:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:41:41 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 12 Jun 2025 22:41:41 GMT
ENV PYTHON_VERSION=3.13.5
# Thu, 12 Jun 2025 22:41:42 GMT
ENV PYTHON_SHA256=c1cb40978b28f696b111c36034a1bdeda17d25e35c74a08ef5e5ff405a63fc20
# Thu, 12 Jun 2025 22:42:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 12 Jun 2025 22:42:22 GMT
CMD ["python"]
# Thu, 12 Jun 2025 22:57:47 GMT
ENV HY_VERSION=1.1.0
# Thu, 12 Jun 2025 22:57:49 GMT
ENV HYRULE_VERSION=1.0.0
# Thu, 12 Jun 2025 22:58:22 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 12 Jun 2025 22:58:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05ba4e2b8285e1daa7ceb86172559e12deedebfe41fa0dbbf3ac14b1f6f50d`  
		Last Modified: Thu, 12 Jun 2025 22:46:04 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e912b85f4824e7665cba5b2ea9f530132d0180d1decec4dd2eb4f1fd6b554d`  
		Last Modified: Thu, 12 Jun 2025 22:46:05 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8c9b4bda20e22281fbffb19871a3b8161dafb6b63bbc05cc0e5e75a5e61cbe`  
		Last Modified: Thu, 12 Jun 2025 22:46:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81f4c7e4688089baf8fb8615dc7bcb40310d17f9d537d568b6e47b15669272e`  
		Last Modified: Thu, 12 Jun 2025 22:46:05 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a30cc6625c37812446fe573752cf3dc16db89f8941a0d0cb38fcd39f9e04907`  
		Last Modified: Thu, 12 Jun 2025 22:52:15 GMT  
		Size: 59.2 MB (59201439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1e44d41176438635a468c41ee3b9a3512944c37dd8b9caf7bd4ea1c94859eb`  
		Last Modified: Thu, 12 Jun 2025 22:46:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3784309d29c6d392b183f60f6ab8e1eae9f7cf5664e24685d7b7a58244f1a0`  
		Last Modified: Thu, 12 Jun 2025 22:58:44 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f5db48645c48f6d77db95c1b9c0435cbdb9c15ac479d7d6739ca542b262bd3`  
		Last Modified: Thu, 12 Jun 2025 22:58:45 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4303289b73681831a8e02df6f47ea88341eb52fae098d1dabc6443d7924ef494`  
		Last Modified: Thu, 12 Jun 2025 22:58:46 GMT  
		Size: 8.6 MB (8553561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12834e74e57a508667ff7acc5704b1e59322163028ee4167d9a125f3f0162f6`  
		Last Modified: Thu, 12 Jun 2025 22:58:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
