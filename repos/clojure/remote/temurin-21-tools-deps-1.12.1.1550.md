## `clojure:temurin-21-tools-deps-1.12.1.1550`

```console
$ docker pull clojure@sha256:763d43e4badead3bc8e98d0c715f24973019b65c28813705b5cf41b2b6a38ee5
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

### `clojure:temurin-21-tools-deps-1.12.1.1550` - linux; amd64

```console
$ docker pull clojure@sha256:3fe2428639e8c0376672d89ea288190fbc35561d10dd514c3f1629ff3b760beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287294108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a371ace9797a0b759a0418f0bc5ced3fcdbb2356008976cc41b24ca6283eeb`
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
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60001837de06e5a0f6b90ea85940e9a406388e404cb599581eb917d713e6f39`  
		Last Modified: Wed, 13 Aug 2025 01:00:55 GMT  
		Size: 157.8 MB (157804748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0526fd0fe8ab32ad930cc5c38355b494af68f5b8c57b5ec7070b98e64931d0f6`  
		Last Modified: Tue, 12 Aug 2025 21:37:21 GMT  
		Size: 81.0 MB (80993807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b023eec4a2804d7a8f496e4beab6d122b62b33ca4ae1a7ac99cf364a7e432e`  
		Last Modified: Tue, 12 Aug 2025 21:37:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9503e4216f42103ca075efc244c865d75708ab0d6ff1d45f9f4d1f899dafb9`  
		Last Modified: Tue, 12 Aug 2025 21:37:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550` - unknown; unknown

```console
$ docker pull clojure@sha256:f0458081eb8f8350846e7394e4f3a80d7f1cf9611d229f59101040a506bd0747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e36f286eca2a7cdc273457c1689921135a3c04792324ce9a808bf681a9f17ab`

```dockerfile
```

-	Layers:
	-	`sha256:5166e65c4fd47d457c4262e1bb59d03a3f24988ea23453b1aa77a5d1c50c06d0`  
		Last Modified: Wed, 13 Aug 2025 00:38:23 GMT  
		Size: 7.4 MB (7373370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b694e9281c9e5f7c2b933ba0259f29c3944334f9cc59df1caa4b90b59b004be9`  
		Last Modified: Wed, 13 Aug 2025 00:38:24 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fda26a6ca5703952ff1156437b18f8aaa573fda6a702f87f85bd850865ec8197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285292914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d71bae7e7ed39633eddae590965052ea4a4a16f49111c27f7951ba208762eb`
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
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e753482983ad3d2a629b620956b3cd49a7214c4f84f167fd737158d8332d4c`  
		Last Modified: Wed, 13 Aug 2025 16:01:51 GMT  
		Size: 156.1 MB (156081215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b233da575bfa6cc23ef534978a65ec161088a69ebc8f5b68e810ad8aa00edfce`  
		Last Modified: Wed, 13 Aug 2025 14:36:10 GMT  
		Size: 80.9 MB (80868209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa22f4f38c281fa0ba96a1d4b765bbea83dbf6a34c261075022c180f1e045d2`  
		Last Modified: Wed, 13 Aug 2025 14:36:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656017ba4309fe21543cbda2cd00d2479fcaedcfd3f264b98c49d4f90f1c07df`  
		Last Modified: Wed, 13 Aug 2025 14:36:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550` - unknown; unknown

```console
$ docker pull clojure@sha256:e000a3c2e504d8bd163542d1560c1f75452438a5c9a09ff78971e906a51f4ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26619f9a05d3b773c8ce87e54e41f7a525f030280510544dc2ccee9479f074d`

```dockerfile
```

-	Layers:
	-	`sha256:f69bdd68eae468ce511149b840c5bf5019b6e4bd077547bb50ff72a1fbad49ef`  
		Last Modified: Wed, 13 Aug 2025 15:38:44 GMT  
		Size: 7.4 MB (7379205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a210d8c1e822beacbcd5bead92bb5c835b122fcfb32f5396d637c03c7f1e9916`  
		Last Modified: Wed, 13 Aug 2025 15:38:44 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550` - linux; ppc64le

```console
$ docker pull clojure@sha256:76ba58c670123422c0591f4e0f7746782f98f948486874a7f53b7979b54c8ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297124564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8210a78e10bb257559de49abf2298ade69afdbc9a0ace25bd120a01fcd4c27fa`
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
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21178e342602edd12ca410499981adb42800eb941f19d77cad58cb797945aa34`  
		Last Modified: Wed, 13 Aug 2025 22:01:26 GMT  
		Size: 158.0 MB (157963474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d51e227726cc802f62c12c99d1e5fd46e70f8cb8634b330b88bd24ce24e268`  
		Last Modified: Wed, 13 Aug 2025 20:11:03 GMT  
		Size: 86.8 MB (86821969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bf8bdb3c966ab787882bb0f5e2c18b65aa9d1ccfb580c1d14b579474f70ad8`  
		Last Modified: Wed, 13 Aug 2025 20:10:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5678c33e728ebb7da8a56b8e610b00fa5f1dcd15465cfe16393924ee45ce8f`  
		Last Modified: Wed, 13 Aug 2025 20:10:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550` - unknown; unknown

```console
$ docker pull clojure@sha256:78b3a9bf5cd96c4591ec77656f2df9c60b2c85fd3439cb9bf50eea8fb9b97479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192c7f740fd2785a9d969e98b2f4ed1fd6ffd6e8a3594f9253f998156dde8cad`

```dockerfile
```

-	Layers:
	-	`sha256:5565f4cf5ddf404cea83a2c00ce7e6c14a9e3bbe7dee0dc869c04b9143a49ff7`  
		Last Modified: Wed, 13 Aug 2025 21:37:51 GMT  
		Size: 7.4 MB (7378610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22634fab349c8edcbd9a693ef7af82a55cb57bb692e87a749e4f34365ad4dc69`  
		Last Modified: Wed, 13 Aug 2025 21:37:52 GMT  
		Size: 17.9 KB (17903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550` - linux; s390x

```console
$ docker pull clojure@sha256:c81053786e987bb6bf662509f872ad163f3a8f681eefd80c630dbc74d2e787ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273980775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7b52007b8a3551d3e04ff92b1b9df85646e8ee3ad1729cba769ef75031d739`
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
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b459e3f0007c17bde237e108936432cad214c379e785f9e98e38f4ecd5eb115`  
		Last Modified: Wed, 13 Aug 2025 10:02:46 GMT  
		Size: 147.0 MB (147026949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1188d1185852757a93f2bf097874c978370b28c40785cd274227adb1cbf938ce`  
		Last Modified: Wed, 13 Aug 2025 10:03:42 GMT  
		Size: 79.8 MB (79802917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d2c7af8f34b12f06a5d55664541fb19c9d6e43cba9927891480642f8c517c2`  
		Last Modified: Wed, 13 Aug 2025 07:23:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7663fd8dea2917e44035e26f09c245613273e3182e74adb39e32cc80a40aa9`  
		Last Modified: Wed, 13 Aug 2025 07:23:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550` - unknown; unknown

```console
$ docker pull clojure@sha256:29ce447df912ec43a2c1c5d08bc15473cfe10efffea94498cb9273768552a656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eed55a1fbbefb617385e6eb31cdfaef54d94dbd42c3502b135cd29d8ab49c0a`

```dockerfile
```

-	Layers:
	-	`sha256:81472392db77669b23cba6c925518a1217b1d298aa8785ddfbce8cc71782ce27`  
		Last Modified: Wed, 13 Aug 2025 09:37:19 GMT  
		Size: 7.4 MB (7364689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d14c17d512fc57297fcd580ea592363eb13ca760a69bfb896de04f9eea135f3`  
		Last Modified: Wed, 13 Aug 2025 09:37:20 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
