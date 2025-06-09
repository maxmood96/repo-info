## `clojure:temurin-17-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:2e1c040735d8bed695825f7936e871a99ce0bd3bb85637ba4177dc4b1fe5cf7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1e854d69339376a1f5073a1c33182ba0c847c73206306ae2a4a6c61a75eb8349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282089907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f96897a83f73f37d48dab8011158a8bc6689d55988cd22842cf9a477a46083`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e513432e22464bd7da0f7fcd93fdb45bb58bee3d06b2c36bf82260f9706122`  
		Last Modified: Mon, 09 Jun 2025 17:18:16 GMT  
		Size: 144.6 MB (144634949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed4a8c26311bf388a240f70cd353266e6b2a863f302b41c9db99b51fe8f471c`  
		Last Modified: Mon, 09 Jun 2025 17:18:19 GMT  
		Size: 88.2 MB (88207009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c00823f4be82f5f959b95855c3f34b95cf01920f03405199dd3ede0882bfbd`  
		Last Modified: Mon, 09 Jun 2025 17:18:15 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b316b9c213c8f33a5959bc43dbc7e0159d9a7e2a18a91e05c32f87f30f75b556`  
		Last Modified: Mon, 09 Jun 2025 17:18:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:67cdc78880bf8a8c2a504bb1aab31b0eb6c04bb769ccdfe8e45709611ba81e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120206ec7204b4fcaa377493977c0a4f60bb95e4a8b8f4a3b589bd9bbd791047`

```dockerfile
```

-	Layers:
	-	`sha256:68e0a798ecb8455ee429a4f807b5593826b455d4508cdb8b67c94d762f65d34a`  
		Last Modified: Mon, 09 Jun 2025 18:38:19 GMT  
		Size: 7.5 MB (7458635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8a1ad929f49b58414a16db4a8f67e7ee61046abf9045b9d27dc1aa51ccd6dd`  
		Last Modified: Mon, 09 Jun 2025 18:38:20 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04bb6716f76b16bf6841bc9f18efcd9242a45c4342b8f69e04f6809304e3fab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281643151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e71c64fd94b15a30ec1563d767712e1d8ea558be3713c879d4d7abd9bd611c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0716c0c482281cd83847775856a8d2b5dd899b670a27f613e6c9f63273d5d058`  
		Last Modified: Fri, 06 Jun 2025 12:50:12 GMT  
		Size: 143.5 MB (143512625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b20f106202c77c1226f8e33ccae56ec009989ab360ad9e78cc99a5d4b2a32ee`  
		Last Modified: Mon, 09 Jun 2025 17:50:21 GMT  
		Size: 88.5 MB (88511193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90f199128bc83ec050fbc662c91877c7af5995082fff9033bb3d02413e7e5a`  
		Last Modified: Mon, 09 Jun 2025 17:50:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07d627a61b498b34c942e540c7ab53ec7da5945558446168fa8eb0ef7948db`  
		Last Modified: Mon, 09 Jun 2025 17:50:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fbe14280fc10e3d7659cb15c758eb8e6f74b8519e0976f39e32787fb5acda473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0772b79940a12e59532346638d31b3f42236ae2e98147997bf51f5ebe2a601`

```dockerfile
```

-	Layers:
	-	`sha256:1c4c08c8bede2f4275a8b7478dcd3745eca9d8438e92a90debb20c3e3c4ad55c`  
		Last Modified: Mon, 09 Jun 2025 18:38:29 GMT  
		Size: 7.5 MB (7465665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f684e5a16efac745911be855112a1fc964ea04503a863b79b280fd33cad677c9`  
		Last Modified: Mon, 09 Jun 2025 18:38:30 GMT  
		Size: 15.9 KB (15914 bytes)  
		MIME: application/vnd.in-toto+json
