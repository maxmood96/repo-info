## `mongo:8-windowsservercore-1809`

```console
$ docker pull mongo@sha256:c3bdf634df8f58b7786c52019df0d3cade85606a9bcca9211ceaaab3d3bae083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `mongo:8-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull mongo@sha256:603dfa84a10eeeb1c9a3a52b50cccf68e120944fc559cd2fe470b3c9b768a06c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2779480666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899d41aa7ea98ba226bd6c06d56e2a46afb53d90754b015f62393ccac6b3af6f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Mon, 09 Dec 2024 21:10:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 09 Dec 2024 21:10:14 GMT
ENV MONGO_VERSION=8.0.4
# Mon, 09 Dec 2024 21:10:14 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.4-signed.msi
# Mon, 09 Dec 2024 21:10:15 GMT
ENV MONGO_DOWNLOAD_SHA256=52d30392e6767eb48c03fc9886b831da5a282af7aba49cc46f45c6b0f85280cb
# Mon, 09 Dec 2024 21:12:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 09 Dec 2024 21:12:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 09 Dec 2024 21:12:22 GMT
EXPOSE 27017
# Mon, 09 Dec 2024 21:12:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f260e36a32b1e060e50eea71b01d9aed7c1e4a275df064b897364249cdaa82c`  
		Last Modified: Mon, 09 Dec 2024 21:12:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc88fe8d6e0cdac0309c8edb2423f6f0599aca2ec432f514565642c1d1aee340`  
		Last Modified: Mon, 09 Dec 2024 21:12:29 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93546bc304805f9f37a1a8383cb623c70cfca34f79b754c0ba0878b0cc67fcad`  
		Last Modified: Mon, 09 Dec 2024 21:12:29 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbab5cc55b50c4d2fbf7366ac05ac7f998fa052c9f321c805f20ce902d94db8a`  
		Last Modified: Mon, 09 Dec 2024 21:12:27 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70bca44663cdffbabb2a420f0f5ff3bf609dfe4a7d8fd83eda68c4ea2ccbbdc`  
		Last Modified: Mon, 09 Dec 2024 21:13:26 GMT  
		Size: 768.8 MB (768817492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d05e3738f8a8c01a8cb80ac962a56f646738586c24e0b37fb1644c56c269bd`  
		Last Modified: Mon, 09 Dec 2024 21:12:27 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e3915ffc107d5aa54b41eb04a31a6868a39feb435a8e38916de65d4715ba7c`  
		Last Modified: Mon, 09 Dec 2024 21:12:27 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4335001f5d684d60f6c2d7bc8a34adf9faf2caceb991e93c175dd6596ed84b1`  
		Last Modified: Mon, 09 Dec 2024 21:12:27 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
