## `clojure:tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:37dd8fdc770c6c420dc38f7166bae0e530f9d5843cb45adf645330cd4e31e138
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

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; amd64

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

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

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

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:659a4532bf4970e58eb7b5f02d31ff6043b9cbdc583d901c757e0588b60f41a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235743586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14d261e662f9658ef985d4fa00d3190f53f4d2c245dbe606a3ba81608ad3d9d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:45:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:45:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:45:16 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:49:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:49:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:49:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:49:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:49:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669e63febae223cfaf9f384c28d5a36e001b69caed965a3c664ae01f400a6a0a`  
		Last Modified: Wed, 22 Apr 2026 08:46:44 GMT  
		Size: 91.6 MB (91633138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee6e5390f6e8e171c10a0f43b15a2632e3bd6bd8f8e68a2bdcced07f5a6994`  
		Last Modified: Wed, 22 Apr 2026 08:50:12 GMT  
		Size: 91.0 MB (90986423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f043b4063cfc44b3b9d3ba522f4731af7512aa5f7944817a02535fd3e2f27029`  
		Last Modified: Wed, 22 Apr 2026 08:50:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d60cb415b6edb2da2104973891d195d8724a9a42fa29cdc790f810ac9bbf22e`  
		Last Modified: Wed, 22 Apr 2026 08:50:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0ccf96d41b423f0b1adf266d145b8de68e90aa8dfa49872a4fe85a92d3f264b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7443005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8eea5c9c9ba34da5c3d6a6f20ba61fa883159585d98f246997261f22a1cd36`

```dockerfile
```

-	Layers:
	-	`sha256:d9aa87d5942be251be4274681f8dfa356053618d08f0785ec0f3f48617efd0b5`  
		Last Modified: Wed, 22 Apr 2026 08:50:10 GMT  
		Size: 7.4 MB (7426532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:527213f853b14b95183a1f65bfa123878ecad97ae33baa17a3544b28c0cefacd`  
		Last Modified: Wed, 22 Apr 2026 08:50:10 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; riscv64

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

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:106d65bf4805f47157cccd342d5059a9deb8c61a6acf7fbe11982d8715307ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224151869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e385b980e509bc8e107cb46f2acc186af1a57e3bd1eb8f05f414fdd9b8004163`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:05:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:05:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:05:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:05:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:05:13 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:06:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:06:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:06:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:06:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:06:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2851cc70aaa7a2aa35ae1940ea4e1870bc73e44a0f31cc961e77ed98cafcd686`  
		Last Modified: Wed, 22 Apr 2026 04:05:53 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55df8e27a38151431e87c272c6e7b36f149992a1c020ce017ab2a6aa655e882a`  
		Last Modified: Wed, 22 Apr 2026 04:06:55 GMT  
		Size: 86.5 MB (86544897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb7f73cc16fff78a99604c20b99c6172781d3dead60c6a9f123b7ce48d9bec8`  
		Last Modified: Wed, 22 Apr 2026 04:06:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4190d6c568b6a4d8d44fdbb1767968ff7a35332e7de8d255e7fe1fa625dbc4a2`  
		Last Modified: Wed, 22 Apr 2026 04:06:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:72dfe7262fbf4834826467b8b5179dfadaa9c02f05a4c3c6bf5564be7cd5f994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f33b779cb4435c3c5cff873ffee4049d2c0ecbf744855f9909f4b3e44f15b5`

```dockerfile
```

-	Layers:
	-	`sha256:8b7af9d65ab33c3dc779462ef635beacff4c3e24edd3059e540c427f69855ab7`  
		Last Modified: Wed, 22 Apr 2026 04:06:54 GMT  
		Size: 7.4 MB (7419271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1879626f5f16c841ab59d0b049d7ea456687b7bd2a3a4c3aeda484850bc5384`  
		Last Modified: Wed, 22 Apr 2026 04:06:53 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
