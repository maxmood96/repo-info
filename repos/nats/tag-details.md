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
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.22`](#nats210-alpine322)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-ltsc2022`](#nats210-nanoserver-ltsc2022)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-ltsc2022`](#nats210-windowsservercore-ltsc2022)
-	[`nats:2.10.29`](#nats21029)
-	[`nats:2.10.29-alpine`](#nats21029-alpine)
-	[`nats:2.10.29-alpine3.22`](#nats21029-alpine322)
-	[`nats:2.10.29-linux`](#nats21029-linux)
-	[`nats:2.10.29-nanoserver`](#nats21029-nanoserver)
-	[`nats:2.10.29-nanoserver-ltsc2022`](#nats21029-nanoserver-ltsc2022)
-	[`nats:2.10.29-scratch`](#nats21029-scratch)
-	[`nats:2.10.29-windowsservercore`](#nats21029-windowsservercore)
-	[`nats:2.10.29-windowsservercore-ltsc2022`](#nats21029-windowsservercore-ltsc2022)
-	[`nats:2.11`](#nats211)
-	[`nats:2.11-alpine`](#nats211-alpine)
-	[`nats:2.11-alpine3.22`](#nats211-alpine322)
-	[`nats:2.11-linux`](#nats211-linux)
-	[`nats:2.11-nanoserver`](#nats211-nanoserver)
-	[`nats:2.11-nanoserver-ltsc2022`](#nats211-nanoserver-ltsc2022)
-	[`nats:2.11-scratch`](#nats211-scratch)
-	[`nats:2.11-windowsservercore`](#nats211-windowsservercore)
-	[`nats:2.11-windowsservercore-ltsc2022`](#nats211-windowsservercore-ltsc2022)
-	[`nats:2.11.4`](#nats2114)
-	[`nats:2.11.4-alpine`](#nats2114-alpine)
-	[`nats:2.11.4-alpine3.22`](#nats2114-alpine322)
-	[`nats:2.11.4-linux`](#nats2114-linux)
-	[`nats:2.11.4-nanoserver`](#nats2114-nanoserver)
-	[`nats:2.11.4-nanoserver-ltsc2022`](#nats2114-nanoserver-ltsc2022)
-	[`nats:2.11.4-scratch`](#nats2114-scratch)
-	[`nats:2.11.4-windowsservercore`](#nats2114-windowsservercore)
-	[`nats:2.11.4-windowsservercore-ltsc2022`](#nats2114-windowsservercore-ltsc2022)
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
$ docker pull nats@sha256:57f45fba83001bfff519e918035305f02eb897a172f82d43933136e0f6aceb1e
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
	-	windows version 10.0.20348.3692; amd64

### `nats:2` - linux; amd64

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

### `nats:2` - unknown; unknown

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

### `nats:2` - linux; arm variant v6

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

### `nats:2` - unknown; unknown

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

### `nats:2` - linux; arm variant v7

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

### `nats:2` - unknown; unknown

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

### `nats:2` - linux; arm64 variant v8

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

### `nats:2` - unknown; unknown

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

### `nats:2` - linux; ppc64le

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

### `nats:2` - unknown; unknown

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

### `nats:2` - linux; s390x

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

### `nats:2` - unknown; unknown

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

### `nats:2` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:5809c0213e200dfdbe56a1d284162f75ce89533ee1eca342e2350fb4b8b384b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129076843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6294ddd46c444e866b505f0226f57df6864ce6cda1545be49e239c008bd011c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f7eba05352cc5df78a901d41dcb3733c4206eb7fd4625541f65326a30e8f`  
		Last Modified: Tue, 03 Jun 2025 18:16:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cf94e1df89f22d940ee5d9efd850e11abeb664ffa179e56c6b22e0dd772fb`  
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.5 MB (6494401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04a0b03d8f9056c543ef2f229fc65a83adff4f5d79e08cc2f95db65cc5da`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91fc443933d1e179f3b885096b15f1d6ac4b086b379a38766604c4ae3fc9bf`  
		Last Modified: Tue, 03 Jun 2025 18:17:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b6a66cc622766c3a994ba752f2a0b9973d6df193bb223dbb101c089689d8d`  
		Last Modified: Tue, 03 Jun 2025 20:57:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68e17b27bdb59114784659909c5bbec158528e884a87fa70e3357643d785c8`  
		Last Modified: Tue, 03 Jun 2025 18:17:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:b8d6a01568a7837d5186f948a3ebfae1bdf5a602268273b50704655982596b22
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
$ docker pull nats@sha256:69435fcc1356278c35dde2a3b3d9f2c4504f57b921d38612d36200a9c7b51067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10580056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e96d11240320c8d079058907e6b1a349c3c164f6d1057c7d4141b67803ef0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be8340a33b28b7069d77e81278e1150e46e62e5739a5ef524f3b10b6315d93`  
		Last Modified: Tue, 03 Jun 2025 18:08:18 GMT  
		Size: 6.8 MB (6782240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:770fc5b17c3e852bea98835c4f770de25350891225d2d5c48a17079cd2a87f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ece4f13433515ab3468766d0750908f38501255daea31da2aab9466abd8dd13`

```dockerfile
```

-	Layers:
	-	`sha256:993a3e77289857e49dcc0d82e8b0a4d01bf97fc1ac52f27adc1b6d9f46be3010`  
		Last Modified: Tue, 03 Jun 2025 20:56:48 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:cc02d2d98d5248ae02ac731a42436bcf7c257a2336cb6ccc18c0a0d33aca7425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10002162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7ffccb3eb9188263f6e9ee5ff6be0d88a00817e7d4a7a880ef153ff6b59861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3cdfa139575e7698957b4ff36ff5e3b9c98dcca74e89a001ef2062de4433d8`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 6.5 MB (6500264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3195bedba82c8298239740a21ea08ee0b417d4c68b4eb96b52ad6c083c2c920`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f93998e0b8d5c431d6f762091f25cb87996747747bf0554bc73c73a2f31e190`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cd850c5ec391a375d438c70b5cc24af732269f5631ab424afdb6f809d708e432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1f72e1e723af723f70095a15f2853df338bcc41fbb18fb2f275a71cf0c8c37`

```dockerfile
```

-	Layers:
	-	`sha256:c0a8dba6556e09db91573b8694623b3159599ceb566967dd357bf582cfdc908c`  
		Last Modified: Tue, 03 Jun 2025 20:56:52 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bd62d7bcee4a2e2d4e3fe84830bbd978a3027b81e7976b723cfce5c113824abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9708379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efdf790e38279933f555c5ef6b82e2fb30e6d8eb6e85274bb375c1c88aced7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c4277d4cc00a376afb142f8ea748e710d48f75eddcf7a2510c5a1e088857e2`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 6.5 MB (6488230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e94ae1fb6404d5eb4989cef0cc09a96573006b7bd7d4e7f7fbab996b9ce90c`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f107f5a32f8d0ab9f4a4a7746509690c6c4845a952c7df17aa5b2e4bc6e7a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:3191c0cbc6ea566ab41e82bdcfd3a1bcfe0757dc82b606a411fdb61d50858d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d3fb67fa07d336d64e774f94f1074d759291d6e8b14b2b24d0c144e3a1ea07`

```dockerfile
```

-	Layers:
	-	`sha256:52a7538138245df9dcdc747a5c3e46f172218df3092764925fdbc21fb2a58298`  
		Last Modified: Tue, 03 Jun 2025 20:56:55 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5dd5eb415f3c3b50eb6e637d9eab8c4ec5726e575550f46a0853226a8da6edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ae7761a85b9922c5be272284ee27fe32bfd3b1a78d3239e429792033c7ced6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6826d2797f1cf0f48d78d168877a33ef918811eaa7ee6146a8653f4218cf6e56`  
		Last Modified: Tue, 03 Jun 2025 18:23:10 GMT  
		Size: 6.3 MB (6271484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2ec423b14754303830aaf58d608bc667aab81252f2b170550982a6c4aee78`  
		Last Modified: Tue, 03 Jun 2025 18:12:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac99aa05c0616d567688e33499eacc91da2b7c79dd4b91fdc6bc363573dccd4`  
		Last Modified: Tue, 03 Jun 2025 18:12:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f57f8e16b74edcba83577e18c83f6c830b2de03df54acd64a65d88ab4b5f5ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6f8fff81a6020fdbd737e9dd518b019a3b205e35d387235d0339aec5b55092`

```dockerfile
```

-	Layers:
	-	`sha256:c61cb3463dab986b2ecb7f263eea6eff56bfdb0d4075df19122df210a8d0a062`  
		Last Modified: Tue, 03 Jun 2025 20:56:59 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:04f768ca98d273ca56dc14213654250fb52045b383bce5db0e58444c23697d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ee2cb1b02b4eeb2714421cdd6b2e9f5ba023f8e508c2b604861f33248ccfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66500e2c223c5a3f4777f4d7f4ffcec1ca21a34f687704db2a6d0e661fe0299`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 6.3 MB (6254211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198db56aeb51065eb35574df93180297f06ba8d180108a952be65d93fa4e7dd2`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df632b2ea33fceba251c68a32d3efed10d3b495018d7e16d1b256225dd38aef8`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a11e45d5ebc10e2f442f0730348545d2ec0f0645f0f047a39364c6073754d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872e45d8950ac438f1cc639d1fde3610446df42c33be57d2ce16b2eef0e02297`

```dockerfile
```

-	Layers:
	-	`sha256:b2fdd3426bf4664ed50234140c9c5e23667db50fb3545c6a3874643740ef5aaf`  
		Last Modified: Tue, 03 Jun 2025 20:57:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:081db236c5c2d779dcea7087bfea30c8252499477626f616458bb70b78054bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9772610e623e3eae3e2949e0e470f0755004398628ced20be8fe593671829030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c44dcd57da31d89c4bf6d887262bfc6e7136e1132734822ddb4586096692a0`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 6.6 MB (6619415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93bad89a83837b6afc8b1128b9f0d132c74ba14e1c7f52f407fbe775cb13a2`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ded513c6eb3a5fff1e0ab2d6ac1560515bbf0389375e4759c71a1b2c0b6e97`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b96db90bf17f90a65aaa3a6fa7ea4250df1f9ee0d9d13d52b7d3c8f926242340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e98ba8254d35c0c12076fa3f077b261896b884cb797b2b50e57f1f79bdaa45`

```dockerfile
```

-	Layers:
	-	`sha256:68ad3f417d73aacb9e3e3a8a3fbde0712715fd19f474e71d7f05c3507eeb168b`  
		Last Modified: Tue, 03 Jun 2025 20:57:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:b8d6a01568a7837d5186f948a3ebfae1bdf5a602268273b50704655982596b22
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
$ docker pull nats@sha256:69435fcc1356278c35dde2a3b3d9f2c4504f57b921d38612d36200a9c7b51067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10580056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e96d11240320c8d079058907e6b1a349c3c164f6d1057c7d4141b67803ef0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be8340a33b28b7069d77e81278e1150e46e62e5739a5ef524f3b10b6315d93`  
		Last Modified: Tue, 03 Jun 2025 18:08:18 GMT  
		Size: 6.8 MB (6782240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:770fc5b17c3e852bea98835c4f770de25350891225d2d5c48a17079cd2a87f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ece4f13433515ab3468766d0750908f38501255daea31da2aab9466abd8dd13`

```dockerfile
```

-	Layers:
	-	`sha256:993a3e77289857e49dcc0d82e8b0a4d01bf97fc1ac52f27adc1b6d9f46be3010`  
		Last Modified: Tue, 03 Jun 2025 20:56:48 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:cc02d2d98d5248ae02ac731a42436bcf7c257a2336cb6ccc18c0a0d33aca7425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10002162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7ffccb3eb9188263f6e9ee5ff6be0d88a00817e7d4a7a880ef153ff6b59861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3cdfa139575e7698957b4ff36ff5e3b9c98dcca74e89a001ef2062de4433d8`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 6.5 MB (6500264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3195bedba82c8298239740a21ea08ee0b417d4c68b4eb96b52ad6c083c2c920`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f93998e0b8d5c431d6f762091f25cb87996747747bf0554bc73c73a2f31e190`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cd850c5ec391a375d438c70b5cc24af732269f5631ab424afdb6f809d708e432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1f72e1e723af723f70095a15f2853df338bcc41fbb18fb2f275a71cf0c8c37`

```dockerfile
```

-	Layers:
	-	`sha256:c0a8dba6556e09db91573b8694623b3159599ceb566967dd357bf582cfdc908c`  
		Last Modified: Tue, 03 Jun 2025 20:56:52 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bd62d7bcee4a2e2d4e3fe84830bbd978a3027b81e7976b723cfce5c113824abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9708379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efdf790e38279933f555c5ef6b82e2fb30e6d8eb6e85274bb375c1c88aced7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c4277d4cc00a376afb142f8ea748e710d48f75eddcf7a2510c5a1e088857e2`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 6.5 MB (6488230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e94ae1fb6404d5eb4989cef0cc09a96573006b7bd7d4e7f7fbab996b9ce90c`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f107f5a32f8d0ab9f4a4a7746509690c6c4845a952c7df17aa5b2e4bc6e7a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:3191c0cbc6ea566ab41e82bdcfd3a1bcfe0757dc82b606a411fdb61d50858d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d3fb67fa07d336d64e774f94f1074d759291d6e8b14b2b24d0c144e3a1ea07`

```dockerfile
```

-	Layers:
	-	`sha256:52a7538138245df9dcdc747a5c3e46f172218df3092764925fdbc21fb2a58298`  
		Last Modified: Tue, 03 Jun 2025 20:56:55 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5dd5eb415f3c3b50eb6e637d9eab8c4ec5726e575550f46a0853226a8da6edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ae7761a85b9922c5be272284ee27fe32bfd3b1a78d3239e429792033c7ced6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6826d2797f1cf0f48d78d168877a33ef918811eaa7ee6146a8653f4218cf6e56`  
		Last Modified: Tue, 03 Jun 2025 18:23:10 GMT  
		Size: 6.3 MB (6271484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2ec423b14754303830aaf58d608bc667aab81252f2b170550982a6c4aee78`  
		Last Modified: Tue, 03 Jun 2025 18:12:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac99aa05c0616d567688e33499eacc91da2b7c79dd4b91fdc6bc363573dccd4`  
		Last Modified: Tue, 03 Jun 2025 18:12:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f57f8e16b74edcba83577e18c83f6c830b2de03df54acd64a65d88ab4b5f5ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6f8fff81a6020fdbd737e9dd518b019a3b205e35d387235d0339aec5b55092`

```dockerfile
```

-	Layers:
	-	`sha256:c61cb3463dab986b2ecb7f263eea6eff56bfdb0d4075df19122df210a8d0a062`  
		Last Modified: Tue, 03 Jun 2025 20:56:59 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:04f768ca98d273ca56dc14213654250fb52045b383bce5db0e58444c23697d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ee2cb1b02b4eeb2714421cdd6b2e9f5ba023f8e508c2b604861f33248ccfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66500e2c223c5a3f4777f4d7f4ffcec1ca21a34f687704db2a6d0e661fe0299`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 6.3 MB (6254211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198db56aeb51065eb35574df93180297f06ba8d180108a952be65d93fa4e7dd2`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df632b2ea33fceba251c68a32d3efed10d3b495018d7e16d1b256225dd38aef8`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a11e45d5ebc10e2f442f0730348545d2ec0f0645f0f047a39364c6073754d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872e45d8950ac438f1cc639d1fde3610446df42c33be57d2ce16b2eef0e02297`

```dockerfile
```

-	Layers:
	-	`sha256:b2fdd3426bf4664ed50234140c9c5e23667db50fb3545c6a3874643740ef5aaf`  
		Last Modified: Tue, 03 Jun 2025 20:57:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:081db236c5c2d779dcea7087bfea30c8252499477626f616458bb70b78054bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9772610e623e3eae3e2949e0e470f0755004398628ced20be8fe593671829030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c44dcd57da31d89c4bf6d887262bfc6e7136e1132734822ddb4586096692a0`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 6.6 MB (6619415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93bad89a83837b6afc8b1128b9f0d132c74ba14e1c7f52f407fbe775cb13a2`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ded513c6eb3a5fff1e0ab2d6ac1560515bbf0389375e4759c71a1b2c0b6e97`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b96db90bf17f90a65aaa3a6fa7ea4250df1f9ee0d9d13d52b7d3c8f926242340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e98ba8254d35c0c12076fa3f077b261896b884cb797b2b50e57f1f79bdaa45`

```dockerfile
```

-	Layers:
	-	`sha256:68ad3f417d73aacb9e3e3a8a3fbde0712715fd19f474e71d7f05c3507eeb168b`  
		Last Modified: Tue, 03 Jun 2025 20:57:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

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

### `nats:2-linux` - linux; amd64

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

### `nats:2-linux` - unknown; unknown

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

### `nats:2-linux` - linux; arm variant v6

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

### `nats:2-linux` - unknown; unknown

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

### `nats:2-linux` - linux; arm variant v7

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

### `nats:2-linux` - unknown; unknown

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

### `nats:2-linux` - linux; arm64 variant v8

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

### `nats:2-linux` - unknown; unknown

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

### `nats:2-linux` - linux; ppc64le

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

### `nats:2-linux` - unknown; unknown

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

### `nats:2-linux` - linux; s390x

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

### `nats:2-linux` - unknown; unknown

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

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:ecc8389817ef21fb2d273b7fe6776b4de22f5f3da3033b00a69151c47e0215a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:5809c0213e200dfdbe56a1d284162f75ce89533ee1eca342e2350fb4b8b384b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129076843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6294ddd46c444e866b505f0226f57df6864ce6cda1545be49e239c008bd011c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f7eba05352cc5df78a901d41dcb3733c4206eb7fd4625541f65326a30e8f`  
		Last Modified: Tue, 03 Jun 2025 18:16:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cf94e1df89f22d940ee5d9efd850e11abeb664ffa179e56c6b22e0dd772fb`  
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.5 MB (6494401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04a0b03d8f9056c543ef2f229fc65a83adff4f5d79e08cc2f95db65cc5da`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91fc443933d1e179f3b885096b15f1d6ac4b086b379a38766604c4ae3fc9bf`  
		Last Modified: Tue, 03 Jun 2025 18:17:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b6a66cc622766c3a994ba752f2a0b9973d6df193bb223dbb101c089689d8d`  
		Last Modified: Tue, 03 Jun 2025 20:57:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68e17b27bdb59114784659909c5bbec158528e884a87fa70e3357643d785c8`  
		Last Modified: Tue, 03 Jun 2025 18:17:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:ecc8389817ef21fb2d273b7fe6776b4de22f5f3da3033b00a69151c47e0215a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:5809c0213e200dfdbe56a1d284162f75ce89533ee1eca342e2350fb4b8b384b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129076843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6294ddd46c444e866b505f0226f57df6864ce6cda1545be49e239c008bd011c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f7eba05352cc5df78a901d41dcb3733c4206eb7fd4625541f65326a30e8f`  
		Last Modified: Tue, 03 Jun 2025 18:16:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cf94e1df89f22d940ee5d9efd850e11abeb664ffa179e56c6b22e0dd772fb`  
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.5 MB (6494401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04a0b03d8f9056c543ef2f229fc65a83adff4f5d79e08cc2f95db65cc5da`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91fc443933d1e179f3b885096b15f1d6ac4b086b379a38766604c4ae3fc9bf`  
		Last Modified: Tue, 03 Jun 2025 18:17:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b6a66cc622766c3a994ba752f2a0b9973d6df193bb223dbb101c089689d8d`  
		Last Modified: Tue, 03 Jun 2025 20:57:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68e17b27bdb59114784659909c5bbec158528e884a87fa70e3357643d785c8`  
		Last Modified: Tue, 03 Jun 2025 18:17:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

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

### `nats:2-scratch` - linux; amd64

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

### `nats:2-scratch` - unknown; unknown

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

### `nats:2-scratch` - linux; arm variant v6

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

### `nats:2-scratch` - unknown; unknown

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

### `nats:2-scratch` - linux; arm variant v7

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

### `nats:2-scratch` - unknown; unknown

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

### `nats:2-scratch` - linux; arm64 variant v8

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

### `nats:2-scratch` - unknown; unknown

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

### `nats:2-scratch` - linux; ppc64le

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

### `nats:2-scratch` - unknown; unknown

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

### `nats:2-scratch` - linux; s390x

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

### `nats:2-scratch` - unknown; unknown

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

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:6f8e77e1231fd3511353f2a8161af5ba6d11565d0d1ece50953a2f9a372d6bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:8317c827fa967bd9f550b8ce662f920ed01c012ca005f14021df3bf5118e4938
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280787628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9160d38e59cf418ea3321c716c7a5c123f40250e646f9a19e44a3d00825101c4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 17:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 17:56:57 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER=2.11.4
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Tue, 03 Jun 2025 17:56:59 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Tue, 03 Jun 2025 17:58:07 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Jun 2025 17:58:34 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 03 Jun 2025 17:58:34 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 17:58:35 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 17:58:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 17:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4b5081f22f0ce90ffb8a283bf6907184ca210d3fa64cc649c175c2403bf48`  
		Last Modified: Tue, 03 Jun 2025 17:59:03 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd1a53f2b89b85d5c147edcb69400d431d2aae95f09eb51615e21d71868b20`  
		Last Modified: Tue, 03 Jun 2025 17:59:04 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05e4d6ed3ee536d39ce8a0564d98ec9fb2830b9aea712e135ef717a9034b58d`  
		Last Modified: Tue, 03 Jun 2025 17:59:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd5804ef666b2af87854e3e84e8513832d69895027327d5563934968d65bfc`  
		Last Modified: Tue, 03 Jun 2025 17:59:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfe49f5d913195c31fdfeae7a261be6ef51da43fb44d9fca4e428ba78fa6064`  
		Last Modified: Tue, 03 Jun 2025 17:59:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af20b8c738d9d92e83bc0e0e5c9b813668bb6deca62e90327f3bff9bac141d0`  
		Last Modified: Tue, 03 Jun 2025 17:59:09 GMT  
		Size: 342.9 KB (342923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9dd708b6fd0131af1f9ae1c1001cf8966b8f9b27bcdd0d022586b3a8489327`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 6.8 MB (6804324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423519a4e3a5a29f15c70595333fab0a6f79736ff478e5e3d66fb7481741151f`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe4b134972dcd390001fc9744ccffb8da5627e4fa055f6fe84918e65df4782d`  
		Last Modified: Tue, 03 Jun 2025 17:59:12 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb328b3dfd00b76b936d43d8a04426cb93cab24be8d294245da02c20ea2df6`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f933a18bfe02980983b3a438f0f485afe7c6592e98c09eb78891959f057c3a55`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:6f8e77e1231fd3511353f2a8161af5ba6d11565d0d1ece50953a2f9a372d6bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:8317c827fa967bd9f550b8ce662f920ed01c012ca005f14021df3bf5118e4938
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280787628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9160d38e59cf418ea3321c716c7a5c123f40250e646f9a19e44a3d00825101c4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 17:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 17:56:57 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER=2.11.4
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Tue, 03 Jun 2025 17:56:59 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Tue, 03 Jun 2025 17:58:07 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Jun 2025 17:58:34 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 03 Jun 2025 17:58:34 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 17:58:35 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 17:58:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 17:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4b5081f22f0ce90ffb8a283bf6907184ca210d3fa64cc649c175c2403bf48`  
		Last Modified: Tue, 03 Jun 2025 17:59:03 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd1a53f2b89b85d5c147edcb69400d431d2aae95f09eb51615e21d71868b20`  
		Last Modified: Tue, 03 Jun 2025 17:59:04 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05e4d6ed3ee536d39ce8a0564d98ec9fb2830b9aea712e135ef717a9034b58d`  
		Last Modified: Tue, 03 Jun 2025 17:59:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd5804ef666b2af87854e3e84e8513832d69895027327d5563934968d65bfc`  
		Last Modified: Tue, 03 Jun 2025 17:59:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfe49f5d913195c31fdfeae7a261be6ef51da43fb44d9fca4e428ba78fa6064`  
		Last Modified: Tue, 03 Jun 2025 17:59:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af20b8c738d9d92e83bc0e0e5c9b813668bb6deca62e90327f3bff9bac141d0`  
		Last Modified: Tue, 03 Jun 2025 17:59:09 GMT  
		Size: 342.9 KB (342923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9dd708b6fd0131af1f9ae1c1001cf8966b8f9b27bcdd0d022586b3a8489327`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 6.8 MB (6804324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423519a4e3a5a29f15c70595333fab0a6f79736ff478e5e3d66fb7481741151f`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe4b134972dcd390001fc9744ccffb8da5627e4fa055f6fe84918e65df4782d`  
		Last Modified: Tue, 03 Jun 2025 17:59:12 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb328b3dfd00b76b936d43d8a04426cb93cab24be8d294245da02c20ea2df6`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f933a18bfe02980983b3a438f0f485afe7c6592e98c09eb78891959f057c3a55`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:318f390cf15f0d300f422e4ba7b8ac7fe2bcedb0286ee48810766b07a64d88f3
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
	-	windows version 10.0.20348.3692; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:f030f79672be88d009b75f61c2cb5fe9d07ad3364742a9b27cd60c9338ffafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4962b82a0ae69663e5a74740285899ca5957c69f6c53bf82311476aa1fae5ef8`
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
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:5edca7674c56d6da9be7a373f78942e4c4aa5f175636ee35ccffba1533772e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3176d2028656537e4bfe7efebe9f8fcc985778a684370b2eff8c909b50c6f3`

```dockerfile
```

-	Layers:
	-	`sha256:5f2aca3d9450c14453dcb34e8c6b2a5a9a11673e6f7baeb3c28b7b435f2789d0`  
		Last Modified: Tue, 03 Jun 2025 20:57:19 GMT  
		Size: 8.7 KB (8710 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a72209661fa798f94ca59fe982425636af6df596e83cc2bdb1b1ebde04a57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f5ba25ee4d10359cc31039d1a9a05f150b96f797eb6ca7d155076fd547bb9`
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
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb3048cc57f790e44bb317519f7d61ce9e2d2cdcd7a57ac04cdf293bdd74a`  
		Last Modified: Tue, 03 Jun 2025 18:08:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:9c3d54e7088aa0eb163c2eeb032e0d168126cdf0af77576fdc60ea726a70e690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8e6de48fcf449ba2519083b4bc5415c135d29db13e6c6b49b06eb5c5b766a1`

```dockerfile
```

-	Layers:
	-	`sha256:224e3a5982d8875c00e7bc85a73e0963da1394057839ae2fc9902d645dfd92ac`  
		Last Modified: Tue, 03 Jun 2025 20:57:22 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:0e599020477e9ff23b27b1865ecb60543ed1535464abc4e188798db623bf31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93191df559a8ac9ecaf2375c3c0650313c7cf85b7a5c1828496f963214a3b7a8`
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
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe6cace6dcb5e8d0b30a41e65b06eac2b2db46153d20610970774ad0c6ae658`  
		Last Modified: Tue, 03 Jun 2025 18:08:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:20322b26c9067df443a4c1d508864fa6c56d75e95c6f7b54af8aa64244c36523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f876797d7587f086738701ffc4137685187baf0e93a73bec7ca91ab37de8e2`

```dockerfile
```

-	Layers:
	-	`sha256:beb15a763ca188b107db77465e3fbd30750125d1abfcb5ce92acbb109fac9e12`  
		Last Modified: Tue, 03 Jun 2025 20:57:26 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:032295d595a30a6e02710d95f3b3371b26f67558194ac6e026d302bda83f82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2122a29fe765e930ef544b90d5626a1b68d149b8d8e01d11af499a44ad680e`
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
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebcf7fe8e5b3a56dc480f7baa83adbd38d2bbed924d023380166bd9981fd69`  
		Last Modified: Tue, 03 Jun 2025 18:23:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:f18a5550f0cb7923ac9d1d849700acba1c8edb7aae430b47bab129cbd920c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59fba1c4b597d8c4c1f24f141dd0eb7e85a15f0bef993397327c84bc7dbc29`

```dockerfile
```

-	Layers:
	-	`sha256:b2f945ed0151cbf2eb4c531a81285a4227388550be1b38523fe42a95a739afba`  
		Last Modified: Tue, 03 Jun 2025 20:57:30 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:a1ee7f0765400218d94bcf05b108750a2c1d828a1ddc229520f68cd1a729772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce2215357ad2fb81086a7d81d51e879117d3d8e82b33a5594ad71cb42c9bd91`
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
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77e33529d308f759dde5ea0c2bc855d0fe710addc9b1ea041e795164831318`  
		Last Modified: Tue, 03 Jun 2025 18:22:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:458018497dd1f52d267442fa606155e76006f16995d106b8de40fab5ce15d07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e4beb2fa95e1452e4c3038fa80d0473aa25a3f0889c913e70dd71ab4adf9b4`

```dockerfile
```

-	Layers:
	-	`sha256:ab157204d16e4104829c5bb33652543a9248eea5ff2da1aa7f73be9a05e080d7`  
		Last Modified: Tue, 03 Jun 2025 20:57:33 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:d6cee6070c0808acf67782ea629ef2b095b877a064ef586239ad9d751fede448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5b2af2bb2f493ce23801f42d46661f10316f40ccd8f2c5fa91526f391f8845`
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
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63335d678adcf565f57b5c9a5020490b91f64dfcb434b646af92d61010878019`  
		Last Modified: Tue, 03 Jun 2025 18:09:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:8d414aad040bcc21d6e5781cc4ef29badad9a7a3274a8a253ec0a84575ca6ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecca08806a2ed272df4613365d603a586113ca6a6aea54411b44f1d3b61d05`

```dockerfile
```

-	Layers:
	-	`sha256:d641a2c5f6581536130597650655cb4668997c123bb18fbf12c0cdab75476fac`  
		Last Modified: Tue, 03 Jun 2025 20:57:38 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:fec67310cfde82241c2679a340f9fc9406516fb93c65a6d19cdbb4e9922ea1b7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128880529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c5ee3146bf8653ea930cfa655c44d0bc355630fddd92e0030c902f33dab838`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205bf2036fc00a819f1b20ae7e74f17c7c9a940bd0dd258616c46fb6e1760700`  
		Last Modified: Tue, 03 Jun 2025 18:13:01 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916bb5d7a2e9f16d1e2680557912b6c86f7e9ae2776dd6afbf2febca98dafcdb`  
		Last Modified: Tue, 03 Jun 2025 18:13:03 GMT  
		Size: 6.3 MB (6298082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a9c816e9f4737757e7ca952d1bd60161ba76a88543efd9351ed3ff255df401`  
		Last Modified: Tue, 03 Jun 2025 18:13:01 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6d81f9d4a7050f2769dadb14d5e17dec74f08d03be47023ffa8e84923d47c5`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd115dcb9313535536aaf899048ce8be8220c2386cc2ced9e4aa687915abed9`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5381b683b657bc05fc21206ec23dfe56d920b8488a2fff13da0650f8cde4c4`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:e4ff89435a697d4dc2269f44a9cc03c0ce206bf2ec0c5e86346eec2c793968c1
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
$ docker pull nats@sha256:165f3f9e87763690201921b55fb96b150d36d84642b6f38bb19597e6d7221e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10437622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1758922c6ce2a574c21623a2d02a76150fe7e8e4e2d52fb16edf9fb7e7e4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c43a19c65dc59aaf516d2615f3588ad1dc1017d49dcb9aa321aeeef4b7ffc1`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 6.6 MB (6639806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:acc886b722ace04957f77e3a1c8e6749940f7041386ce05210e8ea4c69f46932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650a81620e7f82cdb309ecf6157c2da44d151b3566cf6de4864c7dc6d20d683c`

```dockerfile
```

-	Layers:
	-	`sha256:02ec91a27ddca6b7dd03de7acc756b53883df80e809a4ac3e313f849e98fdbc1`  
		Last Modified: Tue, 03 Jun 2025 20:57:34 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:261dc298ca8bb3e809b2fa84c845abe8fc4a133a3a6d81b41d5fa052f2e2d643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de804bb490ce73fbc139af75dd82c0b81800c69fecddde21775f3528a6d7c7f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562b8a11b8ed69d392bd2d9542980acf48db7b4527ff82479fb7de58d715714`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 6.4 MB (6363844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3005b967f68a27687c38d68520bdede8bff0aaf8a4c45416991973c3ceb4a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727afe280399541b9353f4c6fd9eeb040798b41369e880443022658368b70f8d`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c7bc8e0c9bf979f2e1a4b1c68db710249a14826eb638af9a1a90cf60a5860e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f605c808048d40222ff44f9f4fab194ef118bc38ba23cdbd2cb00b66d1f4a768`

```dockerfile
```

-	Layers:
	-	`sha256:8d1a85b4eba1b90277a6099a69d60e91db6dbe50ec0761e7e0713eaba4243490`  
		Last Modified: Tue, 03 Jun 2025 20:57:37 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c49785ef72f6851e19acd1effd844500de145fe8f8b60deb80f4b412acfd8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1c42fbe838dc45066f11b49b3a2b289f1e68ca79a337e2d37a8c9258a4d69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c60b436ca9be1cafae973b2673faaf38e3c6f55f8bcf1808f09815771e3688d`  
		Last Modified: Tue, 03 Jun 2025 20:58:00 GMT  
		Size: 6.4 MB (6351017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd3c878be8ff45a5224d95e5e15f26bbec36e0946930597d58789fb8b90cd85`  
		Last Modified: Tue, 03 Jun 2025 18:02:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde678942fe21a15ddffc4415cc8cdfea1b4ec957fbfddc20b2e769c8f24b887`  
		Last Modified: Tue, 03 Jun 2025 18:02:28 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:0e862f0aa96b7c561038da51377fdd552e6ad618d4148a8abcf19463c287e82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b404fa016eca9854ca662633cbbbed396ffd14707165264453f3887486787cf`

```dockerfile
```

-	Layers:
	-	`sha256:49b59c86b7347c12453d29446f15f08a34553aac5bde9dad6828b2cca678778f`  
		Last Modified: Tue, 03 Jun 2025 20:57:41 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:285a2a4cd223ee5a09948483638d63000a1012062bcecd10558588dcea57af68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1915225864493be141ed87c713508d93dc744b32d85e0c549444133809ac37a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988a5cc26a525b12202b4ede8dbadf7282232fa3202588c82228cc51312a2db`  
		Last Modified: Tue, 03 Jun 2025 18:12:34 GMT  
		Size: 6.1 MB (6145683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ed6725710b37dc92dbdc9beb40eddc4b06a58b847403c608550796d72c7430`  
		Last Modified: Tue, 03 Jun 2025 18:12:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3e1af6617ced1a84b929dfa36cc1aeefede7065ee2c580030f864336d30215`  
		Last Modified: Tue, 03 Jun 2025 18:12:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b58de4f1cc2ff62b12af617c5814335385fc4252143980d31ec8b385b8a0281a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b429f6e62c50bb7cc5184af5e6f318d09a3ca04b31430f71f3d35eaf9c080d52`

```dockerfile
```

-	Layers:
	-	`sha256:be4126cc80da8c7edb98f1b5a8da59348d702f75d87e8375559dbcaa9e628273`  
		Last Modified: Tue, 03 Jun 2025 20:57:45 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9c85f40d23ab0ee0d9ae30d532b565f8a86573f0300420151060cbedcef5e8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9856694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c32a0cc3e550a3e68b0856e8da573eacf0ab169da68dbdccf9b2689d5820d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4574fc8f9c31a7e7c3096b2295a13bb991034e66aaee26f0c8bb92f4965f89`  
		Last Modified: Tue, 03 Jun 2025 18:15:03 GMT  
		Size: 6.1 MB (6125536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26043e6e9cf09cbd98c4343bed49c94ad7825b33e6dc73d6aef9f860bca1f5f7`  
		Last Modified: Tue, 03 Jun 2025 18:11:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d10afb72d6f0cf76c7bb3528287bc589928122df027b23f8226d7c2926290`  
		Last Modified: Tue, 03 Jun 2025 18:11:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:946551fed6e10788bcccc2dddf5722a62178223fd200dd771430b848fdb40f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5564c58fcb5f6b52983f1f0b07658184fab57abaf366dfe4756655fff3c9c166`

```dockerfile
```

-	Layers:
	-	`sha256:c6b4252ac8a827db1eaae604fe622384be59f71e498988ad120c735b8870df72`  
		Last Modified: Tue, 03 Jun 2025 20:57:48 GMT  
		Size: 13.2 KB (13165 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:9b4247153f56677441a4087e2f007d554133f2b656c8e24c4e7f283e13775ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10131011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e1ab87078f53cf2d3de1cc3d84ffcb8a89160be9e97291e74e906c3f21208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeaa39221515ea4113a7177048180cf406a52328259a52ab2741589dbd942be`  
		Last Modified: Tue, 03 Jun 2025 18:09:14 GMT  
		Size: 6.5 MB (6482513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877186488f8186bc3fd5f22ae5055586ca7ba35d22bd8b44e183d8de602b7a86`  
		Last Modified: Tue, 03 Jun 2025 18:03:59 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d673d1efb6b2752e2fcace714fb45f3efb76e03432446c01c5926e0defc8dd`  
		Last Modified: Tue, 03 Jun 2025 18:04:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8271d38fc2c1db1251228a13e31422f50095cebc22fa791967b817d9fab8d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbbb56c5affc65c809913f0c2e71df3151bb57a4f1ec03a70ef0f217a8bc3f8`

```dockerfile
```

-	Layers:
	-	`sha256:0f8a134b43959c10be25f3307dfd04c7c345280c8d0f92932ddf07e454304b3b`  
		Last Modified: Tue, 03 Jun 2025 20:57:52 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.22`

```console
$ docker pull nats@sha256:e4ff89435a697d4dc2269f44a9cc03c0ce206bf2ec0c5e86346eec2c793968c1
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

### `nats:2.10-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:165f3f9e87763690201921b55fb96b150d36d84642b6f38bb19597e6d7221e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10437622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1758922c6ce2a574c21623a2d02a76150fe7e8e4e2d52fb16edf9fb7e7e4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c43a19c65dc59aaf516d2615f3588ad1dc1017d49dcb9aa321aeeef4b7ffc1`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 6.6 MB (6639806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:acc886b722ace04957f77e3a1c8e6749940f7041386ce05210e8ea4c69f46932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650a81620e7f82cdb309ecf6157c2da44d151b3566cf6de4864c7dc6d20d683c`

```dockerfile
```

-	Layers:
	-	`sha256:02ec91a27ddca6b7dd03de7acc756b53883df80e809a4ac3e313f849e98fdbc1`  
		Last Modified: Tue, 03 Jun 2025 20:57:34 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:261dc298ca8bb3e809b2fa84c845abe8fc4a133a3a6d81b41d5fa052f2e2d643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de804bb490ce73fbc139af75dd82c0b81800c69fecddde21775f3528a6d7c7f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562b8a11b8ed69d392bd2d9542980acf48db7b4527ff82479fb7de58d715714`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 6.4 MB (6363844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3005b967f68a27687c38d68520bdede8bff0aaf8a4c45416991973c3ceb4a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727afe280399541b9353f4c6fd9eeb040798b41369e880443022658368b70f8d`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c7bc8e0c9bf979f2e1a4b1c68db710249a14826eb638af9a1a90cf60a5860e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f605c808048d40222ff44f9f4fab194ef118bc38ba23cdbd2cb00b66d1f4a768`

```dockerfile
```

-	Layers:
	-	`sha256:8d1a85b4eba1b90277a6099a69d60e91db6dbe50ec0761e7e0713eaba4243490`  
		Last Modified: Tue, 03 Jun 2025 20:57:37 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c49785ef72f6851e19acd1effd844500de145fe8f8b60deb80f4b412acfd8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1c42fbe838dc45066f11b49b3a2b289f1e68ca79a337e2d37a8c9258a4d69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c60b436ca9be1cafae973b2673faaf38e3c6f55f8bcf1808f09815771e3688d`  
		Last Modified: Tue, 03 Jun 2025 20:58:00 GMT  
		Size: 6.4 MB (6351017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd3c878be8ff45a5224d95e5e15f26bbec36e0946930597d58789fb8b90cd85`  
		Last Modified: Tue, 03 Jun 2025 18:02:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde678942fe21a15ddffc4415cc8cdfea1b4ec957fbfddc20b2e769c8f24b887`  
		Last Modified: Tue, 03 Jun 2025 18:02:28 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:0e862f0aa96b7c561038da51377fdd552e6ad618d4148a8abcf19463c287e82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b404fa016eca9854ca662633cbbbed396ffd14707165264453f3887486787cf`

```dockerfile
```

-	Layers:
	-	`sha256:49b59c86b7347c12453d29446f15f08a34553aac5bde9dad6828b2cca678778f`  
		Last Modified: Tue, 03 Jun 2025 20:57:41 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:285a2a4cd223ee5a09948483638d63000a1012062bcecd10558588dcea57af68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1915225864493be141ed87c713508d93dc744b32d85e0c549444133809ac37a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988a5cc26a525b12202b4ede8dbadf7282232fa3202588c82228cc51312a2db`  
		Last Modified: Tue, 03 Jun 2025 18:12:34 GMT  
		Size: 6.1 MB (6145683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ed6725710b37dc92dbdc9beb40eddc4b06a58b847403c608550796d72c7430`  
		Last Modified: Tue, 03 Jun 2025 18:12:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3e1af6617ced1a84b929dfa36cc1aeefede7065ee2c580030f864336d30215`  
		Last Modified: Tue, 03 Jun 2025 18:12:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b58de4f1cc2ff62b12af617c5814335385fc4252143980d31ec8b385b8a0281a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b429f6e62c50bb7cc5184af5e6f318d09a3ca04b31430f71f3d35eaf9c080d52`

```dockerfile
```

-	Layers:
	-	`sha256:be4126cc80da8c7edb98f1b5a8da59348d702f75d87e8375559dbcaa9e628273`  
		Last Modified: Tue, 03 Jun 2025 20:57:45 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9c85f40d23ab0ee0d9ae30d532b565f8a86573f0300420151060cbedcef5e8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9856694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c32a0cc3e550a3e68b0856e8da573eacf0ab169da68dbdccf9b2689d5820d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4574fc8f9c31a7e7c3096b2295a13bb991034e66aaee26f0c8bb92f4965f89`  
		Last Modified: Tue, 03 Jun 2025 18:15:03 GMT  
		Size: 6.1 MB (6125536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26043e6e9cf09cbd98c4343bed49c94ad7825b33e6dc73d6aef9f860bca1f5f7`  
		Last Modified: Tue, 03 Jun 2025 18:11:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d10afb72d6f0cf76c7bb3528287bc589928122df027b23f8226d7c2926290`  
		Last Modified: Tue, 03 Jun 2025 18:11:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:946551fed6e10788bcccc2dddf5722a62178223fd200dd771430b848fdb40f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5564c58fcb5f6b52983f1f0b07658184fab57abaf366dfe4756655fff3c9c166`

```dockerfile
```

-	Layers:
	-	`sha256:c6b4252ac8a827db1eaae604fe622384be59f71e498988ad120c735b8870df72`  
		Last Modified: Tue, 03 Jun 2025 20:57:48 GMT  
		Size: 13.2 KB (13165 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:9b4247153f56677441a4087e2f007d554133f2b656c8e24c4e7f283e13775ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10131011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e1ab87078f53cf2d3de1cc3d84ffcb8a89160be9e97291e74e906c3f21208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeaa39221515ea4113a7177048180cf406a52328259a52ab2741589dbd942be`  
		Last Modified: Tue, 03 Jun 2025 18:09:14 GMT  
		Size: 6.5 MB (6482513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877186488f8186bc3fd5f22ae5055586ca7ba35d22bd8b44e183d8de602b7a86`  
		Last Modified: Tue, 03 Jun 2025 18:03:59 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d673d1efb6b2752e2fcace714fb45f3efb76e03432446c01c5926e0defc8dd`  
		Last Modified: Tue, 03 Jun 2025 18:04:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8271d38fc2c1db1251228a13e31422f50095cebc22fa791967b817d9fab8d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbbb56c5affc65c809913f0c2e71df3151bb57a4f1ec03a70ef0f217a8bc3f8`

```dockerfile
```

-	Layers:
	-	`sha256:0f8a134b43959c10be25f3307dfd04c7c345280c8d0f92932ddf07e454304b3b`  
		Last Modified: Tue, 03 Jun 2025 20:57:52 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:28edd413f190fb139ed600359da94e5a583e999dce2750488c75bef692250817
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
$ docker pull nats@sha256:f030f79672be88d009b75f61c2cb5fe9d07ad3364742a9b27cd60c9338ffafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4962b82a0ae69663e5a74740285899ca5957c69f6c53bf82311476aa1fae5ef8`
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
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5edca7674c56d6da9be7a373f78942e4c4aa5f175636ee35ccffba1533772e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3176d2028656537e4bfe7efebe9f8fcc985778a684370b2eff8c909b50c6f3`

```dockerfile
```

-	Layers:
	-	`sha256:5f2aca3d9450c14453dcb34e8c6b2a5a9a11673e6f7baeb3c28b7b435f2789d0`  
		Last Modified: Tue, 03 Jun 2025 20:57:19 GMT  
		Size: 8.7 KB (8710 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a72209661fa798f94ca59fe982425636af6df596e83cc2bdb1b1ebde04a57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f5ba25ee4d10359cc31039d1a9a05f150b96f797eb6ca7d155076fd547bb9`
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
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb3048cc57f790e44bb317519f7d61ce9e2d2cdcd7a57ac04cdf293bdd74a`  
		Last Modified: Tue, 03 Jun 2025 18:08:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9c3d54e7088aa0eb163c2eeb032e0d168126cdf0af77576fdc60ea726a70e690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8e6de48fcf449ba2519083b4bc5415c135d29db13e6c6b49b06eb5c5b766a1`

```dockerfile
```

-	Layers:
	-	`sha256:224e3a5982d8875c00e7bc85a73e0963da1394057839ae2fc9902d645dfd92ac`  
		Last Modified: Tue, 03 Jun 2025 20:57:22 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:0e599020477e9ff23b27b1865ecb60543ed1535464abc4e188798db623bf31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93191df559a8ac9ecaf2375c3c0650313c7cf85b7a5c1828496f963214a3b7a8`
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
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe6cace6dcb5e8d0b30a41e65b06eac2b2db46153d20610970774ad0c6ae658`  
		Last Modified: Tue, 03 Jun 2025 18:08:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:20322b26c9067df443a4c1d508864fa6c56d75e95c6f7b54af8aa64244c36523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f876797d7587f086738701ffc4137685187baf0e93a73bec7ca91ab37de8e2`

```dockerfile
```

-	Layers:
	-	`sha256:beb15a763ca188b107db77465e3fbd30750125d1abfcb5ce92acbb109fac9e12`  
		Last Modified: Tue, 03 Jun 2025 20:57:26 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:032295d595a30a6e02710d95f3b3371b26f67558194ac6e026d302bda83f82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2122a29fe765e930ef544b90d5626a1b68d149b8d8e01d11af499a44ad680e`
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
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebcf7fe8e5b3a56dc480f7baa83adbd38d2bbed924d023380166bd9981fd69`  
		Last Modified: Tue, 03 Jun 2025 18:23:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f18a5550f0cb7923ac9d1d849700acba1c8edb7aae430b47bab129cbd920c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59fba1c4b597d8c4c1f24f141dd0eb7e85a15f0bef993397327c84bc7dbc29`

```dockerfile
```

-	Layers:
	-	`sha256:b2f945ed0151cbf2eb4c531a81285a4227388550be1b38523fe42a95a739afba`  
		Last Modified: Tue, 03 Jun 2025 20:57:30 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:a1ee7f0765400218d94bcf05b108750a2c1d828a1ddc229520f68cd1a729772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce2215357ad2fb81086a7d81d51e879117d3d8e82b33a5594ad71cb42c9bd91`
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
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77e33529d308f759dde5ea0c2bc855d0fe710addc9b1ea041e795164831318`  
		Last Modified: Tue, 03 Jun 2025 18:22:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:458018497dd1f52d267442fa606155e76006f16995d106b8de40fab5ce15d07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e4beb2fa95e1452e4c3038fa80d0473aa25a3f0889c913e70dd71ab4adf9b4`

```dockerfile
```

-	Layers:
	-	`sha256:ab157204d16e4104829c5bb33652543a9248eea5ff2da1aa7f73be9a05e080d7`  
		Last Modified: Tue, 03 Jun 2025 20:57:33 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:d6cee6070c0808acf67782ea629ef2b095b877a064ef586239ad9d751fede448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5b2af2bb2f493ce23801f42d46661f10316f40ccd8f2c5fa91526f391f8845`
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
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63335d678adcf565f57b5c9a5020490b91f64dfcb434b646af92d61010878019`  
		Last Modified: Tue, 03 Jun 2025 18:09:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8d414aad040bcc21d6e5781cc4ef29badad9a7a3274a8a253ec0a84575ca6ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecca08806a2ed272df4613365d603a586113ca6a6aea54411b44f1d3b61d05`

```dockerfile
```

-	Layers:
	-	`sha256:d641a2c5f6581536130597650655cb4668997c123bb18fbf12c0cdab75476fac`  
		Last Modified: Tue, 03 Jun 2025 20:57:38 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:48b0017ed68a04ae269efc31a050436377b22dcff094f7bcb8f0523d1d2ae263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.10-nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:fec67310cfde82241c2679a340f9fc9406516fb93c65a6d19cdbb4e9922ea1b7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128880529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c5ee3146bf8653ea930cfa655c44d0bc355630fddd92e0030c902f33dab838`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205bf2036fc00a819f1b20ae7e74f17c7c9a940bd0dd258616c46fb6e1760700`  
		Last Modified: Tue, 03 Jun 2025 18:13:01 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916bb5d7a2e9f16d1e2680557912b6c86f7e9ae2776dd6afbf2febca98dafcdb`  
		Last Modified: Tue, 03 Jun 2025 18:13:03 GMT  
		Size: 6.3 MB (6298082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a9c816e9f4737757e7ca952d1bd60161ba76a88543efd9351ed3ff255df401`  
		Last Modified: Tue, 03 Jun 2025 18:13:01 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6d81f9d4a7050f2769dadb14d5e17dec74f08d03be47023ffa8e84923d47c5`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd115dcb9313535536aaf899048ce8be8220c2386cc2ced9e4aa687915abed9`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5381b683b657bc05fc21206ec23dfe56d920b8488a2fff13da0650f8cde4c4`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:48b0017ed68a04ae269efc31a050436377b22dcff094f7bcb8f0523d1d2ae263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.10-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:fec67310cfde82241c2679a340f9fc9406516fb93c65a6d19cdbb4e9922ea1b7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128880529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c5ee3146bf8653ea930cfa655c44d0bc355630fddd92e0030c902f33dab838`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205bf2036fc00a819f1b20ae7e74f17c7c9a940bd0dd258616c46fb6e1760700`  
		Last Modified: Tue, 03 Jun 2025 18:13:01 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916bb5d7a2e9f16d1e2680557912b6c86f7e9ae2776dd6afbf2febca98dafcdb`  
		Last Modified: Tue, 03 Jun 2025 18:13:03 GMT  
		Size: 6.3 MB (6298082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a9c816e9f4737757e7ca952d1bd60161ba76a88543efd9351ed3ff255df401`  
		Last Modified: Tue, 03 Jun 2025 18:13:01 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6d81f9d4a7050f2769dadb14d5e17dec74f08d03be47023ffa8e84923d47c5`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd115dcb9313535536aaf899048ce8be8220c2386cc2ced9e4aa687915abed9`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5381b683b657bc05fc21206ec23dfe56d920b8488a2fff13da0650f8cde4c4`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:28edd413f190fb139ed600359da94e5a583e999dce2750488c75bef692250817
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
$ docker pull nats@sha256:f030f79672be88d009b75f61c2cb5fe9d07ad3364742a9b27cd60c9338ffafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4962b82a0ae69663e5a74740285899ca5957c69f6c53bf82311476aa1fae5ef8`
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
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5edca7674c56d6da9be7a373f78942e4c4aa5f175636ee35ccffba1533772e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3176d2028656537e4bfe7efebe9f8fcc985778a684370b2eff8c909b50c6f3`

```dockerfile
```

-	Layers:
	-	`sha256:5f2aca3d9450c14453dcb34e8c6b2a5a9a11673e6f7baeb3c28b7b435f2789d0`  
		Last Modified: Tue, 03 Jun 2025 20:57:19 GMT  
		Size: 8.7 KB (8710 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a72209661fa798f94ca59fe982425636af6df596e83cc2bdb1b1ebde04a57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f5ba25ee4d10359cc31039d1a9a05f150b96f797eb6ca7d155076fd547bb9`
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
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb3048cc57f790e44bb317519f7d61ce9e2d2cdcd7a57ac04cdf293bdd74a`  
		Last Modified: Tue, 03 Jun 2025 18:08:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9c3d54e7088aa0eb163c2eeb032e0d168126cdf0af77576fdc60ea726a70e690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8e6de48fcf449ba2519083b4bc5415c135d29db13e6c6b49b06eb5c5b766a1`

```dockerfile
```

-	Layers:
	-	`sha256:224e3a5982d8875c00e7bc85a73e0963da1394057839ae2fc9902d645dfd92ac`  
		Last Modified: Tue, 03 Jun 2025 20:57:22 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:0e599020477e9ff23b27b1865ecb60543ed1535464abc4e188798db623bf31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93191df559a8ac9ecaf2375c3c0650313c7cf85b7a5c1828496f963214a3b7a8`
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
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe6cace6dcb5e8d0b30a41e65b06eac2b2db46153d20610970774ad0c6ae658`  
		Last Modified: Tue, 03 Jun 2025 18:08:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:20322b26c9067df443a4c1d508864fa6c56d75e95c6f7b54af8aa64244c36523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f876797d7587f086738701ffc4137685187baf0e93a73bec7ca91ab37de8e2`

```dockerfile
```

-	Layers:
	-	`sha256:beb15a763ca188b107db77465e3fbd30750125d1abfcb5ce92acbb109fac9e12`  
		Last Modified: Tue, 03 Jun 2025 20:57:26 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:032295d595a30a6e02710d95f3b3371b26f67558194ac6e026d302bda83f82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2122a29fe765e930ef544b90d5626a1b68d149b8d8e01d11af499a44ad680e`
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
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebcf7fe8e5b3a56dc480f7baa83adbd38d2bbed924d023380166bd9981fd69`  
		Last Modified: Tue, 03 Jun 2025 18:23:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f18a5550f0cb7923ac9d1d849700acba1c8edb7aae430b47bab129cbd920c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59fba1c4b597d8c4c1f24f141dd0eb7e85a15f0bef993397327c84bc7dbc29`

```dockerfile
```

-	Layers:
	-	`sha256:b2f945ed0151cbf2eb4c531a81285a4227388550be1b38523fe42a95a739afba`  
		Last Modified: Tue, 03 Jun 2025 20:57:30 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:a1ee7f0765400218d94bcf05b108750a2c1d828a1ddc229520f68cd1a729772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce2215357ad2fb81086a7d81d51e879117d3d8e82b33a5594ad71cb42c9bd91`
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
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77e33529d308f759dde5ea0c2bc855d0fe710addc9b1ea041e795164831318`  
		Last Modified: Tue, 03 Jun 2025 18:22:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:458018497dd1f52d267442fa606155e76006f16995d106b8de40fab5ce15d07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e4beb2fa95e1452e4c3038fa80d0473aa25a3f0889c913e70dd71ab4adf9b4`

```dockerfile
```

-	Layers:
	-	`sha256:ab157204d16e4104829c5bb33652543a9248eea5ff2da1aa7f73be9a05e080d7`  
		Last Modified: Tue, 03 Jun 2025 20:57:33 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d6cee6070c0808acf67782ea629ef2b095b877a064ef586239ad9d751fede448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5b2af2bb2f493ce23801f42d46661f10316f40ccd8f2c5fa91526f391f8845`
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
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63335d678adcf565f57b5c9a5020490b91f64dfcb434b646af92d61010878019`  
		Last Modified: Tue, 03 Jun 2025 18:09:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8d414aad040bcc21d6e5781cc4ef29badad9a7a3274a8a253ec0a84575ca6ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecca08806a2ed272df4613365d603a586113ca6a6aea54411b44f1d3b61d05`

```dockerfile
```

-	Layers:
	-	`sha256:d641a2c5f6581536130597650655cb4668997c123bb18fbf12c0cdab75476fac`  
		Last Modified: Tue, 03 Jun 2025 20:57:38 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:c865099f6431bd38a81b1dbb4c1e9ffe23791ee675edf95df91ae4dd8e3b2d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:09c9d1f6ea65e8b31ef0f5e81c27201ed518b7cc60acc67baaed731ae31c6ed6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280616850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e217a8a9442b4e2c2d9393415d25664e6acf8e2cc04c38c0accc36e02722fd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 17:56:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 17:56:44 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 17:56:45 GMT
ENV NATS_SERVER=2.10.29
# Tue, 03 Jun 2025 17:56:46 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 03 Jun 2025 17:56:46 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 03 Jun 2025 17:58:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Jun 2025 17:58:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 03 Jun 2025 17:58:58 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 17:58:58 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 17:58:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 17:58:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def4758c7b3d08c0f41d6f89e5f9d9f47c4898d6b91fce49249cff24101ac2fa`  
		Last Modified: Tue, 03 Jun 2025 18:02:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573a0db2aab22a0ab2e42e79f1bdd724b33420879a2484800a9fb4c69bf2f283`  
		Last Modified: Tue, 03 Jun 2025 18:02:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0d3d0a876063591e1adc5bf4f932771eddfa0a07a0eb223319deec608b15af`  
		Last Modified: Tue, 03 Jun 2025 18:02:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9ce758cbca798812f754506e7cb5ec7b3273e48fb2fc8e231bfca20d6e0c2`  
		Last Modified: Tue, 03 Jun 2025 18:02:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60f9507f2022affa1a12862e2968b9074ee20390c52e8bcac51762955da4f14`  
		Last Modified: Tue, 03 Jun 2025 18:02:40 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0b9f9d9c2b6c5e9805f2da400483c60f081952b69adf0c37c0c93cae87a718`  
		Last Modified: Tue, 03 Jun 2025 18:02:44 GMT  
		Size: 356.2 KB (356225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75607bc528f29864e75cf56ffe65eda263723bcd1c8b9a20ab355bd9a268936`  
		Last Modified: Tue, 03 Jun 2025 18:08:47 GMT  
		Size: 6.6 MB (6620328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4157813c216e3a6b8bdae9418bfc16ff4c350221ea7dd44e04c6093b95265346`  
		Last Modified: Tue, 03 Jun 2025 18:02:50 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab1f981d7a518e35037d74347f18dc89d7e31959f3f9d495f8f942d2b4e2369`  
		Last Modified: Tue, 03 Jun 2025 18:02:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acdbd2270bd120ae6589ab16ce127edd53a810dbd23f72bc5d70b624ea5c526`  
		Last Modified: Tue, 03 Jun 2025 18:03:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b42133486ae606e623291120d1fe7928f904effcd2815c9dd547f2254a8817`  
		Last Modified: Tue, 03 Jun 2025 18:03:04 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:c865099f6431bd38a81b1dbb4c1e9ffe23791ee675edf95df91ae4dd8e3b2d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.10-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:09c9d1f6ea65e8b31ef0f5e81c27201ed518b7cc60acc67baaed731ae31c6ed6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280616850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e217a8a9442b4e2c2d9393415d25664e6acf8e2cc04c38c0accc36e02722fd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 17:56:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 17:56:44 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 17:56:45 GMT
ENV NATS_SERVER=2.10.29
# Tue, 03 Jun 2025 17:56:46 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 03 Jun 2025 17:56:46 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 03 Jun 2025 17:58:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Jun 2025 17:58:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 03 Jun 2025 17:58:58 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 17:58:58 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 17:58:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 17:58:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def4758c7b3d08c0f41d6f89e5f9d9f47c4898d6b91fce49249cff24101ac2fa`  
		Last Modified: Tue, 03 Jun 2025 18:02:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573a0db2aab22a0ab2e42e79f1bdd724b33420879a2484800a9fb4c69bf2f283`  
		Last Modified: Tue, 03 Jun 2025 18:02:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0d3d0a876063591e1adc5bf4f932771eddfa0a07a0eb223319deec608b15af`  
		Last Modified: Tue, 03 Jun 2025 18:02:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9ce758cbca798812f754506e7cb5ec7b3273e48fb2fc8e231bfca20d6e0c2`  
		Last Modified: Tue, 03 Jun 2025 18:02:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60f9507f2022affa1a12862e2968b9074ee20390c52e8bcac51762955da4f14`  
		Last Modified: Tue, 03 Jun 2025 18:02:40 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0b9f9d9c2b6c5e9805f2da400483c60f081952b69adf0c37c0c93cae87a718`  
		Last Modified: Tue, 03 Jun 2025 18:02:44 GMT  
		Size: 356.2 KB (356225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75607bc528f29864e75cf56ffe65eda263723bcd1c8b9a20ab355bd9a268936`  
		Last Modified: Tue, 03 Jun 2025 18:08:47 GMT  
		Size: 6.6 MB (6620328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4157813c216e3a6b8bdae9418bfc16ff4c350221ea7dd44e04c6093b95265346`  
		Last Modified: Tue, 03 Jun 2025 18:02:50 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab1f981d7a518e35037d74347f18dc89d7e31959f3f9d495f8f942d2b4e2369`  
		Last Modified: Tue, 03 Jun 2025 18:02:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acdbd2270bd120ae6589ab16ce127edd53a810dbd23f72bc5d70b624ea5c526`  
		Last Modified: Tue, 03 Jun 2025 18:03:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b42133486ae606e623291120d1fe7928f904effcd2815c9dd547f2254a8817`  
		Last Modified: Tue, 03 Jun 2025 18:03:04 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29`

```console
$ docker pull nats@sha256:318f390cf15f0d300f422e4ba7b8ac7fe2bcedb0286ee48810766b07a64d88f3
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
	-	windows version 10.0.20348.3692; amd64

### `nats:2.10.29` - linux; amd64

```console
$ docker pull nats@sha256:f030f79672be88d009b75f61c2cb5fe9d07ad3364742a9b27cd60c9338ffafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4962b82a0ae69663e5a74740285899ca5957c69f6c53bf82311476aa1fae5ef8`
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
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:5edca7674c56d6da9be7a373f78942e4c4aa5f175636ee35ccffba1533772e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3176d2028656537e4bfe7efebe9f8fcc985778a684370b2eff8c909b50c6f3`

```dockerfile
```

-	Layers:
	-	`sha256:5f2aca3d9450c14453dcb34e8c6b2a5a9a11673e6f7baeb3c28b7b435f2789d0`  
		Last Modified: Tue, 03 Jun 2025 20:57:19 GMT  
		Size: 8.7 KB (8710 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a72209661fa798f94ca59fe982425636af6df596e83cc2bdb1b1ebde04a57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f5ba25ee4d10359cc31039d1a9a05f150b96f797eb6ca7d155076fd547bb9`
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
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb3048cc57f790e44bb317519f7d61ce9e2d2cdcd7a57ac04cdf293bdd74a`  
		Last Modified: Tue, 03 Jun 2025 18:08:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:9c3d54e7088aa0eb163c2eeb032e0d168126cdf0af77576fdc60ea726a70e690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8e6de48fcf449ba2519083b4bc5415c135d29db13e6c6b49b06eb5c5b766a1`

```dockerfile
```

-	Layers:
	-	`sha256:224e3a5982d8875c00e7bc85a73e0963da1394057839ae2fc9902d645dfd92ac`  
		Last Modified: Tue, 03 Jun 2025 20:57:22 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm variant v7

```console
$ docker pull nats@sha256:0e599020477e9ff23b27b1865ecb60543ed1535464abc4e188798db623bf31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93191df559a8ac9ecaf2375c3c0650313c7cf85b7a5c1828496f963214a3b7a8`
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
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe6cace6dcb5e8d0b30a41e65b06eac2b2db46153d20610970774ad0c6ae658`  
		Last Modified: Tue, 03 Jun 2025 18:08:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:20322b26c9067df443a4c1d508864fa6c56d75e95c6f7b54af8aa64244c36523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f876797d7587f086738701ffc4137685187baf0e93a73bec7ca91ab37de8e2`

```dockerfile
```

-	Layers:
	-	`sha256:beb15a763ca188b107db77465e3fbd30750125d1abfcb5ce92acbb109fac9e12`  
		Last Modified: Tue, 03 Jun 2025 20:57:26 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:032295d595a30a6e02710d95f3b3371b26f67558194ac6e026d302bda83f82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2122a29fe765e930ef544b90d5626a1b68d149b8d8e01d11af499a44ad680e`
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
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebcf7fe8e5b3a56dc480f7baa83adbd38d2bbed924d023380166bd9981fd69`  
		Last Modified: Tue, 03 Jun 2025 18:23:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:f18a5550f0cb7923ac9d1d849700acba1c8edb7aae430b47bab129cbd920c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59fba1c4b597d8c4c1f24f141dd0eb7e85a15f0bef993397327c84bc7dbc29`

```dockerfile
```

-	Layers:
	-	`sha256:b2f945ed0151cbf2eb4c531a81285a4227388550be1b38523fe42a95a739afba`  
		Last Modified: Tue, 03 Jun 2025 20:57:30 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; ppc64le

```console
$ docker pull nats@sha256:a1ee7f0765400218d94bcf05b108750a2c1d828a1ddc229520f68cd1a729772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce2215357ad2fb81086a7d81d51e879117d3d8e82b33a5594ad71cb42c9bd91`
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
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77e33529d308f759dde5ea0c2bc855d0fe710addc9b1ea041e795164831318`  
		Last Modified: Tue, 03 Jun 2025 18:22:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:458018497dd1f52d267442fa606155e76006f16995d106b8de40fab5ce15d07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e4beb2fa95e1452e4c3038fa80d0473aa25a3f0889c913e70dd71ab4adf9b4`

```dockerfile
```

-	Layers:
	-	`sha256:ab157204d16e4104829c5bb33652543a9248eea5ff2da1aa7f73be9a05e080d7`  
		Last Modified: Tue, 03 Jun 2025 20:57:33 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; s390x

```console
$ docker pull nats@sha256:d6cee6070c0808acf67782ea629ef2b095b877a064ef586239ad9d751fede448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5b2af2bb2f493ce23801f42d46661f10316f40ccd8f2c5fa91526f391f8845`
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
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63335d678adcf565f57b5c9a5020490b91f64dfcb434b646af92d61010878019`  
		Last Modified: Tue, 03 Jun 2025 18:09:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:8d414aad040bcc21d6e5781cc4ef29badad9a7a3274a8a253ec0a84575ca6ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecca08806a2ed272df4613365d603a586113ca6a6aea54411b44f1d3b61d05`

```dockerfile
```

-	Layers:
	-	`sha256:d641a2c5f6581536130597650655cb4668997c123bb18fbf12c0cdab75476fac`  
		Last Modified: Tue, 03 Jun 2025 20:57:38 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:fec67310cfde82241c2679a340f9fc9406516fb93c65a6d19cdbb4e9922ea1b7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128880529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c5ee3146bf8653ea930cfa655c44d0bc355630fddd92e0030c902f33dab838`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205bf2036fc00a819f1b20ae7e74f17c7c9a940bd0dd258616c46fb6e1760700`  
		Last Modified: Tue, 03 Jun 2025 18:13:01 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916bb5d7a2e9f16d1e2680557912b6c86f7e9ae2776dd6afbf2febca98dafcdb`  
		Last Modified: Tue, 03 Jun 2025 18:13:03 GMT  
		Size: 6.3 MB (6298082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a9c816e9f4737757e7ca952d1bd60161ba76a88543efd9351ed3ff255df401`  
		Last Modified: Tue, 03 Jun 2025 18:13:01 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6d81f9d4a7050f2769dadb14d5e17dec74f08d03be47023ffa8e84923d47c5`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd115dcb9313535536aaf899048ce8be8220c2386cc2ced9e4aa687915abed9`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5381b683b657bc05fc21206ec23dfe56d920b8488a2fff13da0650f8cde4c4`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-alpine`

```console
$ docker pull nats@sha256:e4ff89435a697d4dc2269f44a9cc03c0ce206bf2ec0c5e86346eec2c793968c1
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
$ docker pull nats@sha256:165f3f9e87763690201921b55fb96b150d36d84642b6f38bb19597e6d7221e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10437622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1758922c6ce2a574c21623a2d02a76150fe7e8e4e2d52fb16edf9fb7e7e4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c43a19c65dc59aaf516d2615f3588ad1dc1017d49dcb9aa321aeeef4b7ffc1`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 6.6 MB (6639806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:acc886b722ace04957f77e3a1c8e6749940f7041386ce05210e8ea4c69f46932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650a81620e7f82cdb309ecf6157c2da44d151b3566cf6de4864c7dc6d20d683c`

```dockerfile
```

-	Layers:
	-	`sha256:02ec91a27ddca6b7dd03de7acc756b53883df80e809a4ac3e313f849e98fdbc1`  
		Last Modified: Tue, 03 Jun 2025 20:57:34 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:261dc298ca8bb3e809b2fa84c845abe8fc4a133a3a6d81b41d5fa052f2e2d643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de804bb490ce73fbc139af75dd82c0b81800c69fecddde21775f3528a6d7c7f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562b8a11b8ed69d392bd2d9542980acf48db7b4527ff82479fb7de58d715714`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 6.4 MB (6363844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3005b967f68a27687c38d68520bdede8bff0aaf8a4c45416991973c3ceb4a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727afe280399541b9353f4c6fd9eeb040798b41369e880443022658368b70f8d`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c7bc8e0c9bf979f2e1a4b1c68db710249a14826eb638af9a1a90cf60a5860e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f605c808048d40222ff44f9f4fab194ef118bc38ba23cdbd2cb00b66d1f4a768`

```dockerfile
```

-	Layers:
	-	`sha256:8d1a85b4eba1b90277a6099a69d60e91db6dbe50ec0761e7e0713eaba4243490`  
		Last Modified: Tue, 03 Jun 2025 20:57:37 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c49785ef72f6851e19acd1effd844500de145fe8f8b60deb80f4b412acfd8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1c42fbe838dc45066f11b49b3a2b289f1e68ca79a337e2d37a8c9258a4d69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c60b436ca9be1cafae973b2673faaf38e3c6f55f8bcf1808f09815771e3688d`  
		Last Modified: Tue, 03 Jun 2025 20:58:00 GMT  
		Size: 6.4 MB (6351017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd3c878be8ff45a5224d95e5e15f26bbec36e0946930597d58789fb8b90cd85`  
		Last Modified: Tue, 03 Jun 2025 18:02:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde678942fe21a15ddffc4415cc8cdfea1b4ec957fbfddc20b2e769c8f24b887`  
		Last Modified: Tue, 03 Jun 2025 18:02:28 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:0e862f0aa96b7c561038da51377fdd552e6ad618d4148a8abcf19463c287e82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b404fa016eca9854ca662633cbbbed396ffd14707165264453f3887486787cf`

```dockerfile
```

-	Layers:
	-	`sha256:49b59c86b7347c12453d29446f15f08a34553aac5bde9dad6828b2cca678778f`  
		Last Modified: Tue, 03 Jun 2025 20:57:41 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:285a2a4cd223ee5a09948483638d63000a1012062bcecd10558588dcea57af68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1915225864493be141ed87c713508d93dc744b32d85e0c549444133809ac37a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988a5cc26a525b12202b4ede8dbadf7282232fa3202588c82228cc51312a2db`  
		Last Modified: Tue, 03 Jun 2025 18:12:34 GMT  
		Size: 6.1 MB (6145683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ed6725710b37dc92dbdc9beb40eddc4b06a58b847403c608550796d72c7430`  
		Last Modified: Tue, 03 Jun 2025 18:12:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3e1af6617ced1a84b929dfa36cc1aeefede7065ee2c580030f864336d30215`  
		Last Modified: Tue, 03 Jun 2025 18:12:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b58de4f1cc2ff62b12af617c5814335385fc4252143980d31ec8b385b8a0281a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b429f6e62c50bb7cc5184af5e6f318d09a3ca04b31430f71f3d35eaf9c080d52`

```dockerfile
```

-	Layers:
	-	`sha256:be4126cc80da8c7edb98f1b5a8da59348d702f75d87e8375559dbcaa9e628273`  
		Last Modified: Tue, 03 Jun 2025 20:57:45 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9c85f40d23ab0ee0d9ae30d532b565f8a86573f0300420151060cbedcef5e8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9856694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c32a0cc3e550a3e68b0856e8da573eacf0ab169da68dbdccf9b2689d5820d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4574fc8f9c31a7e7c3096b2295a13bb991034e66aaee26f0c8bb92f4965f89`  
		Last Modified: Tue, 03 Jun 2025 18:15:03 GMT  
		Size: 6.1 MB (6125536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26043e6e9cf09cbd98c4343bed49c94ad7825b33e6dc73d6aef9f860bca1f5f7`  
		Last Modified: Tue, 03 Jun 2025 18:11:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d10afb72d6f0cf76c7bb3528287bc589928122df027b23f8226d7c2926290`  
		Last Modified: Tue, 03 Jun 2025 18:11:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:946551fed6e10788bcccc2dddf5722a62178223fd200dd771430b848fdb40f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5564c58fcb5f6b52983f1f0b07658184fab57abaf366dfe4756655fff3c9c166`

```dockerfile
```

-	Layers:
	-	`sha256:c6b4252ac8a827db1eaae604fe622384be59f71e498988ad120c735b8870df72`  
		Last Modified: Tue, 03 Jun 2025 20:57:48 GMT  
		Size: 13.2 KB (13165 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; s390x

```console
$ docker pull nats@sha256:9b4247153f56677441a4087e2f007d554133f2b656c8e24c4e7f283e13775ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10131011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e1ab87078f53cf2d3de1cc3d84ffcb8a89160be9e97291e74e906c3f21208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeaa39221515ea4113a7177048180cf406a52328259a52ab2741589dbd942be`  
		Last Modified: Tue, 03 Jun 2025 18:09:14 GMT  
		Size: 6.5 MB (6482513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877186488f8186bc3fd5f22ae5055586ca7ba35d22bd8b44e183d8de602b7a86`  
		Last Modified: Tue, 03 Jun 2025 18:03:59 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d673d1efb6b2752e2fcace714fb45f3efb76e03432446c01c5926e0defc8dd`  
		Last Modified: Tue, 03 Jun 2025 18:04:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8271d38fc2c1db1251228a13e31422f50095cebc22fa791967b817d9fab8d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbbb56c5affc65c809913f0c2e71df3151bb57a4f1ec03a70ef0f217a8bc3f8`

```dockerfile
```

-	Layers:
	-	`sha256:0f8a134b43959c10be25f3307dfd04c7c345280c8d0f92932ddf07e454304b3b`  
		Last Modified: Tue, 03 Jun 2025 20:57:52 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-alpine3.22`

```console
$ docker pull nats@sha256:e4ff89435a697d4dc2269f44a9cc03c0ce206bf2ec0c5e86346eec2c793968c1
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

### `nats:2.10.29-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:165f3f9e87763690201921b55fb96b150d36d84642b6f38bb19597e6d7221e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10437622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1758922c6ce2a574c21623a2d02a76150fe7e8e4e2d52fb16edf9fb7e7e4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c43a19c65dc59aaf516d2615f3588ad1dc1017d49dcb9aa321aeeef4b7ffc1`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 6.6 MB (6639806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:acc886b722ace04957f77e3a1c8e6749940f7041386ce05210e8ea4c69f46932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650a81620e7f82cdb309ecf6157c2da44d151b3566cf6de4864c7dc6d20d683c`

```dockerfile
```

-	Layers:
	-	`sha256:02ec91a27ddca6b7dd03de7acc756b53883df80e809a4ac3e313f849e98fdbc1`  
		Last Modified: Tue, 03 Jun 2025 20:57:34 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:261dc298ca8bb3e809b2fa84c845abe8fc4a133a3a6d81b41d5fa052f2e2d643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de804bb490ce73fbc139af75dd82c0b81800c69fecddde21775f3528a6d7c7f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562b8a11b8ed69d392bd2d9542980acf48db7b4527ff82479fb7de58d715714`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 6.4 MB (6363844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3005b967f68a27687c38d68520bdede8bff0aaf8a4c45416991973c3ceb4a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727afe280399541b9353f4c6fd9eeb040798b41369e880443022658368b70f8d`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c7bc8e0c9bf979f2e1a4b1c68db710249a14826eb638af9a1a90cf60a5860e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f605c808048d40222ff44f9f4fab194ef118bc38ba23cdbd2cb00b66d1f4a768`

```dockerfile
```

-	Layers:
	-	`sha256:8d1a85b4eba1b90277a6099a69d60e91db6dbe50ec0761e7e0713eaba4243490`  
		Last Modified: Tue, 03 Jun 2025 20:57:37 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c49785ef72f6851e19acd1effd844500de145fe8f8b60deb80f4b412acfd8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1c42fbe838dc45066f11b49b3a2b289f1e68ca79a337e2d37a8c9258a4d69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c60b436ca9be1cafae973b2673faaf38e3c6f55f8bcf1808f09815771e3688d`  
		Last Modified: Tue, 03 Jun 2025 20:58:00 GMT  
		Size: 6.4 MB (6351017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd3c878be8ff45a5224d95e5e15f26bbec36e0946930597d58789fb8b90cd85`  
		Last Modified: Tue, 03 Jun 2025 18:02:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde678942fe21a15ddffc4415cc8cdfea1b4ec957fbfddc20b2e769c8f24b887`  
		Last Modified: Tue, 03 Jun 2025 18:02:28 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:0e862f0aa96b7c561038da51377fdd552e6ad618d4148a8abcf19463c287e82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b404fa016eca9854ca662633cbbbed396ffd14707165264453f3887486787cf`

```dockerfile
```

-	Layers:
	-	`sha256:49b59c86b7347c12453d29446f15f08a34553aac5bde9dad6828b2cca678778f`  
		Last Modified: Tue, 03 Jun 2025 20:57:41 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:285a2a4cd223ee5a09948483638d63000a1012062bcecd10558588dcea57af68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1915225864493be141ed87c713508d93dc744b32d85e0c549444133809ac37a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988a5cc26a525b12202b4ede8dbadf7282232fa3202588c82228cc51312a2db`  
		Last Modified: Tue, 03 Jun 2025 18:12:34 GMT  
		Size: 6.1 MB (6145683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ed6725710b37dc92dbdc9beb40eddc4b06a58b847403c608550796d72c7430`  
		Last Modified: Tue, 03 Jun 2025 18:12:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3e1af6617ced1a84b929dfa36cc1aeefede7065ee2c580030f864336d30215`  
		Last Modified: Tue, 03 Jun 2025 18:12:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b58de4f1cc2ff62b12af617c5814335385fc4252143980d31ec8b385b8a0281a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b429f6e62c50bb7cc5184af5e6f318d09a3ca04b31430f71f3d35eaf9c080d52`

```dockerfile
```

-	Layers:
	-	`sha256:be4126cc80da8c7edb98f1b5a8da59348d702f75d87e8375559dbcaa9e628273`  
		Last Modified: Tue, 03 Jun 2025 20:57:45 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9c85f40d23ab0ee0d9ae30d532b565f8a86573f0300420151060cbedcef5e8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9856694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c32a0cc3e550a3e68b0856e8da573eacf0ab169da68dbdccf9b2689d5820d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4574fc8f9c31a7e7c3096b2295a13bb991034e66aaee26f0c8bb92f4965f89`  
		Last Modified: Tue, 03 Jun 2025 18:15:03 GMT  
		Size: 6.1 MB (6125536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26043e6e9cf09cbd98c4343bed49c94ad7825b33e6dc73d6aef9f860bca1f5f7`  
		Last Modified: Tue, 03 Jun 2025 18:11:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d10afb72d6f0cf76c7bb3528287bc589928122df027b23f8226d7c2926290`  
		Last Modified: Tue, 03 Jun 2025 18:11:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:946551fed6e10788bcccc2dddf5722a62178223fd200dd771430b848fdb40f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5564c58fcb5f6b52983f1f0b07658184fab57abaf366dfe4756655fff3c9c166`

```dockerfile
```

-	Layers:
	-	`sha256:c6b4252ac8a827db1eaae604fe622384be59f71e498988ad120c735b8870df72`  
		Last Modified: Tue, 03 Jun 2025 20:57:48 GMT  
		Size: 13.2 KB (13165 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:9b4247153f56677441a4087e2f007d554133f2b656c8e24c4e7f283e13775ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10131011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e1ab87078f53cf2d3de1cc3d84ffcb8a89160be9e97291e74e906c3f21208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeaa39221515ea4113a7177048180cf406a52328259a52ab2741589dbd942be`  
		Last Modified: Tue, 03 Jun 2025 18:09:14 GMT  
		Size: 6.5 MB (6482513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877186488f8186bc3fd5f22ae5055586ca7ba35d22bd8b44e183d8de602b7a86`  
		Last Modified: Tue, 03 Jun 2025 18:03:59 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d673d1efb6b2752e2fcace714fb45f3efb76e03432446c01c5926e0defc8dd`  
		Last Modified: Tue, 03 Jun 2025 18:04:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8271d38fc2c1db1251228a13e31422f50095cebc22fa791967b817d9fab8d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbbb56c5affc65c809913f0c2e71df3151bb57a4f1ec03a70ef0f217a8bc3f8`

```dockerfile
```

-	Layers:
	-	`sha256:0f8a134b43959c10be25f3307dfd04c7c345280c8d0f92932ddf07e454304b3b`  
		Last Modified: Tue, 03 Jun 2025 20:57:52 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-linux`

```console
$ docker pull nats@sha256:28edd413f190fb139ed600359da94e5a583e999dce2750488c75bef692250817
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
$ docker pull nats@sha256:f030f79672be88d009b75f61c2cb5fe9d07ad3364742a9b27cd60c9338ffafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4962b82a0ae69663e5a74740285899ca5957c69f6c53bf82311476aa1fae5ef8`
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
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5edca7674c56d6da9be7a373f78942e4c4aa5f175636ee35ccffba1533772e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3176d2028656537e4bfe7efebe9f8fcc985778a684370b2eff8c909b50c6f3`

```dockerfile
```

-	Layers:
	-	`sha256:5f2aca3d9450c14453dcb34e8c6b2a5a9a11673e6f7baeb3c28b7b435f2789d0`  
		Last Modified: Tue, 03 Jun 2025 20:57:19 GMT  
		Size: 8.7 KB (8710 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a72209661fa798f94ca59fe982425636af6df596e83cc2bdb1b1ebde04a57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f5ba25ee4d10359cc31039d1a9a05f150b96f797eb6ca7d155076fd547bb9`
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
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb3048cc57f790e44bb317519f7d61ce9e2d2cdcd7a57ac04cdf293bdd74a`  
		Last Modified: Tue, 03 Jun 2025 18:08:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9c3d54e7088aa0eb163c2eeb032e0d168126cdf0af77576fdc60ea726a70e690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8e6de48fcf449ba2519083b4bc5415c135d29db13e6c6b49b06eb5c5b766a1`

```dockerfile
```

-	Layers:
	-	`sha256:224e3a5982d8875c00e7bc85a73e0963da1394057839ae2fc9902d645dfd92ac`  
		Last Modified: Tue, 03 Jun 2025 20:57:22 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:0e599020477e9ff23b27b1865ecb60543ed1535464abc4e188798db623bf31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93191df559a8ac9ecaf2375c3c0650313c7cf85b7a5c1828496f963214a3b7a8`
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
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe6cace6dcb5e8d0b30a41e65b06eac2b2db46153d20610970774ad0c6ae658`  
		Last Modified: Tue, 03 Jun 2025 18:08:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:20322b26c9067df443a4c1d508864fa6c56d75e95c6f7b54af8aa64244c36523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f876797d7587f086738701ffc4137685187baf0e93a73bec7ca91ab37de8e2`

```dockerfile
```

-	Layers:
	-	`sha256:beb15a763ca188b107db77465e3fbd30750125d1abfcb5ce92acbb109fac9e12`  
		Last Modified: Tue, 03 Jun 2025 20:57:26 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:032295d595a30a6e02710d95f3b3371b26f67558194ac6e026d302bda83f82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2122a29fe765e930ef544b90d5626a1b68d149b8d8e01d11af499a44ad680e`
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
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebcf7fe8e5b3a56dc480f7baa83adbd38d2bbed924d023380166bd9981fd69`  
		Last Modified: Tue, 03 Jun 2025 18:23:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f18a5550f0cb7923ac9d1d849700acba1c8edb7aae430b47bab129cbd920c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59fba1c4b597d8c4c1f24f141dd0eb7e85a15f0bef993397327c84bc7dbc29`

```dockerfile
```

-	Layers:
	-	`sha256:b2f945ed0151cbf2eb4c531a81285a4227388550be1b38523fe42a95a739afba`  
		Last Modified: Tue, 03 Jun 2025 20:57:30 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:a1ee7f0765400218d94bcf05b108750a2c1d828a1ddc229520f68cd1a729772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce2215357ad2fb81086a7d81d51e879117d3d8e82b33a5594ad71cb42c9bd91`
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
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77e33529d308f759dde5ea0c2bc855d0fe710addc9b1ea041e795164831318`  
		Last Modified: Tue, 03 Jun 2025 18:22:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:458018497dd1f52d267442fa606155e76006f16995d106b8de40fab5ce15d07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e4beb2fa95e1452e4c3038fa80d0473aa25a3f0889c913e70dd71ab4adf9b4`

```dockerfile
```

-	Layers:
	-	`sha256:ab157204d16e4104829c5bb33652543a9248eea5ff2da1aa7f73be9a05e080d7`  
		Last Modified: Tue, 03 Jun 2025 20:57:33 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; s390x

```console
$ docker pull nats@sha256:d6cee6070c0808acf67782ea629ef2b095b877a064ef586239ad9d751fede448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5b2af2bb2f493ce23801f42d46661f10316f40ccd8f2c5fa91526f391f8845`
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
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63335d678adcf565f57b5c9a5020490b91f64dfcb434b646af92d61010878019`  
		Last Modified: Tue, 03 Jun 2025 18:09:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8d414aad040bcc21d6e5781cc4ef29badad9a7a3274a8a253ec0a84575ca6ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecca08806a2ed272df4613365d603a586113ca6a6aea54411b44f1d3b61d05`

```dockerfile
```

-	Layers:
	-	`sha256:d641a2c5f6581536130597650655cb4668997c123bb18fbf12c0cdab75476fac`  
		Last Modified: Tue, 03 Jun 2025 20:57:38 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-nanoserver`

```console
$ docker pull nats@sha256:48b0017ed68a04ae269efc31a050436377b22dcff094f7bcb8f0523d1d2ae263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.10.29-nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:fec67310cfde82241c2679a340f9fc9406516fb93c65a6d19cdbb4e9922ea1b7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128880529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c5ee3146bf8653ea930cfa655c44d0bc355630fddd92e0030c902f33dab838`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205bf2036fc00a819f1b20ae7e74f17c7c9a940bd0dd258616c46fb6e1760700`  
		Last Modified: Tue, 03 Jun 2025 18:13:01 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916bb5d7a2e9f16d1e2680557912b6c86f7e9ae2776dd6afbf2febca98dafcdb`  
		Last Modified: Tue, 03 Jun 2025 18:13:03 GMT  
		Size: 6.3 MB (6298082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a9c816e9f4737757e7ca952d1bd60161ba76a88543efd9351ed3ff255df401`  
		Last Modified: Tue, 03 Jun 2025 18:13:01 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6d81f9d4a7050f2769dadb14d5e17dec74f08d03be47023ffa8e84923d47c5`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd115dcb9313535536aaf899048ce8be8220c2386cc2ced9e4aa687915abed9`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5381b683b657bc05fc21206ec23dfe56d920b8488a2fff13da0650f8cde4c4`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:48b0017ed68a04ae269efc31a050436377b22dcff094f7bcb8f0523d1d2ae263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.10.29-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:fec67310cfde82241c2679a340f9fc9406516fb93c65a6d19cdbb4e9922ea1b7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128880529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c5ee3146bf8653ea930cfa655c44d0bc355630fddd92e0030c902f33dab838`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205bf2036fc00a819f1b20ae7e74f17c7c9a940bd0dd258616c46fb6e1760700`  
		Last Modified: Tue, 03 Jun 2025 18:13:01 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916bb5d7a2e9f16d1e2680557912b6c86f7e9ae2776dd6afbf2febca98dafcdb`  
		Last Modified: Tue, 03 Jun 2025 18:13:03 GMT  
		Size: 6.3 MB (6298082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a9c816e9f4737757e7ca952d1bd60161ba76a88543efd9351ed3ff255df401`  
		Last Modified: Tue, 03 Jun 2025 18:13:01 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6d81f9d4a7050f2769dadb14d5e17dec74f08d03be47023ffa8e84923d47c5`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd115dcb9313535536aaf899048ce8be8220c2386cc2ced9e4aa687915abed9`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5381b683b657bc05fc21206ec23dfe56d920b8488a2fff13da0650f8cde4c4`  
		Last Modified: Tue, 03 Jun 2025 18:13:02 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-scratch`

```console
$ docker pull nats@sha256:28edd413f190fb139ed600359da94e5a583e999dce2750488c75bef692250817
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
$ docker pull nats@sha256:f030f79672be88d009b75f61c2cb5fe9d07ad3364742a9b27cd60c9338ffafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4962b82a0ae69663e5a74740285899ca5957c69f6c53bf82311476aa1fae5ef8`
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
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5edca7674c56d6da9be7a373f78942e4c4aa5f175636ee35ccffba1533772e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3176d2028656537e4bfe7efebe9f8fcc985778a684370b2eff8c909b50c6f3`

```dockerfile
```

-	Layers:
	-	`sha256:5f2aca3d9450c14453dcb34e8c6b2a5a9a11673e6f7baeb3c28b7b435f2789d0`  
		Last Modified: Tue, 03 Jun 2025 20:57:19 GMT  
		Size: 8.7 KB (8710 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a72209661fa798f94ca59fe982425636af6df596e83cc2bdb1b1ebde04a57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f5ba25ee4d10359cc31039d1a9a05f150b96f797eb6ca7d155076fd547bb9`
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
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb3048cc57f790e44bb317519f7d61ce9e2d2cdcd7a57ac04cdf293bdd74a`  
		Last Modified: Tue, 03 Jun 2025 18:08:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9c3d54e7088aa0eb163c2eeb032e0d168126cdf0af77576fdc60ea726a70e690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8e6de48fcf449ba2519083b4bc5415c135d29db13e6c6b49b06eb5c5b766a1`

```dockerfile
```

-	Layers:
	-	`sha256:224e3a5982d8875c00e7bc85a73e0963da1394057839ae2fc9902d645dfd92ac`  
		Last Modified: Tue, 03 Jun 2025 20:57:22 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:0e599020477e9ff23b27b1865ecb60543ed1535464abc4e188798db623bf31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93191df559a8ac9ecaf2375c3c0650313c7cf85b7a5c1828496f963214a3b7a8`
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
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe6cace6dcb5e8d0b30a41e65b06eac2b2db46153d20610970774ad0c6ae658`  
		Last Modified: Tue, 03 Jun 2025 18:08:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:20322b26c9067df443a4c1d508864fa6c56d75e95c6f7b54af8aa64244c36523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f876797d7587f086738701ffc4137685187baf0e93a73bec7ca91ab37de8e2`

```dockerfile
```

-	Layers:
	-	`sha256:beb15a763ca188b107db77465e3fbd30750125d1abfcb5ce92acbb109fac9e12`  
		Last Modified: Tue, 03 Jun 2025 20:57:26 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:032295d595a30a6e02710d95f3b3371b26f67558194ac6e026d302bda83f82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2122a29fe765e930ef544b90d5626a1b68d149b8d8e01d11af499a44ad680e`
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
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebcf7fe8e5b3a56dc480f7baa83adbd38d2bbed924d023380166bd9981fd69`  
		Last Modified: Tue, 03 Jun 2025 18:23:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f18a5550f0cb7923ac9d1d849700acba1c8edb7aae430b47bab129cbd920c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59fba1c4b597d8c4c1f24f141dd0eb7e85a15f0bef993397327c84bc7dbc29`

```dockerfile
```

-	Layers:
	-	`sha256:b2f945ed0151cbf2eb4c531a81285a4227388550be1b38523fe42a95a739afba`  
		Last Modified: Tue, 03 Jun 2025 20:57:30 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:a1ee7f0765400218d94bcf05b108750a2c1d828a1ddc229520f68cd1a729772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce2215357ad2fb81086a7d81d51e879117d3d8e82b33a5594ad71cb42c9bd91`
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
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77e33529d308f759dde5ea0c2bc855d0fe710addc9b1ea041e795164831318`  
		Last Modified: Tue, 03 Jun 2025 18:22:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:458018497dd1f52d267442fa606155e76006f16995d106b8de40fab5ce15d07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e4beb2fa95e1452e4c3038fa80d0473aa25a3f0889c913e70dd71ab4adf9b4`

```dockerfile
```

-	Layers:
	-	`sha256:ab157204d16e4104829c5bb33652543a9248eea5ff2da1aa7f73be9a05e080d7`  
		Last Modified: Tue, 03 Jun 2025 20:57:33 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d6cee6070c0808acf67782ea629ef2b095b877a064ef586239ad9d751fede448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5b2af2bb2f493ce23801f42d46661f10316f40ccd8f2c5fa91526f391f8845`
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
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63335d678adcf565f57b5c9a5020490b91f64dfcb434b646af92d61010878019`  
		Last Modified: Tue, 03 Jun 2025 18:09:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8d414aad040bcc21d6e5781cc4ef29badad9a7a3274a8a253ec0a84575ca6ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecca08806a2ed272df4613365d603a586113ca6a6aea54411b44f1d3b61d05`

```dockerfile
```

-	Layers:
	-	`sha256:d641a2c5f6581536130597650655cb4668997c123bb18fbf12c0cdab75476fac`  
		Last Modified: Tue, 03 Jun 2025 20:57:38 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-windowsservercore`

```console
$ docker pull nats@sha256:c865099f6431bd38a81b1dbb4c1e9ffe23791ee675edf95df91ae4dd8e3b2d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.10.29-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:09c9d1f6ea65e8b31ef0f5e81c27201ed518b7cc60acc67baaed731ae31c6ed6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280616850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e217a8a9442b4e2c2d9393415d25664e6acf8e2cc04c38c0accc36e02722fd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 17:56:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 17:56:44 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 17:56:45 GMT
ENV NATS_SERVER=2.10.29
# Tue, 03 Jun 2025 17:56:46 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 03 Jun 2025 17:56:46 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 03 Jun 2025 17:58:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Jun 2025 17:58:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 03 Jun 2025 17:58:58 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 17:58:58 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 17:58:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 17:58:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def4758c7b3d08c0f41d6f89e5f9d9f47c4898d6b91fce49249cff24101ac2fa`  
		Last Modified: Tue, 03 Jun 2025 18:02:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573a0db2aab22a0ab2e42e79f1bdd724b33420879a2484800a9fb4c69bf2f283`  
		Last Modified: Tue, 03 Jun 2025 18:02:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0d3d0a876063591e1adc5bf4f932771eddfa0a07a0eb223319deec608b15af`  
		Last Modified: Tue, 03 Jun 2025 18:02:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9ce758cbca798812f754506e7cb5ec7b3273e48fb2fc8e231bfca20d6e0c2`  
		Last Modified: Tue, 03 Jun 2025 18:02:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60f9507f2022affa1a12862e2968b9074ee20390c52e8bcac51762955da4f14`  
		Last Modified: Tue, 03 Jun 2025 18:02:40 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0b9f9d9c2b6c5e9805f2da400483c60f081952b69adf0c37c0c93cae87a718`  
		Last Modified: Tue, 03 Jun 2025 18:02:44 GMT  
		Size: 356.2 KB (356225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75607bc528f29864e75cf56ffe65eda263723bcd1c8b9a20ab355bd9a268936`  
		Last Modified: Tue, 03 Jun 2025 18:08:47 GMT  
		Size: 6.6 MB (6620328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4157813c216e3a6b8bdae9418bfc16ff4c350221ea7dd44e04c6093b95265346`  
		Last Modified: Tue, 03 Jun 2025 18:02:50 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab1f981d7a518e35037d74347f18dc89d7e31959f3f9d495f8f942d2b4e2369`  
		Last Modified: Tue, 03 Jun 2025 18:02:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acdbd2270bd120ae6589ab16ce127edd53a810dbd23f72bc5d70b624ea5c526`  
		Last Modified: Tue, 03 Jun 2025 18:03:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b42133486ae606e623291120d1fe7928f904effcd2815c9dd547f2254a8817`  
		Last Modified: Tue, 03 Jun 2025 18:03:04 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:c865099f6431bd38a81b1dbb4c1e9ffe23791ee675edf95df91ae4dd8e3b2d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.10.29-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:09c9d1f6ea65e8b31ef0f5e81c27201ed518b7cc60acc67baaed731ae31c6ed6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280616850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e217a8a9442b4e2c2d9393415d25664e6acf8e2cc04c38c0accc36e02722fd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 17:56:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 17:56:44 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 17:56:45 GMT
ENV NATS_SERVER=2.10.29
# Tue, 03 Jun 2025 17:56:46 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 03 Jun 2025 17:56:46 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 03 Jun 2025 17:58:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Jun 2025 17:58:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 03 Jun 2025 17:58:58 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 17:58:58 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 17:58:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 17:58:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def4758c7b3d08c0f41d6f89e5f9d9f47c4898d6b91fce49249cff24101ac2fa`  
		Last Modified: Tue, 03 Jun 2025 18:02:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573a0db2aab22a0ab2e42e79f1bdd724b33420879a2484800a9fb4c69bf2f283`  
		Last Modified: Tue, 03 Jun 2025 18:02:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0d3d0a876063591e1adc5bf4f932771eddfa0a07a0eb223319deec608b15af`  
		Last Modified: Tue, 03 Jun 2025 18:02:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9ce758cbca798812f754506e7cb5ec7b3273e48fb2fc8e231bfca20d6e0c2`  
		Last Modified: Tue, 03 Jun 2025 18:02:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60f9507f2022affa1a12862e2968b9074ee20390c52e8bcac51762955da4f14`  
		Last Modified: Tue, 03 Jun 2025 18:02:40 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0b9f9d9c2b6c5e9805f2da400483c60f081952b69adf0c37c0c93cae87a718`  
		Last Modified: Tue, 03 Jun 2025 18:02:44 GMT  
		Size: 356.2 KB (356225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75607bc528f29864e75cf56ffe65eda263723bcd1c8b9a20ab355bd9a268936`  
		Last Modified: Tue, 03 Jun 2025 18:08:47 GMT  
		Size: 6.6 MB (6620328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4157813c216e3a6b8bdae9418bfc16ff4c350221ea7dd44e04c6093b95265346`  
		Last Modified: Tue, 03 Jun 2025 18:02:50 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab1f981d7a518e35037d74347f18dc89d7e31959f3f9d495f8f942d2b4e2369`  
		Last Modified: Tue, 03 Jun 2025 18:02:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acdbd2270bd120ae6589ab16ce127edd53a810dbd23f72bc5d70b624ea5c526`  
		Last Modified: Tue, 03 Jun 2025 18:03:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b42133486ae606e623291120d1fe7928f904effcd2815c9dd547f2254a8817`  
		Last Modified: Tue, 03 Jun 2025 18:03:04 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11`

```console
$ docker pull nats@sha256:57f45fba83001bfff519e918035305f02eb897a172f82d43933136e0f6aceb1e
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
	-	windows version 10.0.20348.3692; amd64

### `nats:2.11` - linux; amd64

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

### `nats:2.11` - unknown; unknown

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

### `nats:2.11` - linux; arm variant v6

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

### `nats:2.11` - unknown; unknown

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

### `nats:2.11` - linux; arm variant v7

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

### `nats:2.11` - unknown; unknown

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

### `nats:2.11` - linux; arm64 variant v8

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

### `nats:2.11` - unknown; unknown

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

### `nats:2.11` - linux; ppc64le

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

### `nats:2.11` - unknown; unknown

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

### `nats:2.11` - linux; s390x

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

### `nats:2.11` - unknown; unknown

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

### `nats:2.11` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:5809c0213e200dfdbe56a1d284162f75ce89533ee1eca342e2350fb4b8b384b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129076843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6294ddd46c444e866b505f0226f57df6864ce6cda1545be49e239c008bd011c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f7eba05352cc5df78a901d41dcb3733c4206eb7fd4625541f65326a30e8f`  
		Last Modified: Tue, 03 Jun 2025 18:16:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cf94e1df89f22d940ee5d9efd850e11abeb664ffa179e56c6b22e0dd772fb`  
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.5 MB (6494401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04a0b03d8f9056c543ef2f229fc65a83adff4f5d79e08cc2f95db65cc5da`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91fc443933d1e179f3b885096b15f1d6ac4b086b379a38766604c4ae3fc9bf`  
		Last Modified: Tue, 03 Jun 2025 18:17:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b6a66cc622766c3a994ba752f2a0b9973d6df193bb223dbb101c089689d8d`  
		Last Modified: Tue, 03 Jun 2025 20:57:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68e17b27bdb59114784659909c5bbec158528e884a87fa70e3357643d785c8`  
		Last Modified: Tue, 03 Jun 2025 18:17:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:b8d6a01568a7837d5186f948a3ebfae1bdf5a602268273b50704655982596b22
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
$ docker pull nats@sha256:69435fcc1356278c35dde2a3b3d9f2c4504f57b921d38612d36200a9c7b51067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10580056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e96d11240320c8d079058907e6b1a349c3c164f6d1057c7d4141b67803ef0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be8340a33b28b7069d77e81278e1150e46e62e5739a5ef524f3b10b6315d93`  
		Last Modified: Tue, 03 Jun 2025 18:08:18 GMT  
		Size: 6.8 MB (6782240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:770fc5b17c3e852bea98835c4f770de25350891225d2d5c48a17079cd2a87f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ece4f13433515ab3468766d0750908f38501255daea31da2aab9466abd8dd13`

```dockerfile
```

-	Layers:
	-	`sha256:993a3e77289857e49dcc0d82e8b0a4d01bf97fc1ac52f27adc1b6d9f46be3010`  
		Last Modified: Tue, 03 Jun 2025 20:56:48 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:cc02d2d98d5248ae02ac731a42436bcf7c257a2336cb6ccc18c0a0d33aca7425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10002162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7ffccb3eb9188263f6e9ee5ff6be0d88a00817e7d4a7a880ef153ff6b59861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3cdfa139575e7698957b4ff36ff5e3b9c98dcca74e89a001ef2062de4433d8`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 6.5 MB (6500264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3195bedba82c8298239740a21ea08ee0b417d4c68b4eb96b52ad6c083c2c920`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f93998e0b8d5c431d6f762091f25cb87996747747bf0554bc73c73a2f31e190`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cd850c5ec391a375d438c70b5cc24af732269f5631ab424afdb6f809d708e432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1f72e1e723af723f70095a15f2853df338bcc41fbb18fb2f275a71cf0c8c37`

```dockerfile
```

-	Layers:
	-	`sha256:c0a8dba6556e09db91573b8694623b3159599ceb566967dd357bf582cfdc908c`  
		Last Modified: Tue, 03 Jun 2025 20:56:52 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bd62d7bcee4a2e2d4e3fe84830bbd978a3027b81e7976b723cfce5c113824abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9708379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efdf790e38279933f555c5ef6b82e2fb30e6d8eb6e85274bb375c1c88aced7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c4277d4cc00a376afb142f8ea748e710d48f75eddcf7a2510c5a1e088857e2`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 6.5 MB (6488230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e94ae1fb6404d5eb4989cef0cc09a96573006b7bd7d4e7f7fbab996b9ce90c`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f107f5a32f8d0ab9f4a4a7746509690c6c4845a952c7df17aa5b2e4bc6e7a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:3191c0cbc6ea566ab41e82bdcfd3a1bcfe0757dc82b606a411fdb61d50858d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d3fb67fa07d336d64e774f94f1074d759291d6e8b14b2b24d0c144e3a1ea07`

```dockerfile
```

-	Layers:
	-	`sha256:52a7538138245df9dcdc747a5c3e46f172218df3092764925fdbc21fb2a58298`  
		Last Modified: Tue, 03 Jun 2025 20:56:55 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5dd5eb415f3c3b50eb6e637d9eab8c4ec5726e575550f46a0853226a8da6edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ae7761a85b9922c5be272284ee27fe32bfd3b1a78d3239e429792033c7ced6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6826d2797f1cf0f48d78d168877a33ef918811eaa7ee6146a8653f4218cf6e56`  
		Last Modified: Tue, 03 Jun 2025 18:23:10 GMT  
		Size: 6.3 MB (6271484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2ec423b14754303830aaf58d608bc667aab81252f2b170550982a6c4aee78`  
		Last Modified: Tue, 03 Jun 2025 18:12:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac99aa05c0616d567688e33499eacc91da2b7c79dd4b91fdc6bc363573dccd4`  
		Last Modified: Tue, 03 Jun 2025 18:12:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f57f8e16b74edcba83577e18c83f6c830b2de03df54acd64a65d88ab4b5f5ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6f8fff81a6020fdbd737e9dd518b019a3b205e35d387235d0339aec5b55092`

```dockerfile
```

-	Layers:
	-	`sha256:c61cb3463dab986b2ecb7f263eea6eff56bfdb0d4075df19122df210a8d0a062`  
		Last Modified: Tue, 03 Jun 2025 20:56:59 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:04f768ca98d273ca56dc14213654250fb52045b383bce5db0e58444c23697d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ee2cb1b02b4eeb2714421cdd6b2e9f5ba023f8e508c2b604861f33248ccfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66500e2c223c5a3f4777f4d7f4ffcec1ca21a34f687704db2a6d0e661fe0299`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 6.3 MB (6254211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198db56aeb51065eb35574df93180297f06ba8d180108a952be65d93fa4e7dd2`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df632b2ea33fceba251c68a32d3efed10d3b495018d7e16d1b256225dd38aef8`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a11e45d5ebc10e2f442f0730348545d2ec0f0645f0f047a39364c6073754d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872e45d8950ac438f1cc639d1fde3610446df42c33be57d2ce16b2eef0e02297`

```dockerfile
```

-	Layers:
	-	`sha256:b2fdd3426bf4664ed50234140c9c5e23667db50fb3545c6a3874643740ef5aaf`  
		Last Modified: Tue, 03 Jun 2025 20:57:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:081db236c5c2d779dcea7087bfea30c8252499477626f616458bb70b78054bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9772610e623e3eae3e2949e0e470f0755004398628ced20be8fe593671829030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c44dcd57da31d89c4bf6d887262bfc6e7136e1132734822ddb4586096692a0`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 6.6 MB (6619415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93bad89a83837b6afc8b1128b9f0d132c74ba14e1c7f52f407fbe775cb13a2`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ded513c6eb3a5fff1e0ab2d6ac1560515bbf0389375e4759c71a1b2c0b6e97`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b96db90bf17f90a65aaa3a6fa7ea4250df1f9ee0d9d13d52b7d3c8f926242340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e98ba8254d35c0c12076fa3f077b261896b884cb797b2b50e57f1f79bdaa45`

```dockerfile
```

-	Layers:
	-	`sha256:68ad3f417d73aacb9e3e3a8a3fbde0712715fd19f474e71d7f05c3507eeb168b`  
		Last Modified: Tue, 03 Jun 2025 20:57:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.22`

```console
$ docker pull nats@sha256:b8d6a01568a7837d5186f948a3ebfae1bdf5a602268273b50704655982596b22
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

### `nats:2.11-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:69435fcc1356278c35dde2a3b3d9f2c4504f57b921d38612d36200a9c7b51067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10580056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e96d11240320c8d079058907e6b1a349c3c164f6d1057c7d4141b67803ef0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be8340a33b28b7069d77e81278e1150e46e62e5739a5ef524f3b10b6315d93`  
		Last Modified: Tue, 03 Jun 2025 18:08:18 GMT  
		Size: 6.8 MB (6782240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:770fc5b17c3e852bea98835c4f770de25350891225d2d5c48a17079cd2a87f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ece4f13433515ab3468766d0750908f38501255daea31da2aab9466abd8dd13`

```dockerfile
```

-	Layers:
	-	`sha256:993a3e77289857e49dcc0d82e8b0a4d01bf97fc1ac52f27adc1b6d9f46be3010`  
		Last Modified: Tue, 03 Jun 2025 20:56:48 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:cc02d2d98d5248ae02ac731a42436bcf7c257a2336cb6ccc18c0a0d33aca7425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10002162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7ffccb3eb9188263f6e9ee5ff6be0d88a00817e7d4a7a880ef153ff6b59861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3cdfa139575e7698957b4ff36ff5e3b9c98dcca74e89a001ef2062de4433d8`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 6.5 MB (6500264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3195bedba82c8298239740a21ea08ee0b417d4c68b4eb96b52ad6c083c2c920`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f93998e0b8d5c431d6f762091f25cb87996747747bf0554bc73c73a2f31e190`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cd850c5ec391a375d438c70b5cc24af732269f5631ab424afdb6f809d708e432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1f72e1e723af723f70095a15f2853df338bcc41fbb18fb2f275a71cf0c8c37`

```dockerfile
```

-	Layers:
	-	`sha256:c0a8dba6556e09db91573b8694623b3159599ceb566967dd357bf582cfdc908c`  
		Last Modified: Tue, 03 Jun 2025 20:56:52 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bd62d7bcee4a2e2d4e3fe84830bbd978a3027b81e7976b723cfce5c113824abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9708379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efdf790e38279933f555c5ef6b82e2fb30e6d8eb6e85274bb375c1c88aced7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c4277d4cc00a376afb142f8ea748e710d48f75eddcf7a2510c5a1e088857e2`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 6.5 MB (6488230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e94ae1fb6404d5eb4989cef0cc09a96573006b7bd7d4e7f7fbab996b9ce90c`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f107f5a32f8d0ab9f4a4a7746509690c6c4845a952c7df17aa5b2e4bc6e7a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:3191c0cbc6ea566ab41e82bdcfd3a1bcfe0757dc82b606a411fdb61d50858d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d3fb67fa07d336d64e774f94f1074d759291d6e8b14b2b24d0c144e3a1ea07`

```dockerfile
```

-	Layers:
	-	`sha256:52a7538138245df9dcdc747a5c3e46f172218df3092764925fdbc21fb2a58298`  
		Last Modified: Tue, 03 Jun 2025 20:56:55 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5dd5eb415f3c3b50eb6e637d9eab8c4ec5726e575550f46a0853226a8da6edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ae7761a85b9922c5be272284ee27fe32bfd3b1a78d3239e429792033c7ced6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6826d2797f1cf0f48d78d168877a33ef918811eaa7ee6146a8653f4218cf6e56`  
		Last Modified: Tue, 03 Jun 2025 18:23:10 GMT  
		Size: 6.3 MB (6271484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2ec423b14754303830aaf58d608bc667aab81252f2b170550982a6c4aee78`  
		Last Modified: Tue, 03 Jun 2025 18:12:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac99aa05c0616d567688e33499eacc91da2b7c79dd4b91fdc6bc363573dccd4`  
		Last Modified: Tue, 03 Jun 2025 18:12:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f57f8e16b74edcba83577e18c83f6c830b2de03df54acd64a65d88ab4b5f5ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6f8fff81a6020fdbd737e9dd518b019a3b205e35d387235d0339aec5b55092`

```dockerfile
```

-	Layers:
	-	`sha256:c61cb3463dab986b2ecb7f263eea6eff56bfdb0d4075df19122df210a8d0a062`  
		Last Modified: Tue, 03 Jun 2025 20:56:59 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:04f768ca98d273ca56dc14213654250fb52045b383bce5db0e58444c23697d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ee2cb1b02b4eeb2714421cdd6b2e9f5ba023f8e508c2b604861f33248ccfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66500e2c223c5a3f4777f4d7f4ffcec1ca21a34f687704db2a6d0e661fe0299`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 6.3 MB (6254211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198db56aeb51065eb35574df93180297f06ba8d180108a952be65d93fa4e7dd2`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df632b2ea33fceba251c68a32d3efed10d3b495018d7e16d1b256225dd38aef8`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a11e45d5ebc10e2f442f0730348545d2ec0f0645f0f047a39364c6073754d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872e45d8950ac438f1cc639d1fde3610446df42c33be57d2ce16b2eef0e02297`

```dockerfile
```

-	Layers:
	-	`sha256:b2fdd3426bf4664ed50234140c9c5e23667db50fb3545c6a3874643740ef5aaf`  
		Last Modified: Tue, 03 Jun 2025 20:57:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:081db236c5c2d779dcea7087bfea30c8252499477626f616458bb70b78054bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9772610e623e3eae3e2949e0e470f0755004398628ced20be8fe593671829030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c44dcd57da31d89c4bf6d887262bfc6e7136e1132734822ddb4586096692a0`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 6.6 MB (6619415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93bad89a83837b6afc8b1128b9f0d132c74ba14e1c7f52f407fbe775cb13a2`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ded513c6eb3a5fff1e0ab2d6ac1560515bbf0389375e4759c71a1b2c0b6e97`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b96db90bf17f90a65aaa3a6fa7ea4250df1f9ee0d9d13d52b7d3c8f926242340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e98ba8254d35c0c12076fa3f077b261896b884cb797b2b50e57f1f79bdaa45`

```dockerfile
```

-	Layers:
	-	`sha256:68ad3f417d73aacb9e3e3a8a3fbde0712715fd19f474e71d7f05c3507eeb168b`  
		Last Modified: Tue, 03 Jun 2025 20:57:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

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

### `nats:2.11-linux` - linux; amd64

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

### `nats:2.11-linux` - unknown; unknown

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

### `nats:2.11-linux` - linux; arm variant v6

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

### `nats:2.11-linux` - unknown; unknown

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

### `nats:2.11-linux` - linux; arm variant v7

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

### `nats:2.11-linux` - unknown; unknown

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

### `nats:2.11-linux` - linux; arm64 variant v8

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

### `nats:2.11-linux` - unknown; unknown

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

### `nats:2.11-linux` - linux; ppc64le

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

### `nats:2.11-linux` - unknown; unknown

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

### `nats:2.11-linux` - linux; s390x

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

### `nats:2.11-linux` - unknown; unknown

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

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:ecc8389817ef21fb2d273b7fe6776b4de22f5f3da3033b00a69151c47e0215a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.11-nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:5809c0213e200dfdbe56a1d284162f75ce89533ee1eca342e2350fb4b8b384b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129076843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6294ddd46c444e866b505f0226f57df6864ce6cda1545be49e239c008bd011c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f7eba05352cc5df78a901d41dcb3733c4206eb7fd4625541f65326a30e8f`  
		Last Modified: Tue, 03 Jun 2025 18:16:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cf94e1df89f22d940ee5d9efd850e11abeb664ffa179e56c6b22e0dd772fb`  
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.5 MB (6494401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04a0b03d8f9056c543ef2f229fc65a83adff4f5d79e08cc2f95db65cc5da`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91fc443933d1e179f3b885096b15f1d6ac4b086b379a38766604c4ae3fc9bf`  
		Last Modified: Tue, 03 Jun 2025 18:17:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b6a66cc622766c3a994ba752f2a0b9973d6df193bb223dbb101c089689d8d`  
		Last Modified: Tue, 03 Jun 2025 20:57:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68e17b27bdb59114784659909c5bbec158528e884a87fa70e3357643d785c8`  
		Last Modified: Tue, 03 Jun 2025 18:17:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:ecc8389817ef21fb2d273b7fe6776b4de22f5f3da3033b00a69151c47e0215a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:5809c0213e200dfdbe56a1d284162f75ce89533ee1eca342e2350fb4b8b384b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129076843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6294ddd46c444e866b505f0226f57df6864ce6cda1545be49e239c008bd011c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f7eba05352cc5df78a901d41dcb3733c4206eb7fd4625541f65326a30e8f`  
		Last Modified: Tue, 03 Jun 2025 18:16:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cf94e1df89f22d940ee5d9efd850e11abeb664ffa179e56c6b22e0dd772fb`  
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.5 MB (6494401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04a0b03d8f9056c543ef2f229fc65a83adff4f5d79e08cc2f95db65cc5da`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91fc443933d1e179f3b885096b15f1d6ac4b086b379a38766604c4ae3fc9bf`  
		Last Modified: Tue, 03 Jun 2025 18:17:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b6a66cc622766c3a994ba752f2a0b9973d6df193bb223dbb101c089689d8d`  
		Last Modified: Tue, 03 Jun 2025 20:57:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68e17b27bdb59114784659909c5bbec158528e884a87fa70e3357643d785c8`  
		Last Modified: Tue, 03 Jun 2025 18:17:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

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

### `nats:2.11-scratch` - linux; amd64

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

### `nats:2.11-scratch` - unknown; unknown

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

### `nats:2.11-scratch` - linux; arm variant v6

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

### `nats:2.11-scratch` - unknown; unknown

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

### `nats:2.11-scratch` - linux; arm variant v7

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

### `nats:2.11-scratch` - unknown; unknown

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

### `nats:2.11-scratch` - linux; arm64 variant v8

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

### `nats:2.11-scratch` - unknown; unknown

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

### `nats:2.11-scratch` - linux; ppc64le

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

### `nats:2.11-scratch` - unknown; unknown

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

### `nats:2.11-scratch` - linux; s390x

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

### `nats:2.11-scratch` - unknown; unknown

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

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:6f8e77e1231fd3511353f2a8161af5ba6d11565d0d1ece50953a2f9a372d6bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:8317c827fa967bd9f550b8ce662f920ed01c012ca005f14021df3bf5118e4938
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280787628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9160d38e59cf418ea3321c716c7a5c123f40250e646f9a19e44a3d00825101c4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 17:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 17:56:57 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER=2.11.4
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Tue, 03 Jun 2025 17:56:59 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Tue, 03 Jun 2025 17:58:07 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Jun 2025 17:58:34 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 03 Jun 2025 17:58:34 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 17:58:35 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 17:58:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 17:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4b5081f22f0ce90ffb8a283bf6907184ca210d3fa64cc649c175c2403bf48`  
		Last Modified: Tue, 03 Jun 2025 17:59:03 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd1a53f2b89b85d5c147edcb69400d431d2aae95f09eb51615e21d71868b20`  
		Last Modified: Tue, 03 Jun 2025 17:59:04 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05e4d6ed3ee536d39ce8a0564d98ec9fb2830b9aea712e135ef717a9034b58d`  
		Last Modified: Tue, 03 Jun 2025 17:59:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd5804ef666b2af87854e3e84e8513832d69895027327d5563934968d65bfc`  
		Last Modified: Tue, 03 Jun 2025 17:59:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfe49f5d913195c31fdfeae7a261be6ef51da43fb44d9fca4e428ba78fa6064`  
		Last Modified: Tue, 03 Jun 2025 17:59:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af20b8c738d9d92e83bc0e0e5c9b813668bb6deca62e90327f3bff9bac141d0`  
		Last Modified: Tue, 03 Jun 2025 17:59:09 GMT  
		Size: 342.9 KB (342923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9dd708b6fd0131af1f9ae1c1001cf8966b8f9b27bcdd0d022586b3a8489327`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 6.8 MB (6804324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423519a4e3a5a29f15c70595333fab0a6f79736ff478e5e3d66fb7481741151f`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe4b134972dcd390001fc9744ccffb8da5627e4fa055f6fe84918e65df4782d`  
		Last Modified: Tue, 03 Jun 2025 17:59:12 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb328b3dfd00b76b936d43d8a04426cb93cab24be8d294245da02c20ea2df6`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f933a18bfe02980983b3a438f0f485afe7c6592e98c09eb78891959f057c3a55`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:6f8e77e1231fd3511353f2a8161af5ba6d11565d0d1ece50953a2f9a372d6bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:8317c827fa967bd9f550b8ce662f920ed01c012ca005f14021df3bf5118e4938
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280787628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9160d38e59cf418ea3321c716c7a5c123f40250e646f9a19e44a3d00825101c4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 17:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 17:56:57 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER=2.11.4
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Tue, 03 Jun 2025 17:56:59 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Tue, 03 Jun 2025 17:58:07 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Jun 2025 17:58:34 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 03 Jun 2025 17:58:34 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 17:58:35 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 17:58:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 17:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4b5081f22f0ce90ffb8a283bf6907184ca210d3fa64cc649c175c2403bf48`  
		Last Modified: Tue, 03 Jun 2025 17:59:03 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd1a53f2b89b85d5c147edcb69400d431d2aae95f09eb51615e21d71868b20`  
		Last Modified: Tue, 03 Jun 2025 17:59:04 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05e4d6ed3ee536d39ce8a0564d98ec9fb2830b9aea712e135ef717a9034b58d`  
		Last Modified: Tue, 03 Jun 2025 17:59:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd5804ef666b2af87854e3e84e8513832d69895027327d5563934968d65bfc`  
		Last Modified: Tue, 03 Jun 2025 17:59:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfe49f5d913195c31fdfeae7a261be6ef51da43fb44d9fca4e428ba78fa6064`  
		Last Modified: Tue, 03 Jun 2025 17:59:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af20b8c738d9d92e83bc0e0e5c9b813668bb6deca62e90327f3bff9bac141d0`  
		Last Modified: Tue, 03 Jun 2025 17:59:09 GMT  
		Size: 342.9 KB (342923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9dd708b6fd0131af1f9ae1c1001cf8966b8f9b27bcdd0d022586b3a8489327`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 6.8 MB (6804324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423519a4e3a5a29f15c70595333fab0a6f79736ff478e5e3d66fb7481741151f`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe4b134972dcd390001fc9744ccffb8da5627e4fa055f6fe84918e65df4782d`  
		Last Modified: Tue, 03 Jun 2025 17:59:12 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb328b3dfd00b76b936d43d8a04426cb93cab24be8d294245da02c20ea2df6`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f933a18bfe02980983b3a438f0f485afe7c6592e98c09eb78891959f057c3a55`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.4`

```console
$ docker pull nats@sha256:57f45fba83001bfff519e918035305f02eb897a172f82d43933136e0f6aceb1e
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
	-	windows version 10.0.20348.3692; amd64

### `nats:2.11.4` - linux; amd64

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

### `nats:2.11.4` - unknown; unknown

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

### `nats:2.11.4` - linux; arm variant v6

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

### `nats:2.11.4` - unknown; unknown

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

### `nats:2.11.4` - linux; arm variant v7

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

### `nats:2.11.4` - unknown; unknown

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

### `nats:2.11.4` - linux; arm64 variant v8

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

### `nats:2.11.4` - unknown; unknown

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

### `nats:2.11.4` - linux; ppc64le

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

### `nats:2.11.4` - unknown; unknown

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

### `nats:2.11.4` - linux; s390x

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

### `nats:2.11.4` - unknown; unknown

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

### `nats:2.11.4` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:5809c0213e200dfdbe56a1d284162f75ce89533ee1eca342e2350fb4b8b384b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129076843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6294ddd46c444e866b505f0226f57df6864ce6cda1545be49e239c008bd011c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f7eba05352cc5df78a901d41dcb3733c4206eb7fd4625541f65326a30e8f`  
		Last Modified: Tue, 03 Jun 2025 18:16:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cf94e1df89f22d940ee5d9efd850e11abeb664ffa179e56c6b22e0dd772fb`  
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.5 MB (6494401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04a0b03d8f9056c543ef2f229fc65a83adff4f5d79e08cc2f95db65cc5da`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91fc443933d1e179f3b885096b15f1d6ac4b086b379a38766604c4ae3fc9bf`  
		Last Modified: Tue, 03 Jun 2025 18:17:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b6a66cc622766c3a994ba752f2a0b9973d6df193bb223dbb101c089689d8d`  
		Last Modified: Tue, 03 Jun 2025 20:57:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68e17b27bdb59114784659909c5bbec158528e884a87fa70e3357643d785c8`  
		Last Modified: Tue, 03 Jun 2025 18:17:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.4-alpine`

```console
$ docker pull nats@sha256:b8d6a01568a7837d5186f948a3ebfae1bdf5a602268273b50704655982596b22
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
$ docker pull nats@sha256:69435fcc1356278c35dde2a3b3d9f2c4504f57b921d38612d36200a9c7b51067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10580056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e96d11240320c8d079058907e6b1a349c3c164f6d1057c7d4141b67803ef0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be8340a33b28b7069d77e81278e1150e46e62e5739a5ef524f3b10b6315d93`  
		Last Modified: Tue, 03 Jun 2025 18:08:18 GMT  
		Size: 6.8 MB (6782240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:770fc5b17c3e852bea98835c4f770de25350891225d2d5c48a17079cd2a87f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ece4f13433515ab3468766d0750908f38501255daea31da2aab9466abd8dd13`

```dockerfile
```

-	Layers:
	-	`sha256:993a3e77289857e49dcc0d82e8b0a4d01bf97fc1ac52f27adc1b6d9f46be3010`  
		Last Modified: Tue, 03 Jun 2025 20:56:48 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:cc02d2d98d5248ae02ac731a42436bcf7c257a2336cb6ccc18c0a0d33aca7425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10002162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7ffccb3eb9188263f6e9ee5ff6be0d88a00817e7d4a7a880ef153ff6b59861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3cdfa139575e7698957b4ff36ff5e3b9c98dcca74e89a001ef2062de4433d8`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 6.5 MB (6500264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3195bedba82c8298239740a21ea08ee0b417d4c68b4eb96b52ad6c083c2c920`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f93998e0b8d5c431d6f762091f25cb87996747747bf0554bc73c73a2f31e190`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cd850c5ec391a375d438c70b5cc24af732269f5631ab424afdb6f809d708e432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1f72e1e723af723f70095a15f2853df338bcc41fbb18fb2f275a71cf0c8c37`

```dockerfile
```

-	Layers:
	-	`sha256:c0a8dba6556e09db91573b8694623b3159599ceb566967dd357bf582cfdc908c`  
		Last Modified: Tue, 03 Jun 2025 20:56:52 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bd62d7bcee4a2e2d4e3fe84830bbd978a3027b81e7976b723cfce5c113824abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9708379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efdf790e38279933f555c5ef6b82e2fb30e6d8eb6e85274bb375c1c88aced7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c4277d4cc00a376afb142f8ea748e710d48f75eddcf7a2510c5a1e088857e2`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 6.5 MB (6488230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e94ae1fb6404d5eb4989cef0cc09a96573006b7bd7d4e7f7fbab996b9ce90c`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f107f5a32f8d0ab9f4a4a7746509690c6c4845a952c7df17aa5b2e4bc6e7a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:3191c0cbc6ea566ab41e82bdcfd3a1bcfe0757dc82b606a411fdb61d50858d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d3fb67fa07d336d64e774f94f1074d759291d6e8b14b2b24d0c144e3a1ea07`

```dockerfile
```

-	Layers:
	-	`sha256:52a7538138245df9dcdc747a5c3e46f172218df3092764925fdbc21fb2a58298`  
		Last Modified: Tue, 03 Jun 2025 20:56:55 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5dd5eb415f3c3b50eb6e637d9eab8c4ec5726e575550f46a0853226a8da6edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ae7761a85b9922c5be272284ee27fe32bfd3b1a78d3239e429792033c7ced6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6826d2797f1cf0f48d78d168877a33ef918811eaa7ee6146a8653f4218cf6e56`  
		Last Modified: Tue, 03 Jun 2025 18:23:10 GMT  
		Size: 6.3 MB (6271484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2ec423b14754303830aaf58d608bc667aab81252f2b170550982a6c4aee78`  
		Last Modified: Tue, 03 Jun 2025 18:12:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac99aa05c0616d567688e33499eacc91da2b7c79dd4b91fdc6bc363573dccd4`  
		Last Modified: Tue, 03 Jun 2025 18:12:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f57f8e16b74edcba83577e18c83f6c830b2de03df54acd64a65d88ab4b5f5ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6f8fff81a6020fdbd737e9dd518b019a3b205e35d387235d0339aec5b55092`

```dockerfile
```

-	Layers:
	-	`sha256:c61cb3463dab986b2ecb7f263eea6eff56bfdb0d4075df19122df210a8d0a062`  
		Last Modified: Tue, 03 Jun 2025 20:56:59 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:04f768ca98d273ca56dc14213654250fb52045b383bce5db0e58444c23697d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ee2cb1b02b4eeb2714421cdd6b2e9f5ba023f8e508c2b604861f33248ccfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66500e2c223c5a3f4777f4d7f4ffcec1ca21a34f687704db2a6d0e661fe0299`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 6.3 MB (6254211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198db56aeb51065eb35574df93180297f06ba8d180108a952be65d93fa4e7dd2`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df632b2ea33fceba251c68a32d3efed10d3b495018d7e16d1b256225dd38aef8`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a11e45d5ebc10e2f442f0730348545d2ec0f0645f0f047a39364c6073754d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872e45d8950ac438f1cc639d1fde3610446df42c33be57d2ce16b2eef0e02297`

```dockerfile
```

-	Layers:
	-	`sha256:b2fdd3426bf4664ed50234140c9c5e23667db50fb3545c6a3874643740ef5aaf`  
		Last Modified: Tue, 03 Jun 2025 20:57:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine` - linux; s390x

```console
$ docker pull nats@sha256:081db236c5c2d779dcea7087bfea30c8252499477626f616458bb70b78054bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9772610e623e3eae3e2949e0e470f0755004398628ced20be8fe593671829030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c44dcd57da31d89c4bf6d887262bfc6e7136e1132734822ddb4586096692a0`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 6.6 MB (6619415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93bad89a83837b6afc8b1128b9f0d132c74ba14e1c7f52f407fbe775cb13a2`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ded513c6eb3a5fff1e0ab2d6ac1560515bbf0389375e4759c71a1b2c0b6e97`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b96db90bf17f90a65aaa3a6fa7ea4250df1f9ee0d9d13d52b7d3c8f926242340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e98ba8254d35c0c12076fa3f077b261896b884cb797b2b50e57f1f79bdaa45`

```dockerfile
```

-	Layers:
	-	`sha256:68ad3f417d73aacb9e3e3a8a3fbde0712715fd19f474e71d7f05c3507eeb168b`  
		Last Modified: Tue, 03 Jun 2025 20:57:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.4-alpine3.22`

```console
$ docker pull nats@sha256:b8d6a01568a7837d5186f948a3ebfae1bdf5a602268273b50704655982596b22
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

### `nats:2.11.4-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:69435fcc1356278c35dde2a3b3d9f2c4504f57b921d38612d36200a9c7b51067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10580056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e96d11240320c8d079058907e6b1a349c3c164f6d1057c7d4141b67803ef0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be8340a33b28b7069d77e81278e1150e46e62e5739a5ef524f3b10b6315d93`  
		Last Modified: Tue, 03 Jun 2025 18:08:18 GMT  
		Size: 6.8 MB (6782240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:770fc5b17c3e852bea98835c4f770de25350891225d2d5c48a17079cd2a87f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ece4f13433515ab3468766d0750908f38501255daea31da2aab9466abd8dd13`

```dockerfile
```

-	Layers:
	-	`sha256:993a3e77289857e49dcc0d82e8b0a4d01bf97fc1ac52f27adc1b6d9f46be3010`  
		Last Modified: Tue, 03 Jun 2025 20:56:48 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:cc02d2d98d5248ae02ac731a42436bcf7c257a2336cb6ccc18c0a0d33aca7425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10002162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7ffccb3eb9188263f6e9ee5ff6be0d88a00817e7d4a7a880ef153ff6b59861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3cdfa139575e7698957b4ff36ff5e3b9c98dcca74e89a001ef2062de4433d8`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 6.5 MB (6500264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3195bedba82c8298239740a21ea08ee0b417d4c68b4eb96b52ad6c083c2c920`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f93998e0b8d5c431d6f762091f25cb87996747747bf0554bc73c73a2f31e190`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cd850c5ec391a375d438c70b5cc24af732269f5631ab424afdb6f809d708e432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1f72e1e723af723f70095a15f2853df338bcc41fbb18fb2f275a71cf0c8c37`

```dockerfile
```

-	Layers:
	-	`sha256:c0a8dba6556e09db91573b8694623b3159599ceb566967dd357bf582cfdc908c`  
		Last Modified: Tue, 03 Jun 2025 20:56:52 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bd62d7bcee4a2e2d4e3fe84830bbd978a3027b81e7976b723cfce5c113824abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9708379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efdf790e38279933f555c5ef6b82e2fb30e6d8eb6e85274bb375c1c88aced7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c4277d4cc00a376afb142f8ea748e710d48f75eddcf7a2510c5a1e088857e2`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 6.5 MB (6488230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e94ae1fb6404d5eb4989cef0cc09a96573006b7bd7d4e7f7fbab996b9ce90c`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f107f5a32f8d0ab9f4a4a7746509690c6c4845a952c7df17aa5b2e4bc6e7a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:3191c0cbc6ea566ab41e82bdcfd3a1bcfe0757dc82b606a411fdb61d50858d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d3fb67fa07d336d64e774f94f1074d759291d6e8b14b2b24d0c144e3a1ea07`

```dockerfile
```

-	Layers:
	-	`sha256:52a7538138245df9dcdc747a5c3e46f172218df3092764925fdbc21fb2a58298`  
		Last Modified: Tue, 03 Jun 2025 20:56:55 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5dd5eb415f3c3b50eb6e637d9eab8c4ec5726e575550f46a0853226a8da6edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ae7761a85b9922c5be272284ee27fe32bfd3b1a78d3239e429792033c7ced6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6826d2797f1cf0f48d78d168877a33ef918811eaa7ee6146a8653f4218cf6e56`  
		Last Modified: Tue, 03 Jun 2025 18:23:10 GMT  
		Size: 6.3 MB (6271484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2ec423b14754303830aaf58d608bc667aab81252f2b170550982a6c4aee78`  
		Last Modified: Tue, 03 Jun 2025 18:12:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac99aa05c0616d567688e33499eacc91da2b7c79dd4b91fdc6bc363573dccd4`  
		Last Modified: Tue, 03 Jun 2025 18:12:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f57f8e16b74edcba83577e18c83f6c830b2de03df54acd64a65d88ab4b5f5ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6f8fff81a6020fdbd737e9dd518b019a3b205e35d387235d0339aec5b55092`

```dockerfile
```

-	Layers:
	-	`sha256:c61cb3463dab986b2ecb7f263eea6eff56bfdb0d4075df19122df210a8d0a062`  
		Last Modified: Tue, 03 Jun 2025 20:56:59 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:04f768ca98d273ca56dc14213654250fb52045b383bce5db0e58444c23697d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ee2cb1b02b4eeb2714421cdd6b2e9f5ba023f8e508c2b604861f33248ccfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66500e2c223c5a3f4777f4d7f4ffcec1ca21a34f687704db2a6d0e661fe0299`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 6.3 MB (6254211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198db56aeb51065eb35574df93180297f06ba8d180108a952be65d93fa4e7dd2`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df632b2ea33fceba251c68a32d3efed10d3b495018d7e16d1b256225dd38aef8`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a11e45d5ebc10e2f442f0730348545d2ec0f0645f0f047a39364c6073754d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872e45d8950ac438f1cc639d1fde3610446df42c33be57d2ce16b2eef0e02297`

```dockerfile
```

-	Layers:
	-	`sha256:b2fdd3426bf4664ed50234140c9c5e23667db50fb3545c6a3874643740ef5aaf`  
		Last Modified: Tue, 03 Jun 2025 20:57:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.4-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:081db236c5c2d779dcea7087bfea30c8252499477626f616458bb70b78054bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9772610e623e3eae3e2949e0e470f0755004398628ced20be8fe593671829030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c44dcd57da31d89c4bf6d887262bfc6e7136e1132734822ddb4586096692a0`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 6.6 MB (6619415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93bad89a83837b6afc8b1128b9f0d132c74ba14e1c7f52f407fbe775cb13a2`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ded513c6eb3a5fff1e0ab2d6ac1560515bbf0389375e4759c71a1b2c0b6e97`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.4-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b96db90bf17f90a65aaa3a6fa7ea4250df1f9ee0d9d13d52b7d3c8f926242340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e98ba8254d35c0c12076fa3f077b261896b884cb797b2b50e57f1f79bdaa45`

```dockerfile
```

-	Layers:
	-	`sha256:68ad3f417d73aacb9e3e3a8a3fbde0712715fd19f474e71d7f05c3507eeb168b`  
		Last Modified: Tue, 03 Jun 2025 20:57:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.4-linux`

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

### `nats:2.11.4-linux` - linux; amd64

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

### `nats:2.11.4-linux` - unknown; unknown

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

### `nats:2.11.4-linux` - linux; arm variant v6

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

### `nats:2.11.4-linux` - unknown; unknown

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

### `nats:2.11.4-linux` - linux; arm variant v7

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

### `nats:2.11.4-linux` - unknown; unknown

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

### `nats:2.11.4-linux` - linux; arm64 variant v8

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

### `nats:2.11.4-linux` - unknown; unknown

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

### `nats:2.11.4-linux` - linux; ppc64le

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

### `nats:2.11.4-linux` - unknown; unknown

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

### `nats:2.11.4-linux` - linux; s390x

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

### `nats:2.11.4-linux` - unknown; unknown

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

## `nats:2.11.4-nanoserver`

```console
$ docker pull nats@sha256:ecc8389817ef21fb2d273b7fe6776b4de22f5f3da3033b00a69151c47e0215a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.11.4-nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:5809c0213e200dfdbe56a1d284162f75ce89533ee1eca342e2350fb4b8b384b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129076843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6294ddd46c444e866b505f0226f57df6864ce6cda1545be49e239c008bd011c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f7eba05352cc5df78a901d41dcb3733c4206eb7fd4625541f65326a30e8f`  
		Last Modified: Tue, 03 Jun 2025 18:16:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cf94e1df89f22d940ee5d9efd850e11abeb664ffa179e56c6b22e0dd772fb`  
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.5 MB (6494401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04a0b03d8f9056c543ef2f229fc65a83adff4f5d79e08cc2f95db65cc5da`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91fc443933d1e179f3b885096b15f1d6ac4b086b379a38766604c4ae3fc9bf`  
		Last Modified: Tue, 03 Jun 2025 18:17:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b6a66cc622766c3a994ba752f2a0b9973d6df193bb223dbb101c089689d8d`  
		Last Modified: Tue, 03 Jun 2025 20:57:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68e17b27bdb59114784659909c5bbec158528e884a87fa70e3357643d785c8`  
		Last Modified: Tue, 03 Jun 2025 18:17:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.4-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:ecc8389817ef21fb2d273b7fe6776b4de22f5f3da3033b00a69151c47e0215a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.11.4-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:5809c0213e200dfdbe56a1d284162f75ce89533ee1eca342e2350fb4b8b384b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129076843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6294ddd46c444e866b505f0226f57df6864ce6cda1545be49e239c008bd011c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f7eba05352cc5df78a901d41dcb3733c4206eb7fd4625541f65326a30e8f`  
		Last Modified: Tue, 03 Jun 2025 18:16:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cf94e1df89f22d940ee5d9efd850e11abeb664ffa179e56c6b22e0dd772fb`  
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.5 MB (6494401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04a0b03d8f9056c543ef2f229fc65a83adff4f5d79e08cc2f95db65cc5da`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91fc443933d1e179f3b885096b15f1d6ac4b086b379a38766604c4ae3fc9bf`  
		Last Modified: Tue, 03 Jun 2025 18:17:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b6a66cc622766c3a994ba752f2a0b9973d6df193bb223dbb101c089689d8d`  
		Last Modified: Tue, 03 Jun 2025 20:57:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68e17b27bdb59114784659909c5bbec158528e884a87fa70e3357643d785c8`  
		Last Modified: Tue, 03 Jun 2025 18:17:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.4-scratch`

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

### `nats:2.11.4-scratch` - linux; amd64

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

### `nats:2.11.4-scratch` - unknown; unknown

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

### `nats:2.11.4-scratch` - linux; arm variant v6

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

### `nats:2.11.4-scratch` - unknown; unknown

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

### `nats:2.11.4-scratch` - linux; arm variant v7

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

### `nats:2.11.4-scratch` - unknown; unknown

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

### `nats:2.11.4-scratch` - linux; arm64 variant v8

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

### `nats:2.11.4-scratch` - unknown; unknown

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

### `nats:2.11.4-scratch` - linux; ppc64le

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

### `nats:2.11.4-scratch` - unknown; unknown

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

### `nats:2.11.4-scratch` - linux; s390x

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

### `nats:2.11.4-scratch` - unknown; unknown

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

## `nats:2.11.4-windowsservercore`

```console
$ docker pull nats@sha256:6f8e77e1231fd3511353f2a8161af5ba6d11565d0d1ece50953a2f9a372d6bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.11.4-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:8317c827fa967bd9f550b8ce662f920ed01c012ca005f14021df3bf5118e4938
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280787628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9160d38e59cf418ea3321c716c7a5c123f40250e646f9a19e44a3d00825101c4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 17:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 17:56:57 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER=2.11.4
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Tue, 03 Jun 2025 17:56:59 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Tue, 03 Jun 2025 17:58:07 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Jun 2025 17:58:34 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 03 Jun 2025 17:58:34 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 17:58:35 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 17:58:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 17:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4b5081f22f0ce90ffb8a283bf6907184ca210d3fa64cc649c175c2403bf48`  
		Last Modified: Tue, 03 Jun 2025 17:59:03 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd1a53f2b89b85d5c147edcb69400d431d2aae95f09eb51615e21d71868b20`  
		Last Modified: Tue, 03 Jun 2025 17:59:04 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05e4d6ed3ee536d39ce8a0564d98ec9fb2830b9aea712e135ef717a9034b58d`  
		Last Modified: Tue, 03 Jun 2025 17:59:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd5804ef666b2af87854e3e84e8513832d69895027327d5563934968d65bfc`  
		Last Modified: Tue, 03 Jun 2025 17:59:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfe49f5d913195c31fdfeae7a261be6ef51da43fb44d9fca4e428ba78fa6064`  
		Last Modified: Tue, 03 Jun 2025 17:59:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af20b8c738d9d92e83bc0e0e5c9b813668bb6deca62e90327f3bff9bac141d0`  
		Last Modified: Tue, 03 Jun 2025 17:59:09 GMT  
		Size: 342.9 KB (342923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9dd708b6fd0131af1f9ae1c1001cf8966b8f9b27bcdd0d022586b3a8489327`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 6.8 MB (6804324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423519a4e3a5a29f15c70595333fab0a6f79736ff478e5e3d66fb7481741151f`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe4b134972dcd390001fc9744ccffb8da5627e4fa055f6fe84918e65df4782d`  
		Last Modified: Tue, 03 Jun 2025 17:59:12 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb328b3dfd00b76b936d43d8a04426cb93cab24be8d294245da02c20ea2df6`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f933a18bfe02980983b3a438f0f485afe7c6592e98c09eb78891959f057c3a55`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.4-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:6f8e77e1231fd3511353f2a8161af5ba6d11565d0d1ece50953a2f9a372d6bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:2.11.4-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:8317c827fa967bd9f550b8ce662f920ed01c012ca005f14021df3bf5118e4938
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280787628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9160d38e59cf418ea3321c716c7a5c123f40250e646f9a19e44a3d00825101c4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 17:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 17:56:57 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER=2.11.4
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Tue, 03 Jun 2025 17:56:59 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Tue, 03 Jun 2025 17:58:07 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Jun 2025 17:58:34 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 03 Jun 2025 17:58:34 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 17:58:35 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 17:58:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 17:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4b5081f22f0ce90ffb8a283bf6907184ca210d3fa64cc649c175c2403bf48`  
		Last Modified: Tue, 03 Jun 2025 17:59:03 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd1a53f2b89b85d5c147edcb69400d431d2aae95f09eb51615e21d71868b20`  
		Last Modified: Tue, 03 Jun 2025 17:59:04 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05e4d6ed3ee536d39ce8a0564d98ec9fb2830b9aea712e135ef717a9034b58d`  
		Last Modified: Tue, 03 Jun 2025 17:59:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd5804ef666b2af87854e3e84e8513832d69895027327d5563934968d65bfc`  
		Last Modified: Tue, 03 Jun 2025 17:59:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfe49f5d913195c31fdfeae7a261be6ef51da43fb44d9fca4e428ba78fa6064`  
		Last Modified: Tue, 03 Jun 2025 17:59:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af20b8c738d9d92e83bc0e0e5c9b813668bb6deca62e90327f3bff9bac141d0`  
		Last Modified: Tue, 03 Jun 2025 17:59:09 GMT  
		Size: 342.9 KB (342923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9dd708b6fd0131af1f9ae1c1001cf8966b8f9b27bcdd0d022586b3a8489327`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 6.8 MB (6804324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423519a4e3a5a29f15c70595333fab0a6f79736ff478e5e3d66fb7481741151f`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe4b134972dcd390001fc9744ccffb8da5627e4fa055f6fe84918e65df4782d`  
		Last Modified: Tue, 03 Jun 2025 17:59:12 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb328b3dfd00b76b936d43d8a04426cb93cab24be8d294245da02c20ea2df6`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f933a18bfe02980983b3a438f0f485afe7c6592e98c09eb78891959f057c3a55`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:b8d6a01568a7837d5186f948a3ebfae1bdf5a602268273b50704655982596b22
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
$ docker pull nats@sha256:69435fcc1356278c35dde2a3b3d9f2c4504f57b921d38612d36200a9c7b51067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10580056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e96d11240320c8d079058907e6b1a349c3c164f6d1057c7d4141b67803ef0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be8340a33b28b7069d77e81278e1150e46e62e5739a5ef524f3b10b6315d93`  
		Last Modified: Tue, 03 Jun 2025 18:08:18 GMT  
		Size: 6.8 MB (6782240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:770fc5b17c3e852bea98835c4f770de25350891225d2d5c48a17079cd2a87f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ece4f13433515ab3468766d0750908f38501255daea31da2aab9466abd8dd13`

```dockerfile
```

-	Layers:
	-	`sha256:993a3e77289857e49dcc0d82e8b0a4d01bf97fc1ac52f27adc1b6d9f46be3010`  
		Last Modified: Tue, 03 Jun 2025 20:56:48 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:cc02d2d98d5248ae02ac731a42436bcf7c257a2336cb6ccc18c0a0d33aca7425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10002162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7ffccb3eb9188263f6e9ee5ff6be0d88a00817e7d4a7a880ef153ff6b59861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3cdfa139575e7698957b4ff36ff5e3b9c98dcca74e89a001ef2062de4433d8`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 6.5 MB (6500264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3195bedba82c8298239740a21ea08ee0b417d4c68b4eb96b52ad6c083c2c920`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f93998e0b8d5c431d6f762091f25cb87996747747bf0554bc73c73a2f31e190`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cd850c5ec391a375d438c70b5cc24af732269f5631ab424afdb6f809d708e432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1f72e1e723af723f70095a15f2853df338bcc41fbb18fb2f275a71cf0c8c37`

```dockerfile
```

-	Layers:
	-	`sha256:c0a8dba6556e09db91573b8694623b3159599ceb566967dd357bf582cfdc908c`  
		Last Modified: Tue, 03 Jun 2025 20:56:52 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bd62d7bcee4a2e2d4e3fe84830bbd978a3027b81e7976b723cfce5c113824abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9708379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efdf790e38279933f555c5ef6b82e2fb30e6d8eb6e85274bb375c1c88aced7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c4277d4cc00a376afb142f8ea748e710d48f75eddcf7a2510c5a1e088857e2`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 6.5 MB (6488230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e94ae1fb6404d5eb4989cef0cc09a96573006b7bd7d4e7f7fbab996b9ce90c`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f107f5a32f8d0ab9f4a4a7746509690c6c4845a952c7df17aa5b2e4bc6e7a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:3191c0cbc6ea566ab41e82bdcfd3a1bcfe0757dc82b606a411fdb61d50858d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d3fb67fa07d336d64e774f94f1074d759291d6e8b14b2b24d0c144e3a1ea07`

```dockerfile
```

-	Layers:
	-	`sha256:52a7538138245df9dcdc747a5c3e46f172218df3092764925fdbc21fb2a58298`  
		Last Modified: Tue, 03 Jun 2025 20:56:55 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5dd5eb415f3c3b50eb6e637d9eab8c4ec5726e575550f46a0853226a8da6edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ae7761a85b9922c5be272284ee27fe32bfd3b1a78d3239e429792033c7ced6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6826d2797f1cf0f48d78d168877a33ef918811eaa7ee6146a8653f4218cf6e56`  
		Last Modified: Tue, 03 Jun 2025 18:23:10 GMT  
		Size: 6.3 MB (6271484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2ec423b14754303830aaf58d608bc667aab81252f2b170550982a6c4aee78`  
		Last Modified: Tue, 03 Jun 2025 18:12:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac99aa05c0616d567688e33499eacc91da2b7c79dd4b91fdc6bc363573dccd4`  
		Last Modified: Tue, 03 Jun 2025 18:12:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f57f8e16b74edcba83577e18c83f6c830b2de03df54acd64a65d88ab4b5f5ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6f8fff81a6020fdbd737e9dd518b019a3b205e35d387235d0339aec5b55092`

```dockerfile
```

-	Layers:
	-	`sha256:c61cb3463dab986b2ecb7f263eea6eff56bfdb0d4075df19122df210a8d0a062`  
		Last Modified: Tue, 03 Jun 2025 20:56:59 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:04f768ca98d273ca56dc14213654250fb52045b383bce5db0e58444c23697d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ee2cb1b02b4eeb2714421cdd6b2e9f5ba023f8e508c2b604861f33248ccfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66500e2c223c5a3f4777f4d7f4ffcec1ca21a34f687704db2a6d0e661fe0299`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 6.3 MB (6254211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198db56aeb51065eb35574df93180297f06ba8d180108a952be65d93fa4e7dd2`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df632b2ea33fceba251c68a32d3efed10d3b495018d7e16d1b256225dd38aef8`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a11e45d5ebc10e2f442f0730348545d2ec0f0645f0f047a39364c6073754d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872e45d8950ac438f1cc639d1fde3610446df42c33be57d2ce16b2eef0e02297`

```dockerfile
```

-	Layers:
	-	`sha256:b2fdd3426bf4664ed50234140c9c5e23667db50fb3545c6a3874643740ef5aaf`  
		Last Modified: Tue, 03 Jun 2025 20:57:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:081db236c5c2d779dcea7087bfea30c8252499477626f616458bb70b78054bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9772610e623e3eae3e2949e0e470f0755004398628ced20be8fe593671829030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c44dcd57da31d89c4bf6d887262bfc6e7136e1132734822ddb4586096692a0`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 6.6 MB (6619415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93bad89a83837b6afc8b1128b9f0d132c74ba14e1c7f52f407fbe775cb13a2`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ded513c6eb3a5fff1e0ab2d6ac1560515bbf0389375e4759c71a1b2c0b6e97`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b96db90bf17f90a65aaa3a6fa7ea4250df1f9ee0d9d13d52b7d3c8f926242340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e98ba8254d35c0c12076fa3f077b261896b884cb797b2b50e57f1f79bdaa45`

```dockerfile
```

-	Layers:
	-	`sha256:68ad3f417d73aacb9e3e3a8a3fbde0712715fd19f474e71d7f05c3507eeb168b`  
		Last Modified: Tue, 03 Jun 2025 20:57:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:b8d6a01568a7837d5186f948a3ebfae1bdf5a602268273b50704655982596b22
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
$ docker pull nats@sha256:69435fcc1356278c35dde2a3b3d9f2c4504f57b921d38612d36200a9c7b51067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10580056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e96d11240320c8d079058907e6b1a349c3c164f6d1057c7d4141b67803ef0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be8340a33b28b7069d77e81278e1150e46e62e5739a5ef524f3b10b6315d93`  
		Last Modified: Tue, 03 Jun 2025 18:08:18 GMT  
		Size: 6.8 MB (6782240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:770fc5b17c3e852bea98835c4f770de25350891225d2d5c48a17079cd2a87f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ece4f13433515ab3468766d0750908f38501255daea31da2aab9466abd8dd13`

```dockerfile
```

-	Layers:
	-	`sha256:993a3e77289857e49dcc0d82e8b0a4d01bf97fc1ac52f27adc1b6d9f46be3010`  
		Last Modified: Tue, 03 Jun 2025 20:56:48 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:cc02d2d98d5248ae02ac731a42436bcf7c257a2336cb6ccc18c0a0d33aca7425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10002162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7ffccb3eb9188263f6e9ee5ff6be0d88a00817e7d4a7a880ef153ff6b59861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3cdfa139575e7698957b4ff36ff5e3b9c98dcca74e89a001ef2062de4433d8`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 6.5 MB (6500264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3195bedba82c8298239740a21ea08ee0b417d4c68b4eb96b52ad6c083c2c920`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f93998e0b8d5c431d6f762091f25cb87996747747bf0554bc73c73a2f31e190`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cd850c5ec391a375d438c70b5cc24af732269f5631ab424afdb6f809d708e432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1f72e1e723af723f70095a15f2853df338bcc41fbb18fb2f275a71cf0c8c37`

```dockerfile
```

-	Layers:
	-	`sha256:c0a8dba6556e09db91573b8694623b3159599ceb566967dd357bf582cfdc908c`  
		Last Modified: Tue, 03 Jun 2025 20:56:52 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bd62d7bcee4a2e2d4e3fe84830bbd978a3027b81e7976b723cfce5c113824abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9708379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efdf790e38279933f555c5ef6b82e2fb30e6d8eb6e85274bb375c1c88aced7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c4277d4cc00a376afb142f8ea748e710d48f75eddcf7a2510c5a1e088857e2`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 6.5 MB (6488230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e94ae1fb6404d5eb4989cef0cc09a96573006b7bd7d4e7f7fbab996b9ce90c`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f107f5a32f8d0ab9f4a4a7746509690c6c4845a952c7df17aa5b2e4bc6e7a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:3191c0cbc6ea566ab41e82bdcfd3a1bcfe0757dc82b606a411fdb61d50858d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d3fb67fa07d336d64e774f94f1074d759291d6e8b14b2b24d0c144e3a1ea07`

```dockerfile
```

-	Layers:
	-	`sha256:52a7538138245df9dcdc747a5c3e46f172218df3092764925fdbc21fb2a58298`  
		Last Modified: Tue, 03 Jun 2025 20:56:55 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5dd5eb415f3c3b50eb6e637d9eab8c4ec5726e575550f46a0853226a8da6edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ae7761a85b9922c5be272284ee27fe32bfd3b1a78d3239e429792033c7ced6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6826d2797f1cf0f48d78d168877a33ef918811eaa7ee6146a8653f4218cf6e56`  
		Last Modified: Tue, 03 Jun 2025 18:23:10 GMT  
		Size: 6.3 MB (6271484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2ec423b14754303830aaf58d608bc667aab81252f2b170550982a6c4aee78`  
		Last Modified: Tue, 03 Jun 2025 18:12:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac99aa05c0616d567688e33499eacc91da2b7c79dd4b91fdc6bc363573dccd4`  
		Last Modified: Tue, 03 Jun 2025 18:12:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f57f8e16b74edcba83577e18c83f6c830b2de03df54acd64a65d88ab4b5f5ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6f8fff81a6020fdbd737e9dd518b019a3b205e35d387235d0339aec5b55092`

```dockerfile
```

-	Layers:
	-	`sha256:c61cb3463dab986b2ecb7f263eea6eff56bfdb0d4075df19122df210a8d0a062`  
		Last Modified: Tue, 03 Jun 2025 20:56:59 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:04f768ca98d273ca56dc14213654250fb52045b383bce5db0e58444c23697d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ee2cb1b02b4eeb2714421cdd6b2e9f5ba023f8e508c2b604861f33248ccfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66500e2c223c5a3f4777f4d7f4ffcec1ca21a34f687704db2a6d0e661fe0299`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 6.3 MB (6254211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198db56aeb51065eb35574df93180297f06ba8d180108a952be65d93fa4e7dd2`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df632b2ea33fceba251c68a32d3efed10d3b495018d7e16d1b256225dd38aef8`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a11e45d5ebc10e2f442f0730348545d2ec0f0645f0f047a39364c6073754d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872e45d8950ac438f1cc639d1fde3610446df42c33be57d2ce16b2eef0e02297`

```dockerfile
```

-	Layers:
	-	`sha256:b2fdd3426bf4664ed50234140c9c5e23667db50fb3545c6a3874643740ef5aaf`  
		Last Modified: Tue, 03 Jun 2025 20:57:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:081db236c5c2d779dcea7087bfea30c8252499477626f616458bb70b78054bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9772610e623e3eae3e2949e0e470f0755004398628ced20be8fe593671829030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c44dcd57da31d89c4bf6d887262bfc6e7136e1132734822ddb4586096692a0`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 6.6 MB (6619415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93bad89a83837b6afc8b1128b9f0d132c74ba14e1c7f52f407fbe775cb13a2`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ded513c6eb3a5fff1e0ab2d6ac1560515bbf0389375e4759c71a1b2c0b6e97`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b96db90bf17f90a65aaa3a6fa7ea4250df1f9ee0d9d13d52b7d3c8f926242340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e98ba8254d35c0c12076fa3f077b261896b884cb797b2b50e57f1f79bdaa45`

```dockerfile
```

-	Layers:
	-	`sha256:68ad3f417d73aacb9e3e3a8a3fbde0712715fd19f474e71d7f05c3507eeb168b`  
		Last Modified: Tue, 03 Jun 2025 20:57:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:57f45fba83001bfff519e918035305f02eb897a172f82d43933136e0f6aceb1e
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
	-	windows version 10.0.20348.3692; amd64

### `nats:latest` - linux; amd64

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

### `nats:latest` - unknown; unknown

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

### `nats:latest` - linux; arm variant v6

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

### `nats:latest` - unknown; unknown

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

### `nats:latest` - linux; arm variant v7

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

### `nats:latest` - unknown; unknown

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

### `nats:latest` - linux; arm64 variant v8

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

### `nats:latest` - unknown; unknown

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

### `nats:latest` - linux; ppc64le

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

### `nats:latest` - unknown; unknown

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

### `nats:latest` - linux; s390x

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

### `nats:latest` - unknown; unknown

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

### `nats:latest` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:5809c0213e200dfdbe56a1d284162f75ce89533ee1eca342e2350fb4b8b384b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129076843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6294ddd46c444e866b505f0226f57df6864ce6cda1545be49e239c008bd011c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f7eba05352cc5df78a901d41dcb3733c4206eb7fd4625541f65326a30e8f`  
		Last Modified: Tue, 03 Jun 2025 18:16:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cf94e1df89f22d940ee5d9efd850e11abeb664ffa179e56c6b22e0dd772fb`  
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.5 MB (6494401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04a0b03d8f9056c543ef2f229fc65a83adff4f5d79e08cc2f95db65cc5da`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91fc443933d1e179f3b885096b15f1d6ac4b086b379a38766604c4ae3fc9bf`  
		Last Modified: Tue, 03 Jun 2025 18:17:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b6a66cc622766c3a994ba752f2a0b9973d6df193bb223dbb101c089689d8d`  
		Last Modified: Tue, 03 Jun 2025 20:57:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68e17b27bdb59114784659909c5bbec158528e884a87fa70e3357643d785c8`  
		Last Modified: Tue, 03 Jun 2025 18:17:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

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

### `nats:linux` - linux; amd64

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

### `nats:linux` - unknown; unknown

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

### `nats:linux` - linux; arm variant v6

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

### `nats:linux` - unknown; unknown

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

### `nats:linux` - linux; arm variant v7

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

### `nats:linux` - unknown; unknown

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

### `nats:linux` - linux; arm64 variant v8

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

### `nats:linux` - unknown; unknown

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

### `nats:linux` - linux; ppc64le

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

### `nats:linux` - unknown; unknown

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

### `nats:linux` - linux; s390x

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

### `nats:linux` - unknown; unknown

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

## `nats:nanoserver`

```console
$ docker pull nats@sha256:ecc8389817ef21fb2d273b7fe6776b4de22f5f3da3033b00a69151c47e0215a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:5809c0213e200dfdbe56a1d284162f75ce89533ee1eca342e2350fb4b8b384b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129076843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6294ddd46c444e866b505f0226f57df6864ce6cda1545be49e239c008bd011c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f7eba05352cc5df78a901d41dcb3733c4206eb7fd4625541f65326a30e8f`  
		Last Modified: Tue, 03 Jun 2025 18:16:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cf94e1df89f22d940ee5d9efd850e11abeb664ffa179e56c6b22e0dd772fb`  
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.5 MB (6494401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04a0b03d8f9056c543ef2f229fc65a83adff4f5d79e08cc2f95db65cc5da`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91fc443933d1e179f3b885096b15f1d6ac4b086b379a38766604c4ae3fc9bf`  
		Last Modified: Tue, 03 Jun 2025 18:17:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b6a66cc622766c3a994ba752f2a0b9973d6df193bb223dbb101c089689d8d`  
		Last Modified: Tue, 03 Jun 2025 20:57:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68e17b27bdb59114784659909c5bbec158528e884a87fa70e3357643d785c8`  
		Last Modified: Tue, 03 Jun 2025 18:17:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:ecc8389817ef21fb2d273b7fe6776b4de22f5f3da3033b00a69151c47e0215a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:5809c0213e200dfdbe56a1d284162f75ce89533ee1eca342e2350fb4b8b384b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129076843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6294ddd46c444e866b505f0226f57df6864ce6cda1545be49e239c008bd011c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Tue, 03 Jun 2025 18:09:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 03 Jun 2025 18:09:24 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 18:09:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 18:09:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09f7eba05352cc5df78a901d41dcb3733c4206eb7fd4625541f65326a30e8f`  
		Last Modified: Tue, 03 Jun 2025 18:16:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cf94e1df89f22d940ee5d9efd850e11abeb664ffa179e56c6b22e0dd772fb`  
		Last Modified: Tue, 03 Jun 2025 18:17:01 GMT  
		Size: 6.5 MB (6494401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04a0b03d8f9056c543ef2f229fc65a83adff4f5d79e08cc2f95db65cc5da`  
		Last Modified: Tue, 03 Jun 2025 18:17:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91fc443933d1e179f3b885096b15f1d6ac4b086b379a38766604c4ae3fc9bf`  
		Last Modified: Tue, 03 Jun 2025 18:17:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b6a66cc622766c3a994ba752f2a0b9973d6df193bb223dbb101c089689d8d`  
		Last Modified: Tue, 03 Jun 2025 20:57:01 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68e17b27bdb59114784659909c5bbec158528e884a87fa70e3357643d785c8`  
		Last Modified: Tue, 03 Jun 2025 18:17:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:6f8e77e1231fd3511353f2a8161af5ba6d11565d0d1ece50953a2f9a372d6bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:8317c827fa967bd9f550b8ce662f920ed01c012ca005f14021df3bf5118e4938
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280787628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9160d38e59cf418ea3321c716c7a5c123f40250e646f9a19e44a3d00825101c4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 17:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 17:56:57 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER=2.11.4
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Tue, 03 Jun 2025 17:56:59 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Tue, 03 Jun 2025 17:58:07 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Jun 2025 17:58:34 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 03 Jun 2025 17:58:34 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 17:58:35 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 17:58:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 17:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4b5081f22f0ce90ffb8a283bf6907184ca210d3fa64cc649c175c2403bf48`  
		Last Modified: Tue, 03 Jun 2025 17:59:03 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd1a53f2b89b85d5c147edcb69400d431d2aae95f09eb51615e21d71868b20`  
		Last Modified: Tue, 03 Jun 2025 17:59:04 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05e4d6ed3ee536d39ce8a0564d98ec9fb2830b9aea712e135ef717a9034b58d`  
		Last Modified: Tue, 03 Jun 2025 17:59:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd5804ef666b2af87854e3e84e8513832d69895027327d5563934968d65bfc`  
		Last Modified: Tue, 03 Jun 2025 17:59:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfe49f5d913195c31fdfeae7a261be6ef51da43fb44d9fca4e428ba78fa6064`  
		Last Modified: Tue, 03 Jun 2025 17:59:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af20b8c738d9d92e83bc0e0e5c9b813668bb6deca62e90327f3bff9bac141d0`  
		Last Modified: Tue, 03 Jun 2025 17:59:09 GMT  
		Size: 342.9 KB (342923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9dd708b6fd0131af1f9ae1c1001cf8966b8f9b27bcdd0d022586b3a8489327`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 6.8 MB (6804324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423519a4e3a5a29f15c70595333fab0a6f79736ff478e5e3d66fb7481741151f`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe4b134972dcd390001fc9744ccffb8da5627e4fa055f6fe84918e65df4782d`  
		Last Modified: Tue, 03 Jun 2025 17:59:12 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb328b3dfd00b76b936d43d8a04426cb93cab24be8d294245da02c20ea2df6`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f933a18bfe02980983b3a438f0f485afe7c6592e98c09eb78891959f057c3a55`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:6f8e77e1231fd3511353f2a8161af5ba6d11565d0d1ece50953a2f9a372d6bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull nats@sha256:8317c827fa967bd9f550b8ce662f920ed01c012ca005f14021df3bf5118e4938
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280787628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9160d38e59cf418ea3321c716c7a5c123f40250e646f9a19e44a3d00825101c4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 03 Jun 2025 17:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 17:56:57 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER=2.11.4
# Tue, 03 Jun 2025 17:56:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.4/nats-server-v2.11.4-windows-amd64.zip
# Tue, 03 Jun 2025 17:56:59 GMT
ENV NATS_SERVER_SHASUM=c78771905c52a8590f6c20cb101bb38ab65bd3046bd6ab8edf4e38efd41dce6f
# Tue, 03 Jun 2025 17:58:07 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Jun 2025 17:58:34 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 03 Jun 2025 17:58:34 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 03 Jun 2025 17:58:35 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Jun 2025 17:58:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 03 Jun 2025 17:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4b5081f22f0ce90ffb8a283bf6907184ca210d3fa64cc649c175c2403bf48`  
		Last Modified: Tue, 03 Jun 2025 17:59:03 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd1a53f2b89b85d5c147edcb69400d431d2aae95f09eb51615e21d71868b20`  
		Last Modified: Tue, 03 Jun 2025 17:59:04 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05e4d6ed3ee536d39ce8a0564d98ec9fb2830b9aea712e135ef717a9034b58d`  
		Last Modified: Tue, 03 Jun 2025 17:59:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd5804ef666b2af87854e3e84e8513832d69895027327d5563934968d65bfc`  
		Last Modified: Tue, 03 Jun 2025 17:59:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfe49f5d913195c31fdfeae7a261be6ef51da43fb44d9fca4e428ba78fa6064`  
		Last Modified: Tue, 03 Jun 2025 17:59:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af20b8c738d9d92e83bc0e0e5c9b813668bb6deca62e90327f3bff9bac141d0`  
		Last Modified: Tue, 03 Jun 2025 17:59:09 GMT  
		Size: 342.9 KB (342923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9dd708b6fd0131af1f9ae1c1001cf8966b8f9b27bcdd0d022586b3a8489327`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 6.8 MB (6804324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423519a4e3a5a29f15c70595333fab0a6f79736ff478e5e3d66fb7481741151f`  
		Last Modified: Tue, 03 Jun 2025 17:59:11 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe4b134972dcd390001fc9744ccffb8da5627e4fa055f6fe84918e65df4782d`  
		Last Modified: Tue, 03 Jun 2025 17:59:12 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb328b3dfd00b76b936d43d8a04426cb93cab24be8d294245da02c20ea2df6`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f933a18bfe02980983b3a438f0f485afe7c6592e98c09eb78891959f057c3a55`  
		Last Modified: Tue, 03 Jun 2025 17:59:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
