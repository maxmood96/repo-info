<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.21`](#nats2-alpine321)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.21`](#nats210-alpine321)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.29`](#nats21029)
-	[`nats:2.10.29-alpine`](#nats21029-alpine)
-	[`nats:2.10.29-alpine3.21`](#nats21029-alpine321)
-	[`nats:2.10.29-linux`](#nats21029-linux)
-	[`nats:2.10.29-nanoserver`](#nats21029-nanoserver)
-	[`nats:2.10.29-nanoserver-1809`](#nats21029-nanoserver-1809)
-	[`nats:2.10.29-scratch`](#nats21029-scratch)
-	[`nats:2.10.29-windowsservercore`](#nats21029-windowsservercore)
-	[`nats:2.10.29-windowsservercore-1809`](#nats21029-windowsservercore-1809)
-	[`nats:2.11`](#nats211)
-	[`nats:2.11-alpine`](#nats211-alpine)
-	[`nats:2.11-alpine3.21`](#nats211-alpine321)
-	[`nats:2.11-linux`](#nats211-linux)
-	[`nats:2.11-nanoserver`](#nats211-nanoserver)
-	[`nats:2.11-nanoserver-1809`](#nats211-nanoserver-1809)
-	[`nats:2.11-scratch`](#nats211-scratch)
-	[`nats:2.11-windowsservercore`](#nats211-windowsservercore)
-	[`nats:2.11-windowsservercore-1809`](#nats211-windowsservercore-1809)
-	[`nats:2.11.4`](#nats2114)
-	[`nats:2.11.4-alpine`](#nats2114-alpine)
-	[`nats:2.11.4-alpine3.21`](#nats2114-alpine321)
-	[`nats:2.11.4-linux`](#nats2114-linux)
-	[`nats:2.11.4-nanoserver`](#nats2114-nanoserver)
-	[`nats:2.11.4-nanoserver-1809`](#nats2114-nanoserver-1809)
-	[`nats:2.11.4-scratch`](#nats2114-scratch)
-	[`nats:2.11.4-windowsservercore`](#nats2114-windowsservercore)
-	[`nats:2.11.4-windowsservercore-1809`](#nats2114-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.21`](#natsalpine321)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:7c80eff5349a3ecaffff014f6cdae20a8d2c5f11cab835bcb76a56275e2719e9
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
	-	windows version 10.0.17763.7314; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:3669c7dc73d88251f131a5507f94fe74fef33b461c16666813ac84e7b807bca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2dc40e2ee2ef54306454e58ff7f7b318bd40949cd7d747c67cc26b2daf553`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Thu, 22 May 2025 13:55:01 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Thu, 22 May 2025 16:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:40c2e8c019de84dd8609363ad056325e160ff7d3c22583776cba7d9c14bbb0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ac87fa640a0df9ed5554a115493a87055629ce3f52f77a933bf54b1c5ee29`

```dockerfile
```

-	Layers:
	-	`sha256:edbca2e0be9710afcbe43e2fca6896927d7e6c12d43816973cc4a1e04ec762f6`  
		Last Modified: Thu, 22 May 2025 16:47:18 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:4fbfa5ce075ad78297fbfc8ce0126de19a685b441759d77b6dc6aeb130f38561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279bf33611cd3f2a188a9a0afdb244877743689160627fcf8de576cdda072a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd26e0aad9f1b20096e647e74023489621fc5ba4de7dc4747a0d0d4bb2823fc7`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:06aa17a9acdaae3c275cb86e786faac7651dd30f6b6aab7b648db0e966524ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34ed5638318182fa373a29edf2eae4badc5e5688dd08e8af559b347675e23c`

```dockerfile
```

-	Layers:
	-	`sha256:ea20c201702d517a06fc320a50a878fa897f58fd5a8cb89d7bbeb5af7599f148`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:e1b35decc46dc6b9b6a62e50a10d13095888c34f740a2d2069d5fa4a3a406fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04111c7501581b1636dc5516802ecee6c26dcb627cbbec34e273d2575ac0a9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Thu, 22 May 2025 13:54:58 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9293b5f4677cf2db6d8d8a8a01b039e1134d378f77c7efe3d7b11072a3f4e4`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:e1653a1054fd8a003f0dad883474a71c0d46a243bb3364d28c690e1d5c521e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2828a9839d98f985cc7bb11688ead3394a6003466851fff29ab209a775564`

```dockerfile
```

-	Layers:
	-	`sha256:fddb83fedd24e6e2d6c0afc61f16768121ba63342f1bc0d540cd75cf7e202edc`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6390d133be19faae15ea0b0addf722e3dd60c9412dc5b14c8120e9ff773fcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a4332082216fadc8b7d39be0643a4193e18b21e9a0815bc8a7476b0d9ff39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:c9a882fa6d5de0d1f1a746c11bb26c98258eba146870604781263ee98916694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8632a81f326876343b421492b672bc64785711cd147bece1386ca476b11fbe2`

```dockerfile
```

-	Layers:
	-	`sha256:a3807445f86645a59e75d2d727c573109c35a356652cf8cea33291752e44a501`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:b2a62d6e7160e9fe02b4fbc54a4d38f4854e955277ad06a32a0f9730fb145030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77959cb575e1e4e6a7ed10889593eb60a12b91bc3daef1a047f20d5b849823e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac6089227b1bf8e0c5485c9fafeb79be71f899610ed5cfe50750ec671c2150`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:d61332ce9f2f76ef458a63c4394a0ea8f006176df53c6c854d854c880fb56c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cab1c0c3130120e0299edad95932ca44704b3459f34c83f21aff0efd97ee56`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a85cd3ea43c578ae1c73d84bc6e9c7dbeba30594051365b578136deebce76`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 10.6 KB (10555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:bb999cd435e52627799ba8d3bba323e34937cebdbf4cbaf4747d8b5d0b4f377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5364ba179bbae6d216c47196a0e607812cf16327562d528b0dd7a39275fc7b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Thu, 22 May 2025 13:55:02 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8c9019ec6e6b470ca5a6c4139cddf8579e979b93b02f0847ea6459c5bdf68`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:b5bd7ec7061996df7f9d251b0f55960fc4ea80d15e93923f70faa53a1dfdcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88da26773cc178303a133db9d426aa861f654fb7d59e009907bcc91bd848fb`

```dockerfile
```

-	Layers:
	-	`sha256:a17428cf33c792fdb7174ce215c54081e07fdd09cde209156006d308f5279ebd`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:0451ec62031943afa591cf4e5f9404bce65b55a8671ab93a7d581d8028fc12a9
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
$ docker pull nats@sha256:78c1052292c8d1bdabeca33c5cde417bb3b56c9a9a6707afd896ac74f8010e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10425424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752c0a111d15eafa05314d85b32bdfc63c7a5190ba26712078e014ad5c12906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc83d3e520670ed878bfe5964638db9895fc2873acb2a25b7bd3a8b2916c3e`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 6.8 MB (6782209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1065a99208ad32f21adf1cc2983a318f6d19b678ce12103514758c5e75a1359`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dc1d69fb3bb313c6fce126295baf9e644c735c5b709cb57462cf134d8b7535`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6425e7c42e8f01aed46c0c5a2c0e1538c4703e432be6a853fe400d6c070c46b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd03d3d4671688731cc2113bd6bce676daf486062cf7bf8a0ad509235b375b3`

```dockerfile
```

-	Layers:
	-	`sha256:8d13d777cfed6af6d839ab64cb7dc1dd2e3b2e7c64170ca5695c3a937b560432`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:e9129c76ec8b39cfb61261ea43a529d2b048a22bd43dde23405476211d952fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa20ad8f845d52ef2ede0cc269b4ade46343bd8ae9d91e0f89a101e164019a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedc41dc7d645196f64f183990aac84922d7dfeca30cdd62cc58afacced1e53e`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 6.5 MB (6500243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f84ca9e26add3645800a5d8875d035548ece025cd495d093506600b5fa3639`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a0bc1a6e6b564bac3444b012da7c2bd95b00fc4b30e2183f58fdfe67a29efc`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cfc622005d6c0083932d3a442389e5ba0fed2eee0d382384117e632be9d2cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98224cc21fc700a931065a4257f0f576cb24d83f9f4cf3a756dbb8cfc211de84`

```dockerfile
```

-	Layers:
	-	`sha256:5b980a9b2e5b75054cfabe65a0bb0ca426c2aeb5cb4d1d0a7b3616d6b089aba1`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f51b3ede38c787e45a1c58fe1758aa726cfc126eed5ef13dc9a66dbcfe4d8e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9587301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fcc07ad9637e3d6023e9c3faf8df41d76537efd7136923fe276ce3124a21f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9afbd37259973c94e964e514f1fd5331fdff7c8a20c358c64209a54939892`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 6.5 MB (6488204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e46bef85887a3ca7141cdb651fb0907947c31453e3dd12d5f2e75d659f9bb81`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ada5b8ea797d2e67d9817b4735e298f9e4328503c9b4faff09c816dd2a3fe`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:43fb4c5979976f655a571482f2fb7c95bdcfe76ea5c3d03822e834dba8c8ba43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103eb0538b45ceeaf49344cd2e475459141bba59c3b68cfa4b3f8c81bfaa0292`

```dockerfile
```

-	Layers:
	-	`sha256:48a6d4944ad8da069b2dcc13b6bf204e8ba6994953e03cdc717459fc9bec1bbc`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:361d07db47a72d53a1159ce806effcfaacddb5c24254dc346aa6ed24d2eaff6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c4a01a93d1901d7daaa7ad147102df5dc250516eb1b935b673cb01b2de9436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28900756089c34ef75f78f9bc43820aee795ebced2ef164f4371a469020c319`  
		Last Modified: Thu, 22 May 2025 20:04:29 GMT  
		Size: 6.3 MB (6271430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a19d69a59c9c3d035125ee920379ce8b337cb0de1eb1646fa3b37bcc5bd4eca`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002df6ee873e4c8b8c2d32bc19571ba115cbaeeaa22dbe5e19ea24a00121560a`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:eeec07d9dba12fff9a629635d9822e295cbd2866800be7c10ae0f0eda767c376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb57113d3b7d11444b789b3d12801ddfaf3eadc8944e2457447d1469cc94db`

```dockerfile
```

-	Layers:
	-	`sha256:cac3279af5a354235660e8ed87c54fddc39e37fe276433cdd00c7a04a3f5877c`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:6c62a05e9d2c74252f7e85ca263ff11fa47ca8d6a2314c95ef35830ca7dd5947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9829497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f82ed4f59bb1fc3f2bb1bf520c03a108a4b1201a308129e9f9c437eb69d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab090fb5974c5fbc532a324c8b6ff89147f7b095e88f59c95200ff29b503d4ed`  
		Last Modified: Thu, 22 May 2025 16:46:06 GMT  
		Size: 6.3 MB (6254178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ffdff7943fa553d5c46cd9bfd7cdb0aaf807fd213df6a3be9c0f47276b45d`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b243223ddfaabf20dea42482c30a57a1960b976113f905a07742d49e8fd76`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:209d5ce0eb3e58f76c4baefc159b91c7c24036c43252c4c06634f4218bfc2ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc856abe1e071c3b5e0dd0ac6a265939b68986e20ed0a612a3577747ed39b949`

```dockerfile
```

-	Layers:
	-	`sha256:9d5d8fc63a7e90cae4235128e35cce1f4b9143f897cba2831823fdf635d1c1a3`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:113aca5863f11d04e9dcafd0a79496a1ecc86cdc2ccf02b720467c79eb2c1b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10087904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a783e13b44bb39120f57f582d383ada710ad715fc963f625760233ace3e4ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f6217bb5b7f1a95efe567548c35356165dc66ae69bfe675bd4d750bb78b516`  
		Last Modified: Thu, 22 May 2025 17:33:09 GMT  
		Size: 6.6 MB (6619363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9020a2695371d3927fa6fb04d07c6ee8cfdbdf0c94ab360a4d3e121df860ce`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9b02a9ab09a6778612e627ead79927f9eab9b1f58a792a27d86b207e883eb`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2adcfab66a18b065b7c3a97ae3a3a6266b23138c34d08229363bae6d3eb99f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b88a3ff73d885d4df2ea9e8203001daa5832c33dbba49d1127c7ded5b3724`

```dockerfile
```

-	Layers:
	-	`sha256:2e6f543ee243ec43d02935e873e329d235728c7301898d56b1cc48bf41df88aa`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:0451ec62031943afa591cf4e5f9404bce65b55a8671ab93a7d581d8028fc12a9
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

### `nats:2-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:78c1052292c8d1bdabeca33c5cde417bb3b56c9a9a6707afd896ac74f8010e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10425424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752c0a111d15eafa05314d85b32bdfc63c7a5190ba26712078e014ad5c12906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc83d3e520670ed878bfe5964638db9895fc2873acb2a25b7bd3a8b2916c3e`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 6.8 MB (6782209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1065a99208ad32f21adf1cc2983a318f6d19b678ce12103514758c5e75a1359`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dc1d69fb3bb313c6fce126295baf9e644c735c5b709cb57462cf134d8b7535`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6425e7c42e8f01aed46c0c5a2c0e1538c4703e432be6a853fe400d6c070c46b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd03d3d4671688731cc2113bd6bce676daf486062cf7bf8a0ad509235b375b3`

```dockerfile
```

-	Layers:
	-	`sha256:8d13d777cfed6af6d839ab64cb7dc1dd2e3b2e7c64170ca5695c3a937b560432`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:e9129c76ec8b39cfb61261ea43a529d2b048a22bd43dde23405476211d952fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa20ad8f845d52ef2ede0cc269b4ade46343bd8ae9d91e0f89a101e164019a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedc41dc7d645196f64f183990aac84922d7dfeca30cdd62cc58afacced1e53e`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 6.5 MB (6500243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f84ca9e26add3645800a5d8875d035548ece025cd495d093506600b5fa3639`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a0bc1a6e6b564bac3444b012da7c2bd95b00fc4b30e2183f58fdfe67a29efc`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cfc622005d6c0083932d3a442389e5ba0fed2eee0d382384117e632be9d2cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98224cc21fc700a931065a4257f0f576cb24d83f9f4cf3a756dbb8cfc211de84`

```dockerfile
```

-	Layers:
	-	`sha256:5b980a9b2e5b75054cfabe65a0bb0ca426c2aeb5cb4d1d0a7b3616d6b089aba1`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:f51b3ede38c787e45a1c58fe1758aa726cfc126eed5ef13dc9a66dbcfe4d8e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9587301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fcc07ad9637e3d6023e9c3faf8df41d76537efd7136923fe276ce3124a21f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9afbd37259973c94e964e514f1fd5331fdff7c8a20c358c64209a54939892`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 6.5 MB (6488204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e46bef85887a3ca7141cdb651fb0907947c31453e3dd12d5f2e75d659f9bb81`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ada5b8ea797d2e67d9817b4735e298f9e4328503c9b4faff09c816dd2a3fe`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:43fb4c5979976f655a571482f2fb7c95bdcfe76ea5c3d03822e834dba8c8ba43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103eb0538b45ceeaf49344cd2e475459141bba59c3b68cfa4b3f8c81bfaa0292`

```dockerfile
```

-	Layers:
	-	`sha256:48a6d4944ad8da069b2dcc13b6bf204e8ba6994953e03cdc717459fc9bec1bbc`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:361d07db47a72d53a1159ce806effcfaacddb5c24254dc346aa6ed24d2eaff6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c4a01a93d1901d7daaa7ad147102df5dc250516eb1b935b673cb01b2de9436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28900756089c34ef75f78f9bc43820aee795ebced2ef164f4371a469020c319`  
		Last Modified: Thu, 22 May 2025 20:04:29 GMT  
		Size: 6.3 MB (6271430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a19d69a59c9c3d035125ee920379ce8b337cb0de1eb1646fa3b37bcc5bd4eca`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002df6ee873e4c8b8c2d32bc19571ba115cbaeeaa22dbe5e19ea24a00121560a`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:eeec07d9dba12fff9a629635d9822e295cbd2866800be7c10ae0f0eda767c376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb57113d3b7d11444b789b3d12801ddfaf3eadc8944e2457447d1469cc94db`

```dockerfile
```

-	Layers:
	-	`sha256:cac3279af5a354235660e8ed87c54fddc39e37fe276433cdd00c7a04a3f5877c`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:6c62a05e9d2c74252f7e85ca263ff11fa47ca8d6a2314c95ef35830ca7dd5947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9829497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f82ed4f59bb1fc3f2bb1bf520c03a108a4b1201a308129e9f9c437eb69d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab090fb5974c5fbc532a324c8b6ff89147f7b095e88f59c95200ff29b503d4ed`  
		Last Modified: Thu, 22 May 2025 16:46:06 GMT  
		Size: 6.3 MB (6254178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ffdff7943fa553d5c46cd9bfd7cdb0aaf807fd213df6a3be9c0f47276b45d`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b243223ddfaabf20dea42482c30a57a1960b976113f905a07742d49e8fd76`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:209d5ce0eb3e58f76c4baefc159b91c7c24036c43252c4c06634f4218bfc2ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc856abe1e071c3b5e0dd0ac6a265939b68986e20ed0a612a3577747ed39b949`

```dockerfile
```

-	Layers:
	-	`sha256:9d5d8fc63a7e90cae4235128e35cce1f4b9143f897cba2831823fdf635d1c1a3`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:113aca5863f11d04e9dcafd0a79496a1ecc86cdc2ccf02b720467c79eb2c1b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10087904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a783e13b44bb39120f57f582d383ada710ad715fc963f625760233ace3e4ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f6217bb5b7f1a95efe567548c35356165dc66ae69bfe675bd4d750bb78b516`  
		Last Modified: Thu, 22 May 2025 17:33:09 GMT  
		Size: 6.6 MB (6619363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9020a2695371d3927fa6fb04d07c6ee8cfdbdf0c94ab360a4d3e121df860ce`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9b02a9ab09a6778612e627ead79927f9eab9b1f58a792a27d86b207e883eb`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:2adcfab66a18b065b7c3a97ae3a3a6266b23138c34d08229363bae6d3eb99f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b88a3ff73d885d4df2ea9e8203001daa5832c33dbba49d1127c7ded5b3724`

```dockerfile
```

-	Layers:
	-	`sha256:2e6f543ee243ec43d02935e873e329d235728c7301898d56b1cc48bf41df88aa`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:d0c61f71b425352fd0d54492562dcff4709fdaa5979afbef9a2e13df957fa26e
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
$ docker pull nats@sha256:3669c7dc73d88251f131a5507f94fe74fef33b461c16666813ac84e7b807bca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2dc40e2ee2ef54306454e58ff7f7b318bd40949cd7d747c67cc26b2daf553`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Thu, 22 May 2025 13:55:01 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Thu, 22 May 2025 16:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:40c2e8c019de84dd8609363ad056325e160ff7d3c22583776cba7d9c14bbb0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ac87fa640a0df9ed5554a115493a87055629ce3f52f77a933bf54b1c5ee29`

```dockerfile
```

-	Layers:
	-	`sha256:edbca2e0be9710afcbe43e2fca6896927d7e6c12d43816973cc4a1e04ec762f6`  
		Last Modified: Thu, 22 May 2025 16:47:18 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4fbfa5ce075ad78297fbfc8ce0126de19a685b441759d77b6dc6aeb130f38561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279bf33611cd3f2a188a9a0afdb244877743689160627fcf8de576cdda072a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd26e0aad9f1b20096e647e74023489621fc5ba4de7dc4747a0d0d4bb2823fc7`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:06aa17a9acdaae3c275cb86e786faac7651dd30f6b6aab7b648db0e966524ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34ed5638318182fa373a29edf2eae4badc5e5688dd08e8af559b347675e23c`

```dockerfile
```

-	Layers:
	-	`sha256:ea20c201702d517a06fc320a50a878fa897f58fd5a8cb89d7bbeb5af7599f148`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e1b35decc46dc6b9b6a62e50a10d13095888c34f740a2d2069d5fa4a3a406fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04111c7501581b1636dc5516802ecee6c26dcb627cbbec34e273d2575ac0a9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Thu, 22 May 2025 13:54:58 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9293b5f4677cf2db6d8d8a8a01b039e1134d378f77c7efe3d7b11072a3f4e4`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e1653a1054fd8a003f0dad883474a71c0d46a243bb3364d28c690e1d5c521e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2828a9839d98f985cc7bb11688ead3394a6003466851fff29ab209a775564`

```dockerfile
```

-	Layers:
	-	`sha256:fddb83fedd24e6e2d6c0afc61f16768121ba63342f1bc0d540cd75cf7e202edc`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6390d133be19faae15ea0b0addf722e3dd60c9412dc5b14c8120e9ff773fcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a4332082216fadc8b7d39be0643a4193e18b21e9a0815bc8a7476b0d9ff39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c9a882fa6d5de0d1f1a746c11bb26c98258eba146870604781263ee98916694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8632a81f326876343b421492b672bc64785711cd147bece1386ca476b11fbe2`

```dockerfile
```

-	Layers:
	-	`sha256:a3807445f86645a59e75d2d727c573109c35a356652cf8cea33291752e44a501`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:b2a62d6e7160e9fe02b4fbc54a4d38f4854e955277ad06a32a0f9730fb145030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77959cb575e1e4e6a7ed10889593eb60a12b91bc3daef1a047f20d5b849823e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac6089227b1bf8e0c5485c9fafeb79be71f899610ed5cfe50750ec671c2150`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d61332ce9f2f76ef458a63c4394a0ea8f006176df53c6c854d854c880fb56c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cab1c0c3130120e0299edad95932ca44704b3459f34c83f21aff0efd97ee56`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a85cd3ea43c578ae1c73d84bc6e9c7dbeba30594051365b578136deebce76`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 10.6 KB (10555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:bb999cd435e52627799ba8d3bba323e34937cebdbf4cbaf4747d8b5d0b4f377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5364ba179bbae6d216c47196a0e607812cf16327562d528b0dd7a39275fc7b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Thu, 22 May 2025 13:55:02 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8c9019ec6e6b470ca5a6c4139cddf8579e979b93b02f0847ea6459c5bdf68`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b5bd7ec7061996df7f9d251b0f55960fc4ea80d15e93923f70faa53a1dfdcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88da26773cc178303a133db9d426aa861f654fb7d59e009907bcc91bd848fb`

```dockerfile
```

-	Layers:
	-	`sha256:a17428cf33c792fdb7174ce215c54081e07fdd09cde209156006d308f5279ebd`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:5cc9d495e86b7caa02ed8c6efd98071810a86094d0365b49cd0d6c923575d630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:5cc9d495e86b7caa02ed8c6efd98071810a86094d0365b49cd0d6c923575d630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:d0c61f71b425352fd0d54492562dcff4709fdaa5979afbef9a2e13df957fa26e
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
$ docker pull nats@sha256:3669c7dc73d88251f131a5507f94fe74fef33b461c16666813ac84e7b807bca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2dc40e2ee2ef54306454e58ff7f7b318bd40949cd7d747c67cc26b2daf553`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Thu, 22 May 2025 13:55:01 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Thu, 22 May 2025 16:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:40c2e8c019de84dd8609363ad056325e160ff7d3c22583776cba7d9c14bbb0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ac87fa640a0df9ed5554a115493a87055629ce3f52f77a933bf54b1c5ee29`

```dockerfile
```

-	Layers:
	-	`sha256:edbca2e0be9710afcbe43e2fca6896927d7e6c12d43816973cc4a1e04ec762f6`  
		Last Modified: Thu, 22 May 2025 16:47:18 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4fbfa5ce075ad78297fbfc8ce0126de19a685b441759d77b6dc6aeb130f38561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279bf33611cd3f2a188a9a0afdb244877743689160627fcf8de576cdda072a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd26e0aad9f1b20096e647e74023489621fc5ba4de7dc4747a0d0d4bb2823fc7`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:06aa17a9acdaae3c275cb86e786faac7651dd30f6b6aab7b648db0e966524ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34ed5638318182fa373a29edf2eae4badc5e5688dd08e8af559b347675e23c`

```dockerfile
```

-	Layers:
	-	`sha256:ea20c201702d517a06fc320a50a878fa897f58fd5a8cb89d7bbeb5af7599f148`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e1b35decc46dc6b9b6a62e50a10d13095888c34f740a2d2069d5fa4a3a406fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04111c7501581b1636dc5516802ecee6c26dcb627cbbec34e273d2575ac0a9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Thu, 22 May 2025 13:54:58 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9293b5f4677cf2db6d8d8a8a01b039e1134d378f77c7efe3d7b11072a3f4e4`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e1653a1054fd8a003f0dad883474a71c0d46a243bb3364d28c690e1d5c521e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2828a9839d98f985cc7bb11688ead3394a6003466851fff29ab209a775564`

```dockerfile
```

-	Layers:
	-	`sha256:fddb83fedd24e6e2d6c0afc61f16768121ba63342f1bc0d540cd75cf7e202edc`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6390d133be19faae15ea0b0addf722e3dd60c9412dc5b14c8120e9ff773fcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a4332082216fadc8b7d39be0643a4193e18b21e9a0815bc8a7476b0d9ff39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c9a882fa6d5de0d1f1a746c11bb26c98258eba146870604781263ee98916694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8632a81f326876343b421492b672bc64785711cd147bece1386ca476b11fbe2`

```dockerfile
```

-	Layers:
	-	`sha256:a3807445f86645a59e75d2d727c573109c35a356652cf8cea33291752e44a501`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:b2a62d6e7160e9fe02b4fbc54a4d38f4854e955277ad06a32a0f9730fb145030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77959cb575e1e4e6a7ed10889593eb60a12b91bc3daef1a047f20d5b849823e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac6089227b1bf8e0c5485c9fafeb79be71f899610ed5cfe50750ec671c2150`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d61332ce9f2f76ef458a63c4394a0ea8f006176df53c6c854d854c880fb56c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cab1c0c3130120e0299edad95932ca44704b3459f34c83f21aff0efd97ee56`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a85cd3ea43c578ae1c73d84bc6e9c7dbeba30594051365b578136deebce76`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 10.6 KB (10555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:bb999cd435e52627799ba8d3bba323e34937cebdbf4cbaf4747d8b5d0b4f377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5364ba179bbae6d216c47196a0e607812cf16327562d528b0dd7a39275fc7b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Thu, 22 May 2025 13:55:02 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8c9019ec6e6b470ca5a6c4139cddf8579e979b93b02f0847ea6459c5bdf68`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b5bd7ec7061996df7f9d251b0f55960fc4ea80d15e93923f70faa53a1dfdcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88da26773cc178303a133db9d426aa861f654fb7d59e009907bcc91bd848fb`

```dockerfile
```

-	Layers:
	-	`sha256:a17428cf33c792fdb7174ce215c54081e07fdd09cde209156006d308f5279ebd`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:5eb29aa350e04efd871dc089f00e2332c6fde8340442987c019d24c4d8612952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:3eb16b69114671a8802239d503c0290429cdb314d8a872d6b2e085341c12b4a0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190940335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1f053a6e4022c28324a3e45080faa48d8a7f96dc18ea8250a25af5211529a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 22 May 2025 16:50:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 16:50:25 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Thu, 22 May 2025 16:50:26 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Thu, 22 May 2025 16:51:00 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 May 2025 16:51:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 May 2025 16:51:18 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 16:51:19 GMT
EXPOSE 4222 6222 8222
# Thu, 22 May 2025 16:51:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 16:51:20 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ab467e36de62f69e77619428c80684c172dceff9ed3e77cc0f6ab14e4f32bdfd`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9091f1392b0e4b5a8efd3fa58b0c4a2b6e936430b4e42b68ba16077d4564944d`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf909e97fafaef4ec16a660d02af257e98e54239a7bc6cec966b8e76e70b715`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5d1bc88317b3a5b00e94a85aa69eeff6067de7eacc3b0ae40836597b6b4912`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc3aedb4b361c3a53ea79beee17b5b1e5323e8d429b1c896eb234b053b5198`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1800d06ff1abd05697da24fc89b33bee18003836f4b523b0183785ab5ed2496e`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 357.5 KB (357493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e26a01941a30a2df43651113e13c4254af9daa37d2d460c7eec0e2829bec1`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 6.9 MB (6853143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa50c7d770115bfd2ad8e106b7ba4c236b4240943f9c067a6ea34daf985b973b`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0aea2b23f17071fd4a073f906be4bf64c1c702b06340d09d355bacdc3215a0`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fa330c05a735fa176327db111cb8144a33d927923c98a24221dcfc94ac73cf`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0963e3ada6db5d54c6e1dcfe66033facd31c4474f0a9b67df506cd38b708994a`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:5eb29aa350e04efd871dc089f00e2332c6fde8340442987c019d24c4d8612952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:3eb16b69114671a8802239d503c0290429cdb314d8a872d6b2e085341c12b4a0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190940335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1f053a6e4022c28324a3e45080faa48d8a7f96dc18ea8250a25af5211529a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 22 May 2025 16:50:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 16:50:25 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Thu, 22 May 2025 16:50:26 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Thu, 22 May 2025 16:51:00 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 May 2025 16:51:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 May 2025 16:51:18 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 16:51:19 GMT
EXPOSE 4222 6222 8222
# Thu, 22 May 2025 16:51:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 16:51:20 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ab467e36de62f69e77619428c80684c172dceff9ed3e77cc0f6ab14e4f32bdfd`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9091f1392b0e4b5a8efd3fa58b0c4a2b6e936430b4e42b68ba16077d4564944d`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf909e97fafaef4ec16a660d02af257e98e54239a7bc6cec966b8e76e70b715`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5d1bc88317b3a5b00e94a85aa69eeff6067de7eacc3b0ae40836597b6b4912`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc3aedb4b361c3a53ea79beee17b5b1e5323e8d429b1c896eb234b053b5198`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1800d06ff1abd05697da24fc89b33bee18003836f4b523b0183785ab5ed2496e`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 357.5 KB (357493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e26a01941a30a2df43651113e13c4254af9daa37d2d460c7eec0e2829bec1`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 6.9 MB (6853143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa50c7d770115bfd2ad8e106b7ba4c236b4240943f9c067a6ea34daf985b973b`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0aea2b23f17071fd4a073f906be4bf64c1c702b06340d09d355bacdc3215a0`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fa330c05a735fa176327db111cb8144a33d927923c98a24221dcfc94ac73cf`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0963e3ada6db5d54c6e1dcfe66033facd31c4474f0a9b67df506cd38b708994a`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:90e0218d56c985136af5a251758962585c8f82e64d2a222bb3a0525f28f076a4
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
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:3ccfdfb4f67d6b15d69e5b590eebbd96c3f7ec53f8ced1a9a4aac60d93aa11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a774814288e1fd893f7331df669215f646f6cf98fb4a0b0b67ac130ecbc292`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aeeb60ebe6caabdf00087638b31e612157fb76df70f09daae4aaf298f3339d`  
		Last Modified: Thu, 01 May 2025 16:46:48 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:fb05c36e05cb6fd98ab9578bf3f3522c5dda3b8db87c4b3f994bab4fb2c52bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5217c566ef49ccb62eb72b4d63e24c23407e01d1a483f783d19f43deb31978`

```dockerfile
```

-	Layers:
	-	`sha256:bf329933f2001d892b1db19e56be440c7cc1471cbfd53e85627380b9eeecfa13`  
		Last Modified: Thu, 01 May 2025 16:46:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:b6ca28cb0f26d521de072e0428eda868dfc1053f02ee89da87e122abbbcc5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a244218290447acaf4597f5813cdd9b33d442f548e97ac69f3ba9bf77b007e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2635c150a57e298a8572ecc73e84b470cf6f64d5d04bb81b438de0d2a578e`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:ba5d033bc950f897b411410b7bfb78b5058d32b86b8ffaf7265e62e043e20f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfee55275a487ab6b108c1e0c26fd8d58c5914aac413eaa083766552f361395`

```dockerfile
```

-	Layers:
	-	`sha256:49a95ae7819d7b3b2da785dc18d291000c88914a33318296ef12da97f0616623`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:df20fbfe0bb522658b99afc79ac3890e502c6970a671f3ad578076fe583eb5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b209380767db19497ed31465cd8ea6f57747719a0b7c3424178728fa4ef380`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b68896e7d11974b1313147602b9b9672df2062a2a1ba0fb0254c70bc0dc0e`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:b0cfe6d5686bf2b793b3456b56e58e4709af2b1be8896efd6a883dbf3afd8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4cc0b81dfacb98ca6bbac7f072e0daf502def9b3d32ec1fa94ea2ba790bc8c`

```dockerfile
```

-	Layers:
	-	`sha256:54a912eaf0fc6d63db9786e668ee5fbd92a4b32c3480891aa1db26c32b50284c`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:935fb840a8c73adfaff297b1980187748a4b3fd7816c4a78cb3524165d20a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783285edc88812d5d1cac420dd84fda126b9342da1ddd4a5ad24724d70b0766`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc364f50cefcf174b35bb61af86057cdb8d5030b40433f6a32f2b2c9b8c05d`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:245530ad8e2639d51db319933a737ae5e6d6d451cad28296889bd066ed9e87f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d366dc53cfe6e71c360d90a3e634be45150175d442cc53c416936d03bd1556c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18e0c2e5eab72b82113e68b6bd114b5e2127dae37ea5fdae90468e3f51f31eb`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:75880b6c63b7cebe9255b7608fbc73d00b8933e46ca0cbbe90c2b6c58d8abb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da7825b3708ab6faf26cc9ccdab7321e3396534294da2330041bd16cc10322`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01318be57fae6110f9534fcddaee8e6a1c3e69f25ae1e4d106c4c8de8ae29409`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:5b57ed930c2667fe65ad1bcee2b9818a79e11a7500f81bf6abf002f323a40614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee26f11ca9c8bf7645aaa93d4a9b71a44b8e5eec7c6d2da88292202cb0c94ba0`

```dockerfile
```

-	Layers:
	-	`sha256:8d564d37941aabc78a509d369ad843dd9bbd31e598a5eb086e6ed43f44520de0`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:84075ae55673cd07f22de63d995d5fb6f6ad9237fb03cd9628d8093314717a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8ab527386a9db0e153388584e1d45bde0ef4d42a924ecb08c07492c2cd4188`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d173bad3ebbebf172e48ea474c921f04af212478f36048d2ae48e968fdb19`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:366a7884992207edcdabb534dadc23e5194a82acb271a57feb915092c3161a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a7d69878d9010d1441db5562973317245edebea32c25d731de86833b22a30e`

```dockerfile
```

-	Layers:
	-	`sha256:7d9401f2d8bdddd29f021b02a49ab29c2c347e45f7f6f5fab6e6aaaca052ff85`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2161d1e1f94ac34edd3eeb3e988a132d0b80e1ae578a28901ced25b5d5a4be04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989144758dca5d5bc74a916c0fbc16f6c3d6772d0ac66f3f5c3154a304fb1926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:22:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:23:00 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:23:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:23:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a13d3a2ccb6d6921800013fd2bafb22fdddd0839e1702de9c3ed71d624e01`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcabfa424d4764fde945c8ef78c9a9e3447fe9fa96663564fac1e1ad6b5269`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 6.3 MB (6298138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4d978b7505d1beafe17ec8bd7a83c79d9f90cb9c838cacb0a65ba0d62e925`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b062d5e7dc7c72a41dce15f3c57b7c154f653dbf3f3af39380330b8378d24`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee38558620886b53646fde38cf4bceb3c93944c4c1fbf218d71a2d1ea7d7b1a`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac45ac9cff58dc0e1d04bdba98a370b8fb4b0092dcb07e4f7b213595a395a8`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:93712e2af4500282de4687c70a83f586e4d54c4d70da10d0c4d9c156bd394b47
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

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:c34d45bf23d649a4d37ce201fda0b320a648321400c3a748316e56de6e99fa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad8efc48f3f88e92f1aa1217506d1695658b3d9a6bad7d60e3fedefa53c2579`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f3b2d23beaad798bb05689b7b0c38b571c62de55bb42fe3d53872cc5ff92da`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 6.6 MB (6639761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af882d59a8322a1c938ce881bae1d6f8e4c67a83cd10de3093fe63d84bd4816e`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e33ceb26f25c0ca98ca5658db546fc04ca902221f66297bc2f30b3468abd4`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:279bfc65a9ab0e539497f45337ff6ed2faf7b612fb4839dd6a0fa900508b4ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c778b071dcf85c9d9104248b88336f83be5b3bda6b70cba034976af2f275f57`

```dockerfile
```

-	Layers:
	-	`sha256:129e2409afba42dbf5c67d05ec6eb6f8c873f5904c0ff5f38b4c981d2b7f412c`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d9215923753a980ccecb0dcf2b6841e4d3ef6884ebcd05292cb7a2583a3b8530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eb831cfb4294c6f1b05e21607b2f6872b235265cc47089cb18582b225d1249`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f67ef15a3e6592471363dd18bc7267cd47ab6e65d7d6a0d811a3364d59df6e`  
		Last Modified: Thu, 01 May 2025 16:38:54 GMT  
		Size: 6.4 MB (6363842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb3661b4153de935d2124a23b501709ed0f710a1b9cf9d6a6137525c18d05b9`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ef4f92c061db0ef6d4931e407e1583e53dc6aa441535c15eb5dd789a115773`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c65a6c7bf9a8b042b1f449b053bfe0dfd1cef9fa4249f8747268c49a5740f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe767250ee00671e619eb9b99c513d9cc1e0dd692f51ae4ffd655f0055bd6af`

```dockerfile
```

-	Layers:
	-	`sha256:5615a93039a5f61ab9bef28288f3860598c067c009e128dcd27e42f85ac20301`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 13.2 KB (13196 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e2cef85475714d4ad1c8e8fa1e69852499955d83730737ef2bbd8fe633e7020f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9450061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2ef8b03fec17a1a701077878f52a06d67317d0cb6010c569f3e791633fdbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d33a05d4fc89796e871bbc51f7c2f03473ab7d395ae867ea6ded0925425930`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 6.4 MB (6350965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdfb48057ca2884d5cbbe61f040003470fb7d1eef9df85d1d6d1f106b2e6ae3`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e033463ccd5cbae1b4d8e4c658de11bcd5d60e3a4813360434b14b905b47693`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:bd174726bb7e67dcf23132668b2a382995ff24039238aa054c6375c9cd59d298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cce4b6f193efa833d132fc5128ad9519e927160b35c56112d7e60d8eb9469b3`

```dockerfile
```

-	Layers:
	-	`sha256:f8bb9a0270a41c5386708d530c1e9d2e65144998b4ad8ed0e5d6be7bb9e44baa`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3145ec04db64e45caeb0f29667668a316c36b68e31c2b3d939bb9d958f0a74f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92f22cb37c471307a70200f79c08e245c8bd15242fcf35614f427ca7444321f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438f232ef49cc8a1c095d8de2c048f9e3b5601888fd3765fdfe35a2460f21fe9`  
		Last Modified: Thu, 01 May 2025 16:38:57 GMT  
		Size: 6.1 MB (6145669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d605f23890a635dfb31c63a57f053984f104fb935e1773e0e2fded93c7426b`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa6c6da40fc6e072ba6046754df41177e7d69a56c57fefc409dec3e2f0cc32d`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:0f19f785d00a6cefc980a3a8e6b4005413c51965fdd6766b476dbd39812a05a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15084770e78cbbec61e01f467cf7900076a503f69fcf484cbb8aba6d23e5041e`

```dockerfile
```

-	Layers:
	-	`sha256:e5d13f6b4cb7d8778987db76d62b9476b8ec77826cf66bbf8f51f9ea9c9ce687`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:50117e272809853308376a05ca020eb6e23911a49abff46c55ab692efc3b3669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9700852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aea0efae4f9a3fbbbb9baf1f485e5a90b04723d760946fc74a51f1058bd97b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3b3911883a3d22279373bc74804c2995b36c10520bf9ac1c4667699b5374db`  
		Last Modified: Thu, 01 May 2025 16:39:22 GMT  
		Size: 6.1 MB (6125534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72eea76948941bc50b2efbec987784930fe42c32734bada6dbecd4c52b2a5929`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51479d12c82553566d4db85b775ebe378ffd06e2344f6e86160683723e6902`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f9832a8b75f208a0ab0465377e7fa87f571195898fe81a85ce2913fb69ffd907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229468fb8f66a01208934dcf50680c63131e71f6c657a63de7795f7d99b6854a`

```dockerfile
```

-	Layers:
	-	`sha256:b604ecda47807a4ab87664a2f0113fe11475ceb9affe4d8ddb7f52f062e8ae59`  
		Last Modified: Thu, 01 May 2025 16:39:21 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:82d76d997f357c81c1b979178924d10a329b209d7a040afb9fbb1f4a4ab9160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9951046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f8de5e69e58a8f32dcdcda2a08579afa328c71127508bdbafa8785e78fa8aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0886cbd4a169e692b2e3025d48b7b4eedc22bde576167e4ce914a4fc6be2fabd`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 6.5 MB (6482509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b1086d683042d9331e427a01afd7e8bcc39c56a16a0c83c21ee709f9badf1`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6041a9ca0a4f2a5124f9cb2a670689ec22aee1c2595024425dfc8e7417e39f2f`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ba0291acad692758de3bd8a88cd7ba9adadd48b6656814e1cb476265bffda4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa7f57e04cd4ba1e1494ad1dd08230beb012c65d8d0b062fea2ec2754167687`

```dockerfile
```

-	Layers:
	-	`sha256:b804766c02248fbcab4d51f20fb87a2c613a90e9e3a244f0b1adb142fabbfb3a`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:93712e2af4500282de4687c70a83f586e4d54c4d70da10d0c4d9c156bd394b47
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

### `nats:2.10-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:c34d45bf23d649a4d37ce201fda0b320a648321400c3a748316e56de6e99fa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad8efc48f3f88e92f1aa1217506d1695658b3d9a6bad7d60e3fedefa53c2579`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f3b2d23beaad798bb05689b7b0c38b571c62de55bb42fe3d53872cc5ff92da`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 6.6 MB (6639761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af882d59a8322a1c938ce881bae1d6f8e4c67a83cd10de3093fe63d84bd4816e`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e33ceb26f25c0ca98ca5658db546fc04ca902221f66297bc2f30b3468abd4`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:279bfc65a9ab0e539497f45337ff6ed2faf7b612fb4839dd6a0fa900508b4ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c778b071dcf85c9d9104248b88336f83be5b3bda6b70cba034976af2f275f57`

```dockerfile
```

-	Layers:
	-	`sha256:129e2409afba42dbf5c67d05ec6eb6f8c873f5904c0ff5f38b4c981d2b7f412c`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:d9215923753a980ccecb0dcf2b6841e4d3ef6884ebcd05292cb7a2583a3b8530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eb831cfb4294c6f1b05e21607b2f6872b235265cc47089cb18582b225d1249`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f67ef15a3e6592471363dd18bc7267cd47ab6e65d7d6a0d811a3364d59df6e`  
		Last Modified: Thu, 01 May 2025 16:38:54 GMT  
		Size: 6.4 MB (6363842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb3661b4153de935d2124a23b501709ed0f710a1b9cf9d6a6137525c18d05b9`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ef4f92c061db0ef6d4931e407e1583e53dc6aa441535c15eb5dd789a115773`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c65a6c7bf9a8b042b1f449b053bfe0dfd1cef9fa4249f8747268c49a5740f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe767250ee00671e619eb9b99c513d9cc1e0dd692f51ae4ffd655f0055bd6af`

```dockerfile
```

-	Layers:
	-	`sha256:5615a93039a5f61ab9bef28288f3860598c067c009e128dcd27e42f85ac20301`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 13.2 KB (13196 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:e2cef85475714d4ad1c8e8fa1e69852499955d83730737ef2bbd8fe633e7020f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9450061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2ef8b03fec17a1a701077878f52a06d67317d0cb6010c569f3e791633fdbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d33a05d4fc89796e871bbc51f7c2f03473ab7d395ae867ea6ded0925425930`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 6.4 MB (6350965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdfb48057ca2884d5cbbe61f040003470fb7d1eef9df85d1d6d1f106b2e6ae3`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e033463ccd5cbae1b4d8e4c658de11bcd5d60e3a4813360434b14b905b47693`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:bd174726bb7e67dcf23132668b2a382995ff24039238aa054c6375c9cd59d298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cce4b6f193efa833d132fc5128ad9519e927160b35c56112d7e60d8eb9469b3`

```dockerfile
```

-	Layers:
	-	`sha256:f8bb9a0270a41c5386708d530c1e9d2e65144998b4ad8ed0e5d6be7bb9e44baa`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3145ec04db64e45caeb0f29667668a316c36b68e31c2b3d939bb9d958f0a74f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92f22cb37c471307a70200f79c08e245c8bd15242fcf35614f427ca7444321f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438f232ef49cc8a1c095d8de2c048f9e3b5601888fd3765fdfe35a2460f21fe9`  
		Last Modified: Thu, 01 May 2025 16:38:57 GMT  
		Size: 6.1 MB (6145669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d605f23890a635dfb31c63a57f053984f104fb935e1773e0e2fded93c7426b`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa6c6da40fc6e072ba6046754df41177e7d69a56c57fefc409dec3e2f0cc32d`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:0f19f785d00a6cefc980a3a8e6b4005413c51965fdd6766b476dbd39812a05a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15084770e78cbbec61e01f467cf7900076a503f69fcf484cbb8aba6d23e5041e`

```dockerfile
```

-	Layers:
	-	`sha256:e5d13f6b4cb7d8778987db76d62b9476b8ec77826cf66bbf8f51f9ea9c9ce687`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:50117e272809853308376a05ca020eb6e23911a49abff46c55ab692efc3b3669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9700852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aea0efae4f9a3fbbbb9baf1f485e5a90b04723d760946fc74a51f1058bd97b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3b3911883a3d22279373bc74804c2995b36c10520bf9ac1c4667699b5374db`  
		Last Modified: Thu, 01 May 2025 16:39:22 GMT  
		Size: 6.1 MB (6125534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72eea76948941bc50b2efbec987784930fe42c32734bada6dbecd4c52b2a5929`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51479d12c82553566d4db85b775ebe378ffd06e2344f6e86160683723e6902`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f9832a8b75f208a0ab0465377e7fa87f571195898fe81a85ce2913fb69ffd907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229468fb8f66a01208934dcf50680c63131e71f6c657a63de7795f7d99b6854a`

```dockerfile
```

-	Layers:
	-	`sha256:b604ecda47807a4ab87664a2f0113fe11475ceb9affe4d8ddb7f52f062e8ae59`  
		Last Modified: Thu, 01 May 2025 16:39:21 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:82d76d997f357c81c1b979178924d10a329b209d7a040afb9fbb1f4a4ab9160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9951046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f8de5e69e58a8f32dcdcda2a08579afa328c71127508bdbafa8785e78fa8aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0886cbd4a169e692b2e3025d48b7b4eedc22bde576167e4ce914a4fc6be2fabd`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 6.5 MB (6482509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b1086d683042d9331e427a01afd7e8bcc39c56a16a0c83c21ee709f9badf1`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6041a9ca0a4f2a5124f9cb2a670689ec22aee1c2595024425dfc8e7417e39f2f`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ba0291acad692758de3bd8a88cd7ba9adadd48b6656814e1cb476265bffda4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa7f57e04cd4ba1e1494ad1dd08230beb012c65d8d0b062fea2ec2754167687`

```dockerfile
```

-	Layers:
	-	`sha256:b804766c02248fbcab4d51f20fb87a2c613a90e9e3a244f0b1adb142fabbfb3a`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:f1fc04f650ac4cd8c40aa3c7c46a0f2066999a61b4e3be99945151adb1d24aa5
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

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:3ccfdfb4f67d6b15d69e5b590eebbd96c3f7ec53f8ced1a9a4aac60d93aa11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a774814288e1fd893f7331df669215f646f6cf98fb4a0b0b67ac130ecbc292`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aeeb60ebe6caabdf00087638b31e612157fb76df70f09daae4aaf298f3339d`  
		Last Modified: Thu, 01 May 2025 16:46:48 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:fb05c36e05cb6fd98ab9578bf3f3522c5dda3b8db87c4b3f994bab4fb2c52bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5217c566ef49ccb62eb72b4d63e24c23407e01d1a483f783d19f43deb31978`

```dockerfile
```

-	Layers:
	-	`sha256:bf329933f2001d892b1db19e56be440c7cc1471cbfd53e85627380b9eeecfa13`  
		Last Modified: Thu, 01 May 2025 16:46:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b6ca28cb0f26d521de072e0428eda868dfc1053f02ee89da87e122abbbcc5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a244218290447acaf4597f5813cdd9b33d442f548e97ac69f3ba9bf77b007e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2635c150a57e298a8572ecc73e84b470cf6f64d5d04bb81b438de0d2a578e`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ba5d033bc950f897b411410b7bfb78b5058d32b86b8ffaf7265e62e043e20f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfee55275a487ab6b108c1e0c26fd8d58c5914aac413eaa083766552f361395`

```dockerfile
```

-	Layers:
	-	`sha256:49a95ae7819d7b3b2da785dc18d291000c88914a33318296ef12da97f0616623`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:df20fbfe0bb522658b99afc79ac3890e502c6970a671f3ad578076fe583eb5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b209380767db19497ed31465cd8ea6f57747719a0b7c3424178728fa4ef380`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b68896e7d11974b1313147602b9b9672df2062a2a1ba0fb0254c70bc0dc0e`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b0cfe6d5686bf2b793b3456b56e58e4709af2b1be8896efd6a883dbf3afd8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4cc0b81dfacb98ca6bbac7f072e0daf502def9b3d32ec1fa94ea2ba790bc8c`

```dockerfile
```

-	Layers:
	-	`sha256:54a912eaf0fc6d63db9786e668ee5fbd92a4b32c3480891aa1db26c32b50284c`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:935fb840a8c73adfaff297b1980187748a4b3fd7816c4a78cb3524165d20a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783285edc88812d5d1cac420dd84fda126b9342da1ddd4a5ad24724d70b0766`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc364f50cefcf174b35bb61af86057cdb8d5030b40433f6a32f2b2c9b8c05d`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:245530ad8e2639d51db319933a737ae5e6d6d451cad28296889bd066ed9e87f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d366dc53cfe6e71c360d90a3e634be45150175d442cc53c416936d03bd1556c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18e0c2e5eab72b82113e68b6bd114b5e2127dae37ea5fdae90468e3f51f31eb`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:75880b6c63b7cebe9255b7608fbc73d00b8933e46ca0cbbe90c2b6c58d8abb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da7825b3708ab6faf26cc9ccdab7321e3396534294da2330041bd16cc10322`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01318be57fae6110f9534fcddaee8e6a1c3e69f25ae1e4d106c4c8de8ae29409`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5b57ed930c2667fe65ad1bcee2b9818a79e11a7500f81bf6abf002f323a40614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee26f11ca9c8bf7645aaa93d4a9b71a44b8e5eec7c6d2da88292202cb0c94ba0`

```dockerfile
```

-	Layers:
	-	`sha256:8d564d37941aabc78a509d369ad843dd9bbd31e598a5eb086e6ed43f44520de0`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:84075ae55673cd07f22de63d995d5fb6f6ad9237fb03cd9628d8093314717a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8ab527386a9db0e153388584e1d45bde0ef4d42a924ecb08c07492c2cd4188`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d173bad3ebbebf172e48ea474c921f04af212478f36048d2ae48e968fdb19`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:366a7884992207edcdabb534dadc23e5194a82acb271a57feb915092c3161a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a7d69878d9010d1441db5562973317245edebea32c25d731de86833b22a30e`

```dockerfile
```

-	Layers:
	-	`sha256:7d9401f2d8bdddd29f021b02a49ab29c2c347e45f7f6f5fab6e6aaaca052ff85`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:1bb553cba2972802ff22b0a1281c11e946a66147579ed4ebab3a310058505097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2161d1e1f94ac34edd3eeb3e988a132d0b80e1ae578a28901ced25b5d5a4be04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989144758dca5d5bc74a916c0fbc16f6c3d6772d0ac66f3f5c3154a304fb1926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:22:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:23:00 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:23:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:23:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a13d3a2ccb6d6921800013fd2bafb22fdddd0839e1702de9c3ed71d624e01`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcabfa424d4764fde945c8ef78c9a9e3447fe9fa96663564fac1e1ad6b5269`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 6.3 MB (6298138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4d978b7505d1beafe17ec8bd7a83c79d9f90cb9c838cacb0a65ba0d62e925`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b062d5e7dc7c72a41dce15f3c57b7c154f653dbf3f3af39380330b8378d24`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee38558620886b53646fde38cf4bceb3c93944c4c1fbf218d71a2d1ea7d7b1a`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac45ac9cff58dc0e1d04bdba98a370b8fb4b0092dcb07e4f7b213595a395a8`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:1bb553cba2972802ff22b0a1281c11e946a66147579ed4ebab3a310058505097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2161d1e1f94ac34edd3eeb3e988a132d0b80e1ae578a28901ced25b5d5a4be04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989144758dca5d5bc74a916c0fbc16f6c3d6772d0ac66f3f5c3154a304fb1926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:22:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:23:00 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:23:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:23:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a13d3a2ccb6d6921800013fd2bafb22fdddd0839e1702de9c3ed71d624e01`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcabfa424d4764fde945c8ef78c9a9e3447fe9fa96663564fac1e1ad6b5269`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 6.3 MB (6298138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4d978b7505d1beafe17ec8bd7a83c79d9f90cb9c838cacb0a65ba0d62e925`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b062d5e7dc7c72a41dce15f3c57b7c154f653dbf3f3af39380330b8378d24`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee38558620886b53646fde38cf4bceb3c93944c4c1fbf218d71a2d1ea7d7b1a`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac45ac9cff58dc0e1d04bdba98a370b8fb4b0092dcb07e4f7b213595a395a8`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:f1fc04f650ac4cd8c40aa3c7c46a0f2066999a61b4e3be99945151adb1d24aa5
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

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:3ccfdfb4f67d6b15d69e5b590eebbd96c3f7ec53f8ced1a9a4aac60d93aa11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a774814288e1fd893f7331df669215f646f6cf98fb4a0b0b67ac130ecbc292`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aeeb60ebe6caabdf00087638b31e612157fb76df70f09daae4aaf298f3339d`  
		Last Modified: Thu, 01 May 2025 16:46:48 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:fb05c36e05cb6fd98ab9578bf3f3522c5dda3b8db87c4b3f994bab4fb2c52bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5217c566ef49ccb62eb72b4d63e24c23407e01d1a483f783d19f43deb31978`

```dockerfile
```

-	Layers:
	-	`sha256:bf329933f2001d892b1db19e56be440c7cc1471cbfd53e85627380b9eeecfa13`  
		Last Modified: Thu, 01 May 2025 16:46:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b6ca28cb0f26d521de072e0428eda868dfc1053f02ee89da87e122abbbcc5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a244218290447acaf4597f5813cdd9b33d442f548e97ac69f3ba9bf77b007e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2635c150a57e298a8572ecc73e84b470cf6f64d5d04bb81b438de0d2a578e`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ba5d033bc950f897b411410b7bfb78b5058d32b86b8ffaf7265e62e043e20f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfee55275a487ab6b108c1e0c26fd8d58c5914aac413eaa083766552f361395`

```dockerfile
```

-	Layers:
	-	`sha256:49a95ae7819d7b3b2da785dc18d291000c88914a33318296ef12da97f0616623`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:df20fbfe0bb522658b99afc79ac3890e502c6970a671f3ad578076fe583eb5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b209380767db19497ed31465cd8ea6f57747719a0b7c3424178728fa4ef380`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b68896e7d11974b1313147602b9b9672df2062a2a1ba0fb0254c70bc0dc0e`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b0cfe6d5686bf2b793b3456b56e58e4709af2b1be8896efd6a883dbf3afd8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4cc0b81dfacb98ca6bbac7f072e0daf502def9b3d32ec1fa94ea2ba790bc8c`

```dockerfile
```

-	Layers:
	-	`sha256:54a912eaf0fc6d63db9786e668ee5fbd92a4b32c3480891aa1db26c32b50284c`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:935fb840a8c73adfaff297b1980187748a4b3fd7816c4a78cb3524165d20a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783285edc88812d5d1cac420dd84fda126b9342da1ddd4a5ad24724d70b0766`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc364f50cefcf174b35bb61af86057cdb8d5030b40433f6a32f2b2c9b8c05d`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:245530ad8e2639d51db319933a737ae5e6d6d451cad28296889bd066ed9e87f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d366dc53cfe6e71c360d90a3e634be45150175d442cc53c416936d03bd1556c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18e0c2e5eab72b82113e68b6bd114b5e2127dae37ea5fdae90468e3f51f31eb`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:75880b6c63b7cebe9255b7608fbc73d00b8933e46ca0cbbe90c2b6c58d8abb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da7825b3708ab6faf26cc9ccdab7321e3396534294da2330041bd16cc10322`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01318be57fae6110f9534fcddaee8e6a1c3e69f25ae1e4d106c4c8de8ae29409`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5b57ed930c2667fe65ad1bcee2b9818a79e11a7500f81bf6abf002f323a40614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee26f11ca9c8bf7645aaa93d4a9b71a44b8e5eec7c6d2da88292202cb0c94ba0`

```dockerfile
```

-	Layers:
	-	`sha256:8d564d37941aabc78a509d369ad843dd9bbd31e598a5eb086e6ed43f44520de0`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:84075ae55673cd07f22de63d995d5fb6f6ad9237fb03cd9628d8093314717a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8ab527386a9db0e153388584e1d45bde0ef4d42a924ecb08c07492c2cd4188`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d173bad3ebbebf172e48ea474c921f04af212478f36048d2ae48e968fdb19`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:366a7884992207edcdabb534dadc23e5194a82acb271a57feb915092c3161a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a7d69878d9010d1441db5562973317245edebea32c25d731de86833b22a30e`

```dockerfile
```

-	Layers:
	-	`sha256:7d9401f2d8bdddd29f021b02a49ab29c2c347e45f7f6f5fab6e6aaaca052ff85`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:497a9cb9259dea3157192c47053d210e90285f245a40302113147c78935f415a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7cee34982b9961eca0791af019a96210f3acfb0b541c777fef4674acce9ebffd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190701818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304379749a747af729040c8fc24ea557b571e8851904d77062912ce7f19ed13e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:57:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_SERVER=2.10.29
# Wed, 14 May 2025 20:57:48 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Wed, 14 May 2025 20:57:49 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Wed, 14 May 2025 20:58:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 20:58:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 20:58:40 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 20:58:41 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 20:58:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 20:58:42 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:61077ce6abbdae8515ed8aee8d125e78c4cac8c784a425794f86615c897c5350`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794b39a004828c5754f1625d423719263b57a56c0f9d146dac4f3f4eeca00619`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084927b2191adc36daf6f816dbfc6f7fc2f39616f120eb2651541cc473469c1d`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f419ade08147d57977fc7931cc12b84db32642f88e21afce4da375e7e51dee`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef3124c22d55ce500386d4b4e302947756899e4b22694baa0f983ac49331ec8`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170ce137abceda359d4a3c7b368ea88cf8f545610e1cf97d8b6a883455b6cb49`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 332.9 KB (332919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7d2e2aeda12346ac02cd0fbd2469f9b9139a606a9993af6d38d1f5067291f4`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 6.6 MB (6639239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e924aac8362f8466698a1b3cb28f4d7cc0b32f9ec6db4146dae40bb696b0b9a`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2218925f1c3045fd7b8c4c505a18617b96b18b25084ff3c704702a01def48dcf`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe49501346aad8e6904d0c916ae6c2977054bb03a19422d25bb61fa17f4c048`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eee89edd57fb6cba67f1345aa73742d0a392b8fce89e8db3349b02fab6f9292`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:497a9cb9259dea3157192c47053d210e90285f245a40302113147c78935f415a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7cee34982b9961eca0791af019a96210f3acfb0b541c777fef4674acce9ebffd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190701818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304379749a747af729040c8fc24ea557b571e8851904d77062912ce7f19ed13e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:57:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_SERVER=2.10.29
# Wed, 14 May 2025 20:57:48 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Wed, 14 May 2025 20:57:49 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Wed, 14 May 2025 20:58:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 20:58:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 20:58:40 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 20:58:41 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 20:58:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 20:58:42 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:61077ce6abbdae8515ed8aee8d125e78c4cac8c784a425794f86615c897c5350`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794b39a004828c5754f1625d423719263b57a56c0f9d146dac4f3f4eeca00619`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084927b2191adc36daf6f816dbfc6f7fc2f39616f120eb2651541cc473469c1d`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f419ade08147d57977fc7931cc12b84db32642f88e21afce4da375e7e51dee`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef3124c22d55ce500386d4b4e302947756899e4b22694baa0f983ac49331ec8`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170ce137abceda359d4a3c7b368ea88cf8f545610e1cf97d8b6a883455b6cb49`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 332.9 KB (332919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7d2e2aeda12346ac02cd0fbd2469f9b9139a606a9993af6d38d1f5067291f4`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 6.6 MB (6639239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e924aac8362f8466698a1b3cb28f4d7cc0b32f9ec6db4146dae40bb696b0b9a`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2218925f1c3045fd7b8c4c505a18617b96b18b25084ff3c704702a01def48dcf`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe49501346aad8e6904d0c916ae6c2977054bb03a19422d25bb61fa17f4c048`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eee89edd57fb6cba67f1345aa73742d0a392b8fce89e8db3349b02fab6f9292`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29`

```console
$ docker pull nats@sha256:90e0218d56c985136af5a251758962585c8f82e64d2a222bb3a0525f28f076a4
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
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10.29` - linux; amd64

```console
$ docker pull nats@sha256:3ccfdfb4f67d6b15d69e5b590eebbd96c3f7ec53f8ced1a9a4aac60d93aa11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a774814288e1fd893f7331df669215f646f6cf98fb4a0b0b67ac130ecbc292`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aeeb60ebe6caabdf00087638b31e612157fb76df70f09daae4aaf298f3339d`  
		Last Modified: Thu, 01 May 2025 16:46:48 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:fb05c36e05cb6fd98ab9578bf3f3522c5dda3b8db87c4b3f994bab4fb2c52bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5217c566ef49ccb62eb72b4d63e24c23407e01d1a483f783d19f43deb31978`

```dockerfile
```

-	Layers:
	-	`sha256:bf329933f2001d892b1db19e56be440c7cc1471cbfd53e85627380b9eeecfa13`  
		Last Modified: Thu, 01 May 2025 16:46:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm variant v6

```console
$ docker pull nats@sha256:b6ca28cb0f26d521de072e0428eda868dfc1053f02ee89da87e122abbbcc5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a244218290447acaf4597f5813cdd9b33d442f548e97ac69f3ba9bf77b007e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2635c150a57e298a8572ecc73e84b470cf6f64d5d04bb81b438de0d2a578e`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:ba5d033bc950f897b411410b7bfb78b5058d32b86b8ffaf7265e62e043e20f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfee55275a487ab6b108c1e0c26fd8d58c5914aac413eaa083766552f361395`

```dockerfile
```

-	Layers:
	-	`sha256:49a95ae7819d7b3b2da785dc18d291000c88914a33318296ef12da97f0616623`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm variant v7

```console
$ docker pull nats@sha256:df20fbfe0bb522658b99afc79ac3890e502c6970a671f3ad578076fe583eb5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b209380767db19497ed31465cd8ea6f57747719a0b7c3424178728fa4ef380`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b68896e7d11974b1313147602b9b9672df2062a2a1ba0fb0254c70bc0dc0e`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:b0cfe6d5686bf2b793b3456b56e58e4709af2b1be8896efd6a883dbf3afd8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4cc0b81dfacb98ca6bbac7f072e0daf502def9b3d32ec1fa94ea2ba790bc8c`

```dockerfile
```

-	Layers:
	-	`sha256:54a912eaf0fc6d63db9786e668ee5fbd92a4b32c3480891aa1db26c32b50284c`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:935fb840a8c73adfaff297b1980187748a4b3fd7816c4a78cb3524165d20a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783285edc88812d5d1cac420dd84fda126b9342da1ddd4a5ad24724d70b0766`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc364f50cefcf174b35bb61af86057cdb8d5030b40433f6a32f2b2c9b8c05d`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:245530ad8e2639d51db319933a737ae5e6d6d451cad28296889bd066ed9e87f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d366dc53cfe6e71c360d90a3e634be45150175d442cc53c416936d03bd1556c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18e0c2e5eab72b82113e68b6bd114b5e2127dae37ea5fdae90468e3f51f31eb`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; ppc64le

```console
$ docker pull nats@sha256:75880b6c63b7cebe9255b7608fbc73d00b8933e46ca0cbbe90c2b6c58d8abb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da7825b3708ab6faf26cc9ccdab7321e3396534294da2330041bd16cc10322`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01318be57fae6110f9534fcddaee8e6a1c3e69f25ae1e4d106c4c8de8ae29409`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:5b57ed930c2667fe65ad1bcee2b9818a79e11a7500f81bf6abf002f323a40614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee26f11ca9c8bf7645aaa93d4a9b71a44b8e5eec7c6d2da88292202cb0c94ba0`

```dockerfile
```

-	Layers:
	-	`sha256:8d564d37941aabc78a509d369ad843dd9bbd31e598a5eb086e6ed43f44520de0`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; s390x

```console
$ docker pull nats@sha256:84075ae55673cd07f22de63d995d5fb6f6ad9237fb03cd9628d8093314717a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8ab527386a9db0e153388584e1d45bde0ef4d42a924ecb08c07492c2cd4188`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d173bad3ebbebf172e48ea474c921f04af212478f36048d2ae48e968fdb19`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:366a7884992207edcdabb534dadc23e5194a82acb271a57feb915092c3161a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a7d69878d9010d1441db5562973317245edebea32c25d731de86833b22a30e`

```dockerfile
```

-	Layers:
	-	`sha256:7d9401f2d8bdddd29f021b02a49ab29c2c347e45f7f6f5fab6e6aaaca052ff85`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2161d1e1f94ac34edd3eeb3e988a132d0b80e1ae578a28901ced25b5d5a4be04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989144758dca5d5bc74a916c0fbc16f6c3d6772d0ac66f3f5c3154a304fb1926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:22:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:23:00 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:23:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:23:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a13d3a2ccb6d6921800013fd2bafb22fdddd0839e1702de9c3ed71d624e01`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcabfa424d4764fde945c8ef78c9a9e3447fe9fa96663564fac1e1ad6b5269`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 6.3 MB (6298138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4d978b7505d1beafe17ec8bd7a83c79d9f90cb9c838cacb0a65ba0d62e925`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b062d5e7dc7c72a41dce15f3c57b7c154f653dbf3f3af39380330b8378d24`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee38558620886b53646fde38cf4bceb3c93944c4c1fbf218d71a2d1ea7d7b1a`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac45ac9cff58dc0e1d04bdba98a370b8fb4b0092dcb07e4f7b213595a395a8`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-alpine`

```console
$ docker pull nats@sha256:93712e2af4500282de4687c70a83f586e4d54c4d70da10d0c4d9c156bd394b47
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

### `nats:2.10.29-alpine` - linux; amd64

```console
$ docker pull nats@sha256:c34d45bf23d649a4d37ce201fda0b320a648321400c3a748316e56de6e99fa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad8efc48f3f88e92f1aa1217506d1695658b3d9a6bad7d60e3fedefa53c2579`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f3b2d23beaad798bb05689b7b0c38b571c62de55bb42fe3d53872cc5ff92da`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 6.6 MB (6639761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af882d59a8322a1c938ce881bae1d6f8e4c67a83cd10de3093fe63d84bd4816e`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e33ceb26f25c0ca98ca5658db546fc04ca902221f66297bc2f30b3468abd4`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:279bfc65a9ab0e539497f45337ff6ed2faf7b612fb4839dd6a0fa900508b4ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c778b071dcf85c9d9104248b88336f83be5b3bda6b70cba034976af2f275f57`

```dockerfile
```

-	Layers:
	-	`sha256:129e2409afba42dbf5c67d05ec6eb6f8c873f5904c0ff5f38b4c981d2b7f412c`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d9215923753a980ccecb0dcf2b6841e4d3ef6884ebcd05292cb7a2583a3b8530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eb831cfb4294c6f1b05e21607b2f6872b235265cc47089cb18582b225d1249`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f67ef15a3e6592471363dd18bc7267cd47ab6e65d7d6a0d811a3364d59df6e`  
		Last Modified: Thu, 01 May 2025 16:38:54 GMT  
		Size: 6.4 MB (6363842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb3661b4153de935d2124a23b501709ed0f710a1b9cf9d6a6137525c18d05b9`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ef4f92c061db0ef6d4931e407e1583e53dc6aa441535c15eb5dd789a115773`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c65a6c7bf9a8b042b1f449b053bfe0dfd1cef9fa4249f8747268c49a5740f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe767250ee00671e619eb9b99c513d9cc1e0dd692f51ae4ffd655f0055bd6af`

```dockerfile
```

-	Layers:
	-	`sha256:5615a93039a5f61ab9bef28288f3860598c067c009e128dcd27e42f85ac20301`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 13.2 KB (13196 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e2cef85475714d4ad1c8e8fa1e69852499955d83730737ef2bbd8fe633e7020f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9450061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2ef8b03fec17a1a701077878f52a06d67317d0cb6010c569f3e791633fdbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d33a05d4fc89796e871bbc51f7c2f03473ab7d395ae867ea6ded0925425930`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 6.4 MB (6350965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdfb48057ca2884d5cbbe61f040003470fb7d1eef9df85d1d6d1f106b2e6ae3`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e033463ccd5cbae1b4d8e4c658de11bcd5d60e3a4813360434b14b905b47693`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:bd174726bb7e67dcf23132668b2a382995ff24039238aa054c6375c9cd59d298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cce4b6f193efa833d132fc5128ad9519e927160b35c56112d7e60d8eb9469b3`

```dockerfile
```

-	Layers:
	-	`sha256:f8bb9a0270a41c5386708d530c1e9d2e65144998b4ad8ed0e5d6be7bb9e44baa`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3145ec04db64e45caeb0f29667668a316c36b68e31c2b3d939bb9d958f0a74f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92f22cb37c471307a70200f79c08e245c8bd15242fcf35614f427ca7444321f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438f232ef49cc8a1c095d8de2c048f9e3b5601888fd3765fdfe35a2460f21fe9`  
		Last Modified: Thu, 01 May 2025 16:38:57 GMT  
		Size: 6.1 MB (6145669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d605f23890a635dfb31c63a57f053984f104fb935e1773e0e2fded93c7426b`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa6c6da40fc6e072ba6046754df41177e7d69a56c57fefc409dec3e2f0cc32d`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:0f19f785d00a6cefc980a3a8e6b4005413c51965fdd6766b476dbd39812a05a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15084770e78cbbec61e01f467cf7900076a503f69fcf484cbb8aba6d23e5041e`

```dockerfile
```

-	Layers:
	-	`sha256:e5d13f6b4cb7d8778987db76d62b9476b8ec77826cf66bbf8f51f9ea9c9ce687`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:50117e272809853308376a05ca020eb6e23911a49abff46c55ab692efc3b3669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9700852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aea0efae4f9a3fbbbb9baf1f485e5a90b04723d760946fc74a51f1058bd97b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3b3911883a3d22279373bc74804c2995b36c10520bf9ac1c4667699b5374db`  
		Last Modified: Thu, 01 May 2025 16:39:22 GMT  
		Size: 6.1 MB (6125534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72eea76948941bc50b2efbec987784930fe42c32734bada6dbecd4c52b2a5929`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51479d12c82553566d4db85b775ebe378ffd06e2344f6e86160683723e6902`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f9832a8b75f208a0ab0465377e7fa87f571195898fe81a85ce2913fb69ffd907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229468fb8f66a01208934dcf50680c63131e71f6c657a63de7795f7d99b6854a`

```dockerfile
```

-	Layers:
	-	`sha256:b604ecda47807a4ab87664a2f0113fe11475ceb9affe4d8ddb7f52f062e8ae59`  
		Last Modified: Thu, 01 May 2025 16:39:21 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; s390x

```console
$ docker pull nats@sha256:82d76d997f357c81c1b979178924d10a329b209d7a040afb9fbb1f4a4ab9160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9951046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f8de5e69e58a8f32dcdcda2a08579afa328c71127508bdbafa8785e78fa8aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0886cbd4a169e692b2e3025d48b7b4eedc22bde576167e4ce914a4fc6be2fabd`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 6.5 MB (6482509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b1086d683042d9331e427a01afd7e8bcc39c56a16a0c83c21ee709f9badf1`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6041a9ca0a4f2a5124f9cb2a670689ec22aee1c2595024425dfc8e7417e39f2f`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ba0291acad692758de3bd8a88cd7ba9adadd48b6656814e1cb476265bffda4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa7f57e04cd4ba1e1494ad1dd08230beb012c65d8d0b062fea2ec2754167687`

```dockerfile
```

-	Layers:
	-	`sha256:b804766c02248fbcab4d51f20fb87a2c613a90e9e3a244f0b1adb142fabbfb3a`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-alpine3.21`

```console
$ docker pull nats@sha256:93712e2af4500282de4687c70a83f586e4d54c4d70da10d0c4d9c156bd394b47
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

### `nats:2.10.29-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:c34d45bf23d649a4d37ce201fda0b320a648321400c3a748316e56de6e99fa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad8efc48f3f88e92f1aa1217506d1695658b3d9a6bad7d60e3fedefa53c2579`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f3b2d23beaad798bb05689b7b0c38b571c62de55bb42fe3d53872cc5ff92da`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 6.6 MB (6639761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af882d59a8322a1c938ce881bae1d6f8e4c67a83cd10de3093fe63d84bd4816e`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e33ceb26f25c0ca98ca5658db546fc04ca902221f66297bc2f30b3468abd4`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:279bfc65a9ab0e539497f45337ff6ed2faf7b612fb4839dd6a0fa900508b4ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c778b071dcf85c9d9104248b88336f83be5b3bda6b70cba034976af2f275f57`

```dockerfile
```

-	Layers:
	-	`sha256:129e2409afba42dbf5c67d05ec6eb6f8c873f5904c0ff5f38b4c981d2b7f412c`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:d9215923753a980ccecb0dcf2b6841e4d3ef6884ebcd05292cb7a2583a3b8530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eb831cfb4294c6f1b05e21607b2f6872b235265cc47089cb18582b225d1249`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f67ef15a3e6592471363dd18bc7267cd47ab6e65d7d6a0d811a3364d59df6e`  
		Last Modified: Thu, 01 May 2025 16:38:54 GMT  
		Size: 6.4 MB (6363842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb3661b4153de935d2124a23b501709ed0f710a1b9cf9d6a6137525c18d05b9`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ef4f92c061db0ef6d4931e407e1583e53dc6aa441535c15eb5dd789a115773`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c65a6c7bf9a8b042b1f449b053bfe0dfd1cef9fa4249f8747268c49a5740f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe767250ee00671e619eb9b99c513d9cc1e0dd692f51ae4ffd655f0055bd6af`

```dockerfile
```

-	Layers:
	-	`sha256:5615a93039a5f61ab9bef28288f3860598c067c009e128dcd27e42f85ac20301`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 13.2 KB (13196 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:e2cef85475714d4ad1c8e8fa1e69852499955d83730737ef2bbd8fe633e7020f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9450061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2ef8b03fec17a1a701077878f52a06d67317d0cb6010c569f3e791633fdbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d33a05d4fc89796e871bbc51f7c2f03473ab7d395ae867ea6ded0925425930`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 6.4 MB (6350965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdfb48057ca2884d5cbbe61f040003470fb7d1eef9df85d1d6d1f106b2e6ae3`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e033463ccd5cbae1b4d8e4c658de11bcd5d60e3a4813360434b14b905b47693`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:bd174726bb7e67dcf23132668b2a382995ff24039238aa054c6375c9cd59d298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cce4b6f193efa833d132fc5128ad9519e927160b35c56112d7e60d8eb9469b3`

```dockerfile
```

-	Layers:
	-	`sha256:f8bb9a0270a41c5386708d530c1e9d2e65144998b4ad8ed0e5d6be7bb9e44baa`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3145ec04db64e45caeb0f29667668a316c36b68e31c2b3d939bb9d958f0a74f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92f22cb37c471307a70200f79c08e245c8bd15242fcf35614f427ca7444321f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438f232ef49cc8a1c095d8de2c048f9e3b5601888fd3765fdfe35a2460f21fe9`  
		Last Modified: Thu, 01 May 2025 16:38:57 GMT  
		Size: 6.1 MB (6145669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d605f23890a635dfb31c63a57f053984f104fb935e1773e0e2fded93c7426b`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa6c6da40fc6e072ba6046754df41177e7d69a56c57fefc409dec3e2f0cc32d`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:0f19f785d00a6cefc980a3a8e6b4005413c51965fdd6766b476dbd39812a05a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15084770e78cbbec61e01f467cf7900076a503f69fcf484cbb8aba6d23e5041e`

```dockerfile
```

-	Layers:
	-	`sha256:e5d13f6b4cb7d8778987db76d62b9476b8ec77826cf66bbf8f51f9ea9c9ce687`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:50117e272809853308376a05ca020eb6e23911a49abff46c55ab692efc3b3669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9700852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aea0efae4f9a3fbbbb9baf1f485e5a90b04723d760946fc74a51f1058bd97b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3b3911883a3d22279373bc74804c2995b36c10520bf9ac1c4667699b5374db`  
		Last Modified: Thu, 01 May 2025 16:39:22 GMT  
		Size: 6.1 MB (6125534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72eea76948941bc50b2efbec987784930fe42c32734bada6dbecd4c52b2a5929`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51479d12c82553566d4db85b775ebe378ffd06e2344f6e86160683723e6902`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f9832a8b75f208a0ab0465377e7fa87f571195898fe81a85ce2913fb69ffd907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229468fb8f66a01208934dcf50680c63131e71f6c657a63de7795f7d99b6854a`

```dockerfile
```

-	Layers:
	-	`sha256:b604ecda47807a4ab87664a2f0113fe11475ceb9affe4d8ddb7f52f062e8ae59`  
		Last Modified: Thu, 01 May 2025 16:39:21 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:82d76d997f357c81c1b979178924d10a329b209d7a040afb9fbb1f4a4ab9160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9951046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f8de5e69e58a8f32dcdcda2a08579afa328c71127508bdbafa8785e78fa8aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0886cbd4a169e692b2e3025d48b7b4eedc22bde576167e4ce914a4fc6be2fabd`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 6.5 MB (6482509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b1086d683042d9331e427a01afd7e8bcc39c56a16a0c83c21ee709f9badf1`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6041a9ca0a4f2a5124f9cb2a670689ec22aee1c2595024425dfc8e7417e39f2f`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ba0291acad692758de3bd8a88cd7ba9adadd48b6656814e1cb476265bffda4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa7f57e04cd4ba1e1494ad1dd08230beb012c65d8d0b062fea2ec2754167687`

```dockerfile
```

-	Layers:
	-	`sha256:b804766c02248fbcab4d51f20fb87a2c613a90e9e3a244f0b1adb142fabbfb3a`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-linux`

```console
$ docker pull nats@sha256:f1fc04f650ac4cd8c40aa3c7c46a0f2066999a61b4e3be99945151adb1d24aa5
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

### `nats:2.10.29-linux` - linux; amd64

```console
$ docker pull nats@sha256:3ccfdfb4f67d6b15d69e5b590eebbd96c3f7ec53f8ced1a9a4aac60d93aa11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a774814288e1fd893f7331df669215f646f6cf98fb4a0b0b67ac130ecbc292`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aeeb60ebe6caabdf00087638b31e612157fb76df70f09daae4aaf298f3339d`  
		Last Modified: Thu, 01 May 2025 16:46:48 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:fb05c36e05cb6fd98ab9578bf3f3522c5dda3b8db87c4b3f994bab4fb2c52bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5217c566ef49ccb62eb72b4d63e24c23407e01d1a483f783d19f43deb31978`

```dockerfile
```

-	Layers:
	-	`sha256:bf329933f2001d892b1db19e56be440c7cc1471cbfd53e85627380b9eeecfa13`  
		Last Modified: Thu, 01 May 2025 16:46:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b6ca28cb0f26d521de072e0428eda868dfc1053f02ee89da87e122abbbcc5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a244218290447acaf4597f5813cdd9b33d442f548e97ac69f3ba9bf77b007e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2635c150a57e298a8572ecc73e84b470cf6f64d5d04bb81b438de0d2a578e`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ba5d033bc950f897b411410b7bfb78b5058d32b86b8ffaf7265e62e043e20f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfee55275a487ab6b108c1e0c26fd8d58c5914aac413eaa083766552f361395`

```dockerfile
```

-	Layers:
	-	`sha256:49a95ae7819d7b3b2da785dc18d291000c88914a33318296ef12da97f0616623`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:df20fbfe0bb522658b99afc79ac3890e502c6970a671f3ad578076fe583eb5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b209380767db19497ed31465cd8ea6f57747719a0b7c3424178728fa4ef380`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b68896e7d11974b1313147602b9b9672df2062a2a1ba0fb0254c70bc0dc0e`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b0cfe6d5686bf2b793b3456b56e58e4709af2b1be8896efd6a883dbf3afd8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4cc0b81dfacb98ca6bbac7f072e0daf502def9b3d32ec1fa94ea2ba790bc8c`

```dockerfile
```

-	Layers:
	-	`sha256:54a912eaf0fc6d63db9786e668ee5fbd92a4b32c3480891aa1db26c32b50284c`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:935fb840a8c73adfaff297b1980187748a4b3fd7816c4a78cb3524165d20a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783285edc88812d5d1cac420dd84fda126b9342da1ddd4a5ad24724d70b0766`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc364f50cefcf174b35bb61af86057cdb8d5030b40433f6a32f2b2c9b8c05d`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:245530ad8e2639d51db319933a737ae5e6d6d451cad28296889bd066ed9e87f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d366dc53cfe6e71c360d90a3e634be45150175d442cc53c416936d03bd1556c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18e0c2e5eab72b82113e68b6bd114b5e2127dae37ea5fdae90468e3f51f31eb`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:75880b6c63b7cebe9255b7608fbc73d00b8933e46ca0cbbe90c2b6c58d8abb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da7825b3708ab6faf26cc9ccdab7321e3396534294da2330041bd16cc10322`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01318be57fae6110f9534fcddaee8e6a1c3e69f25ae1e4d106c4c8de8ae29409`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5b57ed930c2667fe65ad1bcee2b9818a79e11a7500f81bf6abf002f323a40614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee26f11ca9c8bf7645aaa93d4a9b71a44b8e5eec7c6d2da88292202cb0c94ba0`

```dockerfile
```

-	Layers:
	-	`sha256:8d564d37941aabc78a509d369ad843dd9bbd31e598a5eb086e6ed43f44520de0`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; s390x

```console
$ docker pull nats@sha256:84075ae55673cd07f22de63d995d5fb6f6ad9237fb03cd9628d8093314717a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8ab527386a9db0e153388584e1d45bde0ef4d42a924ecb08c07492c2cd4188`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d173bad3ebbebf172e48ea474c921f04af212478f36048d2ae48e968fdb19`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:366a7884992207edcdabb534dadc23e5194a82acb271a57feb915092c3161a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a7d69878d9010d1441db5562973317245edebea32c25d731de86833b22a30e`

```dockerfile
```

-	Layers:
	-	`sha256:7d9401f2d8bdddd29f021b02a49ab29c2c347e45f7f6f5fab6e6aaaca052ff85`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-nanoserver`

```console
$ docker pull nats@sha256:1bb553cba2972802ff22b0a1281c11e946a66147579ed4ebab3a310058505097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10.29-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2161d1e1f94ac34edd3eeb3e988a132d0b80e1ae578a28901ced25b5d5a4be04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989144758dca5d5bc74a916c0fbc16f6c3d6772d0ac66f3f5c3154a304fb1926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:22:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:23:00 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:23:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:23:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a13d3a2ccb6d6921800013fd2bafb22fdddd0839e1702de9c3ed71d624e01`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcabfa424d4764fde945c8ef78c9a9e3447fe9fa96663564fac1e1ad6b5269`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 6.3 MB (6298138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4d978b7505d1beafe17ec8bd7a83c79d9f90cb9c838cacb0a65ba0d62e925`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b062d5e7dc7c72a41dce15f3c57b7c154f653dbf3f3af39380330b8378d24`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee38558620886b53646fde38cf4bceb3c93944c4c1fbf218d71a2d1ea7d7b1a`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac45ac9cff58dc0e1d04bdba98a370b8fb4b0092dcb07e4f7b213595a395a8`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-nanoserver-1809`

```console
$ docker pull nats@sha256:1bb553cba2972802ff22b0a1281c11e946a66147579ed4ebab3a310058505097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10.29-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2161d1e1f94ac34edd3eeb3e988a132d0b80e1ae578a28901ced25b5d5a4be04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989144758dca5d5bc74a916c0fbc16f6c3d6772d0ac66f3f5c3154a304fb1926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:22:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:23:00 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:23:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:23:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a13d3a2ccb6d6921800013fd2bafb22fdddd0839e1702de9c3ed71d624e01`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcabfa424d4764fde945c8ef78c9a9e3447fe9fa96663564fac1e1ad6b5269`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 6.3 MB (6298138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4d978b7505d1beafe17ec8bd7a83c79d9f90cb9c838cacb0a65ba0d62e925`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b062d5e7dc7c72a41dce15f3c57b7c154f653dbf3f3af39380330b8378d24`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee38558620886b53646fde38cf4bceb3c93944c4c1fbf218d71a2d1ea7d7b1a`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac45ac9cff58dc0e1d04bdba98a370b8fb4b0092dcb07e4f7b213595a395a8`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-scratch`

```console
$ docker pull nats@sha256:f1fc04f650ac4cd8c40aa3c7c46a0f2066999a61b4e3be99945151adb1d24aa5
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

### `nats:2.10.29-scratch` - linux; amd64

```console
$ docker pull nats@sha256:3ccfdfb4f67d6b15d69e5b590eebbd96c3f7ec53f8ced1a9a4aac60d93aa11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a774814288e1fd893f7331df669215f646f6cf98fb4a0b0b67ac130ecbc292`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aeeb60ebe6caabdf00087638b31e612157fb76df70f09daae4aaf298f3339d`  
		Last Modified: Thu, 01 May 2025 16:46:48 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:fb05c36e05cb6fd98ab9578bf3f3522c5dda3b8db87c4b3f994bab4fb2c52bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5217c566ef49ccb62eb72b4d63e24c23407e01d1a483f783d19f43deb31978`

```dockerfile
```

-	Layers:
	-	`sha256:bf329933f2001d892b1db19e56be440c7cc1471cbfd53e85627380b9eeecfa13`  
		Last Modified: Thu, 01 May 2025 16:46:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b6ca28cb0f26d521de072e0428eda868dfc1053f02ee89da87e122abbbcc5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a244218290447acaf4597f5813cdd9b33d442f548e97ac69f3ba9bf77b007e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2635c150a57e298a8572ecc73e84b470cf6f64d5d04bb81b438de0d2a578e`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ba5d033bc950f897b411410b7bfb78b5058d32b86b8ffaf7265e62e043e20f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfee55275a487ab6b108c1e0c26fd8d58c5914aac413eaa083766552f361395`

```dockerfile
```

-	Layers:
	-	`sha256:49a95ae7819d7b3b2da785dc18d291000c88914a33318296ef12da97f0616623`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:df20fbfe0bb522658b99afc79ac3890e502c6970a671f3ad578076fe583eb5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b209380767db19497ed31465cd8ea6f57747719a0b7c3424178728fa4ef380`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b68896e7d11974b1313147602b9b9672df2062a2a1ba0fb0254c70bc0dc0e`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b0cfe6d5686bf2b793b3456b56e58e4709af2b1be8896efd6a883dbf3afd8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4cc0b81dfacb98ca6bbac7f072e0daf502def9b3d32ec1fa94ea2ba790bc8c`

```dockerfile
```

-	Layers:
	-	`sha256:54a912eaf0fc6d63db9786e668ee5fbd92a4b32c3480891aa1db26c32b50284c`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:935fb840a8c73adfaff297b1980187748a4b3fd7816c4a78cb3524165d20a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783285edc88812d5d1cac420dd84fda126b9342da1ddd4a5ad24724d70b0766`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc364f50cefcf174b35bb61af86057cdb8d5030b40433f6a32f2b2c9b8c05d`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:245530ad8e2639d51db319933a737ae5e6d6d451cad28296889bd066ed9e87f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d366dc53cfe6e71c360d90a3e634be45150175d442cc53c416936d03bd1556c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18e0c2e5eab72b82113e68b6bd114b5e2127dae37ea5fdae90468e3f51f31eb`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:75880b6c63b7cebe9255b7608fbc73d00b8933e46ca0cbbe90c2b6c58d8abb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da7825b3708ab6faf26cc9ccdab7321e3396534294da2330041bd16cc10322`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01318be57fae6110f9534fcddaee8e6a1c3e69f25ae1e4d106c4c8de8ae29409`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5b57ed930c2667fe65ad1bcee2b9818a79e11a7500f81bf6abf002f323a40614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee26f11ca9c8bf7645aaa93d4a9b71a44b8e5eec7c6d2da88292202cb0c94ba0`

```dockerfile
```

-	Layers:
	-	`sha256:8d564d37941aabc78a509d369ad843dd9bbd31e598a5eb086e6ed43f44520de0`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; s390x

```console
$ docker pull nats@sha256:84075ae55673cd07f22de63d995d5fb6f6ad9237fb03cd9628d8093314717a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8ab527386a9db0e153388584e1d45bde0ef4d42a924ecb08c07492c2cd4188`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d173bad3ebbebf172e48ea474c921f04af212478f36048d2ae48e968fdb19`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:366a7884992207edcdabb534dadc23e5194a82acb271a57feb915092c3161a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a7d69878d9010d1441db5562973317245edebea32c25d731de86833b22a30e`

```dockerfile
```

-	Layers:
	-	`sha256:7d9401f2d8bdddd29f021b02a49ab29c2c347e45f7f6f5fab6e6aaaca052ff85`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-windowsservercore`

```console
$ docker pull nats@sha256:497a9cb9259dea3157192c47053d210e90285f245a40302113147c78935f415a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10.29-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7cee34982b9961eca0791af019a96210f3acfb0b541c777fef4674acce9ebffd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190701818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304379749a747af729040c8fc24ea557b571e8851904d77062912ce7f19ed13e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:57:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_SERVER=2.10.29
# Wed, 14 May 2025 20:57:48 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Wed, 14 May 2025 20:57:49 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Wed, 14 May 2025 20:58:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 20:58:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 20:58:40 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 20:58:41 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 20:58:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 20:58:42 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:61077ce6abbdae8515ed8aee8d125e78c4cac8c784a425794f86615c897c5350`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794b39a004828c5754f1625d423719263b57a56c0f9d146dac4f3f4eeca00619`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084927b2191adc36daf6f816dbfc6f7fc2f39616f120eb2651541cc473469c1d`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f419ade08147d57977fc7931cc12b84db32642f88e21afce4da375e7e51dee`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef3124c22d55ce500386d4b4e302947756899e4b22694baa0f983ac49331ec8`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170ce137abceda359d4a3c7b368ea88cf8f545610e1cf97d8b6a883455b6cb49`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 332.9 KB (332919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7d2e2aeda12346ac02cd0fbd2469f9b9139a606a9993af6d38d1f5067291f4`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 6.6 MB (6639239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e924aac8362f8466698a1b3cb28f4d7cc0b32f9ec6db4146dae40bb696b0b9a`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2218925f1c3045fd7b8c4c505a18617b96b18b25084ff3c704702a01def48dcf`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe49501346aad8e6904d0c916ae6c2977054bb03a19422d25bb61fa17f4c048`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eee89edd57fb6cba67f1345aa73742d0a392b8fce89e8db3349b02fab6f9292`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-windowsservercore-1809`

```console
$ docker pull nats@sha256:497a9cb9259dea3157192c47053d210e90285f245a40302113147c78935f415a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10.29-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7cee34982b9961eca0791af019a96210f3acfb0b541c777fef4674acce9ebffd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190701818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304379749a747af729040c8fc24ea557b571e8851904d77062912ce7f19ed13e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:57:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_SERVER=2.10.29
# Wed, 14 May 2025 20:57:48 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Wed, 14 May 2025 20:57:49 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Wed, 14 May 2025 20:58:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 20:58:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 20:58:40 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 20:58:41 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 20:58:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 20:58:42 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:61077ce6abbdae8515ed8aee8d125e78c4cac8c784a425794f86615c897c5350`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794b39a004828c5754f1625d423719263b57a56c0f9d146dac4f3f4eeca00619`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084927b2191adc36daf6f816dbfc6f7fc2f39616f120eb2651541cc473469c1d`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f419ade08147d57977fc7931cc12b84db32642f88e21afce4da375e7e51dee`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef3124c22d55ce500386d4b4e302947756899e4b22694baa0f983ac49331ec8`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170ce137abceda359d4a3c7b368ea88cf8f545610e1cf97d8b6a883455b6cb49`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 332.9 KB (332919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7d2e2aeda12346ac02cd0fbd2469f9b9139a606a9993af6d38d1f5067291f4`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 6.6 MB (6639239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e924aac8362f8466698a1b3cb28f4d7cc0b32f9ec6db4146dae40bb696b0b9a`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2218925f1c3045fd7b8c4c505a18617b96b18b25084ff3c704702a01def48dcf`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe49501346aad8e6904d0c916ae6c2977054bb03a19422d25bb61fa17f4c048`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eee89edd57fb6cba67f1345aa73742d0a392b8fce89e8db3349b02fab6f9292`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11`

```console
$ docker pull nats@sha256:7c80eff5349a3ecaffff014f6cdae20a8d2c5f11cab835bcb76a56275e2719e9
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
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11` - linux; amd64

```console
$ docker pull nats@sha256:3669c7dc73d88251f131a5507f94fe74fef33b461c16666813ac84e7b807bca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2dc40e2ee2ef54306454e58ff7f7b318bd40949cd7d747c67cc26b2daf553`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Thu, 22 May 2025 13:55:01 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Thu, 22 May 2025 16:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:40c2e8c019de84dd8609363ad056325e160ff7d3c22583776cba7d9c14bbb0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ac87fa640a0df9ed5554a115493a87055629ce3f52f77a933bf54b1c5ee29`

```dockerfile
```

-	Layers:
	-	`sha256:edbca2e0be9710afcbe43e2fca6896927d7e6c12d43816973cc4a1e04ec762f6`  
		Last Modified: Thu, 22 May 2025 16:47:18 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:4fbfa5ce075ad78297fbfc8ce0126de19a685b441759d77b6dc6aeb130f38561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279bf33611cd3f2a188a9a0afdb244877743689160627fcf8de576cdda072a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd26e0aad9f1b20096e647e74023489621fc5ba4de7dc4747a0d0d4bb2823fc7`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:06aa17a9acdaae3c275cb86e786faac7651dd30f6b6aab7b648db0e966524ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34ed5638318182fa373a29edf2eae4badc5e5688dd08e8af559b347675e23c`

```dockerfile
```

-	Layers:
	-	`sha256:ea20c201702d517a06fc320a50a878fa897f58fd5a8cb89d7bbeb5af7599f148`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:e1b35decc46dc6b9b6a62e50a10d13095888c34f740a2d2069d5fa4a3a406fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04111c7501581b1636dc5516802ecee6c26dcb627cbbec34e273d2575ac0a9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Thu, 22 May 2025 13:54:58 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9293b5f4677cf2db6d8d8a8a01b039e1134d378f77c7efe3d7b11072a3f4e4`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:e1653a1054fd8a003f0dad883474a71c0d46a243bb3364d28c690e1d5c521e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2828a9839d98f985cc7bb11688ead3394a6003466851fff29ab209a775564`

```dockerfile
```

-	Layers:
	-	`sha256:fddb83fedd24e6e2d6c0afc61f16768121ba63342f1bc0d540cd75cf7e202edc`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6390d133be19faae15ea0b0addf722e3dd60c9412dc5b14c8120e9ff773fcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a4332082216fadc8b7d39be0643a4193e18b21e9a0815bc8a7476b0d9ff39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:c9a882fa6d5de0d1f1a746c11bb26c98258eba146870604781263ee98916694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8632a81f326876343b421492b672bc64785711cd147bece1386ca476b11fbe2`

```dockerfile
```

-	Layers:
	-	`sha256:a3807445f86645a59e75d2d727c573109c35a356652cf8cea33291752e44a501`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:b2a62d6e7160e9fe02b4fbc54a4d38f4854e955277ad06a32a0f9730fb145030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77959cb575e1e4e6a7ed10889593eb60a12b91bc3daef1a047f20d5b849823e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac6089227b1bf8e0c5485c9fafeb79be71f899610ed5cfe50750ec671c2150`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:d61332ce9f2f76ef458a63c4394a0ea8f006176df53c6c854d854c880fb56c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cab1c0c3130120e0299edad95932ca44704b3459f34c83f21aff0efd97ee56`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a85cd3ea43c578ae1c73d84bc6e9c7dbeba30594051365b578136deebce76`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 10.6 KB (10555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:bb999cd435e52627799ba8d3bba323e34937cebdbf4cbaf4747d8b5d0b4f377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5364ba179bbae6d216c47196a0e607812cf16327562d528b0dd7a39275fc7b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Thu, 22 May 2025 13:55:02 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8c9019ec6e6b470ca5a6c4139cddf8579e979b93b02f0847ea6459c5bdf68`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:b5bd7ec7061996df7f9d251b0f55960fc4ea80d15e93923f70faa53a1dfdcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88da26773cc178303a133db9d426aa861f654fb7d59e009907bcc91bd848fb`

```dockerfile
```

-	Layers:
	-	`sha256:a17428cf33c792fdb7174ce215c54081e07fdd09cde209156006d308f5279ebd`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:0451ec62031943afa591cf4e5f9404bce65b55a8671ab93a7d581d8028fc12a9
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

### `nats:2.11-alpine` - linux; amd64

```console
$ docker pull nats@sha256:78c1052292c8d1bdabeca33c5cde417bb3b56c9a9a6707afd896ac74f8010e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10425424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752c0a111d15eafa05314d85b32bdfc63c7a5190ba26712078e014ad5c12906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc83d3e520670ed878bfe5964638db9895fc2873acb2a25b7bd3a8b2916c3e`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 6.8 MB (6782209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1065a99208ad32f21adf1cc2983a318f6d19b678ce12103514758c5e75a1359`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dc1d69fb3bb313c6fce126295baf9e644c735c5b709cb57462cf134d8b7535`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6425e7c42e8f01aed46c0c5a2c0e1538c4703e432be6a853fe400d6c070c46b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd03d3d4671688731cc2113bd6bce676daf486062cf7bf8a0ad509235b375b3`

```dockerfile
```

-	Layers:
	-	`sha256:8d13d777cfed6af6d839ab64cb7dc1dd2e3b2e7c64170ca5695c3a937b560432`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:e9129c76ec8b39cfb61261ea43a529d2b048a22bd43dde23405476211d952fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa20ad8f845d52ef2ede0cc269b4ade46343bd8ae9d91e0f89a101e164019a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedc41dc7d645196f64f183990aac84922d7dfeca30cdd62cc58afacced1e53e`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 6.5 MB (6500243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f84ca9e26add3645800a5d8875d035548ece025cd495d093506600b5fa3639`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a0bc1a6e6b564bac3444b012da7c2bd95b00fc4b30e2183f58fdfe67a29efc`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cfc622005d6c0083932d3a442389e5ba0fed2eee0d382384117e632be9d2cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98224cc21fc700a931065a4257f0f576cb24d83f9f4cf3a756dbb8cfc211de84`

```dockerfile
```

-	Layers:
	-	`sha256:5b980a9b2e5b75054cfabe65a0bb0ca426c2aeb5cb4d1d0a7b3616d6b089aba1`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f51b3ede38c787e45a1c58fe1758aa726cfc126eed5ef13dc9a66dbcfe4d8e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9587301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fcc07ad9637e3d6023e9c3faf8df41d76537efd7136923fe276ce3124a21f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9afbd37259973c94e964e514f1fd5331fdff7c8a20c358c64209a54939892`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 6.5 MB (6488204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e46bef85887a3ca7141cdb651fb0907947c31453e3dd12d5f2e75d659f9bb81`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ada5b8ea797d2e67d9817b4735e298f9e4328503c9b4faff09c816dd2a3fe`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:43fb4c5979976f655a571482f2fb7c95bdcfe76ea5c3d03822e834dba8c8ba43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103eb0538b45ceeaf49344cd2e475459141bba59c3b68cfa4b3f8c81bfaa0292`

```dockerfile
```

-	Layers:
	-	`sha256:48a6d4944ad8da069b2dcc13b6bf204e8ba6994953e03cdc717459fc9bec1bbc`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:361d07db47a72d53a1159ce806effcfaacddb5c24254dc346aa6ed24d2eaff6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c4a01a93d1901d7daaa7ad147102df5dc250516eb1b935b673cb01b2de9436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28900756089c34ef75f78f9bc43820aee795ebced2ef164f4371a469020c319`  
		Last Modified: Thu, 22 May 2025 20:04:29 GMT  
		Size: 6.3 MB (6271430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a19d69a59c9c3d035125ee920379ce8b337cb0de1eb1646fa3b37bcc5bd4eca`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002df6ee873e4c8b8c2d32bc19571ba115cbaeeaa22dbe5e19ea24a00121560a`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:eeec07d9dba12fff9a629635d9822e295cbd2866800be7c10ae0f0eda767c376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb57113d3b7d11444b789b3d12801ddfaf3eadc8944e2457447d1469cc94db`

```dockerfile
```

-	Layers:
	-	`sha256:cac3279af5a354235660e8ed87c54fddc39e37fe276433cdd00c7a04a3f5877c`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:6c62a05e9d2c74252f7e85ca263ff11fa47ca8d6a2314c95ef35830ca7dd5947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9829497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f82ed4f59bb1fc3f2bb1bf520c03a108a4b1201a308129e9f9c437eb69d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab090fb5974c5fbc532a324c8b6ff89147f7b095e88f59c95200ff29b503d4ed`  
		Last Modified: Thu, 22 May 2025 16:46:06 GMT  
		Size: 6.3 MB (6254178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ffdff7943fa553d5c46cd9bfd7cdb0aaf807fd213df6a3be9c0f47276b45d`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b243223ddfaabf20dea42482c30a57a1960b976113f905a07742d49e8fd76`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:209d5ce0eb3e58f76c4baefc159b91c7c24036c43252c4c06634f4218bfc2ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc856abe1e071c3b5e0dd0ac6a265939b68986e20ed0a612a3577747ed39b949`

```dockerfile
```

-	Layers:
	-	`sha256:9d5d8fc63a7e90cae4235128e35cce1f4b9143f897cba2831823fdf635d1c1a3`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:113aca5863f11d04e9dcafd0a79496a1ecc86cdc2ccf02b720467c79eb2c1b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10087904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a783e13b44bb39120f57f582d383ada710ad715fc963f625760233ace3e4ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f6217bb5b7f1a95efe567548c35356165dc66ae69bfe675bd4d750bb78b516`  
		Last Modified: Thu, 22 May 2025 17:33:09 GMT  
		Size: 6.6 MB (6619363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9020a2695371d3927fa6fb04d07c6ee8cfdbdf0c94ab360a4d3e121df860ce`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9b02a9ab09a6778612e627ead79927f9eab9b1f58a792a27d86b207e883eb`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2adcfab66a18b065b7c3a97ae3a3a6266b23138c34d08229363bae6d3eb99f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b88a3ff73d885d4df2ea9e8203001daa5832c33dbba49d1127c7ded5b3724`

```dockerfile
```

-	Layers:
	-	`sha256:2e6f543ee243ec43d02935e873e329d235728c7301898d56b1cc48bf41df88aa`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.21`

```console
$ docker pull nats@sha256:0451ec62031943afa591cf4e5f9404bce65b55a8671ab93a7d581d8028fc12a9
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

### `nats:2.11-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:78c1052292c8d1bdabeca33c5cde417bb3b56c9a9a6707afd896ac74f8010e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10425424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752c0a111d15eafa05314d85b32bdfc63c7a5190ba26712078e014ad5c12906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc83d3e520670ed878bfe5964638db9895fc2873acb2a25b7bd3a8b2916c3e`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 6.8 MB (6782209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1065a99208ad32f21adf1cc2983a318f6d19b678ce12103514758c5e75a1359`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dc1d69fb3bb313c6fce126295baf9e644c735c5b709cb57462cf134d8b7535`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6425e7c42e8f01aed46c0c5a2c0e1538c4703e432be6a853fe400d6c070c46b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd03d3d4671688731cc2113bd6bce676daf486062cf7bf8a0ad509235b375b3`

```dockerfile
```

-	Layers:
	-	`sha256:8d13d777cfed6af6d839ab64cb7dc1dd2e3b2e7c64170ca5695c3a937b560432`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:e9129c76ec8b39cfb61261ea43a529d2b048a22bd43dde23405476211d952fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa20ad8f845d52ef2ede0cc269b4ade46343bd8ae9d91e0f89a101e164019a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedc41dc7d645196f64f183990aac84922d7dfeca30cdd62cc58afacced1e53e`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 6.5 MB (6500243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f84ca9e26add3645800a5d8875d035548ece025cd495d093506600b5fa3639`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a0bc1a6e6b564bac3444b012da7c2bd95b00fc4b30e2183f58fdfe67a29efc`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cfc622005d6c0083932d3a442389e5ba0fed2eee0d382384117e632be9d2cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98224cc21fc700a931065a4257f0f576cb24d83f9f4cf3a756dbb8cfc211de84`

```dockerfile
```

-	Layers:
	-	`sha256:5b980a9b2e5b75054cfabe65a0bb0ca426c2aeb5cb4d1d0a7b3616d6b089aba1`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:f51b3ede38c787e45a1c58fe1758aa726cfc126eed5ef13dc9a66dbcfe4d8e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9587301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fcc07ad9637e3d6023e9c3faf8df41d76537efd7136923fe276ce3124a21f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9afbd37259973c94e964e514f1fd5331fdff7c8a20c358c64209a54939892`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 6.5 MB (6488204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e46bef85887a3ca7141cdb651fb0907947c31453e3dd12d5f2e75d659f9bb81`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ada5b8ea797d2e67d9817b4735e298f9e4328503c9b4faff09c816dd2a3fe`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:43fb4c5979976f655a571482f2fb7c95bdcfe76ea5c3d03822e834dba8c8ba43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103eb0538b45ceeaf49344cd2e475459141bba59c3b68cfa4b3f8c81bfaa0292`

```dockerfile
```

-	Layers:
	-	`sha256:48a6d4944ad8da069b2dcc13b6bf204e8ba6994953e03cdc717459fc9bec1bbc`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:361d07db47a72d53a1159ce806effcfaacddb5c24254dc346aa6ed24d2eaff6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c4a01a93d1901d7daaa7ad147102df5dc250516eb1b935b673cb01b2de9436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28900756089c34ef75f78f9bc43820aee795ebced2ef164f4371a469020c319`  
		Last Modified: Thu, 22 May 2025 20:04:29 GMT  
		Size: 6.3 MB (6271430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a19d69a59c9c3d035125ee920379ce8b337cb0de1eb1646fa3b37bcc5bd4eca`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002df6ee873e4c8b8c2d32bc19571ba115cbaeeaa22dbe5e19ea24a00121560a`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:eeec07d9dba12fff9a629635d9822e295cbd2866800be7c10ae0f0eda767c376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb57113d3b7d11444b789b3d12801ddfaf3eadc8944e2457447d1469cc94db`

```dockerfile
```

-	Layers:
	-	`sha256:cac3279af5a354235660e8ed87c54fddc39e37fe276433cdd00c7a04a3f5877c`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:6c62a05e9d2c74252f7e85ca263ff11fa47ca8d6a2314c95ef35830ca7dd5947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9829497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f82ed4f59bb1fc3f2bb1bf520c03a108a4b1201a308129e9f9c437eb69d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab090fb5974c5fbc532a324c8b6ff89147f7b095e88f59c95200ff29b503d4ed`  
		Last Modified: Thu, 22 May 2025 16:46:06 GMT  
		Size: 6.3 MB (6254178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ffdff7943fa553d5c46cd9bfd7cdb0aaf807fd213df6a3be9c0f47276b45d`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b243223ddfaabf20dea42482c30a57a1960b976113f905a07742d49e8fd76`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:209d5ce0eb3e58f76c4baefc159b91c7c24036c43252c4c06634f4218bfc2ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc856abe1e071c3b5e0dd0ac6a265939b68986e20ed0a612a3577747ed39b949`

```dockerfile
```

-	Layers:
	-	`sha256:9d5d8fc63a7e90cae4235128e35cce1f4b9143f897cba2831823fdf635d1c1a3`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:113aca5863f11d04e9dcafd0a79496a1ecc86cdc2ccf02b720467c79eb2c1b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10087904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a783e13b44bb39120f57f582d383ada710ad715fc963f625760233ace3e4ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f6217bb5b7f1a95efe567548c35356165dc66ae69bfe675bd4d750bb78b516`  
		Last Modified: Thu, 22 May 2025 17:33:09 GMT  
		Size: 6.6 MB (6619363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9020a2695371d3927fa6fb04d07c6ee8cfdbdf0c94ab360a4d3e121df860ce`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9b02a9ab09a6778612e627ead79927f9eab9b1f58a792a27d86b207e883eb`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:2adcfab66a18b065b7c3a97ae3a3a6266b23138c34d08229363bae6d3eb99f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b88a3ff73d885d4df2ea9e8203001daa5832c33dbba49d1127c7ded5b3724`

```dockerfile
```

-	Layers:
	-	`sha256:2e6f543ee243ec43d02935e873e329d235728c7301898d56b1cc48bf41df88aa`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:d0c61f71b425352fd0d54492562dcff4709fdaa5979afbef9a2e13df957fa26e
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

### `nats:2.11-linux` - linux; amd64

```console
$ docker pull nats@sha256:3669c7dc73d88251f131a5507f94fe74fef33b461c16666813ac84e7b807bca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2dc40e2ee2ef54306454e58ff7f7b318bd40949cd7d747c67cc26b2daf553`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Thu, 22 May 2025 13:55:01 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Thu, 22 May 2025 16:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:40c2e8c019de84dd8609363ad056325e160ff7d3c22583776cba7d9c14bbb0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ac87fa640a0df9ed5554a115493a87055629ce3f52f77a933bf54b1c5ee29`

```dockerfile
```

-	Layers:
	-	`sha256:edbca2e0be9710afcbe43e2fca6896927d7e6c12d43816973cc4a1e04ec762f6`  
		Last Modified: Thu, 22 May 2025 16:47:18 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4fbfa5ce075ad78297fbfc8ce0126de19a685b441759d77b6dc6aeb130f38561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279bf33611cd3f2a188a9a0afdb244877743689160627fcf8de576cdda072a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd26e0aad9f1b20096e647e74023489621fc5ba4de7dc4747a0d0d4bb2823fc7`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:06aa17a9acdaae3c275cb86e786faac7651dd30f6b6aab7b648db0e966524ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34ed5638318182fa373a29edf2eae4badc5e5688dd08e8af559b347675e23c`

```dockerfile
```

-	Layers:
	-	`sha256:ea20c201702d517a06fc320a50a878fa897f58fd5a8cb89d7bbeb5af7599f148`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e1b35decc46dc6b9b6a62e50a10d13095888c34f740a2d2069d5fa4a3a406fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04111c7501581b1636dc5516802ecee6c26dcb627cbbec34e273d2575ac0a9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Thu, 22 May 2025 13:54:58 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9293b5f4677cf2db6d8d8a8a01b039e1134d378f77c7efe3d7b11072a3f4e4`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e1653a1054fd8a003f0dad883474a71c0d46a243bb3364d28c690e1d5c521e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2828a9839d98f985cc7bb11688ead3394a6003466851fff29ab209a775564`

```dockerfile
```

-	Layers:
	-	`sha256:fddb83fedd24e6e2d6c0afc61f16768121ba63342f1bc0d540cd75cf7e202edc`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6390d133be19faae15ea0b0addf722e3dd60c9412dc5b14c8120e9ff773fcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a4332082216fadc8b7d39be0643a4193e18b21e9a0815bc8a7476b0d9ff39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c9a882fa6d5de0d1f1a746c11bb26c98258eba146870604781263ee98916694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8632a81f326876343b421492b672bc64785711cd147bece1386ca476b11fbe2`

```dockerfile
```

-	Layers:
	-	`sha256:a3807445f86645a59e75d2d727c573109c35a356652cf8cea33291752e44a501`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:b2a62d6e7160e9fe02b4fbc54a4d38f4854e955277ad06a32a0f9730fb145030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77959cb575e1e4e6a7ed10889593eb60a12b91bc3daef1a047f20d5b849823e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac6089227b1bf8e0c5485c9fafeb79be71f899610ed5cfe50750ec671c2150`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d61332ce9f2f76ef458a63c4394a0ea8f006176df53c6c854d854c880fb56c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cab1c0c3130120e0299edad95932ca44704b3459f34c83f21aff0efd97ee56`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a85cd3ea43c578ae1c73d84bc6e9c7dbeba30594051365b578136deebce76`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 10.6 KB (10555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:bb999cd435e52627799ba8d3bba323e34937cebdbf4cbaf4747d8b5d0b4f377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5364ba179bbae6d216c47196a0e607812cf16327562d528b0dd7a39275fc7b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Thu, 22 May 2025 13:55:02 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8c9019ec6e6b470ca5a6c4139cddf8579e979b93b02f0847ea6459c5bdf68`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b5bd7ec7061996df7f9d251b0f55960fc4ea80d15e93923f70faa53a1dfdcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88da26773cc178303a133db9d426aa861f654fb7d59e009907bcc91bd848fb`

```dockerfile
```

-	Layers:
	-	`sha256:a17428cf33c792fdb7174ce215c54081e07fdd09cde209156006d308f5279ebd`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:5cc9d495e86b7caa02ed8c6efd98071810a86094d0365b49cd0d6c923575d630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-1809`

```console
$ docker pull nats@sha256:5cc9d495e86b7caa02ed8c6efd98071810a86094d0365b49cd0d6c923575d630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

```console
$ docker pull nats@sha256:d0c61f71b425352fd0d54492562dcff4709fdaa5979afbef9a2e13df957fa26e
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

### `nats:2.11-scratch` - linux; amd64

```console
$ docker pull nats@sha256:3669c7dc73d88251f131a5507f94fe74fef33b461c16666813ac84e7b807bca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2dc40e2ee2ef54306454e58ff7f7b318bd40949cd7d747c67cc26b2daf553`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Thu, 22 May 2025 13:55:01 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Thu, 22 May 2025 16:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:40c2e8c019de84dd8609363ad056325e160ff7d3c22583776cba7d9c14bbb0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ac87fa640a0df9ed5554a115493a87055629ce3f52f77a933bf54b1c5ee29`

```dockerfile
```

-	Layers:
	-	`sha256:edbca2e0be9710afcbe43e2fca6896927d7e6c12d43816973cc4a1e04ec762f6`  
		Last Modified: Thu, 22 May 2025 16:47:18 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4fbfa5ce075ad78297fbfc8ce0126de19a685b441759d77b6dc6aeb130f38561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279bf33611cd3f2a188a9a0afdb244877743689160627fcf8de576cdda072a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd26e0aad9f1b20096e647e74023489621fc5ba4de7dc4747a0d0d4bb2823fc7`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:06aa17a9acdaae3c275cb86e786faac7651dd30f6b6aab7b648db0e966524ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34ed5638318182fa373a29edf2eae4badc5e5688dd08e8af559b347675e23c`

```dockerfile
```

-	Layers:
	-	`sha256:ea20c201702d517a06fc320a50a878fa897f58fd5a8cb89d7bbeb5af7599f148`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e1b35decc46dc6b9b6a62e50a10d13095888c34f740a2d2069d5fa4a3a406fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04111c7501581b1636dc5516802ecee6c26dcb627cbbec34e273d2575ac0a9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Thu, 22 May 2025 13:54:58 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9293b5f4677cf2db6d8d8a8a01b039e1134d378f77c7efe3d7b11072a3f4e4`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e1653a1054fd8a003f0dad883474a71c0d46a243bb3364d28c690e1d5c521e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2828a9839d98f985cc7bb11688ead3394a6003466851fff29ab209a775564`

```dockerfile
```

-	Layers:
	-	`sha256:fddb83fedd24e6e2d6c0afc61f16768121ba63342f1bc0d540cd75cf7e202edc`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6390d133be19faae15ea0b0addf722e3dd60c9412dc5b14c8120e9ff773fcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a4332082216fadc8b7d39be0643a4193e18b21e9a0815bc8a7476b0d9ff39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c9a882fa6d5de0d1f1a746c11bb26c98258eba146870604781263ee98916694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8632a81f326876343b421492b672bc64785711cd147bece1386ca476b11fbe2`

```dockerfile
```

-	Layers:
	-	`sha256:a3807445f86645a59e75d2d727c573109c35a356652cf8cea33291752e44a501`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:b2a62d6e7160e9fe02b4fbc54a4d38f4854e955277ad06a32a0f9730fb145030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77959cb575e1e4e6a7ed10889593eb60a12b91bc3daef1a047f20d5b849823e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac6089227b1bf8e0c5485c9fafeb79be71f899610ed5cfe50750ec671c2150`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d61332ce9f2f76ef458a63c4394a0ea8f006176df53c6c854d854c880fb56c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cab1c0c3130120e0299edad95932ca44704b3459f34c83f21aff0efd97ee56`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a85cd3ea43c578ae1c73d84bc6e9c7dbeba30594051365b578136deebce76`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 10.6 KB (10555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:bb999cd435e52627799ba8d3bba323e34937cebdbf4cbaf4747d8b5d0b4f377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5364ba179bbae6d216c47196a0e607812cf16327562d528b0dd7a39275fc7b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Thu, 22 May 2025 13:55:02 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8c9019ec6e6b470ca5a6c4139cddf8579e979b93b02f0847ea6459c5bdf68`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b5bd7ec7061996df7f9d251b0f55960fc4ea80d15e93923f70faa53a1dfdcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88da26773cc178303a133db9d426aa861f654fb7d59e009907bcc91bd848fb`

```dockerfile
```

-	Layers:
	-	`sha256:a17428cf33c792fdb7174ce215c54081e07fdd09cde209156006d308f5279ebd`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:5eb29aa350e04efd871dc089f00e2332c6fde8340442987c019d24c4d8612952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:3eb16b69114671a8802239d503c0290429cdb314d8a872d6b2e085341c12b4a0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190940335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1f053a6e4022c28324a3e45080faa48d8a7f96dc18ea8250a25af5211529a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 22 May 2025 16:50:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 16:50:25 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Thu, 22 May 2025 16:50:26 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Thu, 22 May 2025 16:51:00 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 May 2025 16:51:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 May 2025 16:51:18 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 16:51:19 GMT
EXPOSE 4222 6222 8222
# Thu, 22 May 2025 16:51:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 16:51:20 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ab467e36de62f69e77619428c80684c172dceff9ed3e77cc0f6ab14e4f32bdfd`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9091f1392b0e4b5a8efd3fa58b0c4a2b6e936430b4e42b68ba16077d4564944d`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf909e97fafaef4ec16a660d02af257e98e54239a7bc6cec966b8e76e70b715`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5d1bc88317b3a5b00e94a85aa69eeff6067de7eacc3b0ae40836597b6b4912`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc3aedb4b361c3a53ea79beee17b5b1e5323e8d429b1c896eb234b053b5198`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1800d06ff1abd05697da24fc89b33bee18003836f4b523b0183785ab5ed2496e`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 357.5 KB (357493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e26a01941a30a2df43651113e13c4254af9daa37d2d460c7eec0e2829bec1`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 6.9 MB (6853143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa50c7d770115bfd2ad8e106b7ba4c236b4240943f9c067a6ea34daf985b973b`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0aea2b23f17071fd4a073f906be4bf64c1c702b06340d09d355bacdc3215a0`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fa330c05a735fa176327db111cb8144a33d927923c98a24221dcfc94ac73cf`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0963e3ada6db5d54c6e1dcfe66033facd31c4474f0a9b67df506cd38b708994a`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-1809`

```console
$ docker pull nats@sha256:5eb29aa350e04efd871dc089f00e2332c6fde8340442987c019d24c4d8612952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:3eb16b69114671a8802239d503c0290429cdb314d8a872d6b2e085341c12b4a0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190940335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1f053a6e4022c28324a3e45080faa48d8a7f96dc18ea8250a25af5211529a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 22 May 2025 16:50:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 16:50:25 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Thu, 22 May 2025 16:50:26 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Thu, 22 May 2025 16:51:00 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 May 2025 16:51:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 May 2025 16:51:18 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 16:51:19 GMT
EXPOSE 4222 6222 8222
# Thu, 22 May 2025 16:51:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 16:51:20 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ab467e36de62f69e77619428c80684c172dceff9ed3e77cc0f6ab14e4f32bdfd`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9091f1392b0e4b5a8efd3fa58b0c4a2b6e936430b4e42b68ba16077d4564944d`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf909e97fafaef4ec16a660d02af257e98e54239a7bc6cec966b8e76e70b715`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5d1bc88317b3a5b00e94a85aa69eeff6067de7eacc3b0ae40836597b6b4912`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc3aedb4b361c3a53ea79beee17b5b1e5323e8d429b1c896eb234b053b5198`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1800d06ff1abd05697da24fc89b33bee18003836f4b523b0183785ab5ed2496e`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 357.5 KB (357493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e26a01941a30a2df43651113e13c4254af9daa37d2d460c7eec0e2829bec1`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 6.9 MB (6853143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa50c7d770115bfd2ad8e106b7ba4c236b4240943f9c067a6ea34daf985b973b`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0aea2b23f17071fd4a073f906be4bf64c1c702b06340d09d355bacdc3215a0`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fa330c05a735fa176327db111cb8144a33d927923c98a24221dcfc94ac73cf`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0963e3ada6db5d54c6e1dcfe66033facd31c4474f0a9b67df506cd38b708994a`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.4`

```console
$ docker pull nats@sha256:7c80eff5349a3ecaffff014f6cdae20a8d2c5f11cab835bcb76a56275e2719e9
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
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11.4` - linux; amd64

```console
$ docker pull nats@sha256:3669c7dc73d88251f131a5507f94fe74fef33b461c16666813ac84e7b807bca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2dc40e2ee2ef54306454e58ff7f7b318bd40949cd7d747c67cc26b2daf553`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Thu, 22 May 2025 13:55:01 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Thu, 22 May 2025 16:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4` - unknown; unknown

```console
$ docker pull nats@sha256:40c2e8c019de84dd8609363ad056325e160ff7d3c22583776cba7d9c14bbb0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ac87fa640a0df9ed5554a115493a87055629ce3f52f77a933bf54b1c5ee29`

```dockerfile
```

-	Layers:
	-	`sha256:edbca2e0be9710afcbe43e2fca6896927d7e6c12d43816973cc4a1e04ec762f6`  
		Last Modified: Thu, 22 May 2025 16:47:18 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4` - linux; arm variant v6

```console
$ docker pull nats@sha256:4fbfa5ce075ad78297fbfc8ce0126de19a685b441759d77b6dc6aeb130f38561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279bf33611cd3f2a188a9a0afdb244877743689160627fcf8de576cdda072a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd26e0aad9f1b20096e647e74023489621fc5ba4de7dc4747a0d0d4bb2823fc7`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4` - unknown; unknown

```console
$ docker pull nats@sha256:06aa17a9acdaae3c275cb86e786faac7651dd30f6b6aab7b648db0e966524ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34ed5638318182fa373a29edf2eae4badc5e5688dd08e8af559b347675e23c`

```dockerfile
```

-	Layers:
	-	`sha256:ea20c201702d517a06fc320a50a878fa897f58fd5a8cb89d7bbeb5af7599f148`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4` - linux; arm variant v7

```console
$ docker pull nats@sha256:e1b35decc46dc6b9b6a62e50a10d13095888c34f740a2d2069d5fa4a3a406fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04111c7501581b1636dc5516802ecee6c26dcb627cbbec34e273d2575ac0a9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Thu, 22 May 2025 13:54:58 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9293b5f4677cf2db6d8d8a8a01b039e1134d378f77c7efe3d7b11072a3f4e4`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4` - unknown; unknown

```console
$ docker pull nats@sha256:e1653a1054fd8a003f0dad883474a71c0d46a243bb3364d28c690e1d5c521e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2828a9839d98f985cc7bb11688ead3394a6003466851fff29ab209a775564`

```dockerfile
```

-	Layers:
	-	`sha256:fddb83fedd24e6e2d6c0afc61f16768121ba63342f1bc0d540cd75cf7e202edc`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6390d133be19faae15ea0b0addf722e3dd60c9412dc5b14c8120e9ff773fcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a4332082216fadc8b7d39be0643a4193e18b21e9a0815bc8a7476b0d9ff39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4` - unknown; unknown

```console
$ docker pull nats@sha256:c9a882fa6d5de0d1f1a746c11bb26c98258eba146870604781263ee98916694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8632a81f326876343b421492b672bc64785711cd147bece1386ca476b11fbe2`

```dockerfile
```

-	Layers:
	-	`sha256:a3807445f86645a59e75d2d727c573109c35a356652cf8cea33291752e44a501`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4` - linux; ppc64le

```console
$ docker pull nats@sha256:b2a62d6e7160e9fe02b4fbc54a4d38f4854e955277ad06a32a0f9730fb145030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77959cb575e1e4e6a7ed10889593eb60a12b91bc3daef1a047f20d5b849823e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac6089227b1bf8e0c5485c9fafeb79be71f899610ed5cfe50750ec671c2150`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4` - unknown; unknown

```console
$ docker pull nats@sha256:d61332ce9f2f76ef458a63c4394a0ea8f006176df53c6c854d854c880fb56c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cab1c0c3130120e0299edad95932ca44704b3459f34c83f21aff0efd97ee56`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a85cd3ea43c578ae1c73d84bc6e9c7dbeba30594051365b578136deebce76`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 10.6 KB (10555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4` - linux; s390x

```console
$ docker pull nats@sha256:bb999cd435e52627799ba8d3bba323e34937cebdbf4cbaf4747d8b5d0b4f377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5364ba179bbae6d216c47196a0e607812cf16327562d528b0dd7a39275fc7b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Thu, 22 May 2025 13:55:02 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8c9019ec6e6b470ca5a6c4139cddf8579e979b93b02f0847ea6459c5bdf68`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4` - unknown; unknown

```console
$ docker pull nats@sha256:b5bd7ec7061996df7f9d251b0f55960fc4ea80d15e93923f70faa53a1dfdcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88da26773cc178303a133db9d426aa861f654fb7d59e009907bcc91bd848fb`

```dockerfile
```

-	Layers:
	-	`sha256:a17428cf33c792fdb7174ce215c54081e07fdd09cde209156006d308f5279ebd`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.4-alpine`

```console
$ docker pull nats@sha256:0451ec62031943afa591cf4e5f9404bce65b55a8671ab93a7d581d8028fc12a9
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

### `nats:2.11.4-alpine` - linux; amd64

```console
$ docker pull nats@sha256:78c1052292c8d1bdabeca33c5cde417bb3b56c9a9a6707afd896ac74f8010e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10425424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752c0a111d15eafa05314d85b32bdfc63c7a5190ba26712078e014ad5c12906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc83d3e520670ed878bfe5964638db9895fc2873acb2a25b7bd3a8b2916c3e`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 6.8 MB (6782209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1065a99208ad32f21adf1cc2983a318f6d19b678ce12103514758c5e75a1359`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dc1d69fb3bb313c6fce126295baf9e644c735c5b709cb57462cf134d8b7535`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6425e7c42e8f01aed46c0c5a2c0e1538c4703e432be6a853fe400d6c070c46b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd03d3d4671688731cc2113bd6bce676daf486062cf7bf8a0ad509235b375b3`

```dockerfile
```

-	Layers:
	-	`sha256:8d13d777cfed6af6d839ab64cb7dc1dd2e3b2e7c64170ca5695c3a937b560432`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:e9129c76ec8b39cfb61261ea43a529d2b048a22bd43dde23405476211d952fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa20ad8f845d52ef2ede0cc269b4ade46343bd8ae9d91e0f89a101e164019a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedc41dc7d645196f64f183990aac84922d7dfeca30cdd62cc58afacced1e53e`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 6.5 MB (6500243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f84ca9e26add3645800a5d8875d035548ece025cd495d093506600b5fa3639`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a0bc1a6e6b564bac3444b012da7c2bd95b00fc4b30e2183f58fdfe67a29efc`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cfc622005d6c0083932d3a442389e5ba0fed2eee0d382384117e632be9d2cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98224cc21fc700a931065a4257f0f576cb24d83f9f4cf3a756dbb8cfc211de84`

```dockerfile
```

-	Layers:
	-	`sha256:5b980a9b2e5b75054cfabe65a0bb0ca426c2aeb5cb4d1d0a7b3616d6b089aba1`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f51b3ede38c787e45a1c58fe1758aa726cfc126eed5ef13dc9a66dbcfe4d8e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9587301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fcc07ad9637e3d6023e9c3faf8df41d76537efd7136923fe276ce3124a21f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9afbd37259973c94e964e514f1fd5331fdff7c8a20c358c64209a54939892`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 6.5 MB (6488204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e46bef85887a3ca7141cdb651fb0907947c31453e3dd12d5f2e75d659f9bb81`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ada5b8ea797d2e67d9817b4735e298f9e4328503c9b4faff09c816dd2a3fe`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:43fb4c5979976f655a571482f2fb7c95bdcfe76ea5c3d03822e834dba8c8ba43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103eb0538b45ceeaf49344cd2e475459141bba59c3b68cfa4b3f8c81bfaa0292`

```dockerfile
```

-	Layers:
	-	`sha256:48a6d4944ad8da069b2dcc13b6bf204e8ba6994953e03cdc717459fc9bec1bbc`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:361d07db47a72d53a1159ce806effcfaacddb5c24254dc346aa6ed24d2eaff6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c4a01a93d1901d7daaa7ad147102df5dc250516eb1b935b673cb01b2de9436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28900756089c34ef75f78f9bc43820aee795ebced2ef164f4371a469020c319`  
		Last Modified: Thu, 22 May 2025 20:04:29 GMT  
		Size: 6.3 MB (6271430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a19d69a59c9c3d035125ee920379ce8b337cb0de1eb1646fa3b37bcc5bd4eca`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002df6ee873e4c8b8c2d32bc19571ba115cbaeeaa22dbe5e19ea24a00121560a`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:eeec07d9dba12fff9a629635d9822e295cbd2866800be7c10ae0f0eda767c376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb57113d3b7d11444b789b3d12801ddfaf3eadc8944e2457447d1469cc94db`

```dockerfile
```

-	Layers:
	-	`sha256:cac3279af5a354235660e8ed87c54fddc39e37fe276433cdd00c7a04a3f5877c`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:6c62a05e9d2c74252f7e85ca263ff11fa47ca8d6a2314c95ef35830ca7dd5947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9829497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f82ed4f59bb1fc3f2bb1bf520c03a108a4b1201a308129e9f9c437eb69d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab090fb5974c5fbc532a324c8b6ff89147f7b095e88f59c95200ff29b503d4ed`  
		Last Modified: Thu, 22 May 2025 16:46:06 GMT  
		Size: 6.3 MB (6254178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ffdff7943fa553d5c46cd9bfd7cdb0aaf807fd213df6a3be9c0f47276b45d`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b243223ddfaabf20dea42482c30a57a1960b976113f905a07742d49e8fd76`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:209d5ce0eb3e58f76c4baefc159b91c7c24036c43252c4c06634f4218bfc2ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc856abe1e071c3b5e0dd0ac6a265939b68986e20ed0a612a3577747ed39b949`

```dockerfile
```

-	Layers:
	-	`sha256:9d5d8fc63a7e90cae4235128e35cce1f4b9143f897cba2831823fdf635d1c1a3`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine` - linux; s390x

```console
$ docker pull nats@sha256:113aca5863f11d04e9dcafd0a79496a1ecc86cdc2ccf02b720467c79eb2c1b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10087904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a783e13b44bb39120f57f582d383ada710ad715fc963f625760233ace3e4ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f6217bb5b7f1a95efe567548c35356165dc66ae69bfe675bd4d750bb78b516`  
		Last Modified: Thu, 22 May 2025 17:33:09 GMT  
		Size: 6.6 MB (6619363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9020a2695371d3927fa6fb04d07c6ee8cfdbdf0c94ab360a4d3e121df860ce`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9b02a9ab09a6778612e627ead79927f9eab9b1f58a792a27d86b207e883eb`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2adcfab66a18b065b7c3a97ae3a3a6266b23138c34d08229363bae6d3eb99f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b88a3ff73d885d4df2ea9e8203001daa5832c33dbba49d1127c7ded5b3724`

```dockerfile
```

-	Layers:
	-	`sha256:2e6f543ee243ec43d02935e873e329d235728c7301898d56b1cc48bf41df88aa`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.4-alpine3.21`

```console
$ docker pull nats@sha256:0451ec62031943afa591cf4e5f9404bce65b55a8671ab93a7d581d8028fc12a9
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

### `nats:2.11.4-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:78c1052292c8d1bdabeca33c5cde417bb3b56c9a9a6707afd896ac74f8010e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10425424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752c0a111d15eafa05314d85b32bdfc63c7a5190ba26712078e014ad5c12906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc83d3e520670ed878bfe5964638db9895fc2873acb2a25b7bd3a8b2916c3e`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 6.8 MB (6782209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1065a99208ad32f21adf1cc2983a318f6d19b678ce12103514758c5e75a1359`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dc1d69fb3bb313c6fce126295baf9e644c735c5b709cb57462cf134d8b7535`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6425e7c42e8f01aed46c0c5a2c0e1538c4703e432be6a853fe400d6c070c46b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd03d3d4671688731cc2113bd6bce676daf486062cf7bf8a0ad509235b375b3`

```dockerfile
```

-	Layers:
	-	`sha256:8d13d777cfed6af6d839ab64cb7dc1dd2e3b2e7c64170ca5695c3a937b560432`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:e9129c76ec8b39cfb61261ea43a529d2b048a22bd43dde23405476211d952fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa20ad8f845d52ef2ede0cc269b4ade46343bd8ae9d91e0f89a101e164019a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedc41dc7d645196f64f183990aac84922d7dfeca30cdd62cc58afacced1e53e`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 6.5 MB (6500243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f84ca9e26add3645800a5d8875d035548ece025cd495d093506600b5fa3639`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a0bc1a6e6b564bac3444b012da7c2bd95b00fc4b30e2183f58fdfe67a29efc`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cfc622005d6c0083932d3a442389e5ba0fed2eee0d382384117e632be9d2cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98224cc21fc700a931065a4257f0f576cb24d83f9f4cf3a756dbb8cfc211de84`

```dockerfile
```

-	Layers:
	-	`sha256:5b980a9b2e5b75054cfabe65a0bb0ca426c2aeb5cb4d1d0a7b3616d6b089aba1`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:f51b3ede38c787e45a1c58fe1758aa726cfc126eed5ef13dc9a66dbcfe4d8e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9587301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fcc07ad9637e3d6023e9c3faf8df41d76537efd7136923fe276ce3124a21f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9afbd37259973c94e964e514f1fd5331fdff7c8a20c358c64209a54939892`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 6.5 MB (6488204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e46bef85887a3ca7141cdb651fb0907947c31453e3dd12d5f2e75d659f9bb81`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ada5b8ea797d2e67d9817b4735e298f9e4328503c9b4faff09c816dd2a3fe`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:43fb4c5979976f655a571482f2fb7c95bdcfe76ea5c3d03822e834dba8c8ba43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103eb0538b45ceeaf49344cd2e475459141bba59c3b68cfa4b3f8c81bfaa0292`

```dockerfile
```

-	Layers:
	-	`sha256:48a6d4944ad8da069b2dcc13b6bf204e8ba6994953e03cdc717459fc9bec1bbc`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:361d07db47a72d53a1159ce806effcfaacddb5c24254dc346aa6ed24d2eaff6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c4a01a93d1901d7daaa7ad147102df5dc250516eb1b935b673cb01b2de9436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28900756089c34ef75f78f9bc43820aee795ebced2ef164f4371a469020c319`  
		Last Modified: Thu, 22 May 2025 20:04:29 GMT  
		Size: 6.3 MB (6271430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a19d69a59c9c3d035125ee920379ce8b337cb0de1eb1646fa3b37bcc5bd4eca`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002df6ee873e4c8b8c2d32bc19571ba115cbaeeaa22dbe5e19ea24a00121560a`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:eeec07d9dba12fff9a629635d9822e295cbd2866800be7c10ae0f0eda767c376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb57113d3b7d11444b789b3d12801ddfaf3eadc8944e2457447d1469cc94db`

```dockerfile
```

-	Layers:
	-	`sha256:cac3279af5a354235660e8ed87c54fddc39e37fe276433cdd00c7a04a3f5877c`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:6c62a05e9d2c74252f7e85ca263ff11fa47ca8d6a2314c95ef35830ca7dd5947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9829497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f82ed4f59bb1fc3f2bb1bf520c03a108a4b1201a308129e9f9c437eb69d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab090fb5974c5fbc532a324c8b6ff89147f7b095e88f59c95200ff29b503d4ed`  
		Last Modified: Thu, 22 May 2025 16:46:06 GMT  
		Size: 6.3 MB (6254178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ffdff7943fa553d5c46cd9bfd7cdb0aaf807fd213df6a3be9c0f47276b45d`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b243223ddfaabf20dea42482c30a57a1960b976113f905a07742d49e8fd76`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:209d5ce0eb3e58f76c4baefc159b91c7c24036c43252c4c06634f4218bfc2ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc856abe1e071c3b5e0dd0ac6a265939b68986e20ed0a612a3577747ed39b949`

```dockerfile
```

-	Layers:
	-	`sha256:9d5d8fc63a7e90cae4235128e35cce1f4b9143f897cba2831823fdf635d1c1a3`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:113aca5863f11d04e9dcafd0a79496a1ecc86cdc2ccf02b720467c79eb2c1b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10087904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a783e13b44bb39120f57f582d383ada710ad715fc963f625760233ace3e4ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f6217bb5b7f1a95efe567548c35356165dc66ae69bfe675bd4d750bb78b516`  
		Last Modified: Thu, 22 May 2025 17:33:09 GMT  
		Size: 6.6 MB (6619363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9020a2695371d3927fa6fb04d07c6ee8cfdbdf0c94ab360a4d3e121df860ce`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9b02a9ab09a6778612e627ead79927f9eab9b1f58a792a27d86b207e883eb`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:2adcfab66a18b065b7c3a97ae3a3a6266b23138c34d08229363bae6d3eb99f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b88a3ff73d885d4df2ea9e8203001daa5832c33dbba49d1127c7ded5b3724`

```dockerfile
```

-	Layers:
	-	`sha256:2e6f543ee243ec43d02935e873e329d235728c7301898d56b1cc48bf41df88aa`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.4-linux`

```console
$ docker pull nats@sha256:d0c61f71b425352fd0d54492562dcff4709fdaa5979afbef9a2e13df957fa26e
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

### `nats:2.11.4-linux` - linux; amd64

```console
$ docker pull nats@sha256:3669c7dc73d88251f131a5507f94fe74fef33b461c16666813ac84e7b807bca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2dc40e2ee2ef54306454e58ff7f7b318bd40949cd7d747c67cc26b2daf553`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Thu, 22 May 2025 13:55:01 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Thu, 22 May 2025 16:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-linux` - unknown; unknown

```console
$ docker pull nats@sha256:40c2e8c019de84dd8609363ad056325e160ff7d3c22583776cba7d9c14bbb0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ac87fa640a0df9ed5554a115493a87055629ce3f52f77a933bf54b1c5ee29`

```dockerfile
```

-	Layers:
	-	`sha256:edbca2e0be9710afcbe43e2fca6896927d7e6c12d43816973cc4a1e04ec762f6`  
		Last Modified: Thu, 22 May 2025 16:47:18 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4fbfa5ce075ad78297fbfc8ce0126de19a685b441759d77b6dc6aeb130f38561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279bf33611cd3f2a188a9a0afdb244877743689160627fcf8de576cdda072a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd26e0aad9f1b20096e647e74023489621fc5ba4de7dc4747a0d0d4bb2823fc7`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-linux` - unknown; unknown

```console
$ docker pull nats@sha256:06aa17a9acdaae3c275cb86e786faac7651dd30f6b6aab7b648db0e966524ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34ed5638318182fa373a29edf2eae4badc5e5688dd08e8af559b347675e23c`

```dockerfile
```

-	Layers:
	-	`sha256:ea20c201702d517a06fc320a50a878fa897f58fd5a8cb89d7bbeb5af7599f148`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e1b35decc46dc6b9b6a62e50a10d13095888c34f740a2d2069d5fa4a3a406fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04111c7501581b1636dc5516802ecee6c26dcb627cbbec34e273d2575ac0a9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Thu, 22 May 2025 13:54:58 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9293b5f4677cf2db6d8d8a8a01b039e1134d378f77c7efe3d7b11072a3f4e4`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e1653a1054fd8a003f0dad883474a71c0d46a243bb3364d28c690e1d5c521e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2828a9839d98f985cc7bb11688ead3394a6003466851fff29ab209a775564`

```dockerfile
```

-	Layers:
	-	`sha256:fddb83fedd24e6e2d6c0afc61f16768121ba63342f1bc0d540cd75cf7e202edc`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6390d133be19faae15ea0b0addf722e3dd60c9412dc5b14c8120e9ff773fcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a4332082216fadc8b7d39be0643a4193e18b21e9a0815bc8a7476b0d9ff39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c9a882fa6d5de0d1f1a746c11bb26c98258eba146870604781263ee98916694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8632a81f326876343b421492b672bc64785711cd147bece1386ca476b11fbe2`

```dockerfile
```

-	Layers:
	-	`sha256:a3807445f86645a59e75d2d727c573109c35a356652cf8cea33291752e44a501`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:b2a62d6e7160e9fe02b4fbc54a4d38f4854e955277ad06a32a0f9730fb145030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77959cb575e1e4e6a7ed10889593eb60a12b91bc3daef1a047f20d5b849823e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac6089227b1bf8e0c5485c9fafeb79be71f899610ed5cfe50750ec671c2150`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d61332ce9f2f76ef458a63c4394a0ea8f006176df53c6c854d854c880fb56c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cab1c0c3130120e0299edad95932ca44704b3459f34c83f21aff0efd97ee56`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a85cd3ea43c578ae1c73d84bc6e9c7dbeba30594051365b578136deebce76`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 10.6 KB (10555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-linux` - linux; s390x

```console
$ docker pull nats@sha256:bb999cd435e52627799ba8d3bba323e34937cebdbf4cbaf4747d8b5d0b4f377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5364ba179bbae6d216c47196a0e607812cf16327562d528b0dd7a39275fc7b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Thu, 22 May 2025 13:55:02 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8c9019ec6e6b470ca5a6c4139cddf8579e979b93b02f0847ea6459c5bdf68`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b5bd7ec7061996df7f9d251b0f55960fc4ea80d15e93923f70faa53a1dfdcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88da26773cc178303a133db9d426aa861f654fb7d59e009907bcc91bd848fb`

```dockerfile
```

-	Layers:
	-	`sha256:a17428cf33c792fdb7174ce215c54081e07fdd09cde209156006d308f5279ebd`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.4-nanoserver`

```console
$ docker pull nats@sha256:5cc9d495e86b7caa02ed8c6efd98071810a86094d0365b49cd0d6c923575d630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11.4-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.4-nanoserver-1809`

```console
$ docker pull nats@sha256:5cc9d495e86b7caa02ed8c6efd98071810a86094d0365b49cd0d6c923575d630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11.4-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.4-scratch`

```console
$ docker pull nats@sha256:d0c61f71b425352fd0d54492562dcff4709fdaa5979afbef9a2e13df957fa26e
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

### `nats:2.11.4-scratch` - linux; amd64

```console
$ docker pull nats@sha256:3669c7dc73d88251f131a5507f94fe74fef33b461c16666813ac84e7b807bca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2dc40e2ee2ef54306454e58ff7f7b318bd40949cd7d747c67cc26b2daf553`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Thu, 22 May 2025 13:55:01 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Thu, 22 May 2025 16:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:40c2e8c019de84dd8609363ad056325e160ff7d3c22583776cba7d9c14bbb0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ac87fa640a0df9ed5554a115493a87055629ce3f52f77a933bf54b1c5ee29`

```dockerfile
```

-	Layers:
	-	`sha256:edbca2e0be9710afcbe43e2fca6896927d7e6c12d43816973cc4a1e04ec762f6`  
		Last Modified: Thu, 22 May 2025 16:47:18 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4fbfa5ce075ad78297fbfc8ce0126de19a685b441759d77b6dc6aeb130f38561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279bf33611cd3f2a188a9a0afdb244877743689160627fcf8de576cdda072a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd26e0aad9f1b20096e647e74023489621fc5ba4de7dc4747a0d0d4bb2823fc7`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:06aa17a9acdaae3c275cb86e786faac7651dd30f6b6aab7b648db0e966524ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34ed5638318182fa373a29edf2eae4badc5e5688dd08e8af559b347675e23c`

```dockerfile
```

-	Layers:
	-	`sha256:ea20c201702d517a06fc320a50a878fa897f58fd5a8cb89d7bbeb5af7599f148`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e1b35decc46dc6b9b6a62e50a10d13095888c34f740a2d2069d5fa4a3a406fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04111c7501581b1636dc5516802ecee6c26dcb627cbbec34e273d2575ac0a9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Thu, 22 May 2025 13:54:58 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9293b5f4677cf2db6d8d8a8a01b039e1134d378f77c7efe3d7b11072a3f4e4`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e1653a1054fd8a003f0dad883474a71c0d46a243bb3364d28c690e1d5c521e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2828a9839d98f985cc7bb11688ead3394a6003466851fff29ab209a775564`

```dockerfile
```

-	Layers:
	-	`sha256:fddb83fedd24e6e2d6c0afc61f16768121ba63342f1bc0d540cd75cf7e202edc`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6390d133be19faae15ea0b0addf722e3dd60c9412dc5b14c8120e9ff773fcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a4332082216fadc8b7d39be0643a4193e18b21e9a0815bc8a7476b0d9ff39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c9a882fa6d5de0d1f1a746c11bb26c98258eba146870604781263ee98916694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8632a81f326876343b421492b672bc64785711cd147bece1386ca476b11fbe2`

```dockerfile
```

-	Layers:
	-	`sha256:a3807445f86645a59e75d2d727c573109c35a356652cf8cea33291752e44a501`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:b2a62d6e7160e9fe02b4fbc54a4d38f4854e955277ad06a32a0f9730fb145030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77959cb575e1e4e6a7ed10889593eb60a12b91bc3daef1a047f20d5b849823e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac6089227b1bf8e0c5485c9fafeb79be71f899610ed5cfe50750ec671c2150`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d61332ce9f2f76ef458a63c4394a0ea8f006176df53c6c854d854c880fb56c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cab1c0c3130120e0299edad95932ca44704b3459f34c83f21aff0efd97ee56`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a85cd3ea43c578ae1c73d84bc6e9c7dbeba30594051365b578136deebce76`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 10.6 KB (10555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-scratch` - linux; s390x

```console
$ docker pull nats@sha256:bb999cd435e52627799ba8d3bba323e34937cebdbf4cbaf4747d8b5d0b4f377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5364ba179bbae6d216c47196a0e607812cf16327562d528b0dd7a39275fc7b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Thu, 22 May 2025 13:55:02 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8c9019ec6e6b470ca5a6c4139cddf8579e979b93b02f0847ea6459c5bdf68`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b5bd7ec7061996df7f9d251b0f55960fc4ea80d15e93923f70faa53a1dfdcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88da26773cc178303a133db9d426aa861f654fb7d59e009907bcc91bd848fb`

```dockerfile
```

-	Layers:
	-	`sha256:a17428cf33c792fdb7174ce215c54081e07fdd09cde209156006d308f5279ebd`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.4-windowsservercore`

```console
$ docker pull nats@sha256:5eb29aa350e04efd871dc089f00e2332c6fde8340442987c019d24c4d8612952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11.4-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:3eb16b69114671a8802239d503c0290429cdb314d8a872d6b2e085341c12b4a0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190940335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1f053a6e4022c28324a3e45080faa48d8a7f96dc18ea8250a25af5211529a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 22 May 2025 16:50:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 16:50:25 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Thu, 22 May 2025 16:50:26 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Thu, 22 May 2025 16:51:00 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 May 2025 16:51:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 May 2025 16:51:18 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 16:51:19 GMT
EXPOSE 4222 6222 8222
# Thu, 22 May 2025 16:51:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 16:51:20 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ab467e36de62f69e77619428c80684c172dceff9ed3e77cc0f6ab14e4f32bdfd`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9091f1392b0e4b5a8efd3fa58b0c4a2b6e936430b4e42b68ba16077d4564944d`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf909e97fafaef4ec16a660d02af257e98e54239a7bc6cec966b8e76e70b715`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5d1bc88317b3a5b00e94a85aa69eeff6067de7eacc3b0ae40836597b6b4912`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc3aedb4b361c3a53ea79beee17b5b1e5323e8d429b1c896eb234b053b5198`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1800d06ff1abd05697da24fc89b33bee18003836f4b523b0183785ab5ed2496e`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 357.5 KB (357493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e26a01941a30a2df43651113e13c4254af9daa37d2d460c7eec0e2829bec1`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 6.9 MB (6853143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa50c7d770115bfd2ad8e106b7ba4c236b4240943f9c067a6ea34daf985b973b`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0aea2b23f17071fd4a073f906be4bf64c1c702b06340d09d355bacdc3215a0`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fa330c05a735fa176327db111cb8144a33d927923c98a24221dcfc94ac73cf`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0963e3ada6db5d54c6e1dcfe66033facd31c4474f0a9b67df506cd38b708994a`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.4-windowsservercore-1809`

```console
$ docker pull nats@sha256:5eb29aa350e04efd871dc089f00e2332c6fde8340442987c019d24c4d8612952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11.4-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:3eb16b69114671a8802239d503c0290429cdb314d8a872d6b2e085341c12b4a0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190940335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1f053a6e4022c28324a3e45080faa48d8a7f96dc18ea8250a25af5211529a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 22 May 2025 16:50:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 16:50:25 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Thu, 22 May 2025 16:50:26 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Thu, 22 May 2025 16:51:00 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 May 2025 16:51:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 May 2025 16:51:18 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 16:51:19 GMT
EXPOSE 4222 6222 8222
# Thu, 22 May 2025 16:51:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 16:51:20 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ab467e36de62f69e77619428c80684c172dceff9ed3e77cc0f6ab14e4f32bdfd`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9091f1392b0e4b5a8efd3fa58b0c4a2b6e936430b4e42b68ba16077d4564944d`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf909e97fafaef4ec16a660d02af257e98e54239a7bc6cec966b8e76e70b715`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5d1bc88317b3a5b00e94a85aa69eeff6067de7eacc3b0ae40836597b6b4912`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc3aedb4b361c3a53ea79beee17b5b1e5323e8d429b1c896eb234b053b5198`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1800d06ff1abd05697da24fc89b33bee18003836f4b523b0183785ab5ed2496e`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 357.5 KB (357493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e26a01941a30a2df43651113e13c4254af9daa37d2d460c7eec0e2829bec1`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 6.9 MB (6853143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa50c7d770115bfd2ad8e106b7ba4c236b4240943f9c067a6ea34daf985b973b`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0aea2b23f17071fd4a073f906be4bf64c1c702b06340d09d355bacdc3215a0`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fa330c05a735fa176327db111cb8144a33d927923c98a24221dcfc94ac73cf`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0963e3ada6db5d54c6e1dcfe66033facd31c4474f0a9b67df506cd38b708994a`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:0451ec62031943afa591cf4e5f9404bce65b55a8671ab93a7d581d8028fc12a9
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
$ docker pull nats@sha256:78c1052292c8d1bdabeca33c5cde417bb3b56c9a9a6707afd896ac74f8010e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10425424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752c0a111d15eafa05314d85b32bdfc63c7a5190ba26712078e014ad5c12906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc83d3e520670ed878bfe5964638db9895fc2873acb2a25b7bd3a8b2916c3e`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 6.8 MB (6782209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1065a99208ad32f21adf1cc2983a318f6d19b678ce12103514758c5e75a1359`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dc1d69fb3bb313c6fce126295baf9e644c735c5b709cb57462cf134d8b7535`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6425e7c42e8f01aed46c0c5a2c0e1538c4703e432be6a853fe400d6c070c46b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd03d3d4671688731cc2113bd6bce676daf486062cf7bf8a0ad509235b375b3`

```dockerfile
```

-	Layers:
	-	`sha256:8d13d777cfed6af6d839ab64cb7dc1dd2e3b2e7c64170ca5695c3a937b560432`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:e9129c76ec8b39cfb61261ea43a529d2b048a22bd43dde23405476211d952fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa20ad8f845d52ef2ede0cc269b4ade46343bd8ae9d91e0f89a101e164019a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedc41dc7d645196f64f183990aac84922d7dfeca30cdd62cc58afacced1e53e`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 6.5 MB (6500243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f84ca9e26add3645800a5d8875d035548ece025cd495d093506600b5fa3639`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a0bc1a6e6b564bac3444b012da7c2bd95b00fc4b30e2183f58fdfe67a29efc`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cfc622005d6c0083932d3a442389e5ba0fed2eee0d382384117e632be9d2cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98224cc21fc700a931065a4257f0f576cb24d83f9f4cf3a756dbb8cfc211de84`

```dockerfile
```

-	Layers:
	-	`sha256:5b980a9b2e5b75054cfabe65a0bb0ca426c2aeb5cb4d1d0a7b3616d6b089aba1`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f51b3ede38c787e45a1c58fe1758aa726cfc126eed5ef13dc9a66dbcfe4d8e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9587301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fcc07ad9637e3d6023e9c3faf8df41d76537efd7136923fe276ce3124a21f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9afbd37259973c94e964e514f1fd5331fdff7c8a20c358c64209a54939892`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 6.5 MB (6488204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e46bef85887a3ca7141cdb651fb0907947c31453e3dd12d5f2e75d659f9bb81`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ada5b8ea797d2e67d9817b4735e298f9e4328503c9b4faff09c816dd2a3fe`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:43fb4c5979976f655a571482f2fb7c95bdcfe76ea5c3d03822e834dba8c8ba43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103eb0538b45ceeaf49344cd2e475459141bba59c3b68cfa4b3f8c81bfaa0292`

```dockerfile
```

-	Layers:
	-	`sha256:48a6d4944ad8da069b2dcc13b6bf204e8ba6994953e03cdc717459fc9bec1bbc`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:361d07db47a72d53a1159ce806effcfaacddb5c24254dc346aa6ed24d2eaff6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c4a01a93d1901d7daaa7ad147102df5dc250516eb1b935b673cb01b2de9436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28900756089c34ef75f78f9bc43820aee795ebced2ef164f4371a469020c319`  
		Last Modified: Thu, 22 May 2025 20:04:29 GMT  
		Size: 6.3 MB (6271430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a19d69a59c9c3d035125ee920379ce8b337cb0de1eb1646fa3b37bcc5bd4eca`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002df6ee873e4c8b8c2d32bc19571ba115cbaeeaa22dbe5e19ea24a00121560a`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:eeec07d9dba12fff9a629635d9822e295cbd2866800be7c10ae0f0eda767c376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb57113d3b7d11444b789b3d12801ddfaf3eadc8944e2457447d1469cc94db`

```dockerfile
```

-	Layers:
	-	`sha256:cac3279af5a354235660e8ed87c54fddc39e37fe276433cdd00c7a04a3f5877c`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:6c62a05e9d2c74252f7e85ca263ff11fa47ca8d6a2314c95ef35830ca7dd5947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9829497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f82ed4f59bb1fc3f2bb1bf520c03a108a4b1201a308129e9f9c437eb69d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab090fb5974c5fbc532a324c8b6ff89147f7b095e88f59c95200ff29b503d4ed`  
		Last Modified: Thu, 22 May 2025 16:46:06 GMT  
		Size: 6.3 MB (6254178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ffdff7943fa553d5c46cd9bfd7cdb0aaf807fd213df6a3be9c0f47276b45d`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b243223ddfaabf20dea42482c30a57a1960b976113f905a07742d49e8fd76`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:209d5ce0eb3e58f76c4baefc159b91c7c24036c43252c4c06634f4218bfc2ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc856abe1e071c3b5e0dd0ac6a265939b68986e20ed0a612a3577747ed39b949`

```dockerfile
```

-	Layers:
	-	`sha256:9d5d8fc63a7e90cae4235128e35cce1f4b9143f897cba2831823fdf635d1c1a3`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:113aca5863f11d04e9dcafd0a79496a1ecc86cdc2ccf02b720467c79eb2c1b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10087904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a783e13b44bb39120f57f582d383ada710ad715fc963f625760233ace3e4ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f6217bb5b7f1a95efe567548c35356165dc66ae69bfe675bd4d750bb78b516`  
		Last Modified: Thu, 22 May 2025 17:33:09 GMT  
		Size: 6.6 MB (6619363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9020a2695371d3927fa6fb04d07c6ee8cfdbdf0c94ab360a4d3e121df860ce`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9b02a9ab09a6778612e627ead79927f9eab9b1f58a792a27d86b207e883eb`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2adcfab66a18b065b7c3a97ae3a3a6266b23138c34d08229363bae6d3eb99f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b88a3ff73d885d4df2ea9e8203001daa5832c33dbba49d1127c7ded5b3724`

```dockerfile
```

-	Layers:
	-	`sha256:2e6f543ee243ec43d02935e873e329d235728c7301898d56b1cc48bf41df88aa`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:0451ec62031943afa591cf4e5f9404bce65b55a8671ab93a7d581d8028fc12a9
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

### `nats:alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:78c1052292c8d1bdabeca33c5cde417bb3b56c9a9a6707afd896ac74f8010e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10425424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752c0a111d15eafa05314d85b32bdfc63c7a5190ba26712078e014ad5c12906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc83d3e520670ed878bfe5964638db9895fc2873acb2a25b7bd3a8b2916c3e`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 6.8 MB (6782209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1065a99208ad32f21adf1cc2983a318f6d19b678ce12103514758c5e75a1359`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dc1d69fb3bb313c6fce126295baf9e644c735c5b709cb57462cf134d8b7535`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6425e7c42e8f01aed46c0c5a2c0e1538c4703e432be6a853fe400d6c070c46b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd03d3d4671688731cc2113bd6bce676daf486062cf7bf8a0ad509235b375b3`

```dockerfile
```

-	Layers:
	-	`sha256:8d13d777cfed6af6d839ab64cb7dc1dd2e3b2e7c64170ca5695c3a937b560432`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:e9129c76ec8b39cfb61261ea43a529d2b048a22bd43dde23405476211d952fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa20ad8f845d52ef2ede0cc269b4ade46343bd8ae9d91e0f89a101e164019a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedc41dc7d645196f64f183990aac84922d7dfeca30cdd62cc58afacced1e53e`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 6.5 MB (6500243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f84ca9e26add3645800a5d8875d035548ece025cd495d093506600b5fa3639`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a0bc1a6e6b564bac3444b012da7c2bd95b00fc4b30e2183f58fdfe67a29efc`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cfc622005d6c0083932d3a442389e5ba0fed2eee0d382384117e632be9d2cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98224cc21fc700a931065a4257f0f576cb24d83f9f4cf3a756dbb8cfc211de84`

```dockerfile
```

-	Layers:
	-	`sha256:5b980a9b2e5b75054cfabe65a0bb0ca426c2aeb5cb4d1d0a7b3616d6b089aba1`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:f51b3ede38c787e45a1c58fe1758aa726cfc126eed5ef13dc9a66dbcfe4d8e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9587301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fcc07ad9637e3d6023e9c3faf8df41d76537efd7136923fe276ce3124a21f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9afbd37259973c94e964e514f1fd5331fdff7c8a20c358c64209a54939892`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 6.5 MB (6488204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e46bef85887a3ca7141cdb651fb0907947c31453e3dd12d5f2e75d659f9bb81`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ada5b8ea797d2e67d9817b4735e298f9e4328503c9b4faff09c816dd2a3fe`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:43fb4c5979976f655a571482f2fb7c95bdcfe76ea5c3d03822e834dba8c8ba43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103eb0538b45ceeaf49344cd2e475459141bba59c3b68cfa4b3f8c81bfaa0292`

```dockerfile
```

-	Layers:
	-	`sha256:48a6d4944ad8da069b2dcc13b6bf204e8ba6994953e03cdc717459fc9bec1bbc`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:361d07db47a72d53a1159ce806effcfaacddb5c24254dc346aa6ed24d2eaff6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c4a01a93d1901d7daaa7ad147102df5dc250516eb1b935b673cb01b2de9436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28900756089c34ef75f78f9bc43820aee795ebced2ef164f4371a469020c319`  
		Last Modified: Thu, 22 May 2025 20:04:29 GMT  
		Size: 6.3 MB (6271430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a19d69a59c9c3d035125ee920379ce8b337cb0de1eb1646fa3b37bcc5bd4eca`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002df6ee873e4c8b8c2d32bc19571ba115cbaeeaa22dbe5e19ea24a00121560a`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:eeec07d9dba12fff9a629635d9822e295cbd2866800be7c10ae0f0eda767c376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb57113d3b7d11444b789b3d12801ddfaf3eadc8944e2457447d1469cc94db`

```dockerfile
```

-	Layers:
	-	`sha256:cac3279af5a354235660e8ed87c54fddc39e37fe276433cdd00c7a04a3f5877c`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:6c62a05e9d2c74252f7e85ca263ff11fa47ca8d6a2314c95ef35830ca7dd5947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9829497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f82ed4f59bb1fc3f2bb1bf520c03a108a4b1201a308129e9f9c437eb69d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab090fb5974c5fbc532a324c8b6ff89147f7b095e88f59c95200ff29b503d4ed`  
		Last Modified: Thu, 22 May 2025 16:46:06 GMT  
		Size: 6.3 MB (6254178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ffdff7943fa553d5c46cd9bfd7cdb0aaf807fd213df6a3be9c0f47276b45d`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b243223ddfaabf20dea42482c30a57a1960b976113f905a07742d49e8fd76`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:209d5ce0eb3e58f76c4baefc159b91c7c24036c43252c4c06634f4218bfc2ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc856abe1e071c3b5e0dd0ac6a265939b68986e20ed0a612a3577747ed39b949`

```dockerfile
```

-	Layers:
	-	`sha256:9d5d8fc63a7e90cae4235128e35cce1f4b9143f897cba2831823fdf635d1c1a3`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:113aca5863f11d04e9dcafd0a79496a1ecc86cdc2ccf02b720467c79eb2c1b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10087904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a783e13b44bb39120f57f582d383ada710ad715fc963f625760233ace3e4ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f6217bb5b7f1a95efe567548c35356165dc66ae69bfe675bd4d750bb78b516`  
		Last Modified: Thu, 22 May 2025 17:33:09 GMT  
		Size: 6.6 MB (6619363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9020a2695371d3927fa6fb04d07c6ee8cfdbdf0c94ab360a4d3e121df860ce`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9b02a9ab09a6778612e627ead79927f9eab9b1f58a792a27d86b207e883eb`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:2adcfab66a18b065b7c3a97ae3a3a6266b23138c34d08229363bae6d3eb99f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b88a3ff73d885d4df2ea9e8203001daa5832c33dbba49d1127c7ded5b3724`

```dockerfile
```

-	Layers:
	-	`sha256:2e6f543ee243ec43d02935e873e329d235728c7301898d56b1cc48bf41df88aa`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:7c80eff5349a3ecaffff014f6cdae20a8d2c5f11cab835bcb76a56275e2719e9
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
	-	windows version 10.0.17763.7314; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:3669c7dc73d88251f131a5507f94fe74fef33b461c16666813ac84e7b807bca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2dc40e2ee2ef54306454e58ff7f7b318bd40949cd7d747c67cc26b2daf553`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Thu, 22 May 2025 13:55:01 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Thu, 22 May 2025 16:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:40c2e8c019de84dd8609363ad056325e160ff7d3c22583776cba7d9c14bbb0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ac87fa640a0df9ed5554a115493a87055629ce3f52f77a933bf54b1c5ee29`

```dockerfile
```

-	Layers:
	-	`sha256:edbca2e0be9710afcbe43e2fca6896927d7e6c12d43816973cc4a1e04ec762f6`  
		Last Modified: Thu, 22 May 2025 16:47:18 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:4fbfa5ce075ad78297fbfc8ce0126de19a685b441759d77b6dc6aeb130f38561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279bf33611cd3f2a188a9a0afdb244877743689160627fcf8de576cdda072a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd26e0aad9f1b20096e647e74023489621fc5ba4de7dc4747a0d0d4bb2823fc7`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:06aa17a9acdaae3c275cb86e786faac7651dd30f6b6aab7b648db0e966524ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34ed5638318182fa373a29edf2eae4badc5e5688dd08e8af559b347675e23c`

```dockerfile
```

-	Layers:
	-	`sha256:ea20c201702d517a06fc320a50a878fa897f58fd5a8cb89d7bbeb5af7599f148`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:e1b35decc46dc6b9b6a62e50a10d13095888c34f740a2d2069d5fa4a3a406fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04111c7501581b1636dc5516802ecee6c26dcb627cbbec34e273d2575ac0a9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Thu, 22 May 2025 13:54:58 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9293b5f4677cf2db6d8d8a8a01b039e1134d378f77c7efe3d7b11072a3f4e4`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:e1653a1054fd8a003f0dad883474a71c0d46a243bb3364d28c690e1d5c521e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2828a9839d98f985cc7bb11688ead3394a6003466851fff29ab209a775564`

```dockerfile
```

-	Layers:
	-	`sha256:fddb83fedd24e6e2d6c0afc61f16768121ba63342f1bc0d540cd75cf7e202edc`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6390d133be19faae15ea0b0addf722e3dd60c9412dc5b14c8120e9ff773fcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a4332082216fadc8b7d39be0643a4193e18b21e9a0815bc8a7476b0d9ff39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:c9a882fa6d5de0d1f1a746c11bb26c98258eba146870604781263ee98916694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8632a81f326876343b421492b672bc64785711cd147bece1386ca476b11fbe2`

```dockerfile
```

-	Layers:
	-	`sha256:a3807445f86645a59e75d2d727c573109c35a356652cf8cea33291752e44a501`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:b2a62d6e7160e9fe02b4fbc54a4d38f4854e955277ad06a32a0f9730fb145030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77959cb575e1e4e6a7ed10889593eb60a12b91bc3daef1a047f20d5b849823e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac6089227b1bf8e0c5485c9fafeb79be71f899610ed5cfe50750ec671c2150`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:d61332ce9f2f76ef458a63c4394a0ea8f006176df53c6c854d854c880fb56c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cab1c0c3130120e0299edad95932ca44704b3459f34c83f21aff0efd97ee56`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a85cd3ea43c578ae1c73d84bc6e9c7dbeba30594051365b578136deebce76`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 10.6 KB (10555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:bb999cd435e52627799ba8d3bba323e34937cebdbf4cbaf4747d8b5d0b4f377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5364ba179bbae6d216c47196a0e607812cf16327562d528b0dd7a39275fc7b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Thu, 22 May 2025 13:55:02 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8c9019ec6e6b470ca5a6c4139cddf8579e979b93b02f0847ea6459c5bdf68`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:b5bd7ec7061996df7f9d251b0f55960fc4ea80d15e93923f70faa53a1dfdcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88da26773cc178303a133db9d426aa861f654fb7d59e009907bcc91bd848fb`

```dockerfile
```

-	Layers:
	-	`sha256:a17428cf33c792fdb7174ce215c54081e07fdd09cde209156006d308f5279ebd`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:d0c61f71b425352fd0d54492562dcff4709fdaa5979afbef9a2e13df957fa26e
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
$ docker pull nats@sha256:3669c7dc73d88251f131a5507f94fe74fef33b461c16666813ac84e7b807bca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2dc40e2ee2ef54306454e58ff7f7b318bd40949cd7d747c67cc26b2daf553`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Thu, 22 May 2025 13:55:01 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Thu, 22 May 2025 16:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:40c2e8c019de84dd8609363ad056325e160ff7d3c22583776cba7d9c14bbb0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ac87fa640a0df9ed5554a115493a87055629ce3f52f77a933bf54b1c5ee29`

```dockerfile
```

-	Layers:
	-	`sha256:edbca2e0be9710afcbe43e2fca6896927d7e6c12d43816973cc4a1e04ec762f6`  
		Last Modified: Thu, 22 May 2025 16:47:18 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4fbfa5ce075ad78297fbfc8ce0126de19a685b441759d77b6dc6aeb130f38561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279bf33611cd3f2a188a9a0afdb244877743689160627fcf8de576cdda072a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd26e0aad9f1b20096e647e74023489621fc5ba4de7dc4747a0d0d4bb2823fc7`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:06aa17a9acdaae3c275cb86e786faac7651dd30f6b6aab7b648db0e966524ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34ed5638318182fa373a29edf2eae4badc5e5688dd08e8af559b347675e23c`

```dockerfile
```

-	Layers:
	-	`sha256:ea20c201702d517a06fc320a50a878fa897f58fd5a8cb89d7bbeb5af7599f148`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e1b35decc46dc6b9b6a62e50a10d13095888c34f740a2d2069d5fa4a3a406fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04111c7501581b1636dc5516802ecee6c26dcb627cbbec34e273d2575ac0a9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Thu, 22 May 2025 13:54:58 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9293b5f4677cf2db6d8d8a8a01b039e1134d378f77c7efe3d7b11072a3f4e4`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:e1653a1054fd8a003f0dad883474a71c0d46a243bb3364d28c690e1d5c521e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2828a9839d98f985cc7bb11688ead3394a6003466851fff29ab209a775564`

```dockerfile
```

-	Layers:
	-	`sha256:fddb83fedd24e6e2d6c0afc61f16768121ba63342f1bc0d540cd75cf7e202edc`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6390d133be19faae15ea0b0addf722e3dd60c9412dc5b14c8120e9ff773fcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a4332082216fadc8b7d39be0643a4193e18b21e9a0815bc8a7476b0d9ff39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:c9a882fa6d5de0d1f1a746c11bb26c98258eba146870604781263ee98916694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8632a81f326876343b421492b672bc64785711cd147bece1386ca476b11fbe2`

```dockerfile
```

-	Layers:
	-	`sha256:a3807445f86645a59e75d2d727c573109c35a356652cf8cea33291752e44a501`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:b2a62d6e7160e9fe02b4fbc54a4d38f4854e955277ad06a32a0f9730fb145030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77959cb575e1e4e6a7ed10889593eb60a12b91bc3daef1a047f20d5b849823e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac6089227b1bf8e0c5485c9fafeb79be71f899610ed5cfe50750ec671c2150`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:d61332ce9f2f76ef458a63c4394a0ea8f006176df53c6c854d854c880fb56c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cab1c0c3130120e0299edad95932ca44704b3459f34c83f21aff0efd97ee56`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a85cd3ea43c578ae1c73d84bc6e9c7dbeba30594051365b578136deebce76`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 10.6 KB (10555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:bb999cd435e52627799ba8d3bba323e34937cebdbf4cbaf4747d8b5d0b4f377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5364ba179bbae6d216c47196a0e607812cf16327562d528b0dd7a39275fc7b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Thu, 22 May 2025 13:55:02 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8c9019ec6e6b470ca5a6c4139cddf8579e979b93b02f0847ea6459c5bdf68`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:b5bd7ec7061996df7f9d251b0f55960fc4ea80d15e93923f70faa53a1dfdcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88da26773cc178303a133db9d426aa861f654fb7d59e009907bcc91bd848fb`

```dockerfile
```

-	Layers:
	-	`sha256:a17428cf33c792fdb7174ce215c54081e07fdd09cde209156006d308f5279ebd`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:5cc9d495e86b7caa02ed8c6efd98071810a86094d0365b49cd0d6c923575d630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:5cc9d495e86b7caa02ed8c6efd98071810a86094d0365b49cd0d6c923575d630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:d0c61f71b425352fd0d54492562dcff4709fdaa5979afbef9a2e13df957fa26e
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
$ docker pull nats@sha256:3669c7dc73d88251f131a5507f94fe74fef33b461c16666813ac84e7b807bca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2dc40e2ee2ef54306454e58ff7f7b318bd40949cd7d747c67cc26b2daf553`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Thu, 22 May 2025 13:55:01 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Thu, 22 May 2025 16:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:40c2e8c019de84dd8609363ad056325e160ff7d3c22583776cba7d9c14bbb0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5ac87fa640a0df9ed5554a115493a87055629ce3f52f77a933bf54b1c5ee29`

```dockerfile
```

-	Layers:
	-	`sha256:edbca2e0be9710afcbe43e2fca6896927d7e6c12d43816973cc4a1e04ec762f6`  
		Last Modified: Thu, 22 May 2025 16:47:18 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4fbfa5ce075ad78297fbfc8ce0126de19a685b441759d77b6dc6aeb130f38561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279bf33611cd3f2a188a9a0afdb244877743689160627fcf8de576cdda072a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd26e0aad9f1b20096e647e74023489621fc5ba4de7dc4747a0d0d4bb2823fc7`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:06aa17a9acdaae3c275cb86e786faac7651dd30f6b6aab7b648db0e966524ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b34ed5638318182fa373a29edf2eae4badc5e5688dd08e8af559b347675e23c`

```dockerfile
```

-	Layers:
	-	`sha256:ea20c201702d517a06fc320a50a878fa897f58fd5a8cb89d7bbeb5af7599f148`  
		Last Modified: Thu, 22 May 2025 16:47:01 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e1b35decc46dc6b9b6a62e50a10d13095888c34f740a2d2069d5fa4a3a406fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04111c7501581b1636dc5516802ecee6c26dcb627cbbec34e273d2575ac0a9e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Thu, 22 May 2025 13:54:58 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9293b5f4677cf2db6d8d8a8a01b039e1134d378f77c7efe3d7b11072a3f4e4`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e1653a1054fd8a003f0dad883474a71c0d46a243bb3364d28c690e1d5c521e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2828a9839d98f985cc7bb11688ead3394a6003466851fff29ab209a775564`

```dockerfile
```

-	Layers:
	-	`sha256:fddb83fedd24e6e2d6c0afc61f16768121ba63342f1bc0d540cd75cf7e202edc`  
		Last Modified: Fri, 23 May 2025 12:02:01 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6390d133be19faae15ea0b0addf722e3dd60c9412dc5b14c8120e9ff773fcaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a4332082216fadc8b7d39be0643a4193e18b21e9a0815bc8a7476b0d9ff39`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c9a882fa6d5de0d1f1a746c11bb26c98258eba146870604781263ee98916694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8632a81f326876343b421492b672bc64785711cd147bece1386ca476b11fbe2`

```dockerfile
```

-	Layers:
	-	`sha256:a3807445f86645a59e75d2d727c573109c35a356652cf8cea33291752e44a501`  
		Last Modified: Thu, 22 May 2025 23:11:38 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:b2a62d6e7160e9fe02b4fbc54a4d38f4854e955277ad06a32a0f9730fb145030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77959cb575e1e4e6a7ed10889593eb60a12b91bc3daef1a047f20d5b849823e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Thu, 22 May 2025 13:55:03 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac6089227b1bf8e0c5485c9fafeb79be71f899610ed5cfe50750ec671c2150`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d61332ce9f2f76ef458a63c4394a0ea8f006176df53c6c854d854c880fb56c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cab1c0c3130120e0299edad95932ca44704b3459f34c83f21aff0efd97ee56`

```dockerfile
```

-	Layers:
	-	`sha256:ee7a85cd3ea43c578ae1c73d84bc6e9c7dbeba30594051365b578136deebce76`  
		Last Modified: Thu, 22 May 2025 17:27:42 GMT  
		Size: 10.6 KB (10555 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:bb999cd435e52627799ba8d3bba323e34937cebdbf4cbaf4747d8b5d0b4f377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5364ba179bbae6d216c47196a0e607812cf16327562d528b0dd7a39275fc7b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 22 May 2025 13:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 22 May 2025 13:53:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Thu, 22 May 2025 13:55:02 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8c9019ec6e6b470ca5a6c4139cddf8579e979b93b02f0847ea6459c5bdf68`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b5bd7ec7061996df7f9d251b0f55960fc4ea80d15e93923f70faa53a1dfdcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88da26773cc178303a133db9d426aa861f654fb7d59e009907bcc91bd848fb`

```dockerfile
```

-	Layers:
	-	`sha256:a17428cf33c792fdb7174ce215c54081e07fdd09cde209156006d308f5279ebd`  
		Last Modified: Thu, 22 May 2025 20:38:14 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:5eb29aa350e04efd871dc089f00e2332c6fde8340442987c019d24c4d8612952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:3eb16b69114671a8802239d503c0290429cdb314d8a872d6b2e085341c12b4a0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190940335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1f053a6e4022c28324a3e45080faa48d8a7f96dc18ea8250a25af5211529a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 22 May 2025 16:50:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 16:50:25 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Thu, 22 May 2025 16:50:26 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Thu, 22 May 2025 16:51:00 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 May 2025 16:51:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 May 2025 16:51:18 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 16:51:19 GMT
EXPOSE 4222 6222 8222
# Thu, 22 May 2025 16:51:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 16:51:20 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ab467e36de62f69e77619428c80684c172dceff9ed3e77cc0f6ab14e4f32bdfd`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9091f1392b0e4b5a8efd3fa58b0c4a2b6e936430b4e42b68ba16077d4564944d`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf909e97fafaef4ec16a660d02af257e98e54239a7bc6cec966b8e76e70b715`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5d1bc88317b3a5b00e94a85aa69eeff6067de7eacc3b0ae40836597b6b4912`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc3aedb4b361c3a53ea79beee17b5b1e5323e8d429b1c896eb234b053b5198`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1800d06ff1abd05697da24fc89b33bee18003836f4b523b0183785ab5ed2496e`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 357.5 KB (357493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e26a01941a30a2df43651113e13c4254af9daa37d2d460c7eec0e2829bec1`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 6.9 MB (6853143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa50c7d770115bfd2ad8e106b7ba4c236b4240943f9c067a6ea34daf985b973b`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0aea2b23f17071fd4a073f906be4bf64c1c702b06340d09d355bacdc3215a0`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fa330c05a735fa176327db111cb8144a33d927923c98a24221dcfc94ac73cf`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0963e3ada6db5d54c6e1dcfe66033facd31c4474f0a9b67df506cd38b708994a`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:5eb29aa350e04efd871dc089f00e2332c6fde8340442987c019d24c4d8612952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:3eb16b69114671a8802239d503c0290429cdb314d8a872d6b2e085341c12b4a0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190940335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1f053a6e4022c28324a3e45080faa48d8a7f96dc18ea8250a25af5211529a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Thu, 22 May 2025 16:50:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 16:50:24 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 16:50:25 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Thu, 22 May 2025 16:50:26 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Thu, 22 May 2025 16:51:00 GMT
RUN Set-PSDebug -Trace 2
# Thu, 22 May 2025 16:51:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 22 May 2025 16:51:18 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 16:51:19 GMT
EXPOSE 4222 6222 8222
# Thu, 22 May 2025 16:51:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 16:51:20 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:ab467e36de62f69e77619428c80684c172dceff9ed3e77cc0f6ab14e4f32bdfd`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9091f1392b0e4b5a8efd3fa58b0c4a2b6e936430b4e42b68ba16077d4564944d`  
		Last Modified: Thu, 22 May 2025 16:51:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf909e97fafaef4ec16a660d02af257e98e54239a7bc6cec966b8e76e70b715`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5d1bc88317b3a5b00e94a85aa69eeff6067de7eacc3b0ae40836597b6b4912`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc3aedb4b361c3a53ea79beee17b5b1e5323e8d429b1c896eb234b053b5198`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1800d06ff1abd05697da24fc89b33bee18003836f4b523b0183785ab5ed2496e`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 357.5 KB (357493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e26a01941a30a2df43651113e13c4254af9daa37d2d460c7eec0e2829bec1`  
		Last Modified: Thu, 22 May 2025 16:51:24 GMT  
		Size: 6.9 MB (6853143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa50c7d770115bfd2ad8e106b7ba4c236b4240943f9c067a6ea34daf985b973b`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0aea2b23f17071fd4a073f906be4bf64c1c702b06340d09d355bacdc3215a0`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fa330c05a735fa176327db111cb8144a33d927923c98a24221dcfc94ac73cf`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0963e3ada6db5d54c6e1dcfe66033facd31c4474f0a9b67df506cd38b708994a`  
		Last Modified: Thu, 22 May 2025 16:51:23 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
