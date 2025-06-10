## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:ad7707e88a11ff422e459e4052fe533c9e608a4ce14ce931cb3278aa174ac30e
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:63205b7f0bb8ef497437bb3aa6a6aa2a8a16bbb204f0bf4cf7139c84ef20890a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274117885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7b9782f22e92c1f59d2bc8629b5f7acd5b1d3d6c557d45a65fbb29396a2d5a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baec0f1956e0bb036228054c2dee06347828e7043c017da027a6c7706306de00`  
		Last Modified: Mon, 09 Jun 2025 19:42:34 GMT  
		Size: 144.6 MB (144634963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce82f8cd4adc2106763fbe3d1d0bbc7c3a62f8eb7a756dbee5314282bee5fa16`  
		Last Modified: Mon, 09 Jun 2025 17:19:06 GMT  
		Size: 81.0 MB (80993636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af762ea5b6a93166d49a2da612faf920bae6f3346773079c628c1cbd38b9756f`  
		Last Modified: Mon, 09 Jun 2025 17:18:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c21a3c8477896b4567ff9d24a9091ad2fe7947d1fa27d95c6803c7504e55b09`  
		Last Modified: Mon, 09 Jun 2025 17:18:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:60ad58c7150aebb3acfce0da39f5e6c4cc2caf218c704035f3a383fc2998f9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89b3147c8cd67062e2f5747f0c60638c6b415463ef5871be9c1e2f326f55b1b`

```dockerfile
```

-	Layers:
	-	`sha256:8837f75b084e08ee0918a84406b1a8360320c77ac0e03d354c62a219ce5d42e3`  
		Last Modified: Mon, 09 Jun 2025 18:36:56 GMT  
		Size: 7.4 MB (7366912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb438db498b2455677d0a05476916cb973d41262a2573dacf769cc356eaaaa9`  
		Last Modified: Mon, 09 Jun 2025 18:36:56 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f9acbcb30595447404feb62cc08624be167ff25d2d9973c64944118781d64f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272689746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bc76749e5f56aaa35f90b13502400c03b5ca9cfdc0706f183a9f67de358866`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d616bd6f18b21e8af2a1fae7e0a03786fe00872c2eb14456c4dc4039bfa80bd4`  
		Last Modified: Tue, 03 Jun 2025 21:49:58 GMT  
		Size: 143.5 MB (143512624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e983003ee99b66b9a932c65c15dbb32a1607197c438303a96a0d4d33c92446`  
		Last Modified: Mon, 09 Jun 2025 17:45:41 GMT  
		Size: 80.8 MB (80848898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b446bba9216c6ba2a354abe409d08d5a7bdb014264b5dd0b67e98124d9c8150c`  
		Last Modified: Mon, 09 Jun 2025 17:45:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a30b8e3eb5e8f181dc17382489927c9607523d8264376bac4f9c0c9632de18d`  
		Last Modified: Mon, 09 Jun 2025 17:45:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4ad4f9e406dafe57afdca8596e47b15540b7230929a7d923481a4751e25e1b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126db867b4e1a9d025089d0134b2e8354ec47d583accd931c9bae82b9b00a0b0`

```dockerfile
```

-	Layers:
	-	`sha256:4bae086015aa9791b5798804fb06f5c8dd5a3410aefe91d45b774aa81e934964`  
		Last Modified: Mon, 09 Jun 2025 18:37:02 GMT  
		Size: 7.4 MB (7372675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b864199416bd7e4c1583b9abf756df3561e5b45bdc00a12270f1fdc005b4a3a`  
		Last Modified: Mon, 09 Jun 2025 18:37:03 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:1ddb395b372b5ecf3deccaa4fd5c2621808eb975ff40e5c06401c9a309f6fee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283426441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e11804c6fe93af4f972792c7e326c7f21845d05bc41902667fc8abf4b1e123c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5fca0800952ffd845ecae7a757898651fb9b497615be2e0d7662f4d7ff229e`  
		Last Modified: Mon, 09 Jun 2025 19:43:33 GMT  
		Size: 144.3 MB (144280554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fdea58503233f896127597d21f161ec301bc856ce033344292ddcd6bd38502`  
		Last Modified: Mon, 09 Jun 2025 18:00:37 GMT  
		Size: 86.8 MB (86813226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bea87ee18ff1be50f0396c76d67fa9c1eba512c6032f32c6e520d6765fdaada`  
		Last Modified: Mon, 09 Jun 2025 18:00:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8b3ed57cc76283b5b87d609764bf401310c7c4a695ccb82892a893e9431864`  
		Last Modified: Mon, 09 Jun 2025 18:00:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:50fbe7b58b4b86a28e121510789cbc1ee3712e049e4a29f0d6fc4871d0e8d066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf14d20e2d316effca5768ab922b1d435938deb78bca90c97c3c1e07a3f90866`

```dockerfile
```

-	Layers:
	-	`sha256:6754db586b259742bec60940edbadbadac8487eac54092b2d62fa67000b3609c`  
		Last Modified: Mon, 09 Jun 2025 18:37:09 GMT  
		Size: 7.4 MB (7372116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa7b311840839cf04c14a4b62b6c23406a94459f9de533d283234e2219bce9a`  
		Last Modified: Mon, 09 Jun 2025 18:37:10 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:7c61b073086313a3ee60f1bdcb0e99267fe4421b777f07a00e3804303c44f01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261621013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dfe40c1231897623d5a9a20d1f6a7499aa52c2741e56f72ddb8a57be3a98b48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f22e4165e784cf5cf4630de4aad9261205dcd457d5c03fd507e8f308626656`  
		Last Modified: Tue, 03 Jun 2025 06:12:24 GMT  
		Size: 134.7 MB (134673548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b21ac63ed4cae304da8bdd49ded5dcbaf185f3c3ff93e00bd0be4113e96b74`  
		Last Modified: Mon, 09 Jun 2025 18:46:26 GMT  
		Size: 79.8 MB (79802580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19d84777d1d84e3706153a4077829c9a2f5a954a26eb1a79cb4ad8d2df7eaeb`  
		Last Modified: Mon, 09 Jun 2025 18:46:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93176d3345f6c59c27b673170b2a9ae30ff67dc1ad736557526498d49f2dcb59`  
		Last Modified: Mon, 09 Jun 2025 18:46:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:aa00a4a7c7c42fe1727eb750afee9fbe4a1ec95f10218f6d5972693656dc623f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7374052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976be0124d63ad04c06f2eef3afb2c19bc314bd75517718c1080dd209a1a1f75`

```dockerfile
```

-	Layers:
	-	`sha256:1275da7c6d1c54553c2baaf1a28fea1ba94fdb79d9e9306dbb3ea84a69c69232`  
		Last Modified: Mon, 09 Jun 2025 21:35:55 GMT  
		Size: 7.4 MB (7358231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc89e5752ea2b8f6003012b470facb960a65a7343069a15c793fd99742041b8`  
		Last Modified: Mon, 09 Jun 2025 21:35:55 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
