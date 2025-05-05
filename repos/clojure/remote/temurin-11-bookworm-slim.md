## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:2b0825ca89bd01b5c95070cd713acb1d878643032c9b430527608599ec74e10a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c9ca7c1c38e92537fd9aa8542733efbb5823f318689c00204050a07a606cacd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243389590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6264c92494ffb11a3e3381ea0a843fcb189f19d639d50393ae97232c775621`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a333dbad3be2aeecd0c6a4a552c3e8d84fea1b4142a3ff171a6a8902ab425069`  
		Last Modified: Mon, 05 May 2025 17:08:14 GMT  
		Size: 145.6 MB (145635746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080d79ea9338faf9850096c9f90ba4680dce1597948b8cdced969b94da356625`  
		Last Modified: Mon, 05 May 2025 17:08:12 GMT  
		Size: 69.5 MB (69525557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5eb286c3d830d23bb3e4ebb91887e4f99f9f685b0be59c315b408c6412e6e37`  
		Last Modified: Mon, 05 May 2025 17:08:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:355961dcf034c09d56c412ede13eec24d3c302f74051e1a2804793f30c8050fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4948415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2a0d94ac07d1ebdc4c57d713e38ee5ee67d408063562bfdd0662d593e0982e`

```dockerfile
```

-	Layers:
	-	`sha256:1b7c73dd68320c71d30d12a01852bf9c92ddd5c5d627809f265e112671f2f873`  
		Last Modified: Mon, 05 May 2025 17:08:11 GMT  
		Size: 4.9 MB (4934106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1be6785bf86e516edb9059e2f362a7d2fb8182dfd61797850bc69392aa797c1`  
		Last Modified: Mon, 05 May 2025 17:08:10 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6538d52b15792cadea0ae0107a77c24a3495502827079a5dfe4b7471cf806074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239867113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3353567fc91566a9ee255d8ee547983e6fff42640d32effc97610129a0f34851`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c590bc49e0fce8ff6e7cd73ad8b2604f230758eb3bf03d878908c54e73ce598`  
		Last Modified: Wed, 30 Apr 2025 01:05:20 GMT  
		Size: 142.4 MB (142422077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d73989978d123cc8f83f0bc37e03f73694b369b71092fef032e5e587c5b49c`  
		Last Modified: Wed, 30 Apr 2025 01:08:19 GMT  
		Size: 69.4 MB (69377770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3ad7e61866eb593e2c97e5b4e6dfc1d2c2df989c7a9190ceaf8c8fade88410`  
		Last Modified: Wed, 30 Apr 2025 01:08:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c1249a6161464a6c44dac75950eb9fc63cd86979d52b61058cb9428d10d59f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4954913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd33744776d1c7fec142bcb07278aceca9c3c1ffb9b54492cf852f2a5bfffb6a`

```dockerfile
```

-	Layers:
	-	`sha256:5edd94bd56a1dfac68cbe98957aae4ad702ee28fb852cdc3569412c323cc0aef`  
		Last Modified: Wed, 30 Apr 2025 01:08:17 GMT  
		Size: 4.9 MB (4940485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea8916a28fe0bfde5e977237fe54d5aad82fc740e5d341869a7bc9da95250c17`  
		Last Modified: Wed, 30 Apr 2025 01:08:16 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
