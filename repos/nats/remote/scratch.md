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
		Last Modified: Tue, 03 Jun 2025 13:32:26 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f22c21c502f685c7e82d1ada6e38f2a3b0df420874fc5ee976076a2d5f16fd0`  
		Last Modified: Tue, 03 Jun 2025 13:32:33 GMT  
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
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.0 MB (6035363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d90cf5c3bc2e0f7191f549f5e1ca5fa12842998e5ec7c9dfbfc7299ce6e94`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:31:36 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82e3fbfb4811753e007ff35bd931b328fd9f1a8da66fc4ad1f7ebb02bf05dd2`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
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
		Last Modified: Tue, 03 Jun 2025 14:49:29 GMT  
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
		Last Modified: Tue, 03 Jun 2025 18:23:09 GMT  
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
		Last Modified: Tue, 03 Jun 2025 18:18:23 GMT  
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
