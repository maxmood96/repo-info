## `clojure:tools-deps-trixie`

```console
$ docker pull clojure@sha256:8e81c7c4a1e27a65829cf21526c6f82d902c0469e7f551a02ff0a006d885b1de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:73d71f7a070268546e0bcf5a324539c43fb2a90a25e765d254e853af871ec1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227129914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966f2c39d3afafeb32cb85e12092ce032e102038ed29e5951a2200c30d3f6327`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:21 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:21:21 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff6df917239d3e913de76112b94d5b95a2e5a9cc4a7aafe4c6d35a814487738`  
		Last Modified: Wed, 22 Apr 2026 02:21:58 GMT  
		Size: 92.3 MB (92256281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6346b647072fe5fac35f03da56b3ba11d764c0609845bcdfc55afea708f0c6ce`  
		Last Modified: Wed, 22 Apr 2026 02:22:00 GMT  
		Size: 85.6 MB (85570490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4494044d780b1627f1ab54b3191980266da46947425fdbc717c735065b482c5`  
		Last Modified: Wed, 22 Apr 2026 02:21:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f3975c393a58afe410ffd28d514bf0299a9b057b9f4975b0ec74cf9325f764`  
		Last Modified: Wed, 22 Apr 2026 02:21:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:29ed3cc06e9a5f9f7f1ff6b469fd9abcb3f03a8326c48c2f4289be82cb263942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73058f5b4cc316dc99bd6bddf94c231cdb68fe90cbfd4ae572e0b2ff76fe20e`

```dockerfile
```

-	Layers:
	-	`sha256:a379b5a40753d08d3d77e294eb23ce14a2e994068873ef64a43a5201e82150c2`  
		Last Modified: Wed, 22 Apr 2026 02:21:57 GMT  
		Size: 7.4 MB (7438787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4c53354f7ef8532628301020e98093abe814352e30934b621f5f67d976f92eb`  
		Last Modified: Wed, 22 Apr 2026 02:21:56 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f787a68bbccc7df212b71e4f725c7b55403471099b634347e5430c314fddd4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226342022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b02c498e4ad27614947d626fb29b7dc43c559ba90d8a3ad87d757f02442886`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:24:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:24:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:24:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:24:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:24:06 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:24:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:24:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a456d5d891050ac3d33b62fd8130340afc36aff50c05d4fd976c1947acf06e19`  
		Last Modified: Wed, 22 Apr 2026 02:24:47 GMT  
		Size: 91.3 MB (91288304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce5d0910f572fd3fe6521021302381f5b46c4ddd6929478ad986a14fcdbd884`  
		Last Modified: Wed, 22 Apr 2026 02:24:47 GMT  
		Size: 85.4 MB (85383434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be22b986fae33955e8ce9c83653786b2535a70b95eb61d6ac17103494b7bfe4e`  
		Last Modified: Wed, 22 Apr 2026 02:24:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7048121f2bef0cbe4d5b4d97674fdd3d3fbcf6c3b4150b149c97ff7f723caf`  
		Last Modified: Wed, 22 Apr 2026 02:24:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d6f9f11049036abfc33739d9fd73c157819f886def9ffbdc8818c37bb96bb2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e4979456e592a5b180d08fecac8496e0224b18d3fdd56a9af53a40d4289317`

```dockerfile
```

-	Layers:
	-	`sha256:18ba65478a0c5529fc562c7d9016768b03a2f2434c31cfa276634c4adf039977`  
		Last Modified: Wed, 22 Apr 2026 02:24:43 GMT  
		Size: 7.4 MB (7445838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6cf8d3ceff27af1fa6aefe52058fc8159ef75a8710f649d12d5ee1e3b6701c`  
		Last Modified: Wed, 22 Apr 2026 02:24:43 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8b0b45b685a03f34708e706a24ec4a31b18fb6504748df3edaed23ea723d68f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239474473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7150e0fc43c792f3e282de425d326e08407ded3adb1890d7c3f7e5ce2fdc4c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 03:09:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 03:09:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 03:09:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 03:09:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 03:09:32 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:14:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:14:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:14:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:14:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:14:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04092892db89c3f0f8309ba50439fcd1d5f508bb90c8bab723af681eadbd6ebd`  
		Last Modified: Thu, 16 Apr 2026 03:10:55 GMT  
		Size: 91.6 MB (91633017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc873e735bf0ddc5cec8afba5a7e0e2888512cc8b1c81a36954fa16d029dcdd`  
		Last Modified: Thu, 16 Apr 2026 03:14:52 GMT  
		Size: 94.7 MB (94721740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996c6e20b38778dfebb53de739d0b07dfb8553695a88d42aa1914fa3f0cf67ef`  
		Last Modified: Thu, 16 Apr 2026 03:14:49 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d069ce35a37f8d826145a0546423a93176b2999a633fd6cd5b8d7f329145200`  
		Last Modified: Thu, 16 Apr 2026 03:14:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b9ccf321760efe1e287066adfe38e5df96918a46085ccebc8788a5d17f4333af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b7525a8c23d94e36bf053ad974dd54ce1e7ca39fadd0426e1022b51427ba11`

```dockerfile
```

-	Layers:
	-	`sha256:df408ea668da0ab193fe2b0da6e5715a1a28a2eda15ed1b718dda4bca5dab2f1`  
		Last Modified: Thu, 16 Apr 2026 03:14:50 GMT  
		Size: 7.4 MB (7426478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314f093d962bbd912da1b1385c024d50deae4faf57fb7a5d78b81a6d803ca296`  
		Last Modified: Thu, 16 Apr 2026 03:14:49 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:70bd8c713be80e60b2e7415b27d306935d44f53a22edd2794d9961fb137e7b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226198211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d4e1d90beb11e81b476ea7ca4fbbdc29f30753810edd90cf2886ae9e0e1cf9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:33:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:33:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:33:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:33:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 18 Apr 2026 05:20:11 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 05:38:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 18 Apr 2026 05:38:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 18 Apr 2026 05:38:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 05:38:02 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 05:38:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7224fd307fae2068f62ccce22d637a96c5204dea7af1d7b9116b5323460f86`  
		Last Modified: Sat, 11 Apr 2026 22:38:56 GMT  
		Size: 90.8 MB (90773425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36285e3dcd25f7a44c612fe778c8bfa02539ab933cb5dfab0d73cad6bde9f99`  
		Last Modified: Sat, 18 Apr 2026 05:42:25 GMT  
		Size: 87.6 MB (87631116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fae0c36a735ece9d0072456cd03f8456e3c4edc9b276ff8caefc6d44b19061c`  
		Last Modified: Sat, 18 Apr 2026 05:42:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4e6da25fabe255b73f61f64e62349291cb6a8778d7372ebe8aee9c4665d5ac`  
		Last Modified: Sat, 18 Apr 2026 05:42:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e916eb5531ec1a92cb6a48dd4c168c4b2f24b4df5cc28cc4cd3b7c1ae1156ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d39c73f4cb1fd1c9ccbd030db0b0faedbde0ae178f1585e0a3ba12069c65cf`

```dockerfile
```

-	Layers:
	-	`sha256:6902f2ccfc03419e376164de517c37b1e9f831dc543d60c50a41c360db7d740c`  
		Last Modified: Sat, 18 Apr 2026 05:42:13 GMT  
		Size: 7.4 MB (7408671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:302f1b2422efca550412701c9a5c4c52bce4d0c1fc9fa860054a0d4704d49433`  
		Last Modified: Sat, 18 Apr 2026 05:42:10 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:bf919c43c84eafe52458b275a9a0804228418cd137be755cacfc3274b798aa6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227310524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a2ab9daba956d36848778e859688658582472f60ab445e3c54c25ed68592c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:44:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:44:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:44:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:44:04 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:44:04 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:45:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:45:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:45:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:45:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:45:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af85e16ff2a5e4ef4e7bca442eaf789074eba5dae2548a5309ae1cc069f92daf`  
		Last Modified: Thu, 16 Apr 2026 00:44:45 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d3893f14bdd8b7e4b96dfe283c4d22679a85c5136d4b7dfa76cb2d664cc5bb`  
		Last Modified: Thu, 16 Apr 2026 00:46:15 GMT  
		Size: 89.7 MB (89710555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92891227399ad31b4c349aa68167619a71b8c6613f6d3be4fb1aa5b5b9303da`  
		Last Modified: Thu, 16 Apr 2026 00:46:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59ab526f9c54f993a94974b92e4cbd230af6ee06d615b26a436fd509be3c850`  
		Last Modified: Thu, 16 Apr 2026 00:46:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:206c679d1e1994c9b59d2d194f13a6bebe2ca1a776e35efa61b60b83d7fb0f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9114e6049e36f0b6c29f07421d3e5440d8f0f16e9e544ee1a694e72750d5568f`

```dockerfile
```

-	Layers:
	-	`sha256:8c231f8c72e11ee968ee378552c874b84b5a09f79b79431e6040b2f64deb1e82`  
		Last Modified: Thu, 16 Apr 2026 00:46:12 GMT  
		Size: 7.4 MB (7419217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a8be6f657c97c12e06431390d79c2b793a86ca6ce7a8826dba70e3af4efb7f0`  
		Last Modified: Thu, 16 Apr 2026 00:46:11 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
