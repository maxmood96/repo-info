## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:75e4ff61015f3bf7c22351ff65fa904e8d4dc1323aa7f8881dfa10a7c2ffa49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4651; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4651; amd64

```console
$ docker pull nats@sha256:60236d944179b159cd056561c73729bb8eacaa25db732a8348c089e4553be641
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6276661668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d133c7ce69a5c937d2c6fd5baba8fcea0547fe32f9caa257de095c5333b8fd7d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 13:26:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:43:15 GMT
ENV NATS_DOCKERIZED=1
# Fri, 24 Sep 2021 18:18:36 GMT
ENV NATS_SERVER=2.6.1
# Fri, 24 Sep 2021 18:18:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.1/nats-server-v2.6.1-windows-amd64.zip
# Fri, 24 Sep 2021 18:18:38 GMT
ENV NATS_SERVER_SHASUM=c98118acf708d119adb4d94127efb57825f24209e5e4b855931e3cc941237e35
# Fri, 24 Sep 2021 18:20:06 GMT
RUN Set-PSDebug -Trace 2
# Fri, 24 Sep 2021 18:21:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 24 Sep 2021 18:21:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 24 Sep 2021 18:21:39 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Sep 2021 18:21:40 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 24 Sep 2021 18:21:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5796468f91731000e9a76e836156826a1cd4ed963bcd80e6558c538a12c2132d`  
		Last Modified: Wed, 15 Sep 2021 15:05:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611fe9c559abed986280087eef7d362a6ecb9ad281b1427395fdfc2d99d3d9c4`  
		Last Modified: Wed, 15 Sep 2021 15:46:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5326ce136baa17eaec1fac331c17c4cfccb1ab18ec89885c6e0a72acea536bd8`  
		Last Modified: Fri, 24 Sep 2021 18:23:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3b1fed06b403050de165363f36dadfc9a9a527bbc7c077456a64f1d82c4d5b`  
		Last Modified: Fri, 24 Sep 2021 18:23:21 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd472cc93732a042088cda0ff0d9bb6497ecf25c47d19333c1d5222e3d42e3`  
		Last Modified: Fri, 24 Sep 2021 18:23:20 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b7607aa7457f0141c4f2f4ccacf4f068670acf5c00642aa11429b92c1d4182`  
		Last Modified: Fri, 24 Sep 2021 18:23:20 GMT  
		Size: 343.9 KB (343868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ef2571a70f7261d297cf7d19bbbddc950a9bc276fda13376fae1d091bc49e6`  
		Last Modified: Fri, 24 Sep 2021 18:23:24 GMT  
		Size: 5.0 MB (4976960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d13f276de11afd9152b4309d095c5222ffc53d5f5000bd93f65ce3d0a8358b0`  
		Last Modified: Fri, 24 Sep 2021 18:23:18 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd31e6f667b20a464061770ad947f5343d5c724176047276970528e29475ea1f`  
		Last Modified: Fri, 24 Sep 2021 18:23:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5018883280a197fb7725a0c7f6ce69f5a902ffa816ba93a509e98bef952c69`  
		Last Modified: Fri, 24 Sep 2021 18:23:18 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d57908fe57f032c311e5df72827b4beb15403603b6d4047b329ad4b4cbd828b`  
		Last Modified: Fri, 24 Sep 2021 18:23:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
