## `nats:latest`

```console
$ docker pull nats@sha256:29bb80686e22c4133d99e9b3cba0b131ee82d2dcdc75d179d1ea4efdf5739af9
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
	-	windows version 10.0.17763.7009; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ba3f53e77bfe68ec915e217e98e27eef3c1dc6582312ecfdff74282af83f27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5991108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcde9bd1a6e573a6fb19557dfdccad75ea19c144369fc9f1a996b4c094e67e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 19 Mar 2025 16:37:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 19 Mar 2025 16:37:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 19 Mar 2025 16:37:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 19 Mar 2025 16:37:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b822286bde36186e2380279ead71279ab7294bf250f55aaf8bf6d4770ae84ce5`  
		Last Modified: Wed, 19 Mar 2025 16:42:51 GMT  
		Size: 6.0 MB (5990600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a38020ffc8a376a117c636de2a0eeb692526c89d67e9677c42aae810fa530d`  
		Last Modified: Wed, 19 Mar 2025 21:07:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a44410c0dba1a374562a761d12231155886c33def7b6fe607d386625799021bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160af38107e1688ac5695087999bcb3a2da680ab9885c132a2aad8a01d7a2e99`

```dockerfile
```

-	Layers:
	-	`sha256:1484e4c1fa5f08946b20e11d8a3f03be035fa3c57a3c9413acccdd456a13a161`  
		Last Modified: Wed, 19 Mar 2025 21:07:09 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5b39f18a68d525349b8342743703356df26415df7ddb80854343b28659a15367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1621143ad612f99d3ac9a46b461b1dfbbdaf7cb3ad1f0b2b387d9071d79f0ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 19 Mar 2025 16:37:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 19 Mar 2025 16:37:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 19 Mar 2025 16:37:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 19 Mar 2025 16:37:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f8bea80233611a6393ba9b43e0d5b9487a0e5675862e53cc48c922f0189986`  
		Last Modified: Wed, 19 Mar 2025 16:42:49 GMT  
		Size: 5.8 MB (5775494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1afbd4f0f1a5a28aa16ca864174d0666d154ed2eaf222e29606aa72cddccca1`  
		Last Modified: Wed, 19 Mar 2025 21:57:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:6e8482102e355d0a7d9b8f8184c3bd19c98e57544fe1a79b2db9ab3628f89e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62adb534fedc07f1169dc165a70503ff5da7a9c51e2cadbdbfc03a2f41a798a`

```dockerfile
```

-	Layers:
	-	`sha256:ef5f1dc961aa2787f4175edd0794823fb0c57a526f81ae35e68021d9378b692b`  
		Last Modified: Wed, 19 Mar 2025 21:57:43 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
