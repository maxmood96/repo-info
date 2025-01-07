## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
