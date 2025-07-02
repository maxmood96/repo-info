## `clojure:temurin-24-tools-deps`

```console
$ docker pull clojure@sha256:b477fd74e4c2e292329c9aa616145cfd27d75812bd290aa3fc1fe60b4ffc4bca
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

### `clojure:temurin-24-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:369457bbb6a8f812a8ac5aa2172135bbe54869c9e683a9047e49a895c44e5b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219440359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b545e6ae92c5c54977c49b4de54f1f2576e5034ffa1c57d5de1f6843e6f048`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a1b818c5afe59e81fecd397ce1fc7959e404064670851a83d9ab53e6740a76`  
		Last Modified: Wed, 02 Jul 2025 04:17:41 GMT  
		Size: 90.0 MB (89952000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6550fdf141d0cf2bbdb7496c21da02a8e53c2f67919a4dd48a5628df38b2e55f`  
		Last Modified: Wed, 02 Jul 2025 04:17:37 GMT  
		Size: 81.0 MB (80993037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea8c71b469cdd2fef38ef25e01e3f0f3bb17477e0c8f2701ab65a7d8dbab240`  
		Last Modified: Wed, 02 Jul 2025 04:17:26 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e535c31192eb5793f310384133c47ebde510a4b1a4c25e853321eff872b6ec`  
		Last Modified: Wed, 02 Jul 2025 04:17:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:5da59001a33f64dcb0e05af1ab0715481bbfd5b38667ffd30afe16fb17d58b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7336096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32a1febc4707789597a46a1add58e115c7c390c857ab8697d5c71ebfb17409b`

```dockerfile
```

-	Layers:
	-	`sha256:319f2bd3c3d04f6083f3760683ffebb5aede1446df999e8e41b901a35c0c2462`  
		Last Modified: Wed, 02 Jul 2025 06:40:59 GMT  
		Size: 7.3 MB (7319598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b577b0f864ee778bb09fdfc8df2c96255fddc73aa07e14f23f31acad8c05f20`  
		Last Modified: Wed, 02 Jul 2025 06:41:00 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:67a05e4f401d5331e2eb830ff704d9730078b0994a51f7665e0a20851b9d94d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218283134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ecd4b8f2791a036adaacdd1f056a18de41657c5647f0685804bc4922fb712b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068915118494f0a1e3d96ea0ed10f769bc409d86b4869da7d353f2b54f9fcd84`  
		Last Modified: Tue, 01 Jul 2025 12:36:35 GMT  
		Size: 89.1 MB (89091279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b83c246e868308b884eb0958d33fa31a2a16cb91779defe2cb21172cacdfc1`  
		Last Modified: Tue, 01 Jul 2025 12:42:17 GMT  
		Size: 80.9 MB (80852030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a122e8614175d8ef4f43a74c6404be8fcbbd8bae1caae17a3c50502f5732f9`  
		Last Modified: Tue, 01 Jul 2025 12:42:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ddf731a46b585b66cd36a7fe990062800177e4901b7dba5aa1ffe309a8f1a0`  
		Last Modified: Tue, 01 Jul 2025 12:42:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:017dff469a8c05b637d00e1021551e4024fa956e6c9b1cfd7869ddae9fc8f4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4482dfdb1051b795e74d476236c68349a3d086f87a810bb90793680cf90fbf46`

```dockerfile
```

-	Layers:
	-	`sha256:88e0f2fe8e94852253eb7fe87f278b973e55361dee5a519ca6bb824ddc7afc84`  
		Last Modified: Tue, 01 Jul 2025 15:39:47 GMT  
		Size: 7.3 MB (7325382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e962d6baeeb6f9c7103493c26c625c1f86d2601130d00a3f8c1f667f407944f`  
		Last Modified: Tue, 01 Jul 2025 15:39:48 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:cd1aacab4f2d90fd598af22f406f7c4a9115b95bf643ddc04f2dce2845403a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229077313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa9905fcf6284e9f7b3db9fbf0884320ae9fbe975279eba239208a140f85de9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcfd6874f2794612323526d256ad677942a1f220ad172db56959f104717dfc1`  
		Last Modified: Tue, 01 Jul 2025 09:09:37 GMT  
		Size: 89.9 MB (89920248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd5aa327f5f316536bb9346a14fae01a897d371b690cc84b46f08a4a45611f5`  
		Last Modified: Tue, 01 Jul 2025 09:17:06 GMT  
		Size: 86.8 MB (86818783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4a1ff322632d3b3b615e14863845571b0010ea8a4853af74b0b2ff45b643cd`  
		Last Modified: Tue, 01 Jul 2025 09:16:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220e08b234588333fadafa41c2c0b66037020b29de1a1da32243f2cb012e0d1b`  
		Last Modified: Tue, 01 Jul 2025 09:16:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:ca0fc7ded681a50f9a32f85d154b629c29499eda7431468b018114e372dc4857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4b5bacd172007233122f97457a1bc5dc68aec22da666b9c9672b37baa1c7ea`

```dockerfile
```

-	Layers:
	-	`sha256:b20bc8ac8af23cf995eef7ad516d9f5c70ef1711be6ce30d02ef03de8c288351`  
		Last Modified: Tue, 01 Jul 2025 12:37:17 GMT  
		Size: 7.3 MB (7326112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a18f1fe507fbbea272f675838945fe1220b80dfefef90d0188b03f1290b0df0`  
		Last Modified: Tue, 01 Jul 2025 12:37:18 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:20ca8e0ebf5023efb9cbda7ce0b06b296a1e3738818e479db61ee03093c8332f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212166659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a01ffac05c69c5d78fcd2c7f6a55b03b2d18494558d0b4c1766ca33ad49c772`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d5a54602bfb697ba4ba032fdb5bd7dd65566e4d748c05b7a6ab9306169bfb7`  
		Last Modified: Wed, 02 Jul 2025 06:56:10 GMT  
		Size: 85.2 MB (85216779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1fe512dac936fcf3435a6a221c78c6cb55fd68b82d0391418342c9cef4a3c`  
		Last Modified: Wed, 02 Jul 2025 07:00:40 GMT  
		Size: 79.8 MB (79799550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615914131e016efd7f0235eb94f9f504f80a4b83c485b10e4e36f297b6d7f9bc`  
		Last Modified: Wed, 02 Jul 2025 07:00:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfeb147284db54e7f68cf024e81fda730bd4da94ce39015fa083bb1aa6b0fa2c`  
		Last Modified: Wed, 02 Jul 2025 07:00:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:4afa4a50317fce17fdf899e1783487cdef4c0debae631f98aff0a8f7cdd3d4ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724122c5b05d20a843da77f2cc32185294a4370398b3ec0ea43dfa8675eb1c8f`

```dockerfile
```

-	Layers:
	-	`sha256:370c0b28da40c3e17d4d65f54680b8b20ae61fa97fe6d831ef9fc554022f6ad0`  
		Last Modified: Wed, 02 Jul 2025 09:40:36 GMT  
		Size: 7.3 MB (7313465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6223c32e18f43f4f18b372b32e3c745abd972ef451dfe0dd21c426a44c758af`  
		Last Modified: Wed, 02 Jul 2025 09:40:36 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json
