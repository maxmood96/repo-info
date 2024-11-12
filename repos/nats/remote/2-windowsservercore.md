## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:ab78e2172e61085ae9afc4925e54a987a6d679c9da46d25c484bccf5269d16cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:9448640f937b2f4ee4da3d9937c09b47019f037d5c9e61162580a7d561ce019b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908560921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07a345182b93fdfa8288b594f93c71bc993ca4566321461fecbccf9b0fbbaa2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 12 Nov 2024 00:55:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Nov 2024 00:55:07 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER=2.10.22
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Tue, 12 Nov 2024 00:55:09 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Tue, 12 Nov 2024 00:56:31 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Nov 2024 00:56:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Nov 2024 00:56:57 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 00:56:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 00:56:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 00:56:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ed0f15243f28f3922f00ed16ecfd22d610f79e0e0daf969dcdf0305ee22ec2`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525058aca77fecf4a52d3e5639a8cd7a8b045d1d0bea041de779ac8d8de030de`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d097959e3c6dc4700daf17b4454b636a4c282eceb830d2d505abf9f1251f1b`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1199e5b06310464b9e94c92b4e883c9f6a5e9e1d24e67bf6415a19de08cdc4f`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c315d41fb2fb62d04f1dea32b9c14e351ba070df978fb722d8307a7fc728a3`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d262f864554f378348b8cbf71b9bc91e6871d9397b4238cde655fb93a78e9c`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 493.1 KB (493088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335838a75c168178d65d906d3c3f5b69f20896629cd5b8aa314087add21137a`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 6.2 MB (6230344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b52fdabfa3405a6f81753210b18cb9389020984bfaf4eb657f2d31d772e5af`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494d7679741aeba6e3aca4377b6c2aaa8ad88fc86ef6a81f4cbe969a23d450c9`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4650fb4eadfc488ae6b5d6bcb5272870243a44e7f3bb7e6884d5cc8cff303cf7`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c12c0d16c854801762a89df692d823cfc1dcc0579f4458a11171e6f8b17a4`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
