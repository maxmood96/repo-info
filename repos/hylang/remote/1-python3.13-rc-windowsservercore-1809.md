## `hylang:1-python3.13-rc-windowsservercore-1809`

```console
$ docker pull hylang@sha256:00e6670afdd571a89329013427266dab05d825e93b256fdcda18f3c289a6dbae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `hylang:1-python3.13-rc-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull hylang@sha256:bbd86463bb3e889fd248194abf5540c1046263118ddbac3b148f1bae44e5769c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1785059713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2193e1ff2e227b907571ee68f97973b08bd4545d203231852c8e27acb1b3c945`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 01 Oct 2024 22:21:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 01 Oct 2024 22:21:07 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 01 Oct 2024 22:21:08 GMT
ENV PYTHON_VERSION=3.13.0rc3
# Tue, 01 Oct 2024 22:23:27 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 01 Oct 2024 22:23:27 GMT
CMD ["python"]
# Tue, 01 Oct 2024 22:58:43 GMT
ENV HY_VERSION=1.0.0
# Tue, 01 Oct 2024 22:58:44 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 01 Oct 2024 22:59:46 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 01 Oct 2024 22:59:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3ca900b846e829f866079d36547ea6d6110544579b2f48b92cbc6b85466eba`  
		Last Modified: Tue, 01 Oct 2024 22:23:30 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ed8bd0e38d8ca287fd9e11e68d81a04b9d19193dd6a66bd447d141c40ec8d8`  
		Last Modified: Tue, 01 Oct 2024 22:23:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7273a1e38c751808214d6df18e9c62e2df49c0d501e9bf25178357965e85fdf8`  
		Last Modified: Tue, 01 Oct 2024 22:23:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90954bd7e360916614e842c5edad95a9451516f30676cf8d6558f886cb55782f`  
		Last Modified: Tue, 01 Oct 2024 22:23:34 GMT  
		Size: 57.5 MB (57472928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041ae8ab6cf039f0071a768a3a027afe82474d6a5aee141e36001c58249d652e`  
		Last Modified: Tue, 01 Oct 2024 22:23:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857a230be2b02ae778515b2e2447e1f7280af38aad1facf1ca1bc41dc4392d82`  
		Last Modified: Tue, 01 Oct 2024 22:59:51 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cb99a0026e9aa0da8877cd34fb455c283286db512a721cd052de3edb68bbf4`  
		Last Modified: Tue, 01 Oct 2024 22:59:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901d78499eec5b60ce9aaa72222ab97114e444e728cf6dfaee926331bf8729c1`  
		Last Modified: Tue, 01 Oct 2024 22:59:52 GMT  
		Size: 7.3 MB (7309229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10be92062b4529baf5a3f3b9e23cfb21476980b68c6c7b6ad59099d30bd671b1`  
		Last Modified: Tue, 01 Oct 2024 22:59:51 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
