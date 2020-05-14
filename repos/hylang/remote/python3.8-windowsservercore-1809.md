## `hylang:python3.8-windowsservercore-1809`

```console
$ docker pull hylang@sha256:e786c60ec352bc5058413705586d0f3f49c154ea1967ee8c371ec46ab719f9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `hylang:python3.8-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull hylang@sha256:dfa29df92d36ba2973d892a43f206896cd779a04487e82a5a92d7cc860aaf8f4
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1773161915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fec8e925baa77cf3ac0e243ccd505ec146e90a773bd67a20d8b584769afe25`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 May 2020 18:19:50 GMT
ENV PYTHON_VERSION=3.8.3
# Thu, 14 May 2020 18:19:51 GMT
ENV PYTHON_RELEASE=3.8.3
# Thu, 14 May 2020 18:21:30 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Thu, 14 May 2020 18:21:31 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 18:21:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 18:21:34 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 18:22:12 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 14 May 2020 18:22:13 GMT
CMD ["python"]
# Thu, 14 May 2020 18:40:10 GMT
ENV HY_VERSION=0.18.0
# Thu, 14 May 2020 18:40:41 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Thu, 14 May 2020 18:40:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d4964ba20bfaf4a48d146313f11b4083d5d3c7cf2cb95d74469123994c204d`  
		Last Modified: Thu, 14 May 2020 18:23:42 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cc4677de1ee3385dd73ed7fd582bb396bfe58de6ec3248ffa92ca7b6ce1d7a`  
		Last Modified: Thu, 14 May 2020 18:23:41 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e07d3170a860ee9312e7985a33da087450406dc0f97ef98ebcad17a034af4b3`  
		Last Modified: Thu, 14 May 2020 18:23:50 GMT  
		Size: 48.2 MB (48153425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d5f274dcdcfd10996a232550d02013da08ec91a7a09d00279b770e7dd1fefb`  
		Last Modified: Thu, 14 May 2020 18:23:39 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd8eec8a07a36883752224d293ff13db8117bfac09b674a199e4ff7872a399`  
		Last Modified: Thu, 14 May 2020 18:23:39 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad738ed42f5dc8a36815f59cda6d789ba42e2f10f668d2d8ef60faa37929b1`  
		Last Modified: Thu, 14 May 2020 18:23:39 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfe0251d31f1fadabd768fe8d2443707cc08a46b592e15a48675e308b9d330f`  
		Last Modified: Thu, 14 May 2020 18:23:41 GMT  
		Size: 5.5 MB (5509194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e482075bf2b1684e917548234146d980229d64fd541b9cc8d4ad9afbc43ea3`  
		Last Modified: Thu, 14 May 2020 18:23:39 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d67048e030107cf7c682572f4df8953be9915e5eda913666d24e6f12fbdce2`  
		Last Modified: Thu, 14 May 2020 18:43:19 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef417cb9714a7cacf01a3677e2ac40c6442758d1e657947c60cc8a5b4217338`  
		Last Modified: Thu, 14 May 2020 18:43:21 GMT  
		Size: 1.2 MB (1156476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbbb43bf6532ef30ac97685aced981cf0ef75f30c072a8a6db7c075304434bf`  
		Last Modified: Thu, 14 May 2020 18:43:19 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
