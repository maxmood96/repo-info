## `hylang:python3.13-windowsservercore-1809`

```console
$ docker pull hylang@sha256:c3a29564f7c18a92cfd98cb826a91f0e9ca1c9cefcc7e968eb236560522950c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `hylang:python3.13-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull hylang@sha256:293fc36d70665504e319e0dac3103ccc42422e4ecc21f3d7cab064a7c50ccd31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216555898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b8b32dc6bc74bf7533ed9285b15554c82b9c32b3a1cb7c90b57eca0ea7b530`
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
# Wed, 19 Mar 2025 23:12:08 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 23:12:11 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 23:13:29 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Mar 2025 23:13:30 GMT
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
	-	`sha256:1ba7719d23823c6f77fca8f5138243fab31996b717ff10d6750365469418983d`  
		Last Modified: Wed, 19 Mar 2025 23:13:33 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4dbdf7eb693d67b200f49d06b642c706a32274dba96c6f209b67315fdea0c0`  
		Last Modified: Wed, 19 Mar 2025 23:13:32 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5d812de04b3e7fae5f2db8ef7000c4d19185a06fd394217d1f57fb65887b39`  
		Last Modified: Wed, 19 Mar 2025 23:13:33 GMT  
		Size: 7.2 MB (7159709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5e6b5919fad3785b76d6a459352ffc6f2b9eeb0dc7d44e36c864c5786e4ac9`  
		Last Modified: Wed, 19 Mar 2025 23:13:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
