## `mongo:8-windowsservercore-1809`

```console
$ docker pull mongo@sha256:947f91a9d63c91d5f7292ad3845c6de08f2dec0cf871ebec8644894057be7f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `mongo:8-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull mongo@sha256:2e6aff27177e9c2910bf5db2fc7772a2f869c9284d1bdacd3fc5cb45c0af9810
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2957176794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e45e27787fb7bd8961dbda951fc898627466d97012683bb9b1587d9e765259`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:58:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 20:58:41 GMT
ENV MONGO_VERSION=8.0.9
# Wed, 14 May 2025 20:58:42 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.9-signed.msi
# Wed, 14 May 2025 20:58:43 GMT
ENV MONGO_DOWNLOAD_SHA256=4acf24592a7658cc58b4293cbf0a3f42133c9c1d4f2234f1a249f74aa1c7d22a
# Wed, 14 May 2025 21:00:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 May 2025 21:00:51 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 May 2025 21:00:51 GMT
EXPOSE 27017
# Wed, 14 May 2025 21:00:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20545d7f8da75ba423bb3ac161fc9ba6d4fa1bb93deda4314f5e41a58c4c93d`  
		Last Modified: Wed, 14 May 2025 21:00:55 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f1e5bead40d7da528672258c940c80a70aca7a607dfde72cc3a022ef5f3116`  
		Last Modified: Wed, 14 May 2025 21:00:55 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c89526aa33026170ce8b931ab5ca09a034c9f2fa96ee2292c205e99c0c6fac9`  
		Last Modified: Wed, 14 May 2025 21:00:55 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dd2fb5ee8fc193d7506b8bd815f1dcee480371c59c8f7d1ea5fcb14dbaaf4e`  
		Last Modified: Wed, 14 May 2025 21:00:54 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6735561f6b368310847828448334f9a8ec631681cb714e2f623f67daf7dbe86f`  
		Last Modified: Wed, 14 May 2025 21:01:58 GMT  
		Size: 773.4 MB (773449871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3576c1f6dcaa614dab531fed3807a2c32d1ede1362007e83f434a7af96891187`  
		Last Modified: Wed, 14 May 2025 21:00:55 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe21e288ac83262ee39912ef906ac1c051ee41d950f7bf9abc4e08cc618d2775`  
		Last Modified: Wed, 14 May 2025 21:00:54 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea616424480374dbcf66f423e69b1f807dc2fa47de19fd819384ede9a09e6f1e`  
		Last Modified: Wed, 14 May 2025 21:00:54 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
