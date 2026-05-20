<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.22`](#nats2-alpine322)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-ltsc2022`](#nats2-nanoserver-ltsc2022)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-ltsc2022`](#nats2-windowsservercore-ltsc2022)
-	[`nats:2.12`](#nats212)
-	[`nats:2.12-alpine`](#nats212-alpine)
-	[`nats:2.12-alpine3.22`](#nats212-alpine322)
-	[`nats:2.12-linux`](#nats212-linux)
-	[`nats:2.12-nanoserver`](#nats212-nanoserver)
-	[`nats:2.12-nanoserver-ltsc2022`](#nats212-nanoserver-ltsc2022)
-	[`nats:2.12-scratch`](#nats212-scratch)
-	[`nats:2.12-windowsservercore`](#nats212-windowsservercore)
-	[`nats:2.12-windowsservercore-ltsc2022`](#nats212-windowsservercore-ltsc2022)
-	[`nats:2.12.9`](#nats2129)
-	[`nats:2.12.9-alpine`](#nats2129-alpine)
-	[`nats:2.12.9-alpine3.22`](#nats2129-alpine322)
-	[`nats:2.12.9-linux`](#nats2129-linux)
-	[`nats:2.12.9-nanoserver`](#nats2129-nanoserver)
-	[`nats:2.12.9-nanoserver-ltsc2022`](#nats2129-nanoserver-ltsc2022)
-	[`nats:2.12.9-scratch`](#nats2129-scratch)
-	[`nats:2.12.9-windowsservercore`](#nats2129-windowsservercore)
-	[`nats:2.12.9-windowsservercore-ltsc2022`](#nats2129-windowsservercore-ltsc2022)
-	[`nats:2.14`](#nats214)
-	[`nats:2.14-alpine`](#nats214-alpine)
-	[`nats:2.14-alpine3.22`](#nats214-alpine322)
-	[`nats:2.14-linux`](#nats214-linux)
-	[`nats:2.14-nanoserver`](#nats214-nanoserver)
-	[`nats:2.14-nanoserver-ltsc2022`](#nats214-nanoserver-ltsc2022)
-	[`nats:2.14-scratch`](#nats214-scratch)
-	[`nats:2.14-windowsservercore`](#nats214-windowsservercore)
-	[`nats:2.14-windowsservercore-ltsc2022`](#nats214-windowsservercore-ltsc2022)
-	[`nats:2.14.1`](#nats2141)
-	[`nats:2.14.1-alpine`](#nats2141-alpine)
-	[`nats:2.14.1-alpine3.22`](#nats2141-alpine322)
-	[`nats:2.14.1-linux`](#nats2141-linux)
-	[`nats:2.14.1-nanoserver`](#nats2141-nanoserver)
-	[`nats:2.14.1-nanoserver-ltsc2022`](#nats2141-nanoserver-ltsc2022)
-	[`nats:2.14.1-scratch`](#nats2141-scratch)
-	[`nats:2.14.1-windowsservercore`](#nats2141-windowsservercore)
-	[`nats:2.14.1-windowsservercore-ltsc2022`](#nats2141-windowsservercore-ltsc2022)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.22`](#natsalpine322)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-ltsc2022`](#natsnanoserver-ltsc2022)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-ltsc2022`](#natswindowsservercore-ltsc2022)

## `nats:2`

```console
$ docker pull nats@sha256:ddb480f4b97d90f183123e96bbc7c96ab2a126883f7a380531cc208fc8ba9ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5139; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:e3975ae3c259e07dc00b126ef5cf0570d4b9c1995de29c286314a8c94185f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6842884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a858e4f7943893e252bc83397a059d23acc4bba8780c464abee2a7ca16c7445`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:09:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:09:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:09:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:09:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:09:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:09:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7c3bd50a747eaeeb10f95fa519304e5d461cdf7abfea618bd20f6082ff6662a0`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.8 MB (6842374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de808d2a465a42d8c366fe6a0444bfe0126b0deb5df083e28a6ab5da8f23bd`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:23bcf4e2ed2926d96eea36a58166f435554c690541005e998f5d616db30e45f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507326c78aca26a49af5c475ba8b2e2af04ec277a225d3045596713d6ff37309`

```dockerfile
```

-	Layers:
	-	`sha256:f040bfc84eb63a5f18c5215d1a0b547ad6574a095bc308ed0abb87f0e078fd56`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fec1423119b8e851f070386e125c5834183df6ef68cdf380acc9baeea48437c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddea1197c216967009e6e1e0c22c06b810ad0056259b9aa2d0d4c9116f36a3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:07:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:07:34 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:07:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:07:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:07:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:07:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bf1819a534ff3a05b2ec4b423942e9e9c1db524f8abdf07d0916cc9d7977e963`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.6 MB (6559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b10a626663e338c0bb1dfea4c11c6b38d61cac3eeefbe2918057535336ac6b`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:cf5f1e96a51a5bb900685df5ea819d0c6d2fa448635ed02772654ff2b5d22c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c00aaa6a70cd7d0e9305def7746345074e4a5081f236f2b44b9b79e39464d8`

```dockerfile
```

-	Layers:
	-	`sha256:03d05c80b133e625e60b7cb05cef59b26ce5d7adb0a442fffea4584ab6416a79`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:a34dfd5d492771b140674e5c141027c58b58e4e2cd947f6eba0a5a31e2632e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6550603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093ad3956c6655a303f62a9ce264a18c45b4b863cb96efd842248173c0a606f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:79835d220a3efcc4d8184ca74b4eca9de6abd447cd214ab6d89fae0fc25d71a9`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.6 MB (6550094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e566e5f57a2c944f69e8bf41c06ce6f58e5e383d02e3811ffbdbca2405a03b`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:f9cea913444f7e8acd3d07f2cd7670cd28468d48a2d2f5941c4b6a9a35e0427a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d7b544c9028dc94601084bc0b26038bd215fd585731ffb843b95c11616848f`

```dockerfile
```

-	Layers:
	-	`sha256:f4cd62261a445f98af038b0cbff3f7054ac217b7e36c0e59d370c436c17999ab`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e554388d79522e92428f0a329dd4024becbe133d93cc298e3b3f19fe769c5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d3e785af72753f053cdbe0d272ae32efdb191b73b6d238882b8515e360e55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3086615f9efa498ae9d2f554e2824bdc11572e36270fa30ae141052e9b88120b`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.2 MB (6205728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a682c8240a063be6edb589f7d09954caa2f0a40d3ebb45eac4234abf6fbc5f6`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:9ab349969a32ee01e8bcb841bb52b6d4ffd7a87a867968b3a8111c830d1f667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57daccc6ef4bf25d89aad9d9d9000209b3ee8c6814ed3ccb744d1db6d5761d6`

```dockerfile
```

-	Layers:
	-	`sha256:f1b2616b1d8419ddadbc195580b24cdab43b59899da9485f8b0fd5f06e928676`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:112de0b731fdb92a9c813eee3b0f8a816046a6e882307d335aa4f3d6b64ab2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6261173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67383f85c6e3f28202e7d562786c204a63d766d6840532ad193e6d18b1ed707`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 01:10:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 01:10:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 01:10:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 01:10:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 01:10:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 01:10:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eb0e94a8e853f1e2567208a976f6d1cc5ecfaea1d16c87495229884c956736b7`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.3 MB (6260663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50278529f5f5f05ea6ca0fd0219f7a459b697c47991305f9d63d45b1b23495f8`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:a755da6315e498cab6e9870590b2b34fd8157c20891fed667e5ab5e493e0af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67349f6f4539144ad7678f3284335b4772501bcfa7d9770f035e84b2da04f17`

```dockerfile
```

-	Layers:
	-	`sha256:168e5061e0d664166bd9f7f89a8c07fa6f14f5132924faf8e3f3de8a21fc7cc3`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:2c9846411d4b6d33497d039dd5106ad38464b748f2a0d9886f84d6cfef669524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbc00e62ab08542eecb29f4ca6bb5907e5ad175fd4eb3d6613ec701209e38a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:08 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67ffc5a82b02d8ffc00056ab8c020a3b83a99b6b77157514635e2e300d167911`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.7 MB (6651485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f52004feacf72864a4f4c42486e43587d4dd67df78fc3e13cefbe7e59186ef`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:ff392c940bafbd3cb3b74113b5c1e489c15df878b322dfcc20b22333ce41080d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d79eb9f583d6a49a5d5181dab00ed84cc7ad774999a71fb342154ff015520c3`

```dockerfile
```

-	Layers:
	-	`sha256:7ee6cf5f9d4c2d0e016b2ff289228a30b182caf91592475b3a30063dd252b252`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:10447eaa252bcfb6c3c80118cac7a3b7d51c9a6498cc26d41dea1f72a29a718a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134088579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa19bee47e781cb629295ccf987910ba8172d206a2c5b755715734337341c77`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:19 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:04a1144166eb5b33184d353a4d7fcf95d121b39915427dc4374067d235aa4fae in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba58bc2ff4cb3ed55b80304b80b9c63f18f2df3aa65906a51c4228a916de113b`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ee7a8195af77f60f35ff2d6b86f9b83c3ea7a0787b41513b6d512a38cfbeb1`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 7.0 MB (7043891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a61086d35b626fb6f16c1e6be5566b2c6cafc605ea3ffd8bb0131f0aa62cd`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09595785c206d9c7108fdd885443f316708faa65baaa5229d4727c90dfeb7890`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49d51a826ee74af6afa6df4d7672be2e6d939ce87c78cc52903605ff9aa79c`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25503378a2c0fd04f5a847805ea1d9dca5b4ab6baef186823953f0b0b69d8a`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:5199cd3987b4be19f276542ea06d2218ad38a02acce7f78352c4a890feb5aa7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:e3975ae3c259e07dc00b126ef5cf0570d4b9c1995de29c286314a8c94185f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6842884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a858e4f7943893e252bc83397a059d23acc4bba8780c464abee2a7ca16c7445`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:09:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:09:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:09:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:09:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:09:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:09:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7c3bd50a747eaeeb10f95fa519304e5d461cdf7abfea618bd20f6082ff6662a0`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.8 MB (6842374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de808d2a465a42d8c366fe6a0444bfe0126b0deb5df083e28a6ab5da8f23bd`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:23bcf4e2ed2926d96eea36a58166f435554c690541005e998f5d616db30e45f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507326c78aca26a49af5c475ba8b2e2af04ec277a225d3045596713d6ff37309`

```dockerfile
```

-	Layers:
	-	`sha256:f040bfc84eb63a5f18c5215d1a0b547ad6574a095bc308ed0abb87f0e078fd56`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fec1423119b8e851f070386e125c5834183df6ef68cdf380acc9baeea48437c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddea1197c216967009e6e1e0c22c06b810ad0056259b9aa2d0d4c9116f36a3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:07:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:07:34 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:07:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:07:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:07:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:07:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bf1819a534ff3a05b2ec4b423942e9e9c1db524f8abdf07d0916cc9d7977e963`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.6 MB (6559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b10a626663e338c0bb1dfea4c11c6b38d61cac3eeefbe2918057535336ac6b`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:cf5f1e96a51a5bb900685df5ea819d0c6d2fa448635ed02772654ff2b5d22c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c00aaa6a70cd7d0e9305def7746345074e4a5081f236f2b44b9b79e39464d8`

```dockerfile
```

-	Layers:
	-	`sha256:03d05c80b133e625e60b7cb05cef59b26ce5d7adb0a442fffea4584ab6416a79`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a34dfd5d492771b140674e5c141027c58b58e4e2cd947f6eba0a5a31e2632e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6550603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093ad3956c6655a303f62a9ce264a18c45b4b863cb96efd842248173c0a606f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:79835d220a3efcc4d8184ca74b4eca9de6abd447cd214ab6d89fae0fc25d71a9`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.6 MB (6550094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e566e5f57a2c944f69e8bf41c06ce6f58e5e383d02e3811ffbdbca2405a03b`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9cea913444f7e8acd3d07f2cd7670cd28468d48a2d2f5941c4b6a9a35e0427a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d7b544c9028dc94601084bc0b26038bd215fd585731ffb843b95c11616848f`

```dockerfile
```

-	Layers:
	-	`sha256:f4cd62261a445f98af038b0cbff3f7054ac217b7e36c0e59d370c436c17999ab`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e554388d79522e92428f0a329dd4024becbe133d93cc298e3b3f19fe769c5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d3e785af72753f053cdbe0d272ae32efdb191b73b6d238882b8515e360e55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3086615f9efa498ae9d2f554e2824bdc11572e36270fa30ae141052e9b88120b`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.2 MB (6205728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a682c8240a063be6edb589f7d09954caa2f0a40d3ebb45eac4234abf6fbc5f6`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9ab349969a32ee01e8bcb841bb52b6d4ffd7a87a867968b3a8111c830d1f667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57daccc6ef4bf25d89aad9d9d9000209b3ee8c6814ed3ccb744d1db6d5761d6`

```dockerfile
```

-	Layers:
	-	`sha256:f1b2616b1d8419ddadbc195580b24cdab43b59899da9485f8b0fd5f06e928676`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:112de0b731fdb92a9c813eee3b0f8a816046a6e882307d335aa4f3d6b64ab2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6261173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67383f85c6e3f28202e7d562786c204a63d766d6840532ad193e6d18b1ed707`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 01:10:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 01:10:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 01:10:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 01:10:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 01:10:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 01:10:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eb0e94a8e853f1e2567208a976f6d1cc5ecfaea1d16c87495229884c956736b7`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.3 MB (6260663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50278529f5f5f05ea6ca0fd0219f7a459b697c47991305f9d63d45b1b23495f8`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a755da6315e498cab6e9870590b2b34fd8157c20891fed667e5ab5e493e0af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67349f6f4539144ad7678f3284335b4772501bcfa7d9770f035e84b2da04f17`

```dockerfile
```

-	Layers:
	-	`sha256:168e5061e0d664166bd9f7f89a8c07fa6f14f5132924faf8e3f3de8a21fc7cc3`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:2c9846411d4b6d33497d039dd5106ad38464b748f2a0d9886f84d6cfef669524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbc00e62ab08542eecb29f4ca6bb5907e5ad175fd4eb3d6613ec701209e38a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:08 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67ffc5a82b02d8ffc00056ab8c020a3b83a99b6b77157514635e2e300d167911`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.7 MB (6651485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f52004feacf72864a4f4c42486e43587d4dd67df78fc3e13cefbe7e59186ef`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ff392c940bafbd3cb3b74113b5c1e489c15df878b322dfcc20b22333ce41080d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d79eb9f583d6a49a5d5181dab00ed84cc7ad774999a71fb342154ff015520c3`

```dockerfile
```

-	Layers:
	-	`sha256:7ee6cf5f9d4c2d0e016b2ff289228a30b182caf91592475b3a30063dd252b252`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:2b6839a0f95f211d134087d05f1c2b6985ffe28ad04ab158bedd18b7430ac79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:10447eaa252bcfb6c3c80118cac7a3b7d51c9a6498cc26d41dea1f72a29a718a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134088579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa19bee47e781cb629295ccf987910ba8172d206a2c5b755715734337341c77`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:19 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:04a1144166eb5b33184d353a4d7fcf95d121b39915427dc4374067d235aa4fae in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba58bc2ff4cb3ed55b80304b80b9c63f18f2df3aa65906a51c4228a916de113b`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ee7a8195af77f60f35ff2d6b86f9b83c3ea7a0787b41513b6d512a38cfbeb1`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 7.0 MB (7043891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a61086d35b626fb6f16c1e6be5566b2c6cafc605ea3ffd8bb0131f0aa62cd`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09595785c206d9c7108fdd885443f316708faa65baaa5229d4727c90dfeb7890`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49d51a826ee74af6afa6df4d7672be2e6d939ce87c78cc52903605ff9aa79c`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25503378a2c0fd04f5a847805ea1d9dca5b4ab6baef186823953f0b0b69d8a`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:2b6839a0f95f211d134087d05f1c2b6985ffe28ad04ab158bedd18b7430ac79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:10447eaa252bcfb6c3c80118cac7a3b7d51c9a6498cc26d41dea1f72a29a718a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134088579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa19bee47e781cb629295ccf987910ba8172d206a2c5b755715734337341c77`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:19 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:04a1144166eb5b33184d353a4d7fcf95d121b39915427dc4374067d235aa4fae in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba58bc2ff4cb3ed55b80304b80b9c63f18f2df3aa65906a51c4228a916de113b`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ee7a8195af77f60f35ff2d6b86f9b83c3ea7a0787b41513b6d512a38cfbeb1`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 7.0 MB (7043891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a61086d35b626fb6f16c1e6be5566b2c6cafc605ea3ffd8bb0131f0aa62cd`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09595785c206d9c7108fdd885443f316708faa65baaa5229d4727c90dfeb7890`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49d51a826ee74af6afa6df4d7672be2e6d939ce87c78cc52903605ff9aa79c`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25503378a2c0fd04f5a847805ea1d9dca5b4ab6baef186823953f0b0b69d8a`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:5199cd3987b4be19f276542ea06d2218ad38a02acce7f78352c4a890feb5aa7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:e3975ae3c259e07dc00b126ef5cf0570d4b9c1995de29c286314a8c94185f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6842884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a858e4f7943893e252bc83397a059d23acc4bba8780c464abee2a7ca16c7445`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:09:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:09:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:09:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:09:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:09:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:09:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7c3bd50a747eaeeb10f95fa519304e5d461cdf7abfea618bd20f6082ff6662a0`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.8 MB (6842374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de808d2a465a42d8c366fe6a0444bfe0126b0deb5df083e28a6ab5da8f23bd`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:23bcf4e2ed2926d96eea36a58166f435554c690541005e998f5d616db30e45f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507326c78aca26a49af5c475ba8b2e2af04ec277a225d3045596713d6ff37309`

```dockerfile
```

-	Layers:
	-	`sha256:f040bfc84eb63a5f18c5215d1a0b547ad6574a095bc308ed0abb87f0e078fd56`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fec1423119b8e851f070386e125c5834183df6ef68cdf380acc9baeea48437c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddea1197c216967009e6e1e0c22c06b810ad0056259b9aa2d0d4c9116f36a3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:07:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:07:34 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:07:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:07:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:07:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:07:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bf1819a534ff3a05b2ec4b423942e9e9c1db524f8abdf07d0916cc9d7977e963`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.6 MB (6559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b10a626663e338c0bb1dfea4c11c6b38d61cac3eeefbe2918057535336ac6b`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:cf5f1e96a51a5bb900685df5ea819d0c6d2fa448635ed02772654ff2b5d22c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c00aaa6a70cd7d0e9305def7746345074e4a5081f236f2b44b9b79e39464d8`

```dockerfile
```

-	Layers:
	-	`sha256:03d05c80b133e625e60b7cb05cef59b26ce5d7adb0a442fffea4584ab6416a79`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a34dfd5d492771b140674e5c141027c58b58e4e2cd947f6eba0a5a31e2632e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6550603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093ad3956c6655a303f62a9ce264a18c45b4b863cb96efd842248173c0a606f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:79835d220a3efcc4d8184ca74b4eca9de6abd447cd214ab6d89fae0fc25d71a9`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.6 MB (6550094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e566e5f57a2c944f69e8bf41c06ce6f58e5e383d02e3811ffbdbca2405a03b`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9cea913444f7e8acd3d07f2cd7670cd28468d48a2d2f5941c4b6a9a35e0427a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d7b544c9028dc94601084bc0b26038bd215fd585731ffb843b95c11616848f`

```dockerfile
```

-	Layers:
	-	`sha256:f4cd62261a445f98af038b0cbff3f7054ac217b7e36c0e59d370c436c17999ab`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e554388d79522e92428f0a329dd4024becbe133d93cc298e3b3f19fe769c5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d3e785af72753f053cdbe0d272ae32efdb191b73b6d238882b8515e360e55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3086615f9efa498ae9d2f554e2824bdc11572e36270fa30ae141052e9b88120b`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.2 MB (6205728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a682c8240a063be6edb589f7d09954caa2f0a40d3ebb45eac4234abf6fbc5f6`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9ab349969a32ee01e8bcb841bb52b6d4ffd7a87a867968b3a8111c830d1f667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57daccc6ef4bf25d89aad9d9d9000209b3ee8c6814ed3ccb744d1db6d5761d6`

```dockerfile
```

-	Layers:
	-	`sha256:f1b2616b1d8419ddadbc195580b24cdab43b59899da9485f8b0fd5f06e928676`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:112de0b731fdb92a9c813eee3b0f8a816046a6e882307d335aa4f3d6b64ab2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6261173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67383f85c6e3f28202e7d562786c204a63d766d6840532ad193e6d18b1ed707`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 01:10:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 01:10:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 01:10:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 01:10:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 01:10:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 01:10:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eb0e94a8e853f1e2567208a976f6d1cc5ecfaea1d16c87495229884c956736b7`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.3 MB (6260663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50278529f5f5f05ea6ca0fd0219f7a459b697c47991305f9d63d45b1b23495f8`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a755da6315e498cab6e9870590b2b34fd8157c20891fed667e5ab5e493e0af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67349f6f4539144ad7678f3284335b4772501bcfa7d9770f035e84b2da04f17`

```dockerfile
```

-	Layers:
	-	`sha256:168e5061e0d664166bd9f7f89a8c07fa6f14f5132924faf8e3f3de8a21fc7cc3`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:2c9846411d4b6d33497d039dd5106ad38464b748f2a0d9886f84d6cfef669524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbc00e62ab08542eecb29f4ca6bb5907e5ad175fd4eb3d6613ec701209e38a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:08 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67ffc5a82b02d8ffc00056ab8c020a3b83a99b6b77157514635e2e300d167911`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.7 MB (6651485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f52004feacf72864a4f4c42486e43587d4dd67df78fc3e13cefbe7e59186ef`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ff392c940bafbd3cb3b74113b5c1e489c15df878b322dfcc20b22333ce41080d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d79eb9f583d6a49a5d5181dab00ed84cc7ad774999a71fb342154ff015520c3`

```dockerfile
```

-	Layers:
	-	`sha256:7ee6cf5f9d4c2d0e016b2ff289228a30b182caf91592475b3a30063dd252b252`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12`

```console
$ docker pull nats@sha256:62c48e90af6b4c593d8ad7d8aa24bb6fbc2d64674c5c6b3a40ef6b4cbb38a85b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; s390x

```console
$ docker pull nats@sha256:bdaf5e37416214372851cb6b4bbea4b66dee9bd1fe247cd6aeb82e625e21ab0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897ae89f09ef3bbb94497e713533c7b6260ce8997361cfcfe598da398bddf037`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 01:09:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 01:09:51 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 01:09:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 01:09:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 01:09:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 01:09:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2fe143eda61259a3bebc7076cebb78ddc3177beb70c94b5f394703ffe2e58907`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.5 MB (6495007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdaeaed9338d6c6040a0c39bd903c68d47815c23157a189e380ded49a98af93`  
		Last Modified: Tue, 28 Apr 2026 01:10:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:0c5977840a5d6298d8a0d4b45547b2d4ff563ac1529a331b0a9716844be57652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a102f895cec4d1bd2646eb11fe02b92fb9e8f8eef8255b11592711770ee8cfd2`

```dockerfile
```

-	Layers:
	-	`sha256:e458f081eaf693a236af67cbc7a3bcf45f19c1a7e50999f790047e2e4fab62ac`  
		Last Modified: Tue, 28 Apr 2026 01:10:30 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:24051404fbb2fd485a8755f82e8f0fffc3b3f91d2cc703055f90a6bbb4ca0f3d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133887676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0458a06da0e84fa05b885258b53d9d5faf8b6b358efa0f68d1dc495dd8c6d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:25 GMT
RUN cmd /S /C #(nop) COPY file:5fc27114abfd01a3cd1cfab3df4667aaa1dbe4b0cabe504c346c912774bc8676 in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:25 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7875b8d9e349ac3d54c5938848e334d60ca8d32ad8fc2c730ccaab0f8cbd21b`  
		Last Modified: Wed, 13 May 2026 00:22:32 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085d3090057f4cfc1f8a0980ae34ca07a5efefad65e68958b9a523dd06d6be84`  
		Last Modified: Wed, 13 May 2026 00:22:32 GMT  
		Size: 6.8 MB (6842903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2fd23b487134e5232816e0e14d1d4c6a659b4790338b731afed1b5a6a8203dd`  
		Last Modified: Wed, 13 May 2026 00:22:31 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3b607da2d15bf749b8564e11626a88f58c6bf1c990f21dd54e517bb88fa42`  
		Last Modified: Wed, 13 May 2026 00:22:31 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc4b0c3030085fa50685b8bd04386e47be2448bb31214374af6f262135e1490`  
		Last Modified: Wed, 13 May 2026 00:22:31 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866e3b404be339b2cc3999749e7370612c856f8bdabd3d5007534c8468a498ea`  
		Last Modified: Wed, 13 May 2026 00:22:30 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-alpine`

```console
$ docker pull nats@sha256:d152634b3db31218ca61c794827d04e8133e2538ef2f2cc3ab7be77b2ea8efd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9f005ca5efcae24ddd0413014c8ba5d3464d2a2560233b1bff108cc5563df009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10909206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c4eb9669610892376f2a3886a0c6e7b61fc0f2c5d3f740abe33e501f3f184c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:22 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785afd645f29603dfc502b5aed95092773a9d75614d744ab69f3c90a491db958`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 7.1 MB (7100047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2f75731780f4bdd6e4465ff6aedcfb784f2e04de6f7f593183a54df15a238b`  
		Last Modified: Wed, 20 May 2026 18:37:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea647ca93a5f93dd0481e42085d112026c222e13018b23f940c1798f150ddfc1`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c8082807e13d0ed6d2ad0cebcad6ff56b3a50637c7121d851c85bc76d43e51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c6f5b5e660ea789920f5dadbe9d69a4b9c17b3cb539f1ad32abfe974a8016`

```dockerfile
```

-	Layers:
	-	`sha256:d118d5c6f5a5b003d23105ccb683ce7cbca22c58923371c7a4cad24bb2a0fa7a`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ca666c2519ce831880fc65291a7ba5e6bdde44f1fce5826695e03943924c735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10347662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae81b57a35e9f65ea23549d2183c2c2e7ca7d50ce3f5036fa062e1cafaf518d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:19 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2912b40ddee494992b06ce6cfb3fe8dcb65d8de1892afcc94917eca78b7d9a0e`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 6.8 MB (6839309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c4d072278e3126931517cbe8b2c9ef7cb6deb74558f56fedca986a5290a04c`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f197927573b1036dd0f62c1a4cc9744836b24dbc6a2f4de557bdc47a30ce8be`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c61ccd3efdac690b485d840b7dfeceda69959a897f80949d0526c35a457cf1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecbe0cf18d59940e35cb0d2a6250eef69ca91a9543eb363af073473e44f86c`

```dockerfile
```

-	Layers:
	-	`sha256:18009424a0cc1065f3e1eef0bf7339139ef37661b11ace35f1b5949d76f335d9`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bcaff37bbf2a1f726cb43e74fe7db6b6e753a949c6083b2822d18e14da85ca0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10055590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd657e711d296590c867eb7ef48b021588d25b86bfad505ec5ae8cde2ec1d1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:15 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc50b4a871d38a0cadde4ed4e424bc2187dfef3cd7b5af2f61d284f5000115cd`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 6.8 MB (6828786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549ff00bf4e47e9e775e46e3309a6c2d758382c50d7296865843e1034afe6dc`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ec8720496ec12b71688a575e86930c39ad7b2f5f12bc6e1ea5efa4b6ed815`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c35fea02bd550591fb78b42bc3e5316a3ce215f434775a80bfb9160fbd852a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64701b345d4b8c5c56c71be078a3da0398507cd26e5919d9645432b5788339d9`

```dockerfile
```

-	Layers:
	-	`sha256:98625cfe5efdb1372a3b79cc98481ba6088f0d689b3566d4b9137f4ae7c4e389`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d5e2a634247e27b59ccf258b33f626c0f5949b96b737536496b562f06b7e094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fc2db9d5bb25035d90c05c366a4658fad874a40ee451f2a41188d4f6ead80b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:06 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ff339b51fb101889997a78aaa1897c82810b93750d3c1fad2c9939c172510d`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 6.5 MB (6499312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdeeebd5372e1dc9a2c97c853e72b20a3622eed3457557f5913caa2b335da1`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624ccef5078119f6ce1d17ffcdd69ee710740b23ed841fbd209e80c8b6f3032`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2b097ebfadc88817dcda244513c1536ee40a0fe3e24f28e6094d7eddf30a9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195c6c70cb97e0570c5672af8dc9c1b933cc356306a6daae576ac7e92b55ee69`

```dockerfile
```

-	Layers:
	-	`sha256:9145327976083751cab916e93d4003480e2bc0b428d04a554617da1720ba9788`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 14.3 KB (14308 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:2e2a8c50a862185aabb439c2fe0736bf976ac4f14f840192f46ada06908ec62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6684ad61a65a2f9bf995f867d9d9d9b78d57e72ecbac3ca56cb56b6e407e0ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0b03709a632c9f299b1ef2c2691c1b292ae9f333a7b2083a9b51162a19669`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.6 MB (6557551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5b7ba3b09bf23127b1a75c412fb6e5e3fa773abda140a3f0e45600422968bf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9cec962a037f640085142478803038714db7fa629a4b7e6cad1c2f41371943`

```dockerfile
```

-	Layers:
	-	`sha256:bc2e73ad0cbc0cad27f1667939617eb3a7d77a3ba7dd6d70917518d2ee4fed7f`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:ce14e245951893e72e72ac26599d178e07af3e24fd01a857cc00c484fee718cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f596aa7cbe6e6e80f8063aae3852a811f7045c570a2bf4e89c6b1c0a0d596f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13002ceadd3c101c2cfaa462d93d68f1056f8fd0453fd99269b12c624bc6b38a`  
		Last Modified: Wed, 20 May 2026 18:49:13 GMT  
		Size: 6.9 MB (6948871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaa4e64de2e200c41440e78516f3fbbcf03b5b5e18cb05b20a63bd1661ce87d`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d69a6bdd10e86979de515f61b8c590bea15507a88f17e4f5a7f57ddfac937e`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:92726e2db0802623d76696809568374f168d11a6eb505249100949eb89a74c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1345efb532a7d2fa604c74539fdd13035a959493b0f11f0e962227e91cfe8e`

```dockerfile
```

-	Layers:
	-	`sha256:afc92f71ec0a9bc07c23a3ff65bc6f32afe90cfc974b6e23b25a06cab13804fd`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-alpine3.22`

```console
$ docker pull nats@sha256:d152634b3db31218ca61c794827d04e8133e2538ef2f2cc3ab7be77b2ea8efd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:9f005ca5efcae24ddd0413014c8ba5d3464d2a2560233b1bff108cc5563df009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10909206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c4eb9669610892376f2a3886a0c6e7b61fc0f2c5d3f740abe33e501f3f184c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:22 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785afd645f29603dfc502b5aed95092773a9d75614d744ab69f3c90a491db958`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 7.1 MB (7100047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2f75731780f4bdd6e4465ff6aedcfb784f2e04de6f7f593183a54df15a238b`  
		Last Modified: Wed, 20 May 2026 18:37:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea647ca93a5f93dd0481e42085d112026c222e13018b23f940c1798f150ddfc1`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c8082807e13d0ed6d2ad0cebcad6ff56b3a50637c7121d851c85bc76d43e51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c6f5b5e660ea789920f5dadbe9d69a4b9c17b3cb539f1ad32abfe974a8016`

```dockerfile
```

-	Layers:
	-	`sha256:d118d5c6f5a5b003d23105ccb683ce7cbca22c58923371c7a4cad24bb2a0fa7a`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ca666c2519ce831880fc65291a7ba5e6bdde44f1fce5826695e03943924c735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10347662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae81b57a35e9f65ea23549d2183c2c2e7ca7d50ce3f5036fa062e1cafaf518d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:19 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2912b40ddee494992b06ce6cfb3fe8dcb65d8de1892afcc94917eca78b7d9a0e`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 6.8 MB (6839309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c4d072278e3126931517cbe8b2c9ef7cb6deb74558f56fedca986a5290a04c`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f197927573b1036dd0f62c1a4cc9744836b24dbc6a2f4de557bdc47a30ce8be`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c61ccd3efdac690b485d840b7dfeceda69959a897f80949d0526c35a457cf1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecbe0cf18d59940e35cb0d2a6250eef69ca91a9543eb363af073473e44f86c`

```dockerfile
```

-	Layers:
	-	`sha256:18009424a0cc1065f3e1eef0bf7339139ef37661b11ace35f1b5949d76f335d9`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bcaff37bbf2a1f726cb43e74fe7db6b6e753a949c6083b2822d18e14da85ca0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10055590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd657e711d296590c867eb7ef48b021588d25b86bfad505ec5ae8cde2ec1d1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:15 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc50b4a871d38a0cadde4ed4e424bc2187dfef3cd7b5af2f61d284f5000115cd`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 6.8 MB (6828786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549ff00bf4e47e9e775e46e3309a6c2d758382c50d7296865843e1034afe6dc`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ec8720496ec12b71688a575e86930c39ad7b2f5f12bc6e1ea5efa4b6ed815`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c35fea02bd550591fb78b42bc3e5316a3ce215f434775a80bfb9160fbd852a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64701b345d4b8c5c56c71be078a3da0398507cd26e5919d9645432b5788339d9`

```dockerfile
```

-	Layers:
	-	`sha256:98625cfe5efdb1372a3b79cc98481ba6088f0d689b3566d4b9137f4ae7c4e389`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d5e2a634247e27b59ccf258b33f626c0f5949b96b737536496b562f06b7e094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fc2db9d5bb25035d90c05c366a4658fad874a40ee451f2a41188d4f6ead80b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:06 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ff339b51fb101889997a78aaa1897c82810b93750d3c1fad2c9939c172510d`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 6.5 MB (6499312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdeeebd5372e1dc9a2c97c853e72b20a3622eed3457557f5913caa2b335da1`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624ccef5078119f6ce1d17ffcdd69ee710740b23ed841fbd209e80c8b6f3032`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d2b097ebfadc88817dcda244513c1536ee40a0fe3e24f28e6094d7eddf30a9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195c6c70cb97e0570c5672af8dc9c1b933cc356306a6daae576ac7e92b55ee69`

```dockerfile
```

-	Layers:
	-	`sha256:9145327976083751cab916e93d4003480e2bc0b428d04a554617da1720ba9788`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 14.3 KB (14308 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:2e2a8c50a862185aabb439c2fe0736bf976ac4f14f840192f46ada06908ec62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6684ad61a65a2f9bf995f867d9d9d9b78d57e72ecbac3ca56cb56b6e407e0ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0b03709a632c9f299b1ef2c2691c1b292ae9f333a7b2083a9b51162a19669`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.6 MB (6557551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5b7ba3b09bf23127b1a75c412fb6e5e3fa773abda140a3f0e45600422968bf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9cec962a037f640085142478803038714db7fa629a4b7e6cad1c2f41371943`

```dockerfile
```

-	Layers:
	-	`sha256:bc2e73ad0cbc0cad27f1667939617eb3a7d77a3ba7dd6d70917518d2ee4fed7f`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:ce14e245951893e72e72ac26599d178e07af3e24fd01a857cc00c484fee718cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f596aa7cbe6e6e80f8063aae3852a811f7045c570a2bf4e89c6b1c0a0d596f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13002ceadd3c101c2cfaa462d93d68f1056f8fd0453fd99269b12c624bc6b38a`  
		Last Modified: Wed, 20 May 2026 18:49:13 GMT  
		Size: 6.9 MB (6948871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaa4e64de2e200c41440e78516f3fbbcf03b5b5e18cb05b20a63bd1661ce87d`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d69a6bdd10e86979de515f61b8c590bea15507a88f17e4f5a7f57ddfac937e`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:92726e2db0802623d76696809568374f168d11a6eb505249100949eb89a74c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1345efb532a7d2fa604c74539fdd13035a959493b0f11f0e962227e91cfe8e`

```dockerfile
```

-	Layers:
	-	`sha256:afc92f71ec0a9bc07c23a3ff65bc6f32afe90cfc974b6e23b25a06cab13804fd`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-linux`

```console
$ docker pull nats@sha256:2491f5022944a3bb0a502411cdb5bf10c54a9875363d0acda9f128612982969e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-linux` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:bdaf5e37416214372851cb6b4bbea4b66dee9bd1fe247cd6aeb82e625e21ab0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897ae89f09ef3bbb94497e713533c7b6260ce8997361cfcfe598da398bddf037`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 01:09:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 01:09:51 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 01:09:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 01:09:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 01:09:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 01:09:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2fe143eda61259a3bebc7076cebb78ddc3177beb70c94b5f394703ffe2e58907`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.5 MB (6495007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdaeaed9338d6c6040a0c39bd903c68d47815c23157a189e380ded49a98af93`  
		Last Modified: Tue, 28 Apr 2026 01:10:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0c5977840a5d6298d8a0d4b45547b2d4ff563ac1529a331b0a9716844be57652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a102f895cec4d1bd2646eb11fe02b92fb9e8f8eef8255b11592711770ee8cfd2`

```dockerfile
```

-	Layers:
	-	`sha256:e458f081eaf693a236af67cbc7a3bcf45f19c1a7e50999f790047e2e4fab62ac`  
		Last Modified: Tue, 28 Apr 2026 01:10:30 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-nanoserver`

```console
$ docker pull nats@sha256:770611f015b9f82fa4d5c584cd94b8b7ef9742f97b6519420be8c1d3984258e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:24051404fbb2fd485a8755f82e8f0fffc3b3f91d2cc703055f90a6bbb4ca0f3d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133887676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0458a06da0e84fa05b885258b53d9d5faf8b6b358efa0f68d1dc495dd8c6d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:25 GMT
RUN cmd /S /C #(nop) COPY file:5fc27114abfd01a3cd1cfab3df4667aaa1dbe4b0cabe504c346c912774bc8676 in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:25 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7875b8d9e349ac3d54c5938848e334d60ca8d32ad8fc2c730ccaab0f8cbd21b`  
		Last Modified: Wed, 13 May 2026 00:22:32 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085d3090057f4cfc1f8a0980ae34ca07a5efefad65e68958b9a523dd06d6be84`  
		Last Modified: Wed, 13 May 2026 00:22:32 GMT  
		Size: 6.8 MB (6842903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2fd23b487134e5232816e0e14d1d4c6a659b4790338b731afed1b5a6a8203dd`  
		Last Modified: Wed, 13 May 2026 00:22:31 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3b607da2d15bf749b8564e11626a88f58c6bf1c990f21dd54e517bb88fa42`  
		Last Modified: Wed, 13 May 2026 00:22:31 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc4b0c3030085fa50685b8bd04386e47be2448bb31214374af6f262135e1490`  
		Last Modified: Wed, 13 May 2026 00:22:31 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866e3b404be339b2cc3999749e7370612c856f8bdabd3d5007534c8468a498ea`  
		Last Modified: Wed, 13 May 2026 00:22:30 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:770611f015b9f82fa4d5c584cd94b8b7ef9742f97b6519420be8c1d3984258e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:24051404fbb2fd485a8755f82e8f0fffc3b3f91d2cc703055f90a6bbb4ca0f3d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133887676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0458a06da0e84fa05b885258b53d9d5faf8b6b358efa0f68d1dc495dd8c6d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:25 GMT
RUN cmd /S /C #(nop) COPY file:5fc27114abfd01a3cd1cfab3df4667aaa1dbe4b0cabe504c346c912774bc8676 in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:25 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7875b8d9e349ac3d54c5938848e334d60ca8d32ad8fc2c730ccaab0f8cbd21b`  
		Last Modified: Wed, 13 May 2026 00:22:32 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085d3090057f4cfc1f8a0980ae34ca07a5efefad65e68958b9a523dd06d6be84`  
		Last Modified: Wed, 13 May 2026 00:22:32 GMT  
		Size: 6.8 MB (6842903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2fd23b487134e5232816e0e14d1d4c6a659b4790338b731afed1b5a6a8203dd`  
		Last Modified: Wed, 13 May 2026 00:22:31 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f3b607da2d15bf749b8564e11626a88f58c6bf1c990f21dd54e517bb88fa42`  
		Last Modified: Wed, 13 May 2026 00:22:31 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc4b0c3030085fa50685b8bd04386e47be2448bb31214374af6f262135e1490`  
		Last Modified: Wed, 13 May 2026 00:22:31 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866e3b404be339b2cc3999749e7370612c856f8bdabd3d5007534c8468a498ea`  
		Last Modified: Wed, 13 May 2026 00:22:30 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-scratch`

```console
$ docker pull nats@sha256:2491f5022944a3bb0a502411cdb5bf10c54a9875363d0acda9f128612982969e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-scratch` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:bdaf5e37416214372851cb6b4bbea4b66dee9bd1fe247cd6aeb82e625e21ab0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897ae89f09ef3bbb94497e713533c7b6260ce8997361cfcfe598da398bddf037`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 01:09:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 01:09:51 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 01:09:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 01:09:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 01:09:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 01:09:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2fe143eda61259a3bebc7076cebb78ddc3177beb70c94b5f394703ffe2e58907`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.5 MB (6495007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdaeaed9338d6c6040a0c39bd903c68d47815c23157a189e380ded49a98af93`  
		Last Modified: Tue, 28 Apr 2026 01:10:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0c5977840a5d6298d8a0d4b45547b2d4ff563ac1529a331b0a9716844be57652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a102f895cec4d1bd2646eb11fe02b92fb9e8f8eef8255b11592711770ee8cfd2`

```dockerfile
```

-	Layers:
	-	`sha256:e458f081eaf693a236af67cbc7a3bcf45f19c1a7e50999f790047e2e4fab62ac`  
		Last Modified: Tue, 28 Apr 2026 01:10:30 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-windowsservercore`

```console
$ docker pull nats@sha256:93d7e77dc19ae1d7f04e86c2068da9a3b9e437892b266e13c64f28e1773223b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:e9d6a938ace06e341a366fc78d12f5aa1bd956dac71e4ff82158cb9eb81ac4c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130120651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1df05498b147c8f9c4865e19eb3f2266e06494384130ac34c45806311beb604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:59:48 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:59:48 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:59:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.9/nats-server-v2.12.9-windows-amd64.zip
# Wed, 20 May 2026 18:59:51 GMT
ENV NATS_SERVER_SHASUM=6d8d0b31ba2fbaca4613b9dbb1fd107c335ee26485f59fb9006e7ab34913117d
# Wed, 20 May 2026 18:59:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 19:00:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 19:00:22 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:00:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:00:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:00:23 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f31a04aebe50db6f85e58a4df9a8d34f7df2bf36b2a1485ac21d1af7127d32c`  
		Last Modified: Wed, 20 May 2026 19:00:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c32221a695427881403603d85b9fbe9a208cafa19e27db15a2a87080b977aeb`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb78dc8e8b1e6679429c94711da7ef1a170469e7abd593d612090cbeabfc2ce`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3ca19f5131d5dac1c4bad13e5c900a1330ded4bc79991da462281aa3992a2a`  
		Last Modified: Wed, 20 May 2026 19:00:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67bc96c36328bd4cc9410563bf01b2c2ecae49584ea178bdb62d7b45109d586`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 494.4 KB (494434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a8ebf88f3c30a60da7b6608197c202a69ce7dd0ab6be014efbf6eadd2349f`  
		Last Modified: Wed, 20 May 2026 19:00:33 GMT  
		Size: 7.2 MB (7192011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190bfa12df85ab9f289b0804e966103ffc0c26626f2c50e1a7409f5e5ed0855`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ce3c10c5a9944c33f1b695b2a9f04297226593bbaef9f132405493388c24c`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f580a22501d26e28952ee85653f70663980ab45953d0cfcbef50694db04d6`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4511ea5948cbca6aef9d7517e123f726b38c8a0eb9c947c2c4f6d7f54e0d88`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:93d7e77dc19ae1d7f04e86c2068da9a3b9e437892b266e13c64f28e1773223b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:e9d6a938ace06e341a366fc78d12f5aa1bd956dac71e4ff82158cb9eb81ac4c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130120651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1df05498b147c8f9c4865e19eb3f2266e06494384130ac34c45806311beb604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:59:48 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:59:48 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:59:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.9/nats-server-v2.12.9-windows-amd64.zip
# Wed, 20 May 2026 18:59:51 GMT
ENV NATS_SERVER_SHASUM=6d8d0b31ba2fbaca4613b9dbb1fd107c335ee26485f59fb9006e7ab34913117d
# Wed, 20 May 2026 18:59:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 19:00:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 19:00:22 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:00:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:00:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:00:23 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f31a04aebe50db6f85e58a4df9a8d34f7df2bf36b2a1485ac21d1af7127d32c`  
		Last Modified: Wed, 20 May 2026 19:00:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c32221a695427881403603d85b9fbe9a208cafa19e27db15a2a87080b977aeb`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb78dc8e8b1e6679429c94711da7ef1a170469e7abd593d612090cbeabfc2ce`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3ca19f5131d5dac1c4bad13e5c900a1330ded4bc79991da462281aa3992a2a`  
		Last Modified: Wed, 20 May 2026 19:00:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67bc96c36328bd4cc9410563bf01b2c2ecae49584ea178bdb62d7b45109d586`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 494.4 KB (494434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a8ebf88f3c30a60da7b6608197c202a69ce7dd0ab6be014efbf6eadd2349f`  
		Last Modified: Wed, 20 May 2026 19:00:33 GMT  
		Size: 7.2 MB (7192011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190bfa12df85ab9f289b0804e966103ffc0c26626f2c50e1a7409f5e5ed0855`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ce3c10c5a9944c33f1b695b2a9f04297226593bbaef9f132405493388c24c`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f580a22501d26e28952ee85653f70663980ab45953d0cfcbef50694db04d6`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4511ea5948cbca6aef9d7517e123f726b38c8a0eb9c947c2c4f6d7f54e0d88`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.9`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.9-alpine`

```console
$ docker pull nats@sha256:d152634b3db31218ca61c794827d04e8133e2538ef2f2cc3ab7be77b2ea8efd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9f005ca5efcae24ddd0413014c8ba5d3464d2a2560233b1bff108cc5563df009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10909206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c4eb9669610892376f2a3886a0c6e7b61fc0f2c5d3f740abe33e501f3f184c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:22 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785afd645f29603dfc502b5aed95092773a9d75614d744ab69f3c90a491db958`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 7.1 MB (7100047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2f75731780f4bdd6e4465ff6aedcfb784f2e04de6f7f593183a54df15a238b`  
		Last Modified: Wed, 20 May 2026 18:37:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea647ca93a5f93dd0481e42085d112026c222e13018b23f940c1798f150ddfc1`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c8082807e13d0ed6d2ad0cebcad6ff56b3a50637c7121d851c85bc76d43e51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c6f5b5e660ea789920f5dadbe9d69a4b9c17b3cb539f1ad32abfe974a8016`

```dockerfile
```

-	Layers:
	-	`sha256:d118d5c6f5a5b003d23105ccb683ce7cbca22c58923371c7a4cad24bb2a0fa7a`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ca666c2519ce831880fc65291a7ba5e6bdde44f1fce5826695e03943924c735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10347662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae81b57a35e9f65ea23549d2183c2c2e7ca7d50ce3f5036fa062e1cafaf518d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:19 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2912b40ddee494992b06ce6cfb3fe8dcb65d8de1892afcc94917eca78b7d9a0e`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 6.8 MB (6839309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c4d072278e3126931517cbe8b2c9ef7cb6deb74558f56fedca986a5290a04c`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f197927573b1036dd0f62c1a4cc9744836b24dbc6a2f4de557bdc47a30ce8be`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c61ccd3efdac690b485d840b7dfeceda69959a897f80949d0526c35a457cf1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecbe0cf18d59940e35cb0d2a6250eef69ca91a9543eb363af073473e44f86c`

```dockerfile
```

-	Layers:
	-	`sha256:18009424a0cc1065f3e1eef0bf7339139ef37661b11ace35f1b5949d76f335d9`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bcaff37bbf2a1f726cb43e74fe7db6b6e753a949c6083b2822d18e14da85ca0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10055590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd657e711d296590c867eb7ef48b021588d25b86bfad505ec5ae8cde2ec1d1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:15 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc50b4a871d38a0cadde4ed4e424bc2187dfef3cd7b5af2f61d284f5000115cd`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 6.8 MB (6828786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549ff00bf4e47e9e775e46e3309a6c2d758382c50d7296865843e1034afe6dc`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ec8720496ec12b71688a575e86930c39ad7b2f5f12bc6e1ea5efa4b6ed815`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c35fea02bd550591fb78b42bc3e5316a3ce215f434775a80bfb9160fbd852a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64701b345d4b8c5c56c71be078a3da0398507cd26e5919d9645432b5788339d9`

```dockerfile
```

-	Layers:
	-	`sha256:98625cfe5efdb1372a3b79cc98481ba6088f0d689b3566d4b9137f4ae7c4e389`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d5e2a634247e27b59ccf258b33f626c0f5949b96b737536496b562f06b7e094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fc2db9d5bb25035d90c05c366a4658fad874a40ee451f2a41188d4f6ead80b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:06 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ff339b51fb101889997a78aaa1897c82810b93750d3c1fad2c9939c172510d`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 6.5 MB (6499312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdeeebd5372e1dc9a2c97c853e72b20a3622eed3457557f5913caa2b335da1`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624ccef5078119f6ce1d17ffcdd69ee710740b23ed841fbd209e80c8b6f3032`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2b097ebfadc88817dcda244513c1536ee40a0fe3e24f28e6094d7eddf30a9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195c6c70cb97e0570c5672af8dc9c1b933cc356306a6daae576ac7e92b55ee69`

```dockerfile
```

-	Layers:
	-	`sha256:9145327976083751cab916e93d4003480e2bc0b428d04a554617da1720ba9788`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 14.3 KB (14308 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:2e2a8c50a862185aabb439c2fe0736bf976ac4f14f840192f46ada06908ec62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6684ad61a65a2f9bf995f867d9d9d9b78d57e72ecbac3ca56cb56b6e407e0ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0b03709a632c9f299b1ef2c2691c1b292ae9f333a7b2083a9b51162a19669`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.6 MB (6557551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5b7ba3b09bf23127b1a75c412fb6e5e3fa773abda140a3f0e45600422968bf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9cec962a037f640085142478803038714db7fa629a4b7e6cad1c2f41371943`

```dockerfile
```

-	Layers:
	-	`sha256:bc2e73ad0cbc0cad27f1667939617eb3a7d77a3ba7dd6d70917518d2ee4fed7f`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine` - linux; s390x

```console
$ docker pull nats@sha256:ce14e245951893e72e72ac26599d178e07af3e24fd01a857cc00c484fee718cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f596aa7cbe6e6e80f8063aae3852a811f7045c570a2bf4e89c6b1c0a0d596f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13002ceadd3c101c2cfaa462d93d68f1056f8fd0453fd99269b12c624bc6b38a`  
		Last Modified: Wed, 20 May 2026 18:49:13 GMT  
		Size: 6.9 MB (6948871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaa4e64de2e200c41440e78516f3fbbcf03b5b5e18cb05b20a63bd1661ce87d`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d69a6bdd10e86979de515f61b8c590bea15507a88f17e4f5a7f57ddfac937e`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:92726e2db0802623d76696809568374f168d11a6eb505249100949eb89a74c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1345efb532a7d2fa604c74539fdd13035a959493b0f11f0e962227e91cfe8e`

```dockerfile
```

-	Layers:
	-	`sha256:afc92f71ec0a9bc07c23a3ff65bc6f32afe90cfc974b6e23b25a06cab13804fd`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.9-alpine3.22`

```console
$ docker pull nats@sha256:d152634b3db31218ca61c794827d04e8133e2538ef2f2cc3ab7be77b2ea8efd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12.9-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:9f005ca5efcae24ddd0413014c8ba5d3464d2a2560233b1bff108cc5563df009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10909206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c4eb9669610892376f2a3886a0c6e7b61fc0f2c5d3f740abe33e501f3f184c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:22 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:22 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785afd645f29603dfc502b5aed95092773a9d75614d744ab69f3c90a491db958`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 7.1 MB (7100047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2f75731780f4bdd6e4465ff6aedcfb784f2e04de6f7f593183a54df15a238b`  
		Last Modified: Wed, 20 May 2026 18:37:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea647ca93a5f93dd0481e42085d112026c222e13018b23f940c1798f150ddfc1`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c8082807e13d0ed6d2ad0cebcad6ff56b3a50637c7121d851c85bc76d43e51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c6f5b5e660ea789920f5dadbe9d69a4b9c17b3cb539f1ad32abfe974a8016`

```dockerfile
```

-	Layers:
	-	`sha256:d118d5c6f5a5b003d23105ccb683ce7cbca22c58923371c7a4cad24bb2a0fa7a`  
		Last Modified: Wed, 20 May 2026 18:37:27 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ca666c2519ce831880fc65291a7ba5e6bdde44f1fce5826695e03943924c735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10347662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae81b57a35e9f65ea23549d2183c2c2e7ca7d50ce3f5036fa062e1cafaf518d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:19 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2912b40ddee494992b06ce6cfb3fe8dcb65d8de1892afcc94917eca78b7d9a0e`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 6.8 MB (6839309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c4d072278e3126931517cbe8b2c9ef7cb6deb74558f56fedca986a5290a04c`  
		Last Modified: Wed, 20 May 2026 18:36:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f197927573b1036dd0f62c1a4cc9744836b24dbc6a2f4de557bdc47a30ce8be`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c61ccd3efdac690b485d840b7dfeceda69959a897f80949d0526c35a457cf1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecbe0cf18d59940e35cb0d2a6250eef69ca91a9543eb363af073473e44f86c`

```dockerfile
```

-	Layers:
	-	`sha256:18009424a0cc1065f3e1eef0bf7339139ef37661b11ace35f1b5949d76f335d9`  
		Last Modified: Wed, 20 May 2026 18:36:23 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bcaff37bbf2a1f726cb43e74fe7db6b6e753a949c6083b2822d18e14da85ca0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10055590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd657e711d296590c867eb7ef48b021588d25b86bfad505ec5ae8cde2ec1d1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:36:15 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:36:15 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:36:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:36:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:36:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:36:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc50b4a871d38a0cadde4ed4e424bc2187dfef3cd7b5af2f61d284f5000115cd`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 6.8 MB (6828786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549ff00bf4e47e9e775e46e3309a6c2d758382c50d7296865843e1034afe6dc`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ec8720496ec12b71688a575e86930c39ad7b2f5f12bc6e1ea5efa4b6ed815`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c35fea02bd550591fb78b42bc3e5316a3ce215f434775a80bfb9160fbd852a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64701b345d4b8c5c56c71be078a3da0398507cd26e5919d9645432b5788339d9`

```dockerfile
```

-	Layers:
	-	`sha256:98625cfe5efdb1372a3b79cc98481ba6088f0d689b3566d4b9137f4ae7c4e389`  
		Last Modified: Wed, 20 May 2026 18:36:20 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d5e2a634247e27b59ccf258b33f626c0f5949b96b737536496b562f06b7e094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fc2db9d5bb25035d90c05c366a4658fad874a40ee451f2a41188d4f6ead80b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:06 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:37:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:06 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ff339b51fb101889997a78aaa1897c82810b93750d3c1fad2c9939c172510d`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 6.5 MB (6499312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdeeebd5372e1dc9a2c97c853e72b20a3622eed3457557f5913caa2b335da1`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624ccef5078119f6ce1d17ffcdd69ee710740b23ed841fbd209e80c8b6f3032`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d2b097ebfadc88817dcda244513c1536ee40a0fe3e24f28e6094d7eddf30a9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195c6c70cb97e0570c5672af8dc9c1b933cc356306a6daae576ac7e92b55ee69`

```dockerfile
```

-	Layers:
	-	`sha256:9145327976083751cab916e93d4003480e2bc0b428d04a554617da1720ba9788`  
		Last Modified: Wed, 20 May 2026 18:37:11 GMT  
		Size: 14.3 KB (14308 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:2e2a8c50a862185aabb439c2fe0736bf976ac4f14f840192f46ada06908ec62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6684ad61a65a2f9bf995f867d9d9d9b78d57e72ecbac3ca56cb56b6e407e0ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0b03709a632c9f299b1ef2c2691c1b292ae9f333a7b2083a9b51162a19669`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.6 MB (6557551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5b7ba3b09bf23127b1a75c412fb6e5e3fa773abda140a3f0e45600422968bf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9cec962a037f640085142478803038714db7fa629a4b7e6cad1c2f41371943`

```dockerfile
```

-	Layers:
	-	`sha256:bc2e73ad0cbc0cad27f1667939617eb3a7d77a3ba7dd6d70917518d2ee4fed7f`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.9-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:ce14e245951893e72e72ac26599d178e07af3e24fd01a857cc00c484fee718cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f596aa7cbe6e6e80f8063aae3852a811f7045c570a2bf4e89c6b1c0a0d596f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='72b5841a019f6c5a0be78d3cf21cd293446317e6b4e769e3b9d72090f2d87afc' ;;     armhf) natsArch='arm6'; sha256='eb159297eb8539e47f615180b1de759e6a735cfe3274a31d405301e1c2ee2aec' ;;     armv7) natsArch='arm7'; sha256='2573d1cb723f55d81c58e854e63c771e1a2d954a91ed0a23042e7e38fa0d405c' ;;     x86_64) natsArch='amd64'; sha256='b126515225aa2265a0088e0170f2a9de4c7880b2388cc7584aa77859ce831e3f' ;;     x86) natsArch='386'; sha256='c29a867045b25e300e501101abc3714e4e56c89b35b90ddbfc55ec6e7928eb17' ;;     s390x) natsArch='s390x'; sha256='d508d9f40853828623b50e367a4dd0394361352195b3669d5da7966991e30c03' ;;     ppc64le) natsArch='ppc64le'; sha256='a2dcbabba4aede66b9939d59e829d61417fffa7c08c49635b9a550a23f733cdc' ;;     loong64) natsArch='loong64'; sha256='5a0347fa1400a569cc798da80001fca8c68dc7193daea334df9ea6ec5fe2649c' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13002ceadd3c101c2cfaa462d93d68f1056f8fd0453fd99269b12c624bc6b38a`  
		Last Modified: Wed, 20 May 2026 18:49:13 GMT  
		Size: 6.9 MB (6948871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaa4e64de2e200c41440e78516f3fbbcf03b5b5e18cb05b20a63bd1661ce87d`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d69a6bdd10e86979de515f61b8c590bea15507a88f17e4f5a7f57ddfac937e`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:92726e2db0802623d76696809568374f168d11a6eb505249100949eb89a74c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1345efb532a7d2fa604c74539fdd13035a959493b0f11f0e962227e91cfe8e`

```dockerfile
```

-	Layers:
	-	`sha256:afc92f71ec0a9bc07c23a3ff65bc6f32afe90cfc974b6e23b25a06cab13804fd`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 14.2 KB (14204 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.9-linux`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.9-nanoserver`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.9-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.9-scratch`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.9-windowsservercore`

```console
$ docker pull nats@sha256:93d7e77dc19ae1d7f04e86c2068da9a3b9e437892b266e13c64f28e1773223b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12.9-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:e9d6a938ace06e341a366fc78d12f5aa1bd956dac71e4ff82158cb9eb81ac4c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130120651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1df05498b147c8f9c4865e19eb3f2266e06494384130ac34c45806311beb604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:59:48 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:59:48 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:59:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.9/nats-server-v2.12.9-windows-amd64.zip
# Wed, 20 May 2026 18:59:51 GMT
ENV NATS_SERVER_SHASUM=6d8d0b31ba2fbaca4613b9dbb1fd107c335ee26485f59fb9006e7ab34913117d
# Wed, 20 May 2026 18:59:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 19:00:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 19:00:22 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:00:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:00:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:00:23 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f31a04aebe50db6f85e58a4df9a8d34f7df2bf36b2a1485ac21d1af7127d32c`  
		Last Modified: Wed, 20 May 2026 19:00:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c32221a695427881403603d85b9fbe9a208cafa19e27db15a2a87080b977aeb`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb78dc8e8b1e6679429c94711da7ef1a170469e7abd593d612090cbeabfc2ce`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3ca19f5131d5dac1c4bad13e5c900a1330ded4bc79991da462281aa3992a2a`  
		Last Modified: Wed, 20 May 2026 19:00:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67bc96c36328bd4cc9410563bf01b2c2ecae49584ea178bdb62d7b45109d586`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 494.4 KB (494434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a8ebf88f3c30a60da7b6608197c202a69ce7dd0ab6be014efbf6eadd2349f`  
		Last Modified: Wed, 20 May 2026 19:00:33 GMT  
		Size: 7.2 MB (7192011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190bfa12df85ab9f289b0804e966103ffc0c26626f2c50e1a7409f5e5ed0855`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ce3c10c5a9944c33f1b695b2a9f04297226593bbaef9f132405493388c24c`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f580a22501d26e28952ee85653f70663980ab45953d0cfcbef50694db04d6`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4511ea5948cbca6aef9d7517e123f726b38c8a0eb9c947c2c4f6d7f54e0d88`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.9-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:93d7e77dc19ae1d7f04e86c2068da9a3b9e437892b266e13c64f28e1773223b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12.9-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:e9d6a938ace06e341a366fc78d12f5aa1bd956dac71e4ff82158cb9eb81ac4c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130120651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1df05498b147c8f9c4865e19eb3f2266e06494384130ac34c45806311beb604`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:59:48 GMT
ENV NATS_SERVER=2.12.9
# Wed, 20 May 2026 18:59:48 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.9
# Wed, 20 May 2026 18:59:50 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.9/nats-server-v2.12.9-windows-amd64.zip
# Wed, 20 May 2026 18:59:51 GMT
ENV NATS_SERVER_SHASUM=6d8d0b31ba2fbaca4613b9dbb1fd107c335ee26485f59fb9006e7ab34913117d
# Wed, 20 May 2026 18:59:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 19:00:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 19:00:22 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 19:00:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 19:00:23 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 19:00:23 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f31a04aebe50db6f85e58a4df9a8d34f7df2bf36b2a1485ac21d1af7127d32c`  
		Last Modified: Wed, 20 May 2026 19:00:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c32221a695427881403603d85b9fbe9a208cafa19e27db15a2a87080b977aeb`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb78dc8e8b1e6679429c94711da7ef1a170469e7abd593d612090cbeabfc2ce`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3ca19f5131d5dac1c4bad13e5c900a1330ded4bc79991da462281aa3992a2a`  
		Last Modified: Wed, 20 May 2026 19:00:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67bc96c36328bd4cc9410563bf01b2c2ecae49584ea178bdb62d7b45109d586`  
		Last Modified: Wed, 20 May 2026 19:00:30 GMT  
		Size: 494.4 KB (494434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a8ebf88f3c30a60da7b6608197c202a69ce7dd0ab6be014efbf6eadd2349f`  
		Last Modified: Wed, 20 May 2026 19:00:33 GMT  
		Size: 7.2 MB (7192011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190bfa12df85ab9f289b0804e966103ffc0c26626f2c50e1a7409f5e5ed0855`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ce3c10c5a9944c33f1b695b2a9f04297226593bbaef9f132405493388c24c`  
		Last Modified: Wed, 20 May 2026 19:00:27 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f580a22501d26e28952ee85653f70663980ab45953d0cfcbef50694db04d6`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4511ea5948cbca6aef9d7517e123f726b38c8a0eb9c947c2c4f6d7f54e0d88`  
		Last Modified: Wed, 20 May 2026 19:00:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14`

```console
$ docker pull nats@sha256:ddb480f4b97d90f183123e96bbc7c96ab2a126883f7a380531cc208fc8ba9ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14` - linux; amd64

```console
$ docker pull nats@sha256:e3975ae3c259e07dc00b126ef5cf0570d4b9c1995de29c286314a8c94185f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6842884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a858e4f7943893e252bc83397a059d23acc4bba8780c464abee2a7ca16c7445`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:09:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:09:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:09:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:09:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:09:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:09:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7c3bd50a747eaeeb10f95fa519304e5d461cdf7abfea618bd20f6082ff6662a0`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.8 MB (6842374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de808d2a465a42d8c366fe6a0444bfe0126b0deb5df083e28a6ab5da8f23bd`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:23bcf4e2ed2926d96eea36a58166f435554c690541005e998f5d616db30e45f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507326c78aca26a49af5c475ba8b2e2af04ec277a225d3045596713d6ff37309`

```dockerfile
```

-	Layers:
	-	`sha256:f040bfc84eb63a5f18c5215d1a0b547ad6574a095bc308ed0abb87f0e078fd56`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fec1423119b8e851f070386e125c5834183df6ef68cdf380acc9baeea48437c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddea1197c216967009e6e1e0c22c06b810ad0056259b9aa2d0d4c9116f36a3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:07:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:07:34 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:07:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:07:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:07:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:07:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bf1819a534ff3a05b2ec4b423942e9e9c1db524f8abdf07d0916cc9d7977e963`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.6 MB (6559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b10a626663e338c0bb1dfea4c11c6b38d61cac3eeefbe2918057535336ac6b`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:cf5f1e96a51a5bb900685df5ea819d0c6d2fa448635ed02772654ff2b5d22c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c00aaa6a70cd7d0e9305def7746345074e4a5081f236f2b44b9b79e39464d8`

```dockerfile
```

-	Layers:
	-	`sha256:03d05c80b133e625e60b7cb05cef59b26ce5d7adb0a442fffea4584ab6416a79`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:a34dfd5d492771b140674e5c141027c58b58e4e2cd947f6eba0a5a31e2632e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6550603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093ad3956c6655a303f62a9ce264a18c45b4b863cb96efd842248173c0a606f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:79835d220a3efcc4d8184ca74b4eca9de6abd447cd214ab6d89fae0fc25d71a9`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.6 MB (6550094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e566e5f57a2c944f69e8bf41c06ce6f58e5e383d02e3811ffbdbca2405a03b`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:f9cea913444f7e8acd3d07f2cd7670cd28468d48a2d2f5941c4b6a9a35e0427a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d7b544c9028dc94601084bc0b26038bd215fd585731ffb843b95c11616848f`

```dockerfile
```

-	Layers:
	-	`sha256:f4cd62261a445f98af038b0cbff3f7054ac217b7e36c0e59d370c436c17999ab`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e554388d79522e92428f0a329dd4024becbe133d93cc298e3b3f19fe769c5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d3e785af72753f053cdbe0d272ae32efdb191b73b6d238882b8515e360e55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3086615f9efa498ae9d2f554e2824bdc11572e36270fa30ae141052e9b88120b`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.2 MB (6205728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a682c8240a063be6edb589f7d09954caa2f0a40d3ebb45eac4234abf6fbc5f6`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:9ab349969a32ee01e8bcb841bb52b6d4ffd7a87a867968b3a8111c830d1f667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57daccc6ef4bf25d89aad9d9d9000209b3ee8c6814ed3ccb744d1db6d5761d6`

```dockerfile
```

-	Layers:
	-	`sha256:f1b2616b1d8419ddadbc195580b24cdab43b59899da9485f8b0fd5f06e928676`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; ppc64le

```console
$ docker pull nats@sha256:112de0b731fdb92a9c813eee3b0f8a816046a6e882307d335aa4f3d6b64ab2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6261173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67383f85c6e3f28202e7d562786c204a63d766d6840532ad193e6d18b1ed707`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 01:10:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 01:10:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 01:10:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 01:10:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 01:10:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 01:10:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eb0e94a8e853f1e2567208a976f6d1cc5ecfaea1d16c87495229884c956736b7`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.3 MB (6260663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50278529f5f5f05ea6ca0fd0219f7a459b697c47991305f9d63d45b1b23495f8`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:a755da6315e498cab6e9870590b2b34fd8157c20891fed667e5ab5e493e0af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67349f6f4539144ad7678f3284335b4772501bcfa7d9770f035e84b2da04f17`

```dockerfile
```

-	Layers:
	-	`sha256:168e5061e0d664166bd9f7f89a8c07fa6f14f5132924faf8e3f3de8a21fc7cc3`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; s390x

```console
$ docker pull nats@sha256:2c9846411d4b6d33497d039dd5106ad38464b748f2a0d9886f84d6cfef669524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbc00e62ab08542eecb29f4ca6bb5907e5ad175fd4eb3d6613ec701209e38a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:08 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67ffc5a82b02d8ffc00056ab8c020a3b83a99b6b77157514635e2e300d167911`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.7 MB (6651485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f52004feacf72864a4f4c42486e43587d4dd67df78fc3e13cefbe7e59186ef`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:ff392c940bafbd3cb3b74113b5c1e489c15df878b322dfcc20b22333ce41080d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d79eb9f583d6a49a5d5181dab00ed84cc7ad774999a71fb342154ff015520c3`

```dockerfile
```

-	Layers:
	-	`sha256:7ee6cf5f9d4c2d0e016b2ff289228a30b182caf91592475b3a30063dd252b252`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:10447eaa252bcfb6c3c80118cac7a3b7d51c9a6498cc26d41dea1f72a29a718a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134088579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa19bee47e781cb629295ccf987910ba8172d206a2c5b755715734337341c77`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:19 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:04a1144166eb5b33184d353a4d7fcf95d121b39915427dc4374067d235aa4fae in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba58bc2ff4cb3ed55b80304b80b9c63f18f2df3aa65906a51c4228a916de113b`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ee7a8195af77f60f35ff2d6b86f9b83c3ea7a0787b41513b6d512a38cfbeb1`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 7.0 MB (7043891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a61086d35b626fb6f16c1e6be5566b2c6cafc605ea3ffd8bb0131f0aa62cd`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09595785c206d9c7108fdd885443f316708faa65baaa5229d4727c90dfeb7890`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49d51a826ee74af6afa6df4d7672be2e6d939ce87c78cc52903605ff9aa79c`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25503378a2c0fd04f5a847805ea1d9dca5b4ab6baef186823953f0b0b69d8a`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-alpine`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.14-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-alpine3.22`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.14-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-linux`

```console
$ docker pull nats@sha256:5199cd3987b4be19f276542ea06d2218ad38a02acce7f78352c4a890feb5aa7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.14-linux` - linux; amd64

```console
$ docker pull nats@sha256:e3975ae3c259e07dc00b126ef5cf0570d4b9c1995de29c286314a8c94185f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6842884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a858e4f7943893e252bc83397a059d23acc4bba8780c464abee2a7ca16c7445`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:09:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:09:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:09:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:09:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:09:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:09:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7c3bd50a747eaeeb10f95fa519304e5d461cdf7abfea618bd20f6082ff6662a0`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.8 MB (6842374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de808d2a465a42d8c366fe6a0444bfe0126b0deb5df083e28a6ab5da8f23bd`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:23bcf4e2ed2926d96eea36a58166f435554c690541005e998f5d616db30e45f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507326c78aca26a49af5c475ba8b2e2af04ec277a225d3045596713d6ff37309`

```dockerfile
```

-	Layers:
	-	`sha256:f040bfc84eb63a5f18c5215d1a0b547ad6574a095bc308ed0abb87f0e078fd56`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fec1423119b8e851f070386e125c5834183df6ef68cdf380acc9baeea48437c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddea1197c216967009e6e1e0c22c06b810ad0056259b9aa2d0d4c9116f36a3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:07:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:07:34 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:07:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:07:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:07:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:07:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bf1819a534ff3a05b2ec4b423942e9e9c1db524f8abdf07d0916cc9d7977e963`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.6 MB (6559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b10a626663e338c0bb1dfea4c11c6b38d61cac3eeefbe2918057535336ac6b`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:cf5f1e96a51a5bb900685df5ea819d0c6d2fa448635ed02772654ff2b5d22c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c00aaa6a70cd7d0e9305def7746345074e4a5081f236f2b44b9b79e39464d8`

```dockerfile
```

-	Layers:
	-	`sha256:03d05c80b133e625e60b7cb05cef59b26ce5d7adb0a442fffea4584ab6416a79`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a34dfd5d492771b140674e5c141027c58b58e4e2cd947f6eba0a5a31e2632e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6550603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093ad3956c6655a303f62a9ce264a18c45b4b863cb96efd842248173c0a606f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:79835d220a3efcc4d8184ca74b4eca9de6abd447cd214ab6d89fae0fc25d71a9`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.6 MB (6550094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e566e5f57a2c944f69e8bf41c06ce6f58e5e383d02e3811ffbdbca2405a03b`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9cea913444f7e8acd3d07f2cd7670cd28468d48a2d2f5941c4b6a9a35e0427a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d7b544c9028dc94601084bc0b26038bd215fd585731ffb843b95c11616848f`

```dockerfile
```

-	Layers:
	-	`sha256:f4cd62261a445f98af038b0cbff3f7054ac217b7e36c0e59d370c436c17999ab`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e554388d79522e92428f0a329dd4024becbe133d93cc298e3b3f19fe769c5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d3e785af72753f053cdbe0d272ae32efdb191b73b6d238882b8515e360e55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3086615f9efa498ae9d2f554e2824bdc11572e36270fa30ae141052e9b88120b`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.2 MB (6205728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a682c8240a063be6edb589f7d09954caa2f0a40d3ebb45eac4234abf6fbc5f6`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9ab349969a32ee01e8bcb841bb52b6d4ffd7a87a867968b3a8111c830d1f667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57daccc6ef4bf25d89aad9d9d9000209b3ee8c6814ed3ccb744d1db6d5761d6`

```dockerfile
```

-	Layers:
	-	`sha256:f1b2616b1d8419ddadbc195580b24cdab43b59899da9485f8b0fd5f06e928676`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:112de0b731fdb92a9c813eee3b0f8a816046a6e882307d335aa4f3d6b64ab2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6261173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67383f85c6e3f28202e7d562786c204a63d766d6840532ad193e6d18b1ed707`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 01:10:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 01:10:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 01:10:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 01:10:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 01:10:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 01:10:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eb0e94a8e853f1e2567208a976f6d1cc5ecfaea1d16c87495229884c956736b7`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.3 MB (6260663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50278529f5f5f05ea6ca0fd0219f7a459b697c47991305f9d63d45b1b23495f8`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a755da6315e498cab6e9870590b2b34fd8157c20891fed667e5ab5e493e0af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67349f6f4539144ad7678f3284335b4772501bcfa7d9770f035e84b2da04f17`

```dockerfile
```

-	Layers:
	-	`sha256:168e5061e0d664166bd9f7f89a8c07fa6f14f5132924faf8e3f3de8a21fc7cc3`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; s390x

```console
$ docker pull nats@sha256:2c9846411d4b6d33497d039dd5106ad38464b748f2a0d9886f84d6cfef669524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbc00e62ab08542eecb29f4ca6bb5907e5ad175fd4eb3d6613ec701209e38a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:08 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67ffc5a82b02d8ffc00056ab8c020a3b83a99b6b77157514635e2e300d167911`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.7 MB (6651485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f52004feacf72864a4f4c42486e43587d4dd67df78fc3e13cefbe7e59186ef`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ff392c940bafbd3cb3b74113b5c1e489c15df878b322dfcc20b22333ce41080d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d79eb9f583d6a49a5d5181dab00ed84cc7ad774999a71fb342154ff015520c3`

```dockerfile
```

-	Layers:
	-	`sha256:7ee6cf5f9d4c2d0e016b2ff289228a30b182caf91592475b3a30063dd252b252`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-nanoserver`

```console
$ docker pull nats@sha256:2b6839a0f95f211d134087d05f1c2b6985ffe28ad04ab158bedd18b7430ac79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:10447eaa252bcfb6c3c80118cac7a3b7d51c9a6498cc26d41dea1f72a29a718a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134088579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa19bee47e781cb629295ccf987910ba8172d206a2c5b755715734337341c77`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:19 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:04a1144166eb5b33184d353a4d7fcf95d121b39915427dc4374067d235aa4fae in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba58bc2ff4cb3ed55b80304b80b9c63f18f2df3aa65906a51c4228a916de113b`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ee7a8195af77f60f35ff2d6b86f9b83c3ea7a0787b41513b6d512a38cfbeb1`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 7.0 MB (7043891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a61086d35b626fb6f16c1e6be5566b2c6cafc605ea3ffd8bb0131f0aa62cd`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09595785c206d9c7108fdd885443f316708faa65baaa5229d4727c90dfeb7890`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49d51a826ee74af6afa6df4d7672be2e6d939ce87c78cc52903605ff9aa79c`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25503378a2c0fd04f5a847805ea1d9dca5b4ab6baef186823953f0b0b69d8a`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:2b6839a0f95f211d134087d05f1c2b6985ffe28ad04ab158bedd18b7430ac79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:10447eaa252bcfb6c3c80118cac7a3b7d51c9a6498cc26d41dea1f72a29a718a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134088579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa19bee47e781cb629295ccf987910ba8172d206a2c5b755715734337341c77`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:19 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:04a1144166eb5b33184d353a4d7fcf95d121b39915427dc4374067d235aa4fae in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba58bc2ff4cb3ed55b80304b80b9c63f18f2df3aa65906a51c4228a916de113b`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ee7a8195af77f60f35ff2d6b86f9b83c3ea7a0787b41513b6d512a38cfbeb1`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 7.0 MB (7043891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a61086d35b626fb6f16c1e6be5566b2c6cafc605ea3ffd8bb0131f0aa62cd`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09595785c206d9c7108fdd885443f316708faa65baaa5229d4727c90dfeb7890`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49d51a826ee74af6afa6df4d7672be2e6d939ce87c78cc52903605ff9aa79c`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25503378a2c0fd04f5a847805ea1d9dca5b4ab6baef186823953f0b0b69d8a`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-scratch`

```console
$ docker pull nats@sha256:5199cd3987b4be19f276542ea06d2218ad38a02acce7f78352c4a890feb5aa7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.14-scratch` - linux; amd64

```console
$ docker pull nats@sha256:e3975ae3c259e07dc00b126ef5cf0570d4b9c1995de29c286314a8c94185f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6842884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a858e4f7943893e252bc83397a059d23acc4bba8780c464abee2a7ca16c7445`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:09:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:09:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:09:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:09:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:09:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:09:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7c3bd50a747eaeeb10f95fa519304e5d461cdf7abfea618bd20f6082ff6662a0`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.8 MB (6842374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de808d2a465a42d8c366fe6a0444bfe0126b0deb5df083e28a6ab5da8f23bd`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:23bcf4e2ed2926d96eea36a58166f435554c690541005e998f5d616db30e45f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507326c78aca26a49af5c475ba8b2e2af04ec277a225d3045596713d6ff37309`

```dockerfile
```

-	Layers:
	-	`sha256:f040bfc84eb63a5f18c5215d1a0b547ad6574a095bc308ed0abb87f0e078fd56`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fec1423119b8e851f070386e125c5834183df6ef68cdf380acc9baeea48437c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddea1197c216967009e6e1e0c22c06b810ad0056259b9aa2d0d4c9116f36a3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:07:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:07:34 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:07:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:07:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:07:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:07:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bf1819a534ff3a05b2ec4b423942e9e9c1db524f8abdf07d0916cc9d7977e963`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.6 MB (6559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b10a626663e338c0bb1dfea4c11c6b38d61cac3eeefbe2918057535336ac6b`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:cf5f1e96a51a5bb900685df5ea819d0c6d2fa448635ed02772654ff2b5d22c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c00aaa6a70cd7d0e9305def7746345074e4a5081f236f2b44b9b79e39464d8`

```dockerfile
```

-	Layers:
	-	`sha256:03d05c80b133e625e60b7cb05cef59b26ce5d7adb0a442fffea4584ab6416a79`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a34dfd5d492771b140674e5c141027c58b58e4e2cd947f6eba0a5a31e2632e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6550603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093ad3956c6655a303f62a9ce264a18c45b4b863cb96efd842248173c0a606f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:79835d220a3efcc4d8184ca74b4eca9de6abd447cd214ab6d89fae0fc25d71a9`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.6 MB (6550094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e566e5f57a2c944f69e8bf41c06ce6f58e5e383d02e3811ffbdbca2405a03b`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9cea913444f7e8acd3d07f2cd7670cd28468d48a2d2f5941c4b6a9a35e0427a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d7b544c9028dc94601084bc0b26038bd215fd585731ffb843b95c11616848f`

```dockerfile
```

-	Layers:
	-	`sha256:f4cd62261a445f98af038b0cbff3f7054ac217b7e36c0e59d370c436c17999ab`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e554388d79522e92428f0a329dd4024becbe133d93cc298e3b3f19fe769c5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d3e785af72753f053cdbe0d272ae32efdb191b73b6d238882b8515e360e55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3086615f9efa498ae9d2f554e2824bdc11572e36270fa30ae141052e9b88120b`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.2 MB (6205728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a682c8240a063be6edb589f7d09954caa2f0a40d3ebb45eac4234abf6fbc5f6`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9ab349969a32ee01e8bcb841bb52b6d4ffd7a87a867968b3a8111c830d1f667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57daccc6ef4bf25d89aad9d9d9000209b3ee8c6814ed3ccb744d1db6d5761d6`

```dockerfile
```

-	Layers:
	-	`sha256:f1b2616b1d8419ddadbc195580b24cdab43b59899da9485f8b0fd5f06e928676`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:112de0b731fdb92a9c813eee3b0f8a816046a6e882307d335aa4f3d6b64ab2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6261173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67383f85c6e3f28202e7d562786c204a63d766d6840532ad193e6d18b1ed707`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 01:10:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 01:10:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 01:10:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 01:10:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 01:10:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 01:10:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eb0e94a8e853f1e2567208a976f6d1cc5ecfaea1d16c87495229884c956736b7`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.3 MB (6260663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50278529f5f5f05ea6ca0fd0219f7a459b697c47991305f9d63d45b1b23495f8`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a755da6315e498cab6e9870590b2b34fd8157c20891fed667e5ab5e493e0af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67349f6f4539144ad7678f3284335b4772501bcfa7d9770f035e84b2da04f17`

```dockerfile
```

-	Layers:
	-	`sha256:168e5061e0d664166bd9f7f89a8c07fa6f14f5132924faf8e3f3de8a21fc7cc3`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; s390x

```console
$ docker pull nats@sha256:2c9846411d4b6d33497d039dd5106ad38464b748f2a0d9886f84d6cfef669524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbc00e62ab08542eecb29f4ca6bb5907e5ad175fd4eb3d6613ec701209e38a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:08 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67ffc5a82b02d8ffc00056ab8c020a3b83a99b6b77157514635e2e300d167911`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.7 MB (6651485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f52004feacf72864a4f4c42486e43587d4dd67df78fc3e13cefbe7e59186ef`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ff392c940bafbd3cb3b74113b5c1e489c15df878b322dfcc20b22333ce41080d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d79eb9f583d6a49a5d5181dab00ed84cc7ad774999a71fb342154ff015520c3`

```dockerfile
```

-	Layers:
	-	`sha256:7ee6cf5f9d4c2d0e016b2ff289228a30b182caf91592475b3a30063dd252b252`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-windowsservercore`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.1`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.14.1-alpine`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.14.1-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.1-alpine3.22`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.14.1-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.1-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.1-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.1-linux`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.14.1-nanoserver`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.14.1-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.14.1-scratch`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.14.1-windowsservercore`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14.1-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.1-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14.1-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:ea17b9b7f74279b9239cf65e5786c0133e9a7c353bf218d29004abf2e7a33181
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:4c516667ffae4977a0b4ee1d8caa5b663a0d147b66c6b2adc8ee8f3e23728bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133130b2f2f46568f11546ffef920fccb739e99fd733ef11ea43fc1737887c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:17 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887181943c337b002058eb52d1b08afbc55add7c29a34ac80e3949090e15495`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 7.3 MB (7294060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070bfd7422a373dc1b206300e1798aef404bf1bac5a04a3293b33f5468a167e`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a08ddee9fc679f6a40d1ca0c325ec632bebcbb19437245764df5d7ccb6e0d`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:16deabb6f9a013834b95f04987ebab3d889f6704db15b71e13e10a4109b2e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0fdb19df33d866a3c0b19c2d8aa933518ea4afc5b2f7562f2fd9364bb805ec`

```dockerfile
```

-	Layers:
	-	`sha256:650380b0910269f4395d628fbfafe98d4c910cc7a775ff48fa5093aaddc18b1f`  
		Last Modified: Wed, 20 May 2026 18:37:22 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:32e7eb3bde61b1a81ba030cf21530f82b3713f20585f14da348ed9ff0099cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10540472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1b400cc41fb9599883d47ee0cc98f26d14432cafaa79d7b00c36500c3be581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac441e30d31da40cce92ca13be29a2ec33b8e530c12f39c4e6e6f821d36fa5f7`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7032117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efc9734efaa0feb255b7c30b046fb56094635c7d947db2f21f7a873a06b52a`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e8fdb1f5ad9c517ef1795cc413d10f4304bac0bfacca20197b1324ceed658bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67da2ba5e6d5168c0687521d71e8357c05504026864365687620573485a04e0`

```dockerfile
```

-	Layers:
	-	`sha256:63de3f19bc13cbd3dc2f28506681e74ef898d6cddd4ed65551521f9d641ff6b5`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8805cf2aaa214d58393f7373011c4fe330f5225fb9bc4da6d715a6ab72ff8dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10246493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32278cb7a1bf5e3ea24f7381d52c844e152750efbf7684af40245538a2fadaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:35:40 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:35:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:35:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e43a7f3a2149acbd98329815e7e03d9dcf933d2131db6f8e1eecd1c01e173`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 7.0 MB (7019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588069c44453627769cbea386971dc510fa0a2a33fc33bc21795cbe4c6ceeb2e`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9213cf8ea08c3ce1080672b9ea4c12034482854a1829a814ec22933ea91379a0`  
		Last Modified: Wed, 20 May 2026 18:35:44 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83439ca6685120afbf799cb62bebb64b76d3419bd2523ae781dfad0b8bd8db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f56fa87064674ea90080bd544ca88fd1b1f257088b93998a8cd46405b6249c`

```dockerfile
```

-	Layers:
	-	`sha256:22deddd2f98e84c9bc37c96058b3e88416465a5ea1004b4985cef2385de5a8be`  
		Last Modified: Wed, 20 May 2026 18:35:45 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abc668a25359714d7320be16684a7a6096d82a6d41aa9fbb4275c02f3fb1e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c04c7a60cc127abb4b03f7f7593fb48cd0124f4f2cd959996fdcb5caba71e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:37:01 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:37:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:37:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:37:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b89c7be0c2d2557967711fd66cb73b3b64361381d066e02f0b52b2abeedd6b9`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 6.6 MB (6648233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1bf5ee681da0d7929bf7d0e36bf5d24df48f214a25c32a7692f9fd0bc5eab`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2e67e1deca529e76612c525c5a8e12050d9ec84c3691673953e51573c1e653`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5ae7b0317944de344d87247e9cb05a11dcd4f796e1800294193d7b60f43c9d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059f595926bbcc76e88f995c69a532e5bfdb37e53db7d9cbd26077b9a0f52d1`

```dockerfile
```

-	Layers:
	-	`sha256:a10a07e60572ceb3113b276c9a02c5aa46bf940b8f2a491e7064608fcac2409c`  
		Last Modified: Wed, 20 May 2026 18:37:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:7c13d10c1f7169aaedc2ac8ecbc1f431dda7e906455b836d09a14b3b948f3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10448793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa266dd5df001f7f566ffb0c8c8acff2de160efa06508788758a4e3022c8e98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:39:54 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:39:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:39:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:39:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe06b0c545d8e510a8131fe2984aa46a7c4d7502148ce8f2e94df5ffeed78f`  
		Last Modified: Wed, 20 May 2026 18:40:02 GMT  
		Size: 6.7 MB (6711165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c6e5710602d0c65abfcc3a4aac8676e3cd1f849d5967bee0654b0ec045abe`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fcc4ed5f0f4848feb91f0e5c409cb87bfd693a7056f2c0e574dbf0fc8ff4ab`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7878f9d371c5d9227beef40f16b5dfd6d37465bab0104f835171af841d4c4a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a1ee27b4ce5d60016cbff052995f2dbab1c7c6c61dcf79e2f75cbb1430fbad`

```dockerfile
```

-	Layers:
	-	`sha256:c27fc7351e2a880436edb13f3b1eaf0c5d83b4ec4a761386db3f8a0e0e8642a5`  
		Last Modified: Wed, 20 May 2026 18:40:01 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:458d20eff2bdbc011304724399fc06b3db7dae7c95d0c806969fc503389a70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10757148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a7df6776ecf8e0df1b73510a6014c1f519a3c9692cd787d8568dd8021d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 18:48:37 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:48:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0bdd20ad850e66a484dcb126f6ce610079520b56d9e8518d099e0864ab8171a1' ;;     armhf) natsArch='arm6'; sha256='261accad99256ee7c7e320cac1df4fbb7fe11c28e324a3e8ae15738b6d4f0e35' ;;     armv7) natsArch='arm7'; sha256='15c7a984f586891bd573cf8bfa28aa453786dd7e42fa0315b2c7a85c2bdfef47' ;;     x86_64) natsArch='amd64'; sha256='4638c389af67d4c747f5b3e6a9d363bfe8f6b86de37d7c4ee3a36b283a5c2ce2' ;;     x86) natsArch='386'; sha256='851034aefaa2540951e9c6c86d144a407478da27e941f0c662f419ae1993c472' ;;     s390x) natsArch='s390x'; sha256='fefbeff1d6e259dfbb0a4514501a369d8c57e9d856fcc392c4da3c242162ee35' ;;     ppc64le) natsArch='ppc64le'; sha256='784c75d2c0430ff0dada016f36bc0ef8fef56e2117df8170eb33a37c65f81365' ;;     loong64) natsArch='loong64'; sha256='3cfb6bee7ec72c722b6480425edd87e96ca16fe76b31f5b8c43fae5d033c8fdf' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 20 May 2026 18:48:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 20 May 2026 18:48:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 18:48:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 20 May 2026 18:48:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:48:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728aea4976117b7918cb9446c013c273cae16aa21337089d91cbd93761d10ae5`  
		Last Modified: Wed, 20 May 2026 18:49:10 GMT  
		Size: 7.1 MB (7102303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e102ba28952cc8bf83cffaefb3ec4b38d56cd736120ece8c71362ff603fd09b`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec22f8c91bd1e1b2e7f49773754ab16299137dd3226c8bb660a538d249364ae6`  
		Last Modified: Wed, 20 May 2026 18:49:08 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:38a69833b514d10d0b925fa5c4639cb5d17abe985f2b30699a0f305324397aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc57189208991582e7a0262e60b1415e19ac3919981144973c3d19428e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:ccc40928ae38a1bd914e972d9acbe81dbc2e36b6132cee1761b8e20e7dda2db5`  
		Last Modified: Wed, 20 May 2026 18:49:09 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:ddb480f4b97d90f183123e96bbc7c96ab2a126883f7a380531cc208fc8ba9ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5139; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:e3975ae3c259e07dc00b126ef5cf0570d4b9c1995de29c286314a8c94185f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6842884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a858e4f7943893e252bc83397a059d23acc4bba8780c464abee2a7ca16c7445`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:09:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:09:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:09:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:09:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:09:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:09:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7c3bd50a747eaeeb10f95fa519304e5d461cdf7abfea618bd20f6082ff6662a0`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.8 MB (6842374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de808d2a465a42d8c366fe6a0444bfe0126b0deb5df083e28a6ab5da8f23bd`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:23bcf4e2ed2926d96eea36a58166f435554c690541005e998f5d616db30e45f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507326c78aca26a49af5c475ba8b2e2af04ec277a225d3045596713d6ff37309`

```dockerfile
```

-	Layers:
	-	`sha256:f040bfc84eb63a5f18c5215d1a0b547ad6574a095bc308ed0abb87f0e078fd56`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fec1423119b8e851f070386e125c5834183df6ef68cdf380acc9baeea48437c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddea1197c216967009e6e1e0c22c06b810ad0056259b9aa2d0d4c9116f36a3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:07:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:07:34 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:07:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:07:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:07:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:07:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bf1819a534ff3a05b2ec4b423942e9e9c1db524f8abdf07d0916cc9d7977e963`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.6 MB (6559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b10a626663e338c0bb1dfea4c11c6b38d61cac3eeefbe2918057535336ac6b`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:cf5f1e96a51a5bb900685df5ea819d0c6d2fa448635ed02772654ff2b5d22c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c00aaa6a70cd7d0e9305def7746345074e4a5081f236f2b44b9b79e39464d8`

```dockerfile
```

-	Layers:
	-	`sha256:03d05c80b133e625e60b7cb05cef59b26ce5d7adb0a442fffea4584ab6416a79`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:a34dfd5d492771b140674e5c141027c58b58e4e2cd947f6eba0a5a31e2632e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6550603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093ad3956c6655a303f62a9ce264a18c45b4b863cb96efd842248173c0a606f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:79835d220a3efcc4d8184ca74b4eca9de6abd447cd214ab6d89fae0fc25d71a9`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.6 MB (6550094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e566e5f57a2c944f69e8bf41c06ce6f58e5e383d02e3811ffbdbca2405a03b`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:f9cea913444f7e8acd3d07f2cd7670cd28468d48a2d2f5941c4b6a9a35e0427a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d7b544c9028dc94601084bc0b26038bd215fd585731ffb843b95c11616848f`

```dockerfile
```

-	Layers:
	-	`sha256:f4cd62261a445f98af038b0cbff3f7054ac217b7e36c0e59d370c436c17999ab`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e554388d79522e92428f0a329dd4024becbe133d93cc298e3b3f19fe769c5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d3e785af72753f053cdbe0d272ae32efdb191b73b6d238882b8515e360e55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3086615f9efa498ae9d2f554e2824bdc11572e36270fa30ae141052e9b88120b`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.2 MB (6205728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a682c8240a063be6edb589f7d09954caa2f0a40d3ebb45eac4234abf6fbc5f6`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:9ab349969a32ee01e8bcb841bb52b6d4ffd7a87a867968b3a8111c830d1f667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57daccc6ef4bf25d89aad9d9d9000209b3ee8c6814ed3ccb744d1db6d5761d6`

```dockerfile
```

-	Layers:
	-	`sha256:f1b2616b1d8419ddadbc195580b24cdab43b59899da9485f8b0fd5f06e928676`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:112de0b731fdb92a9c813eee3b0f8a816046a6e882307d335aa4f3d6b64ab2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6261173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67383f85c6e3f28202e7d562786c204a63d766d6840532ad193e6d18b1ed707`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 01:10:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 01:10:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 01:10:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 01:10:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 01:10:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 01:10:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eb0e94a8e853f1e2567208a976f6d1cc5ecfaea1d16c87495229884c956736b7`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.3 MB (6260663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50278529f5f5f05ea6ca0fd0219f7a459b697c47991305f9d63d45b1b23495f8`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a755da6315e498cab6e9870590b2b34fd8157c20891fed667e5ab5e493e0af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67349f6f4539144ad7678f3284335b4772501bcfa7d9770f035e84b2da04f17`

```dockerfile
```

-	Layers:
	-	`sha256:168e5061e0d664166bd9f7f89a8c07fa6f14f5132924faf8e3f3de8a21fc7cc3`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:2c9846411d4b6d33497d039dd5106ad38464b748f2a0d9886f84d6cfef669524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbc00e62ab08542eecb29f4ca6bb5907e5ad175fd4eb3d6613ec701209e38a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:08 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67ffc5a82b02d8ffc00056ab8c020a3b83a99b6b77157514635e2e300d167911`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.7 MB (6651485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f52004feacf72864a4f4c42486e43587d4dd67df78fc3e13cefbe7e59186ef`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:ff392c940bafbd3cb3b74113b5c1e489c15df878b322dfcc20b22333ce41080d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d79eb9f583d6a49a5d5181dab00ed84cc7ad774999a71fb342154ff015520c3`

```dockerfile
```

-	Layers:
	-	`sha256:7ee6cf5f9d4c2d0e016b2ff289228a30b182caf91592475b3a30063dd252b252`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:10447eaa252bcfb6c3c80118cac7a3b7d51c9a6498cc26d41dea1f72a29a718a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134088579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa19bee47e781cb629295ccf987910ba8172d206a2c5b755715734337341c77`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:19 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:04a1144166eb5b33184d353a4d7fcf95d121b39915427dc4374067d235aa4fae in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba58bc2ff4cb3ed55b80304b80b9c63f18f2df3aa65906a51c4228a916de113b`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ee7a8195af77f60f35ff2d6b86f9b83c3ea7a0787b41513b6d512a38cfbeb1`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 7.0 MB (7043891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a61086d35b626fb6f16c1e6be5566b2c6cafc605ea3ffd8bb0131f0aa62cd`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09595785c206d9c7108fdd885443f316708faa65baaa5229d4727c90dfeb7890`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49d51a826ee74af6afa6df4d7672be2e6d939ce87c78cc52903605ff9aa79c`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25503378a2c0fd04f5a847805ea1d9dca5b4ab6baef186823953f0b0b69d8a`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:5199cd3987b4be19f276542ea06d2218ad38a02acce7f78352c4a890feb5aa7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:e3975ae3c259e07dc00b126ef5cf0570d4b9c1995de29c286314a8c94185f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6842884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a858e4f7943893e252bc83397a059d23acc4bba8780c464abee2a7ca16c7445`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:09:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:09:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:09:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:09:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:09:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:09:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7c3bd50a747eaeeb10f95fa519304e5d461cdf7abfea618bd20f6082ff6662a0`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.8 MB (6842374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de808d2a465a42d8c366fe6a0444bfe0126b0deb5df083e28a6ab5da8f23bd`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:23bcf4e2ed2926d96eea36a58166f435554c690541005e998f5d616db30e45f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507326c78aca26a49af5c475ba8b2e2af04ec277a225d3045596713d6ff37309`

```dockerfile
```

-	Layers:
	-	`sha256:f040bfc84eb63a5f18c5215d1a0b547ad6574a095bc308ed0abb87f0e078fd56`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fec1423119b8e851f070386e125c5834183df6ef68cdf380acc9baeea48437c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddea1197c216967009e6e1e0c22c06b810ad0056259b9aa2d0d4c9116f36a3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:07:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:07:34 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:07:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:07:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:07:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:07:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bf1819a534ff3a05b2ec4b423942e9e9c1db524f8abdf07d0916cc9d7977e963`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.6 MB (6559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b10a626663e338c0bb1dfea4c11c6b38d61cac3eeefbe2918057535336ac6b`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:cf5f1e96a51a5bb900685df5ea819d0c6d2fa448635ed02772654ff2b5d22c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c00aaa6a70cd7d0e9305def7746345074e4a5081f236f2b44b9b79e39464d8`

```dockerfile
```

-	Layers:
	-	`sha256:03d05c80b133e625e60b7cb05cef59b26ce5d7adb0a442fffea4584ab6416a79`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a34dfd5d492771b140674e5c141027c58b58e4e2cd947f6eba0a5a31e2632e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6550603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093ad3956c6655a303f62a9ce264a18c45b4b863cb96efd842248173c0a606f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:79835d220a3efcc4d8184ca74b4eca9de6abd447cd214ab6d89fae0fc25d71a9`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.6 MB (6550094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e566e5f57a2c944f69e8bf41c06ce6f58e5e383d02e3811ffbdbca2405a03b`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9cea913444f7e8acd3d07f2cd7670cd28468d48a2d2f5941c4b6a9a35e0427a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d7b544c9028dc94601084bc0b26038bd215fd585731ffb843b95c11616848f`

```dockerfile
```

-	Layers:
	-	`sha256:f4cd62261a445f98af038b0cbff3f7054ac217b7e36c0e59d370c436c17999ab`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e554388d79522e92428f0a329dd4024becbe133d93cc298e3b3f19fe769c5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d3e785af72753f053cdbe0d272ae32efdb191b73b6d238882b8515e360e55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3086615f9efa498ae9d2f554e2824bdc11572e36270fa30ae141052e9b88120b`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.2 MB (6205728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a682c8240a063be6edb589f7d09954caa2f0a40d3ebb45eac4234abf6fbc5f6`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:9ab349969a32ee01e8bcb841bb52b6d4ffd7a87a867968b3a8111c830d1f667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57daccc6ef4bf25d89aad9d9d9000209b3ee8c6814ed3ccb744d1db6d5761d6`

```dockerfile
```

-	Layers:
	-	`sha256:f1b2616b1d8419ddadbc195580b24cdab43b59899da9485f8b0fd5f06e928676`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:112de0b731fdb92a9c813eee3b0f8a816046a6e882307d335aa4f3d6b64ab2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6261173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67383f85c6e3f28202e7d562786c204a63d766d6840532ad193e6d18b1ed707`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 01:10:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 01:10:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 01:10:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 01:10:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 01:10:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 01:10:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eb0e94a8e853f1e2567208a976f6d1cc5ecfaea1d16c87495229884c956736b7`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.3 MB (6260663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50278529f5f5f05ea6ca0fd0219f7a459b697c47991305f9d63d45b1b23495f8`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:a755da6315e498cab6e9870590b2b34fd8157c20891fed667e5ab5e493e0af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67349f6f4539144ad7678f3284335b4772501bcfa7d9770f035e84b2da04f17`

```dockerfile
```

-	Layers:
	-	`sha256:168e5061e0d664166bd9f7f89a8c07fa6f14f5132924faf8e3f3de8a21fc7cc3`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:2c9846411d4b6d33497d039dd5106ad38464b748f2a0d9886f84d6cfef669524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbc00e62ab08542eecb29f4ca6bb5907e5ad175fd4eb3d6613ec701209e38a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:08 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67ffc5a82b02d8ffc00056ab8c020a3b83a99b6b77157514635e2e300d167911`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.7 MB (6651485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f52004feacf72864a4f4c42486e43587d4dd67df78fc3e13cefbe7e59186ef`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:ff392c940bafbd3cb3b74113b5c1e489c15df878b322dfcc20b22333ce41080d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d79eb9f583d6a49a5d5181dab00ed84cc7ad774999a71fb342154ff015520c3`

```dockerfile
```

-	Layers:
	-	`sha256:7ee6cf5f9d4c2d0e016b2ff289228a30b182caf91592475b3a30063dd252b252`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:2b6839a0f95f211d134087d05f1c2b6985ffe28ad04ab158bedd18b7430ac79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:10447eaa252bcfb6c3c80118cac7a3b7d51c9a6498cc26d41dea1f72a29a718a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134088579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa19bee47e781cb629295ccf987910ba8172d206a2c5b755715734337341c77`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:19 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:04a1144166eb5b33184d353a4d7fcf95d121b39915427dc4374067d235aa4fae in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba58bc2ff4cb3ed55b80304b80b9c63f18f2df3aa65906a51c4228a916de113b`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ee7a8195af77f60f35ff2d6b86f9b83c3ea7a0787b41513b6d512a38cfbeb1`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 7.0 MB (7043891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a61086d35b626fb6f16c1e6be5566b2c6cafc605ea3ffd8bb0131f0aa62cd`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09595785c206d9c7108fdd885443f316708faa65baaa5229d4727c90dfeb7890`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49d51a826ee74af6afa6df4d7672be2e6d939ce87c78cc52903605ff9aa79c`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25503378a2c0fd04f5a847805ea1d9dca5b4ab6baef186823953f0b0b69d8a`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:2b6839a0f95f211d134087d05f1c2b6985ffe28ad04ab158bedd18b7430ac79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:10447eaa252bcfb6c3c80118cac7a3b7d51c9a6498cc26d41dea1f72a29a718a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134088579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa19bee47e781cb629295ccf987910ba8172d206a2c5b755715734337341c77`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:22:19 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:04a1144166eb5b33184d353a4d7fcf95d121b39915427dc4374067d235aa4fae in C:\nats-server.exe 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 13 May 2026 00:22:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 May 2026 00:22:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba58bc2ff4cb3ed55b80304b80b9c63f18f2df3aa65906a51c4228a916de113b`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ee7a8195af77f60f35ff2d6b86f9b83c3ea7a0787b41513b6d512a38cfbeb1`  
		Last Modified: Wed, 13 May 2026 00:22:27 GMT  
		Size: 7.0 MB (7043891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a61086d35b626fb6f16c1e6be5566b2c6cafc605ea3ffd8bb0131f0aa62cd`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09595785c206d9c7108fdd885443f316708faa65baaa5229d4727c90dfeb7890`  
		Last Modified: Wed, 13 May 2026 00:22:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa49d51a826ee74af6afa6df4d7672be2e6d939ce87c78cc52903605ff9aa79c`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25503378a2c0fd04f5a847805ea1d9dca5b4ab6baef186823953f0b0b69d8a`  
		Last Modified: Wed, 13 May 2026 00:22:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:5199cd3987b4be19f276542ea06d2218ad38a02acce7f78352c4a890feb5aa7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:e3975ae3c259e07dc00b126ef5cf0570d4b9c1995de29c286314a8c94185f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6842884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a858e4f7943893e252bc83397a059d23acc4bba8780c464abee2a7ca16c7445`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:09:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:09:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:09:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:09:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:09:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:09:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7c3bd50a747eaeeb10f95fa519304e5d461cdf7abfea618bd20f6082ff6662a0`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.8 MB (6842374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de808d2a465a42d8c366fe6a0444bfe0126b0deb5df083e28a6ab5da8f23bd`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:23bcf4e2ed2926d96eea36a58166f435554c690541005e998f5d616db30e45f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507326c78aca26a49af5c475ba8b2e2af04ec277a225d3045596713d6ff37309`

```dockerfile
```

-	Layers:
	-	`sha256:f040bfc84eb63a5f18c5215d1a0b547ad6574a095bc308ed0abb87f0e078fd56`  
		Last Modified: Fri, 01 May 2026 00:09:40 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fec1423119b8e851f070386e125c5834183df6ef68cdf380acc9baeea48437c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddea1197c216967009e6e1e0c22c06b810ad0056259b9aa2d0d4c9116f36a3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:07:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:07:34 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:07:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:07:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:07:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:07:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bf1819a534ff3a05b2ec4b423942e9e9c1db524f8abdf07d0916cc9d7977e963`  
		Last Modified: Thu, 30 Apr 2026 12:42:00 GMT  
		Size: 6.6 MB (6559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b10a626663e338c0bb1dfea4c11c6b38d61cac3eeefbe2918057535336ac6b`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:cf5f1e96a51a5bb900685df5ea819d0c6d2fa448635ed02772654ff2b5d22c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c00aaa6a70cd7d0e9305def7746345074e4a5081f236f2b44b9b79e39464d8`

```dockerfile
```

-	Layers:
	-	`sha256:03d05c80b133e625e60b7cb05cef59b26ce5d7adb0a442fffea4584ab6416a79`  
		Last Modified: Fri, 01 May 2026 00:07:39 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a34dfd5d492771b140674e5c141027c58b58e4e2cd947f6eba0a5a31e2632e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6550603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093ad3956c6655a303f62a9ce264a18c45b4b863cb96efd842248173c0a606f0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:03 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:79835d220a3efcc4d8184ca74b4eca9de6abd447cd214ab6d89fae0fc25d71a9`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.6 MB (6550094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e566e5f57a2c944f69e8bf41c06ce6f58e5e383d02e3811ffbdbca2405a03b`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9cea913444f7e8acd3d07f2cd7670cd28468d48a2d2f5941c4b6a9a35e0427a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d7b544c9028dc94601084bc0b26038bd215fd585731ffb843b95c11616848f`

```dockerfile
```

-	Layers:
	-	`sha256:f4cd62261a445f98af038b0cbff3f7054ac217b7e36c0e59d370c436c17999ab`  
		Last Modified: Fri, 01 May 2026 00:08:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e554388d79522e92428f0a329dd4024becbe133d93cc298e3b3f19fe769c5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d3e785af72753f053cdbe0d272ae32efdb191b73b6d238882b8515e360e55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3086615f9efa498ae9d2f554e2824bdc11572e36270fa30ae141052e9b88120b`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.2 MB (6205728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a682c8240a063be6edb589f7d09954caa2f0a40d3ebb45eac4234abf6fbc5f6`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9ab349969a32ee01e8bcb841bb52b6d4ffd7a87a867968b3a8111c830d1f667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57daccc6ef4bf25d89aad9d9d9000209b3ee8c6814ed3ccb744d1db6d5761d6`

```dockerfile
```

-	Layers:
	-	`sha256:f1b2616b1d8419ddadbc195580b24cdab43b59899da9485f8b0fd5f06e928676`  
		Last Modified: Fri, 01 May 2026 00:08:50 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:112de0b731fdb92a9c813eee3b0f8a816046a6e882307d335aa4f3d6b64ab2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6261173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67383f85c6e3f28202e7d562786c204a63d766d6840532ad193e6d18b1ed707`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 01:10:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 01:10:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 01:10:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 01:10:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 01:10:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 01:10:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eb0e94a8e853f1e2567208a976f6d1cc5ecfaea1d16c87495229884c956736b7`  
		Last Modified: Thu, 30 Apr 2026 12:41:56 GMT  
		Size: 6.3 MB (6260663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50278529f5f5f05ea6ca0fd0219f7a459b697c47991305f9d63d45b1b23495f8`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a755da6315e498cab6e9870590b2b34fd8157c20891fed667e5ab5e493e0af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67349f6f4539144ad7678f3284335b4772501bcfa7d9770f035e84b2da04f17`

```dockerfile
```

-	Layers:
	-	`sha256:168e5061e0d664166bd9f7f89a8c07fa6f14f5132924faf8e3f3de8a21fc7cc3`  
		Last Modified: Fri, 01 May 2026 01:10:13 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:2c9846411d4b6d33497d039dd5106ad38464b748f2a0d9886f84d6cfef669524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbc00e62ab08542eecb29f4ca6bb5907e5ad175fd4eb3d6613ec701209e38a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 May 2026 00:08:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 May 2026 00:08:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 May 2026 00:08:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 May 2026 00:08:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:08:08 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 May 2026 00:08:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67ffc5a82b02d8ffc00056ab8c020a3b83a99b6b77157514635e2e300d167911`  
		Last Modified: Thu, 30 Apr 2026 12:41:59 GMT  
		Size: 6.7 MB (6651485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f52004feacf72864a4f4c42486e43587d4dd67df78fc3e13cefbe7e59186ef`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ff392c940bafbd3cb3b74113b5c1e489c15df878b322dfcc20b22333ce41080d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d79eb9f583d6a49a5d5181dab00ed84cc7ad774999a71fb342154ff015520c3`

```dockerfile
```

-	Layers:
	-	`sha256:7ee6cf5f9d4c2d0e016b2ff289228a30b182caf91592475b3a30063dd252b252`  
		Last Modified: Fri, 01 May 2026 00:08:16 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:1ba584aa4a0b9afe4503a0bb74145174a5a8bd168c74991253e74a0f28cb7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:7c0d2cfcb1ac8b9c5c8667631fe266d5058f54979c724dbc779cd1303cf56e41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2e9ee9e3b452a65f51ce4b7daa32d3b40f548b8548d8e18d6af0f98c1a6fd8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 20 May 2026 18:42:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 20 May 2026 18:42:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 20 May 2026 18:42:49 GMT
ENV NATS_SERVER=2.14.1
# Wed, 20 May 2026 18:42:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.1
# Wed, 20 May 2026 18:42:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.1/nats-server-v2.14.1-windows-amd64.zip
# Wed, 20 May 2026 18:42:55 GMT
ENV NATS_SERVER_SHASUM=fb7ddfdde7da0ce89a5174c00b0f7fa9d559ee88c6de638c681b464d35e7caca
# Wed, 20 May 2026 18:44:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 20 May 2026 18:44:38 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 20 May 2026 18:44:39 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 20 May 2026 18:44:40 GMT
EXPOSE 4222 6222 8222
# Wed, 20 May 2026 18:44:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 May 2026 18:44:44 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ff9541aea3e55bd746462fb4c6e57da81839bbdd92cde8c45bec531dc275c949`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaeb80d5acbf745ec935e19b9c27aac2c1c36569184a441931640832febb401`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53700d3104e235624a186296ebdbc80307001a56022c9d7a56ca8e8441f1352e`  
		Last Modified: Wed, 20 May 2026 18:44:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698b50a4704844bff262f3486b8d21762a0b2216da94ee49cf3304647a202cf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39739d4a0333d45798f9c82521d794f7861019e48fcbfc35cec644df0ae2a4bf`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785912cbc50e52449bd79d36df3b0b1c35e93f26131aeb601005aa38d99d9f2`  
		Last Modified: Wed, 20 May 2026 18:44:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ecfff99aabce085a608a58a3bc33d019a6c6a474f26cd2f037294ab00c29d`  
		Last Modified: Wed, 20 May 2026 18:44:51 GMT  
		Size: 501.6 KB (501598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653bb3e0442eb7d700abb5d1a972abb676d295a6e84793deb25232914a8e833e`  
		Last Modified: Wed, 20 May 2026 18:44:53 GMT  
		Size: 7.4 MB (7397859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d62953cb63a3accb3782436a9739838d80e2f9610ceac2e47628cc18600fe`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7ba9d33ea88ed49cf0a5cf22fe293c829f1ad64c930e440993b2cb04a3e59a`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd31c298d20b844c00bdce2ffe2a2370b1d271d45448caa64c2c4c9817afcf`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf0d23ad307ba86365cfda67df65a63a9b427078a3ba2715c22735719e8dd0`  
		Last Modified: Wed, 20 May 2026 18:44:48 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
