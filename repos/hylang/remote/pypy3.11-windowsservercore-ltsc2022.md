## `hylang:pypy3.11-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:7c4162803ceae958740b5644bb5f0b88c691fa5f3d3c7bc75af0ce972f73af34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `hylang:pypy3.11-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull hylang@sha256:732ccbfcfccad06a39c5dceefb997a8834b9cfc0a0bb8b29c929c37eaede0462
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177354781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23330148b9ab8089b4b57c5bc25fbef494b0b6e8e2a77720b0902104cbb5e92d`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:39:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:57:01 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 12 May 2026 23:57:10 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:57:10 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 12 May 2026 23:57:47 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.22-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '748f393e69726f32c908bfd8d778dda267482c0b15b2d4957c97f0842f37d33f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.22-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:57:47 GMT
CMD ["pypy"]
# Wed, 13 May 2026 00:30:40 GMT
ENV HY_VERSION=1.2.0
# Wed, 13 May 2026 00:30:41 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 13 May 2026 00:31:16 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 13 May 2026 00:31:16 GMT
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
	-	`sha256:917dd62015b1447671d0b141b1522081735e979c185e6644bec43931db85c017`  
		Last Modified: Tue, 12 May 2026 23:40:45 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4cff043552c33dcacac0b36ebaadff80a89cede4e38cf7eaf76bb53b102128`  
		Last Modified: Tue, 12 May 2026 23:57:54 GMT  
		Size: 485.6 KB (485554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e247f0a5b622301cd9996cbae19c8e1ac852f6224b3cb5dfa14cc80670c416b1`  
		Last Modified: Tue, 12 May 2026 23:57:55 GMT  
		Size: 15.5 MB (15527565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a0f5a85ac87f2cb41c3eb08693d43df60623a0d2222e95fa9db62166dec1b9`  
		Last Modified: Tue, 12 May 2026 23:57:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28de71c613d6aa41f9b7981cb899556d4da6e2efbc880258b21126f6551ae375`  
		Last Modified: Tue, 12 May 2026 23:57:58 GMT  
		Size: 30.9 MB (30903525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cb083ae1b31bf86ac191f4ca0d052c71dda1c9810ca7c5485edcdb5aa13c6d`  
		Last Modified: Tue, 12 May 2026 23:57:53 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbff23db496e1ef39984e3bb071ca7668c325f18f3502dbf131d51a011944ca0`  
		Last Modified: Wed, 13 May 2026 00:31:21 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d42da7165c21d5d89f4745abbe1ce5c030fa88b13336846f8b5031c4b6e1fcb`  
		Last Modified: Wed, 13 May 2026 00:31:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4276b4b348d272d76855f759efb914dd8e3c2848f9fed761f6d8949ca11b9c`  
		Last Modified: Wed, 13 May 2026 00:31:22 GMT  
		Size: 8.0 MB (8009728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7960b61228500826d49f9061485ea8383588ec704a1d0cd6758977d0474a828e`  
		Last Modified: Wed, 13 May 2026 00:31:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
