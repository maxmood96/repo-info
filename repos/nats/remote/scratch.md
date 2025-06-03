## `nats:scratch`

```console
$ docker pull nats@sha256:c84c11287032a77732ffa96a15addac23c44cc481d36a5c3fec68a7516942e9c
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
$ docker pull nats@sha256:5a4c01a644b44d17b7cdf14cd49079eb14b9d76c3e50a97345764aa94e16b7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6761b0e777f1656a13ecd956c00dcf171bcf4f9c8e72b7d03d7d324b81c13ee0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5cddbb8d6266a65aa48c8bd9de5ecf842f476d2cf76fe49afb41db4c8d1fed7c`  
		Last Modified: Tue, 03 Jun 2025 13:32:26 GMT  
		Size: 6.3 MB (6317727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e6e2aea52b865ca0f4e8726605aa7502c28bdb550f6e56d4749dcbb4b7112fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b470cb36e12dad1b579eb0695f5ef8e3011be338684bde5dc72b71400e172d3`

```dockerfile
```

-	Layers:
	-	`sha256:ebc274ab86a0228adc819ef51ffcd905b807d88dcda2fe983fcbe63f5a6db656`  
		Last Modified: Tue, 03 Jun 2025 20:56:34 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f39257d3dd5e64d3343a3d16b40e9912ab6b9f929fc735d511596ec4704aa948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7425cbbfd2b7defc688e761d4d6f8719f740269ee5c44f5582a13a54c4f802`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
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
$ docker pull nats@sha256:df2ff2ae6263fd7cbe22e8404dc060da52a014680c5ea7ba0f7ce70dba1343d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb050731cd2bbb5e3735cfad2fe0f92bc1fbe30da3160dc6c23f1f9d9d160a5`

```dockerfile
```

-	Layers:
	-	`sha256:82226dcc3c8e02cda238d3a1b1ceae90c3a60e366e3fa30e15db329afc3eed1b`  
		Last Modified: Tue, 03 Jun 2025 20:56:38 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:2f734a41d83c961cefe2d503caabfa12bda12a818af521e350a64348f3372714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8949bc842e33479e0c65ca5b2bcc964a0ea431188763cea4e827217dc986ff29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:19256435976b7157e2b1275cbb60c3207747f51bdb7fb339a257b3be2e49c499`  
		Last Modified: Tue, 03 Jun 2025 20:07:54 GMT  
		Size: 6.0 MB (6025008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3568f71094b6f78ed94e1dd9dc00d752b08ab814a7fdaa1866c93480e58d837`  
		Last Modified: Tue, 03 Jun 2025 18:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d76d4c6dfdeb480c6e85debcc22ee60c770911a0f2cfb049f053d42932bc3890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756b6575e916df10fa0a9cb303e61849957e6b1b8acd6cab9189994666cde907`

```dockerfile
```

-	Layers:
	-	`sha256:ce6e6b5979aaffb174240f878e77114f723e2909f249d79aef9d7687d65ebfab`  
		Last Modified: Tue, 03 Jun 2025 20:56:41 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:27ad94aecdfe9893619b73d467480974607c5e8a3c627e42b25f69ec808e3e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c358ff9d437dd513fabb5d6f5bc49da7a9c4f96f5f6ffe76c61f515397b8866`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24c53d616c82bde7f96dcb78eb89ee9efca180493e68fb6f1179ae5d798f3540`  
		Last Modified: Tue, 03 Jun 2025 13:31:36 GMT  
		Size: 5.8 MB (5809599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f765892e1f10e18cf789b8069601203dfb151fde60bf77da9ca4358cb8d75914`  
		Last Modified: Tue, 03 Jun 2025 18:23:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:3ab58e4d1860db54121514d639efedf390a066c26d33d98ea5f4e1b95a2061e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2344925e7a004012cf9579f2444d84cf8baa7a67be26b89241e300eaf09840ce`

```dockerfile
```

-	Layers:
	-	`sha256:f8dd4d8bd22598379fa42d263f5c636b99cf68d9d0ed03767bfeee16d8bf1b81`  
		Last Modified: Tue, 03 Jun 2025 20:56:45 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:0d81e452139ab144f511b38999109476a34d918704cfdbc68273a82d8196baa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ed58af84c3144cc2f9b930310c002266cfe787641b52e751d720e4847af4af`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57be46b4ea67fc4a82253207a77c64e54d879210f7238768704d05fa2cbde0d0`  
		Last Modified: Tue, 03 Jun 2025 18:23:09 GMT  
		Size: 5.8 MB (5791123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19074d91deea2b005d397f5f9f1befb7bd85f26b0ad01585ccfdd7f37325b4dd`  
		Last Modified: Tue, 03 Jun 2025 18:15:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e213dae133d3af46342b22d3e6e58fbfcbb2b8465e42ccec58ab95f41795088d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7e6dda19bfa7741bebdb11e63b1176fa8e8d02934e2eecb60afee1049b4677`

```dockerfile
```

-	Layers:
	-	`sha256:af64346c4dd1c505a06c132a2bd813990f6a1cc86d685405b638988cc3b91f10`  
		Last Modified: Tue, 03 Jun 2025 20:56:48 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:16e076eb01d8f140eeff0291074a0687f70c9c507b3c28792896b133c6d36a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6156666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f2e28eab09665dd9e986c17dc60226b0a67f71725474c09e1bf88e1e8ebbd1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c45330677ca92d779a584c8b60cd7fed6fbea73ad55c596f77c23ebb08986cc2`  
		Last Modified: Tue, 03 Jun 2025 18:18:23 GMT  
		Size: 6.2 MB (6156156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dfbf79b8a3293f73cd47460099ae825d911c2d44e4f97ac2ea4c712771373c`  
		Last Modified: Tue, 03 Jun 2025 18:18:29 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4ee83a4eeaafbb94e83ecf1c824160a672c5191401043796840f0befd3f17a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44e159273c49e67a5e3311f84671845eb2966b422a7760a8a30ff1b2aaec0ff`

```dockerfile
```

-	Layers:
	-	`sha256:f6d542382b4f4c94f9818ac9cb11509c72c5721a019de770c4fb9880a4775788`  
		Last Modified: Tue, 03 Jun 2025 20:56:52 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json
