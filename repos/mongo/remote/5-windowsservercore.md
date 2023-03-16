## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:2b7cf759d51a517f89703e83a031e446ed31d8ac707fae297c1e4107cf2c7cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `mongo:5-windowsservercore` - windows version 10.0.20348.1607; amd64

```console
$ docker pull mongo@sha256:187185160eaa4054632ac1b685bf1f72d52e93b5c4b503bc5867e576a25a57c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2026524772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d24f73b561f2dc9314c1bd5e063774ca15c910e11b6b4550e3bfa172067af3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 02:55:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Mar 2023 03:09:50 GMT
ENV MONGO_VERSION=5.0.15
# Thu, 16 Mar 2023 03:09:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.15-signed.msi
# Thu, 16 Mar 2023 03:09:53 GMT
ENV MONGO_DOWNLOAD_SHA256=882dce3858f3580011cd295f5c6502a4effd19178968abd7c20f8aabb50a7c15
# Thu, 16 Mar 2023 03:12:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Mar 2023 03:12:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Mar 2023 03:12:39 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 03:12:40 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d31bb6c06d038a3e1a69943be5f72e0ad656773c3f446d934ff816b71b0d631`  
		Last Modified: Thu, 16 Mar 2023 03:42:14 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d302f83c186ac423bee02906453b44bda402a616151916cdea7ecb6d7665efd3`  
		Last Modified: Thu, 16 Mar 2023 03:49:30 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16d51a76cd6d08b0337cf1834c539284e82d06dba611c5f9f0678a89305b2a1`  
		Last Modified: Thu, 16 Mar 2023 03:49:30 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fcb12dae3350d1f64faccebcb8a9247a2f4627749cc67f921d5b2662f6398f`  
		Last Modified: Thu, 16 Mar 2023 03:49:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39946dff517888ba631168d69884f11a8f459a00f9c08c8df3c4e3a112819d53`  
		Last Modified: Thu, 16 Mar 2023 03:50:30 GMT  
		Size: 312.6 MB (312574710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b52b1008b58ebc0b5b1536cf33c02bb61f6ead93e241efe41aac7d13dda96`  
		Last Modified: Thu, 16 Mar 2023 03:49:28 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2cd92ca6f53ecf3636424f18dc486fcf71ac295b55d51492e7db914f5d1ab1`  
		Last Modified: Thu, 16 Mar 2023 03:49:28 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692522975bd57169265849063a007bb0e1e76097df4fe18fdd3c182484650a8e`  
		Last Modified: Thu, 16 Mar 2023 03:49:28 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.4131; amd64

```console
$ docker pull mongo@sha256:b1d42d8d0b64f5a2d363c1d0045eb0a00ef6aaae6d5af7e68410b1353d6c9d2c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325874542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5b72753aaa348a2b53bde048469924090fb1c4399efe102cee5cae73d5832b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 02:59:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Mar 2023 03:12:51 GMT
ENV MONGO_VERSION=5.0.15
# Thu, 16 Mar 2023 03:12:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.15-signed.msi
# Thu, 16 Mar 2023 03:12:53 GMT
ENV MONGO_DOWNLOAD_SHA256=882dce3858f3580011cd295f5c6502a4effd19178968abd7c20f8aabb50a7c15
# Thu, 16 Mar 2023 03:16:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Mar 2023 03:16:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Mar 2023 03:16:51 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 03:16:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474eedda733dad347e4baad9fb9f3d700b58e5788f7453d1979cebb167746b32`  
		Last Modified: Thu, 16 Mar 2023 03:44:11 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11bb1215dad8fa83b964a9f7248cc62df7c23cc3dc25af4d6eaf9ab504d6863`  
		Last Modified: Thu, 16 Mar 2023 03:50:44 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49be84008b64fef1637dddabf413f17c16a0c6fd127065043553cc23ee0bca6d`  
		Last Modified: Thu, 16 Mar 2023 03:50:44 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c73106881371c62f8dc9170b9e1c4b27f8640cb2c04f70287ca39cc04ee9bb`  
		Last Modified: Thu, 16 Mar 2023 03:50:42 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac920e9a24ea4347629986261f08fe0f553e95eead99ddb5d7f450c9d9838a7`  
		Last Modified: Thu, 16 Mar 2023 03:51:43 GMT  
		Size: 312.4 MB (312355945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf3e4bd832a1836f08ee44bf1b0ceb5f2e9931661da3b09b65846f8dcb5b69f`  
		Last Modified: Thu, 16 Mar 2023 03:50:42 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f67488af39862666ff6cafb3348a77cbfa15ec31608f7c610b2b9523abc91e9`  
		Last Modified: Thu, 16 Mar 2023 03:50:42 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3434fc6085624835ee564d0f7e89ca0ecd42286b08a037b53fe5110f728ef5`  
		Last Modified: Thu, 16 Mar 2023 03:50:42 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
