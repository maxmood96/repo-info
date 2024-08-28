## `nats:windowsservercore`

```console
$ docker pull nats@sha256:03d5e78291171396a4502d8239e0f86a1c651f82af0393cdd4612a5e3ad49af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull nats@sha256:f4b25057f884e6da7e57c1f7c8d2f16480c1d60a9ea48c0548987b850ff7c05f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251865048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54a0c2ac4d53bf85b59f44f9e19ab5a90038e066cffce96541b87cb3a155cb0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:45:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 28 Aug 2024 00:17:00 GMT
ENV NATS_SERVER=2.10.19
# Wed, 28 Aug 2024 00:17:01 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.19/nats-server-v2.10.19-windows-amd64.zip
# Wed, 28 Aug 2024 00:17:02 GMT
ENV NATS_SERVER_SHASUM=1d7b4409cf70c302c09702732078d684be9a1d8ec797e57e77344f79086feaf8
# Wed, 28 Aug 2024 00:18:27 GMT
RUN Set-PSDebug -Trace 2
# Wed, 28 Aug 2024 00:20:15 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 28 Aug 2024 00:20:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 28 Aug 2024 00:20:17 GMT
EXPOSE 4222 6222 8222
# Wed, 28 Aug 2024 00:20:18 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 28 Aug 2024 00:20:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a022697aef59a6692fd1a03334c036f85c795eb0dc574e189565788b877520`  
		Last Modified: Tue, 13 Aug 2024 20:51:12 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181549f74e6a3a7aab547a8610ede0ec1509da5a0da4268e51db7ea8af372362`  
		Last Modified: Wed, 28 Aug 2024 00:21:16 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e4a651de153ff077419fedb40d445c702fa93da062f6d4566310a885961c31`  
		Last Modified: Wed, 28 Aug 2024 00:21:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554e25c09b4d2b5ab153b3cf4996326318dccf53fa8683ad60554a4b00541ab4`  
		Last Modified: Wed, 28 Aug 2024 00:21:15 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203ab59e81d101e37a68b602ab3bb41a272ad516a1a64bebd5ef3c161d26f9c1`  
		Last Modified: Wed, 28 Aug 2024 00:21:15 GMT  
		Size: 476.6 KB (476565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a27ed24d0cc018dbded9a0e66f8debe88f8f34eac7032133f357457050f6f7`  
		Last Modified: Wed, 28 Aug 2024 00:21:14 GMT  
		Size: 6.2 MB (6171987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce1d1cc29d19aecb0eddd7ca3008af14f5f36ef6cafc23fd1282e08b3be1f96`  
		Last Modified: Wed, 28 Aug 2024 00:21:13 GMT  
		Size: 2.0 KB (1974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce56ed941c0f3a3a1c1bfecf9328f612510f42267c447a9c111bc223c3178b3`  
		Last Modified: Wed, 28 Aug 2024 00:21:13 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8875e46dd2dbdd1c778412d0df4909c9fa7c10aea6972091c002c99b86c5e47f`  
		Last Modified: Wed, 28 Aug 2024 00:21:13 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547eb816c48c3bd50836b125ed00b84cd4e42579050fbf6b1e3db620f4dfb85d`  
		Last Modified: Wed, 28 Aug 2024 00:21:13 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
