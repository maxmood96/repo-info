## `clojure:temurin-24-bookworm-slim`

```console
$ docker pull clojure@sha256:745306f33d54e1243de9f9f2a72c33ee162ed8f42ea9595034df056906165991
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:834f37c065161780b860fe1fb31116d01deeca148f0ed44b582b677ebee25981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187740720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33455409e6364d94a053dc7a92971289a182463dd0b9f782ba4c1edb01c6026a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e7788ba0bfa208d01abe6cf86c3e1cf5eb4722fd0172503fa3bedc721a2b9`  
		Last Modified: Tue, 12 Aug 2025 21:38:20 GMT  
		Size: 90.0 MB (89975180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2304d246ab8820bb932f1a8777f2a04b26adab99694f0fa90724d3a956b8089e`  
		Last Modified: Tue, 12 Aug 2025 21:38:19 GMT  
		Size: 69.5 MB (69534244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c43555fb3b6a62539e5f14acf122769e27de6c8d032f944f40f818aea07c36`  
		Last Modified: Tue, 12 Aug 2025 21:37:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094d41590ff75734e0004f039ac8f21f0ead9de2172c2ea0f0c132ea97d4524c`  
		Last Modified: Tue, 12 Aug 2025 21:37:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:08fd57feefb3148ac0964c74234f498838dca25a0199fefed741aabcb32e559a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d36317a41986e0c06d9b086179d5f9f81433ac0a625f7ce198aecec56b682a`

```dockerfile
```

-	Layers:
	-	`sha256:4897de7b1d372c72ed0d553b987cef1ba73d4d69be91d85812b0e4c2234d9307`  
		Last Modified: Wed, 13 Aug 2025 00:39:51 GMT  
		Size: 5.1 MB (5061892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec25110d25586d964c23a9134769e115859723058f2408f47088ad3294c03b29`  
		Last Modified: Wed, 13 Aug 2025 00:39:52 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:56649b157110cdbdda0def3950708c64d176d4826fccc090523264131cacd0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186580576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba65af5998d6422e56dbf92e8757314976f20b52d8a7cdddaaf954548acf6b42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b8f023124eee06ec9146925d397fb71c9e699d923adb2dc32191e722e62223`  
		Last Modified: Wed, 13 Aug 2025 17:30:50 GMT  
		Size: 89.1 MB (89092502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49aa1c448a830ed04f3d9a446f454da1d5cc93cc82745f0e1096a4467c61c683`  
		Last Modified: Wed, 13 Aug 2025 17:31:00 GMT  
		Size: 69.4 MB (69405033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ac89e4e9e0e74732f1a41c1b006b7f58f40d7bbbeae898082cf899041ce97e`  
		Last Modified: Wed, 13 Aug 2025 17:31:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27d32403f96eb5177cbef6362073b1d7653e85f8a20b46c231eab9d0a99d85a`  
		Last Modified: Wed, 13 Aug 2025 17:31:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:473af6a977b1abd0b22b5b776ba11bd9146d0b0926a080e3936f7b6261a8a8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f02c6a5a9001ae93f3539b6572ac7fdf5bf30e8d28382fcf3288298e9e99c7`

```dockerfile
```

-	Layers:
	-	`sha256:b543cec6fc97bc5bba9c45b9861ba21bd703b76d41e23131f669575f8c1ecf22`  
		Last Modified: Wed, 13 Aug 2025 15:40:24 GMT  
		Size: 5.1 MB (5067650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c088359cad236f5827fb2da422d2d34252cde24c124c5c428a4b57289014c79b`  
		Last Modified: Wed, 13 Aug 2025 15:40:25 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:933bd6cbfbe8536cff8f0650ef8fea28e29ce4ee5500c6d043c41717196b81c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 MB (197354323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f6d1d2776782897ecdd40d50eea095be323c96992a0aeff1f26973e99c9833`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9424f5f28a173ccfe6825eeb39f1ac7f69b8904acac93f3b05fc953f30434dde`  
		Last Modified: Wed, 13 Aug 2025 20:19:32 GMT  
		Size: 89.9 MB (89918237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c19f52c6a4fe2562994b40fbe74e19ca75564d6ec2f2077d558ca4b711f9d45`  
		Last Modified: Wed, 13 Aug 2025 20:27:59 GMT  
		Size: 75.4 MB (75361625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3c48dac4a990cb700d6eb8b7583399fcb113690be1c6b79bb231f7d6d7ba47`  
		Last Modified: Wed, 13 Aug 2025 20:27:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c00e612364ca56ae0f1956badc39620eec44c12251f0ec222e332a43cf692e`  
		Last Modified: Wed, 13 Aug 2025 20:27:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db47f19783789ab3bf27aa3fa16bda2d9f3ee3990f2f4c540a40897ac9a66784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00a258c0053de135f4d1bd22a3b74e8f3c01585967e6f9d420174b62fd26f5e`

```dockerfile
```

-	Layers:
	-	`sha256:4a40131e64294deea85c381825581e4d0a8122d9552fc192f7d596320f5ad4e8`  
		Last Modified: Wed, 13 Aug 2025 21:39:03 GMT  
		Size: 5.1 MB (5068348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c68d4270e9c0ea8bb6a3cdb878bba12edae72ad825cdae1d0d214f9be9983e3`  
		Last Modified: Wed, 13 Aug 2025 21:39:04 GMT  
		Size: 15.9 KB (15920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b5404ccbf2ed51b3971193c41039676eced675412a28583b909dba6083d89feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180457287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0733f803c62452728014ed9e9b817142de565413f51272254ba55c6ac084dae1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94aa6edd5ef2455ec9053295a37e8950ea22ff4805d862dd5baba16d5ff1451`  
		Last Modified: Wed, 13 Aug 2025 18:14:31 GMT  
		Size: 85.2 MB (85226400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebf3bea4a633e9da9cd7ff40924334db3ec19dd44cec2501fbc23e22a97c872`  
		Last Modified: Wed, 13 Aug 2025 18:15:11 GMT  
		Size: 68.3 MB (68342007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613455bb695efae56cc7d67f05ca56b393cd68fd3f562056501050df54760c41`  
		Last Modified: Wed, 13 Aug 2025 18:15:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268ee7895136e2e0686dd3303a17eaca0855061ddb66f2ed6d385f87ccd3f5ae`  
		Last Modified: Wed, 13 Aug 2025 18:15:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb0d7867adb3e04c8fe85913352ea51eab53b64f43558061d48ecfe6838a0b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8761147c717ee4da16b2aad67f764518bf7bc80a528485b8c2c216d255edfcb4`

```dockerfile
```

-	Layers:
	-	`sha256:d5537234e9dfcf21c0987219f0492152ab6dde75b0992b7c17885e1da8221256`  
		Last Modified: Wed, 13 Aug 2025 18:37:17 GMT  
		Size: 5.1 MB (5055761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69f5fb5f49a38dc970fedce703402a634105143749c81f62ce208521975b12be`  
		Last Modified: Wed, 13 Aug 2025 18:37:18 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
