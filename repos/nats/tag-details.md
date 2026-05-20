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
$ docker pull nats@sha256:df3dbf7615519c64c1ecf5bff1811e0f1349e980e12cf8edac882a53cf3f9dd9
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
$ docker pull nats@sha256:4e4b6c6da8e5dd1c1972aef235279bb99a4554e3277969c25baf06fe75bf3a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11111423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aa95f5acd85535217858bde3f513b2fd61fcded722bdd5d17bb9d89f124eb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b74c94101f0c98ee2c3a1cfe1857a9d00f6d49ce060aac8c3e709731ff6e6c`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 7.3 MB (7302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1171202a810bee209cebae3b516e5dc187466c7efada92079b4cb6da26cc2196`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c58df7044a7df1b6d31a8bff11256dc9480ccd2f85f73edd8393509074d239`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:603015575bf6c3db29393d6ebdf202853ed9636544435f710b2ca3c09536a075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b2bea654035fe919b77ca44ff2adc24191ed65e513b5046faeb2ffb325b5c`

```dockerfile
```

-	Layers:
	-	`sha256:4f302bf75b042b6174b0022d5f48276cef4a2d88e48c27eead53470b13c0d940`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:f50039ea7bec9263cf0a5e88f88d07fd6ebdce50aa9b135611f858acd512f2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10526198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5883c39c5192e03c75b4224b245435c9d6161e83fe57b250935914bd24001668`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccac10855b16bbd9dacf92801d18f2dcabc07188eeffa283aeeaf3f75d832ce`  
		Last Modified: Thu, 30 Apr 2026 23:41:29 GMT  
		Size: 7.0 MB (7017844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbe36b4e25cffbd5ff5634a3fbd1b13a52d111c40121037c010104f6108763`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c11d0705e172884bff3c4d474533693e7de0fa05a5917a78d773a5de329d0`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6471a93f16c111840eacd768e23308cdf960a1cfe889095d78003195e0a0ea6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecff6d4ed848b72ba06ee95a83bd748bd4ca11c6a640da4e12694ac5179e87`

```dockerfile
```

-	Layers:
	-	`sha256:d3bff562dcf6b3117fa78f4a3e590eee7581451e02a99962b05600f583a9cf27`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e9297bbd9fb68cd33a16528c1571b4dafe2dd9ab4142ec024db5ee531ddc68da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10231865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f606a353fc4e59f45057730ace4c11a67caf47eff4f28e41b42b788d8c2414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c367a285a39c8c8c79b4ea0aa7c6247702d54f43f100dd5c3ddbd51c94d3211`  
		Last Modified: Thu, 30 Apr 2026 23:41:35 GMT  
		Size: 7.0 MB (7005064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117013b561496f590f9a60f99c816fe4a564bf0889f6e0df758ada57c96d4e6d`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963d6d4f8ca7ced9d60d1ad7d51774145a90f68ef921fe87ead7831bf25f4bea`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:370298f66cb1801078ab77ec09d0abe92e1c78e845edcbf19512b2f7fd142d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca1a27ff1c3c7b822bd6661b9c47440a8e25f7b4b9cd588c4c3c801ac6451b6`

```dockerfile
```

-	Layers:
	-	`sha256:b570c31a499e86a57fa446b3882375a52d71cc1f961560ff9e1ae810a4efff8b`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d12972d669f1b377199d2741e1fa077ea1168ce25e2c42404f250313a187fe43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eedd13f74e4fec45f3a450d999030f19561f09cfdd980981bbc3a63f0b4cd7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:39 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402c5214fc465210f9c99ad940c17598d6c6af48826c7eb608e07ae485a3e588`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 6.7 MB (6667294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18810920ce9ca341b83ab1017aef4513c4174d891f67342d611c5f3bbda38999`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794d09af1fbaa55736af3f4e2575cea602bd620f628f9e9b546f10970a504934`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:740ee1c9829ccceb669d434cb446164b4b61620f027a57838adf0b32213a1a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a48f299143dbcbdb7d18a8680dc39a2c782baecb38582281887840bab6ca165`

```dockerfile
```

-	Layers:
	-	`sha256:b926ca76b9cf11b2e4ffad4954b37d9fe5b9f4884e5d7fb6c57adb38e84b9a1e`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 15.6 KB (15555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3edda2d951ada7baee76eac3997620987fd3b6ad34abf3b3aeafb4a33d23d47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10458042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c140c21478922b87a2c72b28bd2c0f8c5503c54edc400ab38da1761ca0396c8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:18:52 GMT
ENV NATS_SERVER=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 01 May 2026 00:18:53 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 00:18:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47da398408150920ce8738775297259fe6972d60691a7bd593a28f145b641ef7`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 6.7 MB (6720417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e284a50fe36dcd81f24a73cf5ff5bfe4361b05c60af1c49247d6876489ebdd77`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b453cbccc82afdd9cb5ca438319699b9a61c0fbe5cca06a89fb0a818535827`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:927bcfc16a9e30312116c9c098acc4ed1f96d59ece262eedec4dcc6f7791f494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4306275a207ecd844610df04fafdf166bc2d50d693f22c9adea013222821e7`

```dockerfile
```

-	Layers:
	-	`sha256:fef755e27c5c797a2fd43121851e5482553e3c71c07f36853f09346ec055a853`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:39a52f21d83100719820a826546974edb5b9cd196bda48644d6bde9955650bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10765798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d57f91b93856a000a606780ec5363bc1eb9fb5a2e11112703d73d6e2cfe151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:02 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2085d200b4339b2fc1f02d3ff2827df89f8e4de23b30c3a01197cb364b6e077`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 7.1 MB (7110955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dd256e0fb0cd7e8b86422d79adf837656f750a9ef09f0f36a340664e797d66`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9c615faf9438fa6dc56c180f588bd2e8c3452bbb70bc934ae5e478c052a4c4`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4d12d33eb8b4b9a3886edda118f27a14fab07b1ddfd21129db90309db7b7e483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffc7fca774a22b7dbba927d7c8965de3a26790e226cc50a5ed1fd3bff355aa9`

```dockerfile
```

-	Layers:
	-	`sha256:3313afa82fcfd90aaae86adae7b450d6d5bc98452781ead8d7734b255d058565`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:df3dbf7615519c64c1ecf5bff1811e0f1349e980e12cf8edac882a53cf3f9dd9
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
$ docker pull nats@sha256:4e4b6c6da8e5dd1c1972aef235279bb99a4554e3277969c25baf06fe75bf3a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11111423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aa95f5acd85535217858bde3f513b2fd61fcded722bdd5d17bb9d89f124eb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b74c94101f0c98ee2c3a1cfe1857a9d00f6d49ce060aac8c3e709731ff6e6c`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 7.3 MB (7302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1171202a810bee209cebae3b516e5dc187466c7efada92079b4cb6da26cc2196`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c58df7044a7df1b6d31a8bff11256dc9480ccd2f85f73edd8393509074d239`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:603015575bf6c3db29393d6ebdf202853ed9636544435f710b2ca3c09536a075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b2bea654035fe919b77ca44ff2adc24191ed65e513b5046faeb2ffb325b5c`

```dockerfile
```

-	Layers:
	-	`sha256:4f302bf75b042b6174b0022d5f48276cef4a2d88e48c27eead53470b13c0d940`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:f50039ea7bec9263cf0a5e88f88d07fd6ebdce50aa9b135611f858acd512f2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10526198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5883c39c5192e03c75b4224b245435c9d6161e83fe57b250935914bd24001668`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccac10855b16bbd9dacf92801d18f2dcabc07188eeffa283aeeaf3f75d832ce`  
		Last Modified: Thu, 30 Apr 2026 23:41:29 GMT  
		Size: 7.0 MB (7017844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbe36b4e25cffbd5ff5634a3fbd1b13a52d111c40121037c010104f6108763`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c11d0705e172884bff3c4d474533693e7de0fa05a5917a78d773a5de329d0`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6471a93f16c111840eacd768e23308cdf960a1cfe889095d78003195e0a0ea6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecff6d4ed848b72ba06ee95a83bd748bd4ca11c6a640da4e12694ac5179e87`

```dockerfile
```

-	Layers:
	-	`sha256:d3bff562dcf6b3117fa78f4a3e590eee7581451e02a99962b05600f583a9cf27`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:e9297bbd9fb68cd33a16528c1571b4dafe2dd9ab4142ec024db5ee531ddc68da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10231865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f606a353fc4e59f45057730ace4c11a67caf47eff4f28e41b42b788d8c2414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c367a285a39c8c8c79b4ea0aa7c6247702d54f43f100dd5c3ddbd51c94d3211`  
		Last Modified: Thu, 30 Apr 2026 23:41:35 GMT  
		Size: 7.0 MB (7005064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117013b561496f590f9a60f99c816fe4a564bf0889f6e0df758ada57c96d4e6d`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963d6d4f8ca7ced9d60d1ad7d51774145a90f68ef921fe87ead7831bf25f4bea`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:370298f66cb1801078ab77ec09d0abe92e1c78e845edcbf19512b2f7fd142d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca1a27ff1c3c7b822bd6661b9c47440a8e25f7b4b9cd588c4c3c801ac6451b6`

```dockerfile
```

-	Layers:
	-	`sha256:b570c31a499e86a57fa446b3882375a52d71cc1f961560ff9e1ae810a4efff8b`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d12972d669f1b377199d2741e1fa077ea1168ce25e2c42404f250313a187fe43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eedd13f74e4fec45f3a450d999030f19561f09cfdd980981bbc3a63f0b4cd7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:39 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402c5214fc465210f9c99ad940c17598d6c6af48826c7eb608e07ae485a3e588`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 6.7 MB (6667294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18810920ce9ca341b83ab1017aef4513c4174d891f67342d611c5f3bbda38999`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794d09af1fbaa55736af3f4e2575cea602bd620f628f9e9b546f10970a504934`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:740ee1c9829ccceb669d434cb446164b4b61620f027a57838adf0b32213a1a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a48f299143dbcbdb7d18a8680dc39a2c782baecb38582281887840bab6ca165`

```dockerfile
```

-	Layers:
	-	`sha256:b926ca76b9cf11b2e4ffad4954b37d9fe5b9f4884e5d7fb6c57adb38e84b9a1e`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 15.6 KB (15555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:3edda2d951ada7baee76eac3997620987fd3b6ad34abf3b3aeafb4a33d23d47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10458042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c140c21478922b87a2c72b28bd2c0f8c5503c54edc400ab38da1761ca0396c8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:18:52 GMT
ENV NATS_SERVER=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 01 May 2026 00:18:53 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 00:18:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47da398408150920ce8738775297259fe6972d60691a7bd593a28f145b641ef7`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 6.7 MB (6720417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e284a50fe36dcd81f24a73cf5ff5bfe4361b05c60af1c49247d6876489ebdd77`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b453cbccc82afdd9cb5ca438319699b9a61c0fbe5cca06a89fb0a818535827`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:927bcfc16a9e30312116c9c098acc4ed1f96d59ece262eedec4dcc6f7791f494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4306275a207ecd844610df04fafdf166bc2d50d693f22c9adea013222821e7`

```dockerfile
```

-	Layers:
	-	`sha256:fef755e27c5c797a2fd43121851e5482553e3c71c07f36853f09346ec055a853`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:39a52f21d83100719820a826546974edb5b9cd196bda48644d6bde9955650bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10765798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d57f91b93856a000a606780ec5363bc1eb9fb5a2e11112703d73d6e2cfe151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:02 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2085d200b4339b2fc1f02d3ff2827df89f8e4de23b30c3a01197cb364b6e077`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 7.1 MB (7110955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dd256e0fb0cd7e8b86422d79adf837656f750a9ef09f0f36a340664e797d66`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9c615faf9438fa6dc56c180f588bd2e8c3452bbb70bc934ae5e478c052a4c4`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4d12d33eb8b4b9a3886edda118f27a14fab07b1ddfd21129db90309db7b7e483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffc7fca774a22b7dbba927d7c8965de3a26790e226cc50a5ed1fd3bff355aa9`

```dockerfile
```

-	Layers:
	-	`sha256:3313afa82fcfd90aaae86adae7b450d6d5bc98452781ead8d7734b255d058565`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
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
$ docker pull nats@sha256:9b61497122cf4b3a8c30fc687c66344968c0fda6bbfe4a1b60d4361d9120229b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:8ac046d6c8660a1941079c55460e369623171da1242db0212c4e4e1ea04a7265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130301845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f8c7306fbc93a9072eae8b2e82245da9da5581b928cf98f6a43f3a5bb18c8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:46:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_SERVER=2.14.0
# Tue, 12 May 2026 23:46:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Tue, 12 May 2026 23:46:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.0/nats-server-v2.14.0-windows-amd64.zip
# Tue, 12 May 2026 23:46:37 GMT
ENV NATS_SERVER_SHASUM=09ba382669cc4df390f97f16f08481f040eef0bb17ca5f2d71104b4be4cd613a
# Tue, 12 May 2026 23:46:42 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 May 2026 23:46:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 May 2026 23:46:58 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 12 May 2026 23:46:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 May 2026 23:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 May 2026 23:47:00 GMT
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
	-	`sha256:a023c5625d2ee5d4db03516e4189696fe76d51e9b025badea7507457ee0ec780`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d3b4fd74d9cea43b61086e3be13f8fd68aaf7dcbed8869eb7654b13022210`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef61b238d44d24f9216b2e1eaaa99046523561ff4f907e645d7893a7d29e400`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1308c0e658293e66b16726765790666ac8d0da20ba6ac45c4b5bf07e871e7e`  
		Last Modified: Tue, 12 May 2026 23:47:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10dbe3d84a9d708da963fba429a9d97b30ad3d3f55cf2b215db3226cef086cd`  
		Last Modified: Tue, 12 May 2026 23:47:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eb792b599093b403901940e5a5809475ebdca2d28b347159b0ccd4fe52c402`  
		Last Modified: Tue, 12 May 2026 23:47:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c94b5c81292e032d68bd1ba5bd819b3390645f9e9b43e5f30b714c0fd65c469`  
		Last Modified: Tue, 12 May 2026 23:47:06 GMT  
		Size: 480.0 KB (479956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6159ce96c550fe0e2723ad3256060f48ed487a7021d8036f0e6ae4fb1cee9618`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 7.4 MB (7387702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa8177fcaa7207011be892ae542dcc77b7bc62eea167a839cc7da6d2d1ac9a5`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4971bfb6dede78606066a89134eecb700883a65fe50996cd78914085969b4c3`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cff0aa25bd3783b982c3d8cbb8c921e7850bdea723a6759a7caf9cb0664baca`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bbf4adc2716b36dbfba894764c1c3cd1f07280637c15aa87c0c6fd22518d5d3`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:9b61497122cf4b3a8c30fc687c66344968c0fda6bbfe4a1b60d4361d9120229b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:8ac046d6c8660a1941079c55460e369623171da1242db0212c4e4e1ea04a7265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130301845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f8c7306fbc93a9072eae8b2e82245da9da5581b928cf98f6a43f3a5bb18c8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:46:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_SERVER=2.14.0
# Tue, 12 May 2026 23:46:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Tue, 12 May 2026 23:46:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.0/nats-server-v2.14.0-windows-amd64.zip
# Tue, 12 May 2026 23:46:37 GMT
ENV NATS_SERVER_SHASUM=09ba382669cc4df390f97f16f08481f040eef0bb17ca5f2d71104b4be4cd613a
# Tue, 12 May 2026 23:46:42 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 May 2026 23:46:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 May 2026 23:46:58 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 12 May 2026 23:46:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 May 2026 23:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 May 2026 23:47:00 GMT
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
	-	`sha256:a023c5625d2ee5d4db03516e4189696fe76d51e9b025badea7507457ee0ec780`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d3b4fd74d9cea43b61086e3be13f8fd68aaf7dcbed8869eb7654b13022210`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef61b238d44d24f9216b2e1eaaa99046523561ff4f907e645d7893a7d29e400`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1308c0e658293e66b16726765790666ac8d0da20ba6ac45c4b5bf07e871e7e`  
		Last Modified: Tue, 12 May 2026 23:47:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10dbe3d84a9d708da963fba429a9d97b30ad3d3f55cf2b215db3226cef086cd`  
		Last Modified: Tue, 12 May 2026 23:47:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eb792b599093b403901940e5a5809475ebdca2d28b347159b0ccd4fe52c402`  
		Last Modified: Tue, 12 May 2026 23:47:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c94b5c81292e032d68bd1ba5bd819b3390645f9e9b43e5f30b714c0fd65c469`  
		Last Modified: Tue, 12 May 2026 23:47:06 GMT  
		Size: 480.0 KB (479956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6159ce96c550fe0e2723ad3256060f48ed487a7021d8036f0e6ae4fb1cee9618`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 7.4 MB (7387702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa8177fcaa7207011be892ae542dcc77b7bc62eea167a839cc7da6d2d1ac9a5`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4971bfb6dede78606066a89134eecb700883a65fe50996cd78914085969b4c3`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cff0aa25bd3783b982c3d8cbb8c921e7850bdea723a6759a7caf9cb0664baca`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bbf4adc2716b36dbfba894764c1c3cd1f07280637c15aa87c0c6fd22518d5d3`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1282 bytes)  
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
$ docker pull nats@sha256:6b2156f7491cdeddfa8b7ca15cd6fd59b9cabadec5019e933c65c01cf82b1c5f
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
$ docker pull nats@sha256:d11cbec9afb91f27adb44a1e36c74b6ae59a674258531cb045acba39730d53b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10920773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27082b56ef0e728c0b25055b2a8297d49f499bbf5df5d491272af38a7c44cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a74686f11568e98d1e391b903678ee618b9a39aa5ceaa255da2a7ff23ed7c`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 7.1 MB (7111614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed50c18d13cc5345f43115a144cb1c8b81b8372631c87bf8d7dc83cdea031b`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5afa1e4cafbcd5b1672cb7a8effb2e2a63673c56c1f6b57f4a4cac7830b8d9`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f072e0c0cb980ba295d6d09ffab0720392b9051fbc587df9d3a1546baa020b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6762e2789ffcec0a32eec4d90db5348f0a420b61c14b288991a8ce5988c0f005`

```dockerfile
```

-	Layers:
	-	`sha256:3a11e1b7b0fe61acdca91af7d67d2bfa36475246e9ee47e374f181f6d774a204`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:de64f8fbea0904878bf0709cb3115130600bd3fb8c8775d8b5a6556be0a6cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3186438c73a75ded34b50aba9a315007ddd4f2861b160d9afb3c863948abcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c03acd4f097cbf133e82f8d4452cccdb54257260b2f85dbd386b038f430521`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6829604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1460c92b264e4ac559d4e544ec3a0cd7d6127a531fffdb0db2154ccdfda82f98`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7104b49da8cc9c42091091216f1d29564cd20dc28a154cb48933c382073ea327`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ff7edffe58c50fa5dc64a1d234009d9f618d1d925d0b56286919045e4e95ce4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdee6938423b9a114c22acb9699fdd4022c8969cfe341fb47e3022a29e7d2657`

```dockerfile
```

-	Layers:
	-	`sha256:bc2be06e9d1d8bad4d5e67284d5051946b9aabf787aab6e75467498c13b5bb68`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:83c6bbdb6f6930bd8f77a9c53556fe708b64c69cebc0fb281df0ce1e85599f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10044884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5404d1316a2dbeb592a121da51851996d2b456fc90d76663684a2ee4395fa598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c0c1cdfba8772720f404d6560ec4c5c7b210c2c1342cc3232f9cbb95aaac2`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6818083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee1d8aa61dc7fe184a4afa412505957c2b4a7e1538b23e9eb0567c217b221`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67374b5796f89fbf4825af6ff83925281b51e3a597fc4b5baef090c6eacdb129`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:729af97741ea84b7cd43a0f5b68e6a01b844eda27473601c214d5fcd756584a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c69f772e4d0413f8faa402d1a944a672814c9f0cc459abd865225bb251b8d22`

```dockerfile
```

-	Layers:
	-	`sha256:bc6466cc1dfda6baac01df16d9cb34bf26a929c5008b8e9c83c260eefec91008`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:309c3a317f98e396a5687b31ee3eccc5fd14121d27e96f99d307055c33afb154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c31459ac1dd3166e7b6a56dc48799e3355fc3c2eee66c73bcb6982c096d124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0264ec65d1c94e26eb13ece3293fd0f1a223a083f07123a89ab6533fa7f3ea3`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 6.5 MB (6516368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8720fa9574209724faf15869ee142fb3465e685ab0377192bf9b2d6b801df158`  
		Last Modified: Tue, 28 Apr 2026 00:11:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cab18aed7cf17ef64ccb91a99fc238c3c88fde554678d1f90ded2f38ecaf0d7`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e05fe41e9457ed0d7b0738daa11b7ed4df2ef0483d42e415d92d3d866847bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da164679dfd40fa005a81bdee8a8f4f929cdec1bdfac87231b7fe5e7457ba99`

```dockerfile
```

-	Layers:
	-	`sha256:25926700f4d2f5b98eae89a4bd6d3f6b0df83af058030add1eb43f93db01d776`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9182046bc9c75c50fe6738ac524dab8187db8317900daec750a58666ca89fc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10302333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d38dd3a196967303aeefe505d29ff782d68870c62bd38b262f89436ced913d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4d9d616afa995dc3996e50baa1ead256ff76b85ea197302fa8f17b5e6ec8c`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.6 MB (6564704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:109c930003fb0d902fc75741c7f2aa1a5d20a060b6348fb6b50dd3a436020eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d1f2e6d3c5103a4a8ce89d1eea6f6cb28092efd4a529280969f99c9112a934`

```dockerfile
```

-	Layers:
	-	`sha256:73c35d38c6c10ef3f24aef75adfe3c8135cca707abd0a557d78aa623c05137b6`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:765cf41f86293cbfc817903a2e95c9fc460095ffa6a2afd14e9fbf6098a863e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a300b10c87307999e280d8044bc933dc6a769bf134c71dc069b7df45c1acf71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:06 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b00d570ea6fe160e330c54a027a3541fb1ca0795604be5975cba634fb9327b`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.9 MB (6949611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51608ad68619bc3a9ab77b844278637a43da5a519228babd3caee4d0be374c7f`  
		Last Modified: Tue, 28 Apr 2026 00:16:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4568a16c47624175fa8b3ccb3e0db1369f5afb9048bbdcf0d2462d19429c3b`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:66210453cac12e4f00ea8be9a556a70ab26a636163a953598ed5290b8b1ab0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa02bb916d5e127a400bf5a556ddc9a617cdb97906db85765c21264c02b7d1d9`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9e7d40544704e8408524131ac7132b11191a74051051f016bdb84f132d5a1`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-alpine3.22`

```console
$ docker pull nats@sha256:6b2156f7491cdeddfa8b7ca15cd6fd59b9cabadec5019e933c65c01cf82b1c5f
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
$ docker pull nats@sha256:d11cbec9afb91f27adb44a1e36c74b6ae59a674258531cb045acba39730d53b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10920773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27082b56ef0e728c0b25055b2a8297d49f499bbf5df5d491272af38a7c44cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a74686f11568e98d1e391b903678ee618b9a39aa5ceaa255da2a7ff23ed7c`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 7.1 MB (7111614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed50c18d13cc5345f43115a144cb1c8b81b8372631c87bf8d7dc83cdea031b`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5afa1e4cafbcd5b1672cb7a8effb2e2a63673c56c1f6b57f4a4cac7830b8d9`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f072e0c0cb980ba295d6d09ffab0720392b9051fbc587df9d3a1546baa020b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6762e2789ffcec0a32eec4d90db5348f0a420b61c14b288991a8ce5988c0f005`

```dockerfile
```

-	Layers:
	-	`sha256:3a11e1b7b0fe61acdca91af7d67d2bfa36475246e9ee47e374f181f6d774a204`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:de64f8fbea0904878bf0709cb3115130600bd3fb8c8775d8b5a6556be0a6cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3186438c73a75ded34b50aba9a315007ddd4f2861b160d9afb3c863948abcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c03acd4f097cbf133e82f8d4452cccdb54257260b2f85dbd386b038f430521`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6829604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1460c92b264e4ac559d4e544ec3a0cd7d6127a531fffdb0db2154ccdfda82f98`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7104b49da8cc9c42091091216f1d29564cd20dc28a154cb48933c382073ea327`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ff7edffe58c50fa5dc64a1d234009d9f618d1d925d0b56286919045e4e95ce4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdee6938423b9a114c22acb9699fdd4022c8969cfe341fb47e3022a29e7d2657`

```dockerfile
```

-	Layers:
	-	`sha256:bc2be06e9d1d8bad4d5e67284d5051946b9aabf787aab6e75467498c13b5bb68`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:83c6bbdb6f6930bd8f77a9c53556fe708b64c69cebc0fb281df0ce1e85599f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10044884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5404d1316a2dbeb592a121da51851996d2b456fc90d76663684a2ee4395fa598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c0c1cdfba8772720f404d6560ec4c5c7b210c2c1342cc3232f9cbb95aaac2`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6818083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee1d8aa61dc7fe184a4afa412505957c2b4a7e1538b23e9eb0567c217b221`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67374b5796f89fbf4825af6ff83925281b51e3a597fc4b5baef090c6eacdb129`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:729af97741ea84b7cd43a0f5b68e6a01b844eda27473601c214d5fcd756584a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c69f772e4d0413f8faa402d1a944a672814c9f0cc459abd865225bb251b8d22`

```dockerfile
```

-	Layers:
	-	`sha256:bc6466cc1dfda6baac01df16d9cb34bf26a929c5008b8e9c83c260eefec91008`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:309c3a317f98e396a5687b31ee3eccc5fd14121d27e96f99d307055c33afb154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c31459ac1dd3166e7b6a56dc48799e3355fc3c2eee66c73bcb6982c096d124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0264ec65d1c94e26eb13ece3293fd0f1a223a083f07123a89ab6533fa7f3ea3`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 6.5 MB (6516368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8720fa9574209724faf15869ee142fb3465e685ab0377192bf9b2d6b801df158`  
		Last Modified: Tue, 28 Apr 2026 00:11:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cab18aed7cf17ef64ccb91a99fc238c3c88fde554678d1f90ded2f38ecaf0d7`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e05fe41e9457ed0d7b0738daa11b7ed4df2ef0483d42e415d92d3d866847bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da164679dfd40fa005a81bdee8a8f4f929cdec1bdfac87231b7fe5e7457ba99`

```dockerfile
```

-	Layers:
	-	`sha256:25926700f4d2f5b98eae89a4bd6d3f6b0df83af058030add1eb43f93db01d776`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9182046bc9c75c50fe6738ac524dab8187db8317900daec750a58666ca89fc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10302333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d38dd3a196967303aeefe505d29ff782d68870c62bd38b262f89436ced913d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4d9d616afa995dc3996e50baa1ead256ff76b85ea197302fa8f17b5e6ec8c`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.6 MB (6564704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:109c930003fb0d902fc75741c7f2aa1a5d20a060b6348fb6b50dd3a436020eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d1f2e6d3c5103a4a8ce89d1eea6f6cb28092efd4a529280969f99c9112a934`

```dockerfile
```

-	Layers:
	-	`sha256:73c35d38c6c10ef3f24aef75adfe3c8135cca707abd0a557d78aa623c05137b6`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:765cf41f86293cbfc817903a2e95c9fc460095ffa6a2afd14e9fbf6098a863e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a300b10c87307999e280d8044bc933dc6a769bf134c71dc069b7df45c1acf71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:06 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b00d570ea6fe160e330c54a027a3541fb1ca0795604be5975cba634fb9327b`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.9 MB (6949611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51608ad68619bc3a9ab77b844278637a43da5a519228babd3caee4d0be374c7f`  
		Last Modified: Tue, 28 Apr 2026 00:16:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4568a16c47624175fa8b3ccb3e0db1369f5afb9048bbdcf0d2462d19429c3b`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:66210453cac12e4f00ea8be9a556a70ab26a636163a953598ed5290b8b1ab0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa02bb916d5e127a400bf5a556ddc9a617cdb97906db85765c21264c02b7d1d9`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9e7d40544704e8408524131ac7132b11191a74051051f016bdb84f132d5a1`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 15.4 KB (15404 bytes)  
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
$ docker pull nats@sha256:87893863e742226f3316afb031314820d1b8973ba30c1e1a75b1f00c86a89d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:3fb6f659c8dbdaeef131ca3140a6b4937b6771133cec2c89cf60c617ed37e4f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130102262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee00c85b850ab103ef7e30b0d050a957da1faac84e62a08fcb037cabdc18a8e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:46:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 May 2026 23:46:36 GMT
ENV NATS_SERVER=2.12.8
# Tue, 12 May 2026 23:46:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 12 May 2026 23:46:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.8/nats-server-v2.12.8-windows-amd64.zip
# Tue, 12 May 2026 23:46:38 GMT
ENV NATS_SERVER_SHASUM=61836ff8d0cecbb773faf7daa22f5212b7ed3ab5a0c58c12b013d67d64edd6cc
# Tue, 12 May 2026 23:46:44 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 May 2026 23:47:00 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 May 2026 23:47:01 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 12 May 2026 23:47:02 GMT
EXPOSE 4222 6222 8222
# Tue, 12 May 2026 23:47:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 May 2026 23:47:03 GMT
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
	-	`sha256:90afc8fac618acea85025416d5c796cadc00fc70c25d63769a357427f3930150`  
		Last Modified: Tue, 12 May 2026 23:47:10 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302e2335d581f68b42e1acb4b0e8994e851657c270218296525a0465ff17e5ac`  
		Last Modified: Tue, 12 May 2026 23:47:10 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4d18df94ec15b5e6320e68b43be0a558a420fc8347b5f54a4fe14649307d12`  
		Last Modified: Tue, 12 May 2026 23:47:10 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d55ef458fd472061f34dbd4286cb8ef2de111dbb1aa9b560e10b762ec4908`  
		Last Modified: Tue, 12 May 2026 23:47:09 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53f2338143924ca83eb935bda452456f612172e267913bd2a8e79091f7ff053`  
		Last Modified: Tue, 12 May 2026 23:47:09 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ff9b2dcaa7872875ebd54907e5600ddf0af31ce4900d7b279fd6e87b7ae21d`  
		Last Modified: Tue, 12 May 2026 23:47:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a78bc650abccc33a98a6f67b91e9ab62582efe3bd1defafbfa03c78a71407e1`  
		Last Modified: Tue, 12 May 2026 23:47:09 GMT  
		Size: 481.5 KB (481485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d1bbf3c5c71237ca6d7d69fe9e2576f4211d71403b32eefdd7b8683c9c7c05`  
		Last Modified: Tue, 12 May 2026 23:47:08 GMT  
		Size: 7.2 MB (7186516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1ff8131266b0b3700edcc696086427d834a345dd22fc9c6c0974e9904189ec`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b8362fb7a76b9b960350dba68764f61a5741abb6f2b08acb51537f31d6cd6`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78a1a3f986533d642ddd69fcc9db90739a50a9c11e2a9212a504c814e32010b`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccac0d0833c9776bea08fc241398796a780029b3cf0e9ee5004e337e023241e3`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:87893863e742226f3316afb031314820d1b8973ba30c1e1a75b1f00c86a89d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:3fb6f659c8dbdaeef131ca3140a6b4937b6771133cec2c89cf60c617ed37e4f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130102262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee00c85b850ab103ef7e30b0d050a957da1faac84e62a08fcb037cabdc18a8e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:46:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 May 2026 23:46:36 GMT
ENV NATS_SERVER=2.12.8
# Tue, 12 May 2026 23:46:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 12 May 2026 23:46:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.8/nats-server-v2.12.8-windows-amd64.zip
# Tue, 12 May 2026 23:46:38 GMT
ENV NATS_SERVER_SHASUM=61836ff8d0cecbb773faf7daa22f5212b7ed3ab5a0c58c12b013d67d64edd6cc
# Tue, 12 May 2026 23:46:44 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 May 2026 23:47:00 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 May 2026 23:47:01 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 12 May 2026 23:47:02 GMT
EXPOSE 4222 6222 8222
# Tue, 12 May 2026 23:47:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 May 2026 23:47:03 GMT
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
	-	`sha256:90afc8fac618acea85025416d5c796cadc00fc70c25d63769a357427f3930150`  
		Last Modified: Tue, 12 May 2026 23:47:10 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302e2335d581f68b42e1acb4b0e8994e851657c270218296525a0465ff17e5ac`  
		Last Modified: Tue, 12 May 2026 23:47:10 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4d18df94ec15b5e6320e68b43be0a558a420fc8347b5f54a4fe14649307d12`  
		Last Modified: Tue, 12 May 2026 23:47:10 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d55ef458fd472061f34dbd4286cb8ef2de111dbb1aa9b560e10b762ec4908`  
		Last Modified: Tue, 12 May 2026 23:47:09 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53f2338143924ca83eb935bda452456f612172e267913bd2a8e79091f7ff053`  
		Last Modified: Tue, 12 May 2026 23:47:09 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ff9b2dcaa7872875ebd54907e5600ddf0af31ce4900d7b279fd6e87b7ae21d`  
		Last Modified: Tue, 12 May 2026 23:47:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a78bc650abccc33a98a6f67b91e9ab62582efe3bd1defafbfa03c78a71407e1`  
		Last Modified: Tue, 12 May 2026 23:47:09 GMT  
		Size: 481.5 KB (481485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d1bbf3c5c71237ca6d7d69fe9e2576f4211d71403b32eefdd7b8683c9c7c05`  
		Last Modified: Tue, 12 May 2026 23:47:08 GMT  
		Size: 7.2 MB (7186516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1ff8131266b0b3700edcc696086427d834a345dd22fc9c6c0974e9904189ec`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b8362fb7a76b9b960350dba68764f61a5741abb6f2b08acb51537f31d6cd6`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78a1a3f986533d642ddd69fcc9db90739a50a9c11e2a9212a504c814e32010b`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccac0d0833c9776bea08fc241398796a780029b3cf0e9ee5004e337e023241e3`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.9`

**does not exist** (yet?)

## `nats:2.12.9-alpine`

**does not exist** (yet?)

## `nats:2.12.9-alpine3.22`

**does not exist** (yet?)

## `nats:2.12.9-linux`

**does not exist** (yet?)

## `nats:2.12.9-nanoserver`

**does not exist** (yet?)

## `nats:2.12.9-nanoserver-ltsc2022`

**does not exist** (yet?)

## `nats:2.12.9-scratch`

**does not exist** (yet?)

## `nats:2.12.9-windowsservercore`

**does not exist** (yet?)

## `nats:2.12.9-windowsservercore-ltsc2022`

**does not exist** (yet?)

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
$ docker pull nats@sha256:df3dbf7615519c64c1ecf5bff1811e0f1349e980e12cf8edac882a53cf3f9dd9
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
$ docker pull nats@sha256:4e4b6c6da8e5dd1c1972aef235279bb99a4554e3277969c25baf06fe75bf3a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11111423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aa95f5acd85535217858bde3f513b2fd61fcded722bdd5d17bb9d89f124eb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b74c94101f0c98ee2c3a1cfe1857a9d00f6d49ce060aac8c3e709731ff6e6c`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 7.3 MB (7302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1171202a810bee209cebae3b516e5dc187466c7efada92079b4cb6da26cc2196`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c58df7044a7df1b6d31a8bff11256dc9480ccd2f85f73edd8393509074d239`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:603015575bf6c3db29393d6ebdf202853ed9636544435f710b2ca3c09536a075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b2bea654035fe919b77ca44ff2adc24191ed65e513b5046faeb2ffb325b5c`

```dockerfile
```

-	Layers:
	-	`sha256:4f302bf75b042b6174b0022d5f48276cef4a2d88e48c27eead53470b13c0d940`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:f50039ea7bec9263cf0a5e88f88d07fd6ebdce50aa9b135611f858acd512f2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10526198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5883c39c5192e03c75b4224b245435c9d6161e83fe57b250935914bd24001668`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccac10855b16bbd9dacf92801d18f2dcabc07188eeffa283aeeaf3f75d832ce`  
		Last Modified: Thu, 30 Apr 2026 23:41:29 GMT  
		Size: 7.0 MB (7017844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbe36b4e25cffbd5ff5634a3fbd1b13a52d111c40121037c010104f6108763`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c11d0705e172884bff3c4d474533693e7de0fa05a5917a78d773a5de329d0`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6471a93f16c111840eacd768e23308cdf960a1cfe889095d78003195e0a0ea6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecff6d4ed848b72ba06ee95a83bd748bd4ca11c6a640da4e12694ac5179e87`

```dockerfile
```

-	Layers:
	-	`sha256:d3bff562dcf6b3117fa78f4a3e590eee7581451e02a99962b05600f583a9cf27`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e9297bbd9fb68cd33a16528c1571b4dafe2dd9ab4142ec024db5ee531ddc68da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10231865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f606a353fc4e59f45057730ace4c11a67caf47eff4f28e41b42b788d8c2414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c367a285a39c8c8c79b4ea0aa7c6247702d54f43f100dd5c3ddbd51c94d3211`  
		Last Modified: Thu, 30 Apr 2026 23:41:35 GMT  
		Size: 7.0 MB (7005064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117013b561496f590f9a60f99c816fe4a564bf0889f6e0df758ada57c96d4e6d`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963d6d4f8ca7ced9d60d1ad7d51774145a90f68ef921fe87ead7831bf25f4bea`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:370298f66cb1801078ab77ec09d0abe92e1c78e845edcbf19512b2f7fd142d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca1a27ff1c3c7b822bd6661b9c47440a8e25f7b4b9cd588c4c3c801ac6451b6`

```dockerfile
```

-	Layers:
	-	`sha256:b570c31a499e86a57fa446b3882375a52d71cc1f961560ff9e1ae810a4efff8b`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d12972d669f1b377199d2741e1fa077ea1168ce25e2c42404f250313a187fe43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eedd13f74e4fec45f3a450d999030f19561f09cfdd980981bbc3a63f0b4cd7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:39 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402c5214fc465210f9c99ad940c17598d6c6af48826c7eb608e07ae485a3e588`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 6.7 MB (6667294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18810920ce9ca341b83ab1017aef4513c4174d891f67342d611c5f3bbda38999`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794d09af1fbaa55736af3f4e2575cea602bd620f628f9e9b546f10970a504934`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:740ee1c9829ccceb669d434cb446164b4b61620f027a57838adf0b32213a1a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a48f299143dbcbdb7d18a8680dc39a2c782baecb38582281887840bab6ca165`

```dockerfile
```

-	Layers:
	-	`sha256:b926ca76b9cf11b2e4ffad4954b37d9fe5b9f4884e5d7fb6c57adb38e84b9a1e`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 15.6 KB (15555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3edda2d951ada7baee76eac3997620987fd3b6ad34abf3b3aeafb4a33d23d47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10458042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c140c21478922b87a2c72b28bd2c0f8c5503c54edc400ab38da1761ca0396c8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:18:52 GMT
ENV NATS_SERVER=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 01 May 2026 00:18:53 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 00:18:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47da398408150920ce8738775297259fe6972d60691a7bd593a28f145b641ef7`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 6.7 MB (6720417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e284a50fe36dcd81f24a73cf5ff5bfe4361b05c60af1c49247d6876489ebdd77`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b453cbccc82afdd9cb5ca438319699b9a61c0fbe5cca06a89fb0a818535827`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:927bcfc16a9e30312116c9c098acc4ed1f96d59ece262eedec4dcc6f7791f494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4306275a207ecd844610df04fafdf166bc2d50d693f22c9adea013222821e7`

```dockerfile
```

-	Layers:
	-	`sha256:fef755e27c5c797a2fd43121851e5482553e3c71c07f36853f09346ec055a853`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; s390x

```console
$ docker pull nats@sha256:39a52f21d83100719820a826546974edb5b9cd196bda48644d6bde9955650bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10765798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d57f91b93856a000a606780ec5363bc1eb9fb5a2e11112703d73d6e2cfe151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:02 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2085d200b4339b2fc1f02d3ff2827df89f8e4de23b30c3a01197cb364b6e077`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 7.1 MB (7110955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dd256e0fb0cd7e8b86422d79adf837656f750a9ef09f0f36a340664e797d66`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9c615faf9438fa6dc56c180f588bd2e8c3452bbb70bc934ae5e478c052a4c4`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4d12d33eb8b4b9a3886edda118f27a14fab07b1ddfd21129db90309db7b7e483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffc7fca774a22b7dbba927d7c8965de3a26790e226cc50a5ed1fd3bff355aa9`

```dockerfile
```

-	Layers:
	-	`sha256:3313afa82fcfd90aaae86adae7b450d6d5bc98452781ead8d7734b255d058565`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-alpine3.22`

```console
$ docker pull nats@sha256:df3dbf7615519c64c1ecf5bff1811e0f1349e980e12cf8edac882a53cf3f9dd9
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
$ docker pull nats@sha256:4e4b6c6da8e5dd1c1972aef235279bb99a4554e3277969c25baf06fe75bf3a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11111423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aa95f5acd85535217858bde3f513b2fd61fcded722bdd5d17bb9d89f124eb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b74c94101f0c98ee2c3a1cfe1857a9d00f6d49ce060aac8c3e709731ff6e6c`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 7.3 MB (7302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1171202a810bee209cebae3b516e5dc187466c7efada92079b4cb6da26cc2196`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c58df7044a7df1b6d31a8bff11256dc9480ccd2f85f73edd8393509074d239`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:603015575bf6c3db29393d6ebdf202853ed9636544435f710b2ca3c09536a075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b2bea654035fe919b77ca44ff2adc24191ed65e513b5046faeb2ffb325b5c`

```dockerfile
```

-	Layers:
	-	`sha256:4f302bf75b042b6174b0022d5f48276cef4a2d88e48c27eead53470b13c0d940`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:f50039ea7bec9263cf0a5e88f88d07fd6ebdce50aa9b135611f858acd512f2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10526198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5883c39c5192e03c75b4224b245435c9d6161e83fe57b250935914bd24001668`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccac10855b16bbd9dacf92801d18f2dcabc07188eeffa283aeeaf3f75d832ce`  
		Last Modified: Thu, 30 Apr 2026 23:41:29 GMT  
		Size: 7.0 MB (7017844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbe36b4e25cffbd5ff5634a3fbd1b13a52d111c40121037c010104f6108763`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c11d0705e172884bff3c4d474533693e7de0fa05a5917a78d773a5de329d0`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6471a93f16c111840eacd768e23308cdf960a1cfe889095d78003195e0a0ea6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecff6d4ed848b72ba06ee95a83bd748bd4ca11c6a640da4e12694ac5179e87`

```dockerfile
```

-	Layers:
	-	`sha256:d3bff562dcf6b3117fa78f4a3e590eee7581451e02a99962b05600f583a9cf27`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:e9297bbd9fb68cd33a16528c1571b4dafe2dd9ab4142ec024db5ee531ddc68da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10231865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f606a353fc4e59f45057730ace4c11a67caf47eff4f28e41b42b788d8c2414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c367a285a39c8c8c79b4ea0aa7c6247702d54f43f100dd5c3ddbd51c94d3211`  
		Last Modified: Thu, 30 Apr 2026 23:41:35 GMT  
		Size: 7.0 MB (7005064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117013b561496f590f9a60f99c816fe4a564bf0889f6e0df758ada57c96d4e6d`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963d6d4f8ca7ced9d60d1ad7d51774145a90f68ef921fe87ead7831bf25f4bea`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:370298f66cb1801078ab77ec09d0abe92e1c78e845edcbf19512b2f7fd142d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca1a27ff1c3c7b822bd6661b9c47440a8e25f7b4b9cd588c4c3c801ac6451b6`

```dockerfile
```

-	Layers:
	-	`sha256:b570c31a499e86a57fa446b3882375a52d71cc1f961560ff9e1ae810a4efff8b`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d12972d669f1b377199d2741e1fa077ea1168ce25e2c42404f250313a187fe43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eedd13f74e4fec45f3a450d999030f19561f09cfdd980981bbc3a63f0b4cd7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:39 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402c5214fc465210f9c99ad940c17598d6c6af48826c7eb608e07ae485a3e588`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 6.7 MB (6667294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18810920ce9ca341b83ab1017aef4513c4174d891f67342d611c5f3bbda38999`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794d09af1fbaa55736af3f4e2575cea602bd620f628f9e9b546f10970a504934`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:740ee1c9829ccceb669d434cb446164b4b61620f027a57838adf0b32213a1a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a48f299143dbcbdb7d18a8680dc39a2c782baecb38582281887840bab6ca165`

```dockerfile
```

-	Layers:
	-	`sha256:b926ca76b9cf11b2e4ffad4954b37d9fe5b9f4884e5d7fb6c57adb38e84b9a1e`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 15.6 KB (15555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:3edda2d951ada7baee76eac3997620987fd3b6ad34abf3b3aeafb4a33d23d47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10458042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c140c21478922b87a2c72b28bd2c0f8c5503c54edc400ab38da1761ca0396c8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:18:52 GMT
ENV NATS_SERVER=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 01 May 2026 00:18:53 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 00:18:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47da398408150920ce8738775297259fe6972d60691a7bd593a28f145b641ef7`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 6.7 MB (6720417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e284a50fe36dcd81f24a73cf5ff5bfe4361b05c60af1c49247d6876489ebdd77`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b453cbccc82afdd9cb5ca438319699b9a61c0fbe5cca06a89fb0a818535827`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:927bcfc16a9e30312116c9c098acc4ed1f96d59ece262eedec4dcc6f7791f494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4306275a207ecd844610df04fafdf166bc2d50d693f22c9adea013222821e7`

```dockerfile
```

-	Layers:
	-	`sha256:fef755e27c5c797a2fd43121851e5482553e3c71c07f36853f09346ec055a853`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:39a52f21d83100719820a826546974edb5b9cd196bda48644d6bde9955650bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10765798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d57f91b93856a000a606780ec5363bc1eb9fb5a2e11112703d73d6e2cfe151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:02 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2085d200b4339b2fc1f02d3ff2827df89f8e4de23b30c3a01197cb364b6e077`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 7.1 MB (7110955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dd256e0fb0cd7e8b86422d79adf837656f750a9ef09f0f36a340664e797d66`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9c615faf9438fa6dc56c180f588bd2e8c3452bbb70bc934ae5e478c052a4c4`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4d12d33eb8b4b9a3886edda118f27a14fab07b1ddfd21129db90309db7b7e483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffc7fca774a22b7dbba927d7c8965de3a26790e226cc50a5ed1fd3bff355aa9`

```dockerfile
```

-	Layers:
	-	`sha256:3313afa82fcfd90aaae86adae7b450d6d5bc98452781ead8d7734b255d058565`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
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
$ docker pull nats@sha256:9b61497122cf4b3a8c30fc687c66344968c0fda6bbfe4a1b60d4361d9120229b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:8ac046d6c8660a1941079c55460e369623171da1242db0212c4e4e1ea04a7265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130301845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f8c7306fbc93a9072eae8b2e82245da9da5581b928cf98f6a43f3a5bb18c8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:46:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_SERVER=2.14.0
# Tue, 12 May 2026 23:46:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Tue, 12 May 2026 23:46:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.0/nats-server-v2.14.0-windows-amd64.zip
# Tue, 12 May 2026 23:46:37 GMT
ENV NATS_SERVER_SHASUM=09ba382669cc4df390f97f16f08481f040eef0bb17ca5f2d71104b4be4cd613a
# Tue, 12 May 2026 23:46:42 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 May 2026 23:46:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 May 2026 23:46:58 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 12 May 2026 23:46:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 May 2026 23:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 May 2026 23:47:00 GMT
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
	-	`sha256:a023c5625d2ee5d4db03516e4189696fe76d51e9b025badea7507457ee0ec780`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d3b4fd74d9cea43b61086e3be13f8fd68aaf7dcbed8869eb7654b13022210`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef61b238d44d24f9216b2e1eaaa99046523561ff4f907e645d7893a7d29e400`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1308c0e658293e66b16726765790666ac8d0da20ba6ac45c4b5bf07e871e7e`  
		Last Modified: Tue, 12 May 2026 23:47:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10dbe3d84a9d708da963fba429a9d97b30ad3d3f55cf2b215db3226cef086cd`  
		Last Modified: Tue, 12 May 2026 23:47:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eb792b599093b403901940e5a5809475ebdca2d28b347159b0ccd4fe52c402`  
		Last Modified: Tue, 12 May 2026 23:47:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c94b5c81292e032d68bd1ba5bd819b3390645f9e9b43e5f30b714c0fd65c469`  
		Last Modified: Tue, 12 May 2026 23:47:06 GMT  
		Size: 480.0 KB (479956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6159ce96c550fe0e2723ad3256060f48ed487a7021d8036f0e6ae4fb1cee9618`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 7.4 MB (7387702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa8177fcaa7207011be892ae542dcc77b7bc62eea167a839cc7da6d2d1ac9a5`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4971bfb6dede78606066a89134eecb700883a65fe50996cd78914085969b4c3`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cff0aa25bd3783b982c3d8cbb8c921e7850bdea723a6759a7caf9cb0664baca`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bbf4adc2716b36dbfba894764c1c3cd1f07280637c15aa87c0c6fd22518d5d3`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:9b61497122cf4b3a8c30fc687c66344968c0fda6bbfe4a1b60d4361d9120229b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:8ac046d6c8660a1941079c55460e369623171da1242db0212c4e4e1ea04a7265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130301845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f8c7306fbc93a9072eae8b2e82245da9da5581b928cf98f6a43f3a5bb18c8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:46:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_SERVER=2.14.0
# Tue, 12 May 2026 23:46:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Tue, 12 May 2026 23:46:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.0/nats-server-v2.14.0-windows-amd64.zip
# Tue, 12 May 2026 23:46:37 GMT
ENV NATS_SERVER_SHASUM=09ba382669cc4df390f97f16f08481f040eef0bb17ca5f2d71104b4be4cd613a
# Tue, 12 May 2026 23:46:42 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 May 2026 23:46:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 May 2026 23:46:58 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 12 May 2026 23:46:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 May 2026 23:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 May 2026 23:47:00 GMT
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
	-	`sha256:a023c5625d2ee5d4db03516e4189696fe76d51e9b025badea7507457ee0ec780`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d3b4fd74d9cea43b61086e3be13f8fd68aaf7dcbed8869eb7654b13022210`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef61b238d44d24f9216b2e1eaaa99046523561ff4f907e645d7893a7d29e400`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1308c0e658293e66b16726765790666ac8d0da20ba6ac45c4b5bf07e871e7e`  
		Last Modified: Tue, 12 May 2026 23:47:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10dbe3d84a9d708da963fba429a9d97b30ad3d3f55cf2b215db3226cef086cd`  
		Last Modified: Tue, 12 May 2026 23:47:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eb792b599093b403901940e5a5809475ebdca2d28b347159b0ccd4fe52c402`  
		Last Modified: Tue, 12 May 2026 23:47:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c94b5c81292e032d68bd1ba5bd819b3390645f9e9b43e5f30b714c0fd65c469`  
		Last Modified: Tue, 12 May 2026 23:47:06 GMT  
		Size: 480.0 KB (479956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6159ce96c550fe0e2723ad3256060f48ed487a7021d8036f0e6ae4fb1cee9618`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 7.4 MB (7387702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa8177fcaa7207011be892ae542dcc77b7bc62eea167a839cc7da6d2d1ac9a5`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4971bfb6dede78606066a89134eecb700883a65fe50996cd78914085969b4c3`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cff0aa25bd3783b982c3d8cbb8c921e7850bdea723a6759a7caf9cb0664baca`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bbf4adc2716b36dbfba894764c1c3cd1f07280637c15aa87c0c6fd22518d5d3`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.1`

**does not exist** (yet?)

## `nats:2.14.1-alpine`

**does not exist** (yet?)

## `nats:2.14.1-alpine3.22`

**does not exist** (yet?)

## `nats:2.14.1-linux`

**does not exist** (yet?)

## `nats:2.14.1-nanoserver`

**does not exist** (yet?)

## `nats:2.14.1-nanoserver-ltsc2022`

**does not exist** (yet?)

## `nats:2.14.1-scratch`

**does not exist** (yet?)

## `nats:2.14.1-windowsservercore`

**does not exist** (yet?)

## `nats:2.14.1-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `nats:alpine`

```console
$ docker pull nats@sha256:df3dbf7615519c64c1ecf5bff1811e0f1349e980e12cf8edac882a53cf3f9dd9
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
$ docker pull nats@sha256:4e4b6c6da8e5dd1c1972aef235279bb99a4554e3277969c25baf06fe75bf3a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11111423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aa95f5acd85535217858bde3f513b2fd61fcded722bdd5d17bb9d89f124eb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b74c94101f0c98ee2c3a1cfe1857a9d00f6d49ce060aac8c3e709731ff6e6c`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 7.3 MB (7302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1171202a810bee209cebae3b516e5dc187466c7efada92079b4cb6da26cc2196`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c58df7044a7df1b6d31a8bff11256dc9480ccd2f85f73edd8393509074d239`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:603015575bf6c3db29393d6ebdf202853ed9636544435f710b2ca3c09536a075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b2bea654035fe919b77ca44ff2adc24191ed65e513b5046faeb2ffb325b5c`

```dockerfile
```

-	Layers:
	-	`sha256:4f302bf75b042b6174b0022d5f48276cef4a2d88e48c27eead53470b13c0d940`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:f50039ea7bec9263cf0a5e88f88d07fd6ebdce50aa9b135611f858acd512f2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10526198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5883c39c5192e03c75b4224b245435c9d6161e83fe57b250935914bd24001668`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccac10855b16bbd9dacf92801d18f2dcabc07188eeffa283aeeaf3f75d832ce`  
		Last Modified: Thu, 30 Apr 2026 23:41:29 GMT  
		Size: 7.0 MB (7017844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbe36b4e25cffbd5ff5634a3fbd1b13a52d111c40121037c010104f6108763`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c11d0705e172884bff3c4d474533693e7de0fa05a5917a78d773a5de329d0`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6471a93f16c111840eacd768e23308cdf960a1cfe889095d78003195e0a0ea6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecff6d4ed848b72ba06ee95a83bd748bd4ca11c6a640da4e12694ac5179e87`

```dockerfile
```

-	Layers:
	-	`sha256:d3bff562dcf6b3117fa78f4a3e590eee7581451e02a99962b05600f583a9cf27`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e9297bbd9fb68cd33a16528c1571b4dafe2dd9ab4142ec024db5ee531ddc68da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10231865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f606a353fc4e59f45057730ace4c11a67caf47eff4f28e41b42b788d8c2414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c367a285a39c8c8c79b4ea0aa7c6247702d54f43f100dd5c3ddbd51c94d3211`  
		Last Modified: Thu, 30 Apr 2026 23:41:35 GMT  
		Size: 7.0 MB (7005064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117013b561496f590f9a60f99c816fe4a564bf0889f6e0df758ada57c96d4e6d`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963d6d4f8ca7ced9d60d1ad7d51774145a90f68ef921fe87ead7831bf25f4bea`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:370298f66cb1801078ab77ec09d0abe92e1c78e845edcbf19512b2f7fd142d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca1a27ff1c3c7b822bd6661b9c47440a8e25f7b4b9cd588c4c3c801ac6451b6`

```dockerfile
```

-	Layers:
	-	`sha256:b570c31a499e86a57fa446b3882375a52d71cc1f961560ff9e1ae810a4efff8b`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d12972d669f1b377199d2741e1fa077ea1168ce25e2c42404f250313a187fe43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eedd13f74e4fec45f3a450d999030f19561f09cfdd980981bbc3a63f0b4cd7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:39 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402c5214fc465210f9c99ad940c17598d6c6af48826c7eb608e07ae485a3e588`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 6.7 MB (6667294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18810920ce9ca341b83ab1017aef4513c4174d891f67342d611c5f3bbda38999`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794d09af1fbaa55736af3f4e2575cea602bd620f628f9e9b546f10970a504934`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:740ee1c9829ccceb669d434cb446164b4b61620f027a57838adf0b32213a1a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a48f299143dbcbdb7d18a8680dc39a2c782baecb38582281887840bab6ca165`

```dockerfile
```

-	Layers:
	-	`sha256:b926ca76b9cf11b2e4ffad4954b37d9fe5b9f4884e5d7fb6c57adb38e84b9a1e`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 15.6 KB (15555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3edda2d951ada7baee76eac3997620987fd3b6ad34abf3b3aeafb4a33d23d47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10458042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c140c21478922b87a2c72b28bd2c0f8c5503c54edc400ab38da1761ca0396c8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:18:52 GMT
ENV NATS_SERVER=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 01 May 2026 00:18:53 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 00:18:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47da398408150920ce8738775297259fe6972d60691a7bd593a28f145b641ef7`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 6.7 MB (6720417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e284a50fe36dcd81f24a73cf5ff5bfe4361b05c60af1c49247d6876489ebdd77`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b453cbccc82afdd9cb5ca438319699b9a61c0fbe5cca06a89fb0a818535827`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:927bcfc16a9e30312116c9c098acc4ed1f96d59ece262eedec4dcc6f7791f494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4306275a207ecd844610df04fafdf166bc2d50d693f22c9adea013222821e7`

```dockerfile
```

-	Layers:
	-	`sha256:fef755e27c5c797a2fd43121851e5482553e3c71c07f36853f09346ec055a853`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:39a52f21d83100719820a826546974edb5b9cd196bda48644d6bde9955650bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10765798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d57f91b93856a000a606780ec5363bc1eb9fb5a2e11112703d73d6e2cfe151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:02 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2085d200b4339b2fc1f02d3ff2827df89f8e4de23b30c3a01197cb364b6e077`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 7.1 MB (7110955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dd256e0fb0cd7e8b86422d79adf837656f750a9ef09f0f36a340664e797d66`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9c615faf9438fa6dc56c180f588bd2e8c3452bbb70bc934ae5e478c052a4c4`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4d12d33eb8b4b9a3886edda118f27a14fab07b1ddfd21129db90309db7b7e483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffc7fca774a22b7dbba927d7c8965de3a26790e226cc50a5ed1fd3bff355aa9`

```dockerfile
```

-	Layers:
	-	`sha256:3313afa82fcfd90aaae86adae7b450d6d5bc98452781ead8d7734b255d058565`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:df3dbf7615519c64c1ecf5bff1811e0f1349e980e12cf8edac882a53cf3f9dd9
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
$ docker pull nats@sha256:4e4b6c6da8e5dd1c1972aef235279bb99a4554e3277969c25baf06fe75bf3a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11111423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aa95f5acd85535217858bde3f513b2fd61fcded722bdd5d17bb9d89f124eb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:43 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b74c94101f0c98ee2c3a1cfe1857a9d00f6d49ce060aac8c3e709731ff6e6c`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 7.3 MB (7302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1171202a810bee209cebae3b516e5dc187466c7efada92079b4cb6da26cc2196`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c58df7044a7df1b6d31a8bff11256dc9480ccd2f85f73edd8393509074d239`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:603015575bf6c3db29393d6ebdf202853ed9636544435f710b2ca3c09536a075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b2bea654035fe919b77ca44ff2adc24191ed65e513b5046faeb2ffb325b5c`

```dockerfile
```

-	Layers:
	-	`sha256:4f302bf75b042b6174b0022d5f48276cef4a2d88e48c27eead53470b13c0d940`  
		Last Modified: Thu, 30 Apr 2026 23:54:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:f50039ea7bec9263cf0a5e88f88d07fd6ebdce50aa9b135611f858acd512f2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10526198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5883c39c5192e03c75b4224b245435c9d6161e83fe57b250935914bd24001668`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccac10855b16bbd9dacf92801d18f2dcabc07188eeffa283aeeaf3f75d832ce`  
		Last Modified: Thu, 30 Apr 2026 23:41:29 GMT  
		Size: 7.0 MB (7017844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbe36b4e25cffbd5ff5634a3fbd1b13a52d111c40121037c010104f6108763`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c11d0705e172884bff3c4d474533693e7de0fa05a5917a78d773a5de329d0`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6471a93f16c111840eacd768e23308cdf960a1cfe889095d78003195e0a0ea6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecff6d4ed848b72ba06ee95a83bd748bd4ca11c6a640da4e12694ac5179e87`

```dockerfile
```

-	Layers:
	-	`sha256:d3bff562dcf6b3117fa78f4a3e590eee7581451e02a99962b05600f583a9cf27`  
		Last Modified: Thu, 30 Apr 2026 23:41:28 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:e9297bbd9fb68cd33a16528c1571b4dafe2dd9ab4142ec024db5ee531ddc68da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10231865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f606a353fc4e59f45057730ace4c11a67caf47eff4f28e41b42b788d8c2414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:41:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:41:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:41:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c367a285a39c8c8c79b4ea0aa7c6247702d54f43f100dd5c3ddbd51c94d3211`  
		Last Modified: Thu, 30 Apr 2026 23:41:35 GMT  
		Size: 7.0 MB (7005064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117013b561496f590f9a60f99c816fe4a564bf0889f6e0df758ada57c96d4e6d`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963d6d4f8ca7ced9d60d1ad7d51774145a90f68ef921fe87ead7831bf25f4bea`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:370298f66cb1801078ab77ec09d0abe92e1c78e845edcbf19512b2f7fd142d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca1a27ff1c3c7b822bd6661b9c47440a8e25f7b4b9cd588c4c3c801ac6451b6`

```dockerfile
```

-	Layers:
	-	`sha256:b570c31a499e86a57fa446b3882375a52d71cc1f961560ff9e1ae810a4efff8b`  
		Last Modified: Thu, 30 Apr 2026 23:41:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d12972d669f1b377199d2741e1fa077ea1168ce25e2c42404f250313a187fe43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eedd13f74e4fec45f3a450d999030f19561f09cfdd980981bbc3a63f0b4cd7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:39 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402c5214fc465210f9c99ad940c17598d6c6af48826c7eb608e07ae485a3e588`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 6.7 MB (6667294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18810920ce9ca341b83ab1017aef4513c4174d891f67342d611c5f3bbda38999`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794d09af1fbaa55736af3f4e2575cea602bd620f628f9e9b546f10970a504934`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:740ee1c9829ccceb669d434cb446164b4b61620f027a57838adf0b32213a1a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a48f299143dbcbdb7d18a8680dc39a2c782baecb38582281887840bab6ca165`

```dockerfile
```

-	Layers:
	-	`sha256:b926ca76b9cf11b2e4ffad4954b37d9fe5b9f4884e5d7fb6c57adb38e84b9a1e`  
		Last Modified: Thu, 30 Apr 2026 23:54:44 GMT  
		Size: 15.6 KB (15555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:3edda2d951ada7baee76eac3997620987fd3b6ad34abf3b3aeafb4a33d23d47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10458042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c140c21478922b87a2c72b28bd2c0f8c5503c54edc400ab38da1761ca0396c8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:18:52 GMT
ENV NATS_SERVER=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Fri, 01 May 2026 00:18:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 01 May 2026 00:18:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 01 May 2026 00:18:53 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 May 2026 00:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 00:18:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47da398408150920ce8738775297259fe6972d60691a7bd593a28f145b641ef7`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 6.7 MB (6720417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e284a50fe36dcd81f24a73cf5ff5bfe4361b05c60af1c49247d6876489ebdd77`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b453cbccc82afdd9cb5ca438319699b9a61c0fbe5cca06a89fb0a818535827`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:927bcfc16a9e30312116c9c098acc4ed1f96d59ece262eedec4dcc6f7791f494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4306275a207ecd844610df04fafdf166bc2d50d693f22c9adea013222821e7`

```dockerfile
```

-	Layers:
	-	`sha256:fef755e27c5c797a2fd43121851e5482553e3c71c07f36853f09346ec055a853`  
		Last Modified: Fri, 01 May 2026 00:19:03 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:39a52f21d83100719820a826546974edb5b9cd196bda48644d6bde9955650bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10765798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d57f91b93856a000a606780ec5363bc1eb9fb5a2e11112703d73d6e2cfe151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:54:02 GMT
ENV NATS_SERVER=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Thu, 30 Apr 2026 23:54:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='ce7dc5f7d97b70dabc38b13157fed28d7d06227860676143c15c62c5c297996c' ;;     armhf) natsArch='arm6'; sha256='b87842c1eb7268286dd873513e0ffc21c7b54d14636c5a5ecb3637deeb523337' ;;     armv7) natsArch='arm7'; sha256='3b66be75d9e5ef2ec5c3c66012ff3d03401996c8aa463291ccdd38307b9cac52' ;;     x86_64) natsArch='amd64'; sha256='3d8b74dfad39af184c765a6dd120441ed1c648d6672eddf6b304f222661251b8' ;;     x86) natsArch='386'; sha256='83528c239f917783fb25e5997bab18ce75e4a8959711ab8fce31fca2174e1d6d' ;;     s390x) natsArch='s390x'; sha256='4801bf5e945c50b654f1151129a1e28671bf892cd8a6401ff4b53dd4788e21d7' ;;     ppc64le) natsArch='ppc64le'; sha256='8534c79f8eb341ce9dd45fb63ddec40dbbcfd0ba28747e1f9eae35fb93b2381e' ;;     loong64) natsArch='loong64'; sha256='89c64b70915dd2f73317cb413f7f3ad373d4602f2b7b16e2417ebf7d5eee5876' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 30 Apr 2026 23:54:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 30 Apr 2026 23:54:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 30 Apr 2026 23:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:54:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2085d200b4339b2fc1f02d3ff2827df89f8e4de23b30c3a01197cb364b6e077`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 7.1 MB (7110955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dd256e0fb0cd7e8b86422d79adf837656f750a9ef09f0f36a340664e797d66`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9c615faf9438fa6dc56c180f588bd2e8c3452bbb70bc934ae5e478c052a4c4`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4d12d33eb8b4b9a3886edda118f27a14fab07b1ddfd21129db90309db7b7e483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffc7fca774a22b7dbba927d7c8965de3a26790e226cc50a5ed1fd3bff355aa9`

```dockerfile
```

-	Layers:
	-	`sha256:3313afa82fcfd90aaae86adae7b450d6d5bc98452781ead8d7734b255d058565`  
		Last Modified: Thu, 30 Apr 2026 23:54:10 GMT  
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
$ docker pull nats@sha256:9b61497122cf4b3a8c30fc687c66344968c0fda6bbfe4a1b60d4361d9120229b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:8ac046d6c8660a1941079c55460e369623171da1242db0212c4e4e1ea04a7265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130301845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f8c7306fbc93a9072eae8b2e82245da9da5581b928cf98f6a43f3a5bb18c8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:46:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_SERVER=2.14.0
# Tue, 12 May 2026 23:46:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Tue, 12 May 2026 23:46:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.0/nats-server-v2.14.0-windows-amd64.zip
# Tue, 12 May 2026 23:46:37 GMT
ENV NATS_SERVER_SHASUM=09ba382669cc4df390f97f16f08481f040eef0bb17ca5f2d71104b4be4cd613a
# Tue, 12 May 2026 23:46:42 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 May 2026 23:46:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 May 2026 23:46:58 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 12 May 2026 23:46:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 May 2026 23:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 May 2026 23:47:00 GMT
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
	-	`sha256:a023c5625d2ee5d4db03516e4189696fe76d51e9b025badea7507457ee0ec780`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d3b4fd74d9cea43b61086e3be13f8fd68aaf7dcbed8869eb7654b13022210`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef61b238d44d24f9216b2e1eaaa99046523561ff4f907e645d7893a7d29e400`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1308c0e658293e66b16726765790666ac8d0da20ba6ac45c4b5bf07e871e7e`  
		Last Modified: Tue, 12 May 2026 23:47:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10dbe3d84a9d708da963fba429a9d97b30ad3d3f55cf2b215db3226cef086cd`  
		Last Modified: Tue, 12 May 2026 23:47:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eb792b599093b403901940e5a5809475ebdca2d28b347159b0ccd4fe52c402`  
		Last Modified: Tue, 12 May 2026 23:47:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c94b5c81292e032d68bd1ba5bd819b3390645f9e9b43e5f30b714c0fd65c469`  
		Last Modified: Tue, 12 May 2026 23:47:06 GMT  
		Size: 480.0 KB (479956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6159ce96c550fe0e2723ad3256060f48ed487a7021d8036f0e6ae4fb1cee9618`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 7.4 MB (7387702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa8177fcaa7207011be892ae542dcc77b7bc62eea167a839cc7da6d2d1ac9a5`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4971bfb6dede78606066a89134eecb700883a65fe50996cd78914085969b4c3`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cff0aa25bd3783b982c3d8cbb8c921e7850bdea723a6759a7caf9cb0664baca`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bbf4adc2716b36dbfba894764c1c3cd1f07280637c15aa87c0c6fd22518d5d3`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:9b61497122cf4b3a8c30fc687c66344968c0fda6bbfe4a1b60d4361d9120229b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:8ac046d6c8660a1941079c55460e369623171da1242db0212c4e4e1ea04a7265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130301845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f8c7306fbc93a9072eae8b2e82245da9da5581b928cf98f6a43f3a5bb18c8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:46:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 May 2026 23:46:35 GMT
ENV NATS_SERVER=2.14.0
# Tue, 12 May 2026 23:46:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.0
# Tue, 12 May 2026 23:46:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.0/nats-server-v2.14.0-windows-amd64.zip
# Tue, 12 May 2026 23:46:37 GMT
ENV NATS_SERVER_SHASUM=09ba382669cc4df390f97f16f08481f040eef0bb17ca5f2d71104b4be4cd613a
# Tue, 12 May 2026 23:46:42 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 May 2026 23:46:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 May 2026 23:46:58 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 12 May 2026 23:46:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 May 2026 23:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 May 2026 23:47:00 GMT
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
	-	`sha256:a023c5625d2ee5d4db03516e4189696fe76d51e9b025badea7507457ee0ec780`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d3b4fd74d9cea43b61086e3be13f8fd68aaf7dcbed8869eb7654b13022210`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef61b238d44d24f9216b2e1eaaa99046523561ff4f907e645d7893a7d29e400`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1308c0e658293e66b16726765790666ac8d0da20ba6ac45c4b5bf07e871e7e`  
		Last Modified: Tue, 12 May 2026 23:47:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10dbe3d84a9d708da963fba429a9d97b30ad3d3f55cf2b215db3226cef086cd`  
		Last Modified: Tue, 12 May 2026 23:47:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eb792b599093b403901940e5a5809475ebdca2d28b347159b0ccd4fe52c402`  
		Last Modified: Tue, 12 May 2026 23:47:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c94b5c81292e032d68bd1ba5bd819b3390645f9e9b43e5f30b714c0fd65c469`  
		Last Modified: Tue, 12 May 2026 23:47:06 GMT  
		Size: 480.0 KB (479956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6159ce96c550fe0e2723ad3256060f48ed487a7021d8036f0e6ae4fb1cee9618`  
		Last Modified: Tue, 12 May 2026 23:47:07 GMT  
		Size: 7.4 MB (7387702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa8177fcaa7207011be892ae542dcc77b7bc62eea167a839cc7da6d2d1ac9a5`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4971bfb6dede78606066a89134eecb700883a65fe50996cd78914085969b4c3`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cff0aa25bd3783b982c3d8cbb8c921e7850bdea723a6759a7caf9cb0664baca`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bbf4adc2716b36dbfba894764c1c3cd1f07280637c15aa87c0c6fd22518d5d3`  
		Last Modified: Tue, 12 May 2026 23:47:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
