## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:843ac0bf35e069562dcfaead07e5f1379e4eba78ba57d2163ddecbe4caebd29b
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:70a69a3ec30d0021cfa9d78b99a63e33667ff9885651affdeb3cd1e19533e29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256904963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957ad43125d6f5313a530fec7a078d18cb5872cf24e7258c0e3dca5aaf0e03ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:15 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:20:15 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:20:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:20:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:20:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:20:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33efa46ab61c56f8562346a487b2cc91be18238eda6ab672370549a02fba706`  
		Last Modified: Thu, 11 Jun 2026 01:20:54 GMT  
		Size: 158.2 MB (158166925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e2bacc5c1efe6f61ec9aa99d2fc5114189e1caddd383cc414072955c357c90`  
		Last Modified: Thu, 11 Jun 2026 01:20:53 GMT  
		Size: 69.0 MB (68951586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd995e703b0b8c799fdda8d68c9aa67f681098a3965e941dda1671572dc278e`  
		Last Modified: Thu, 11 Jun 2026 01:20:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290736e770b93ea606f12085203fb03bc5721b8c5e97c8792873c17d1db3ac6c`  
		Last Modified: Thu, 11 Jun 2026 01:20:50 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:603e287fb9f9d8a3d41c01cc330067806c37355f11000dedae687e68831d600b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f42fa5ccc03e60605290685598b03365e1a453177e94df1ac827b71d2de4eca`

```dockerfile
```

-	Layers:
	-	`sha256:1ceac42e2462174d80a647ee532c15b11fc4aa25bd7d88d7af5db0399ac01810`  
		Last Modified: Thu, 11 Jun 2026 01:20:50 GMT  
		Size: 5.3 MB (5259094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc32baa10c04f8c58c6dae841bb693a525d6650c271519477a7d477feb841493`  
		Last Modified: Thu, 11 Jun 2026 01:20:49 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:698db731b6ca62283a180a1e1355481f9737d1306c80428d45e1951988351acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255388427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60604300523093994649d9b9730f8c9f82947f8230ff4a8275c7c43b04e542c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:24:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:24:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:24:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:24:11 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:24:11 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:24:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:24:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:24:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:24:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:24:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92614660574d51736c3e9ebe84c78276c9c9806e74def12595865b0493c7a137`  
		Last Modified: Thu, 11 Jun 2026 01:24:51 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3025abc295656e1c69476fbed0a069a3b36a5788902c2330271bab324536918`  
		Last Modified: Thu, 11 Jun 2026 01:24:52 GMT  
		Size: 68.8 MB (68777533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1f68aef8adb5d2351325ddbbe49170eb41551a3e0784001fbd018cd0446db6`  
		Last Modified: Thu, 11 Jun 2026 01:24:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3145bac13d61d25ed3790b28217854dcd1d4cad64d6a1d209282af78371a451`  
		Last Modified: Thu, 11 Jun 2026 01:24:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4b076d067b5d6477027fd89ead9d3e4624f4477f377aa433a71e2cc9045d2b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c58552409249ad3fb657b8ec0b3578548e9c3213692ab1118cc48d3e194a5a`

```dockerfile
```

-	Layers:
	-	`sha256:d02fc1079f23e2b90a1cd03eac963022479a994b61a3dbd20ab616c42372be71`  
		Last Modified: Thu, 11 Jun 2026 01:24:47 GMT  
		Size: 5.3 MB (5264855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e685e1a9dc1984ea431d12bdae09e5424740ca0996dee71767e43b5b4a7496`  
		Last Modified: Thu, 11 Jun 2026 01:24:47 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:73c712dfe4fcc7e6ef76a455f30832d2146afbaad4b388524bd14961ccc7fecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266319511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5b4525ecb7a31e1f6ce9151b6d91fd044a848ff198387c6465bdd223287550`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 09:38:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:38:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:38:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:38:46 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:38:49 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:42:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:42:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:42:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:42:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:42:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c6f1693c2d1a740f7e38923550d778aebd862c314039e0dfef07d577243eb5`  
		Last Modified: Thu, 11 Jun 2026 09:40:09 GMT  
		Size: 158.3 MB (158343198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d58fccf9b39e002eb6651e2642ad40890dea7fa983716795aa073d7e0a15682`  
		Last Modified: Thu, 11 Jun 2026 09:43:26 GMT  
		Size: 74.4 MB (74368933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86e0f699da94fd2ad2d18f1ae2211a418380d50c26ccefc90bd1a74f1f03d4d`  
		Last Modified: Thu, 11 Jun 2026 09:43:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4301b5daea0cba3082800d2e70745ed644ecce53014802b8620ac9cc70621709`  
		Last Modified: Thu, 11 Jun 2026 09:43:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:07631b59f5839d5789244933eb5b13dc92fd6929c1a76c0a0adf1ce6f4d66722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de13a65f6c874968aea3da2be69de70e3e12edb9a999408ab11430c57b35522a`

```dockerfile
```

-	Layers:
	-	`sha256:65a9e80a40f4dc7cd09b41c0b197d35251220aa689800b1e0955f9ccdc7e2099`  
		Last Modified: Thu, 11 Jun 2026 09:43:24 GMT  
		Size: 5.3 MB (5263465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f4c9eb036ba2086773ded2dee2fe5cd1a3a38d837068a0edbcd95cca90e699`  
		Last Modified: Thu, 11 Jun 2026 09:43:24 GMT  
		Size: 15.1 KB (15059 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:afe380101f0c9dadebacc32815417052cd4fea3213b832d5a104eb69e521aae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247173173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7624e71661d95efc771732f6d304f9fd0f4c10e56fb55ca177fc8fdaad87bd67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:12:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:12:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:12:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:12:07 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:12:08 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:13:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:13:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:13:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:13:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:13:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fe9d476bfc26aecb65233f2a84a64c452218d93474e5ac0581302972abb9cc`  
		Last Modified: Thu, 11 Jun 2026 03:12:49 GMT  
		Size: 147.4 MB (147388365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e96e8e5d393cdb15f7ac1c890bf9d8ab60e65815a5fc7193746bcf9a96668a7`  
		Last Modified: Thu, 11 Jun 2026 03:13:52 GMT  
		Size: 69.9 MB (69932414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87fdf635a17538fbc4f6ec14268d661da4f087b8e4699d98ad2191235ec4c3b`  
		Last Modified: Thu, 11 Jun 2026 03:13:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4013add0521cdc89332f8b1f166501035a726cff458b5bebd4e3f7ff33b35`  
		Last Modified: Thu, 11 Jun 2026 03:13:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f48296eaabdaafd6f9017d7cedb7d9b995312546f43d35f6186637880ee27f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e7c2c26483dc651176c01142a9f7bc5be937064af9ed2b96c45cb780aac508`

```dockerfile
```

-	Layers:
	-	`sha256:e3746bc33dd7c99ed309258b0d68f0d8defe996d3829d001a87c8752c0da3aba`  
		Last Modified: Thu, 11 Jun 2026 03:13:50 GMT  
		Size: 5.3 MB (5255018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d0a8e074cd7e8a2bf8d144112f9a0aaeb57952bd5eb0b86d02320bd448fa24`  
		Last Modified: Thu, 11 Jun 2026 03:13:50 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json
