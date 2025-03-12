## `hylang:windowsservercore-1809`

```console
$ docker pull hylang@sha256:75a90ee8fc868220b893de8c66a191b91bb05d8a4d0f3707a91c8f5de5ec26d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `hylang:windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull hylang@sha256:fe2dc2204f1702e97a85024ae7dcf3e64fb812e248c942cd3261d515892837b0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216527368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75af516c614aca1a19cfcb32b571c37178a9bfc2dc02ebb023e8c543df8ac079`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:55:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:55:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 18:55:46 GMT
ENV PYTHON_VERSION=3.13.2
# Wed, 12 Mar 2025 18:55:46 GMT
ENV PYTHON_SHA256=9aaa1075d0bd3e8abd0623d2d05de692ff00780579e1b232f259028bac19bb51
# Wed, 12 Mar 2025 18:57:25 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:26 GMT
CMD ["python"]
# Wed, 12 Mar 2025 19:25:13 GMT
ENV HY_VERSION=1.0.0
# Wed, 12 Mar 2025 19:25:15 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 12 Mar 2025 19:26:46 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 12 Mar 2025 19:26:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a22a4c42a919099f93eb0448bbf22221e5f1ad7f8e0cb797dd2c576c582d8e`  
		Last Modified: Wed, 12 Mar 2025 18:57:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930bb580d3662cfda06ce17cf4317350a4e86cf9d9fc4e65e2b92fe383ba8a6`  
		Last Modified: Wed, 12 Mar 2025 18:57:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69339a3e609449ec77a0db937e8a3c351c2733f98b759f939f6f0902c6d49a50`  
		Last Modified: Wed, 12 Mar 2025 18:57:28 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6d13cd637afb7ffa35035e4e52059652b8cc5d29c88fd6fd174ca75f32d8dc`  
		Last Modified: Wed, 12 Mar 2025 18:57:28 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161a85e590b107d865f863fc00bfa1985305617d4e88642df9ed4a0d945217e4`  
		Last Modified: Wed, 12 Mar 2025 18:57:33 GMT  
		Size: 57.8 MB (57751070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c49f0a8a406b17ca17c02c84a230128dff721fa57def525e725c2fcdf47a4b`  
		Last Modified: Wed, 12 Mar 2025 18:57:28 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4489d272ca505eb42602389f118ac50aff5b09ef3b8d419ce085e312039c60c`  
		Last Modified: Wed, 12 Mar 2025 19:26:49 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543e77c121c970d7c26afa2f74ca328e08a4eac23367c75d9ef2785b21bec150`  
		Last Modified: Wed, 12 Mar 2025 19:26:49 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5049ffe88b4eb1b1673498b61d32dbc35f293584b73c741f01531712167887`  
		Last Modified: Wed, 12 Mar 2025 19:26:50 GMT  
		Size: 7.1 MB (7131142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f41bb0758b8d7df9a2f88ddc849d16c3cecc0befe98cb3b2c3f9b4fb1c6239e`  
		Last Modified: Wed, 12 Mar 2025 19:26:49 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
