## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:7d3acce778d7db23c4ac116b93822afc5f6f25f0ad6585d2442455a4e7bbb3bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e152d40fd69bf68573ac8c2147276db6d5a4178682513dca14bedaada5118bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156488037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff2d95605f019ea1aab376ffeab291825040741fa46421cbf0c5ac1f069997e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dff2577801ad47dd1f447ec0a9e17f76595381ee7767170b923afd6259f71b`  
		Last Modified: Mon, 08 Sep 2025 21:42:08 GMT  
		Size: 54.7 MB (54731353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dced6aa308eb3e899894dc15fd6846907e2cd019776a2972861f952000458c`  
		Last Modified: Mon, 08 Sep 2025 21:42:09 GMT  
		Size: 72.0 MB (71982544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9ef5723a5a74b2a3f1184f10be75acda749d65ba36feb197247fdfeef7730c`  
		Last Modified: Mon, 08 Sep 2025 22:26:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6d32cf30e1f7fa538e08cacf95d0d5361cfe79ec6f9353b7f1d3d8e7fd1a1eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f743bb220705ddcde1210848a973c8be56beba396f429796d9216f25cc05efb`

```dockerfile
```

-	Layers:
	-	`sha256:57d45c2e5fe2f0f0716ee44f8babb03dcdcb3bd2029748154f7097990a302f79`  
		Last Modified: Tue, 09 Sep 2025 00:47:00 GMT  
		Size: 5.4 MB (5377723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29433fba2ce43bdd3fe1b9d97c6a407ef0972f5f1e20a834dfeb351a958dafa6`  
		Last Modified: Tue, 09 Sep 2025 00:47:01 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cdb8f244b9c54c25260e52422b349b7980bfc19630d1906049e537dc2d74cecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155776190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28a4193a93e3758fd84432879588a6d6940191e1cfc40e4356b82315cb26184`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cfc01299a2aefbcd2528420b2458f8e612ac351a67b5c408207eda11571f5c`  
		Last Modified: Tue, 02 Sep 2025 07:38:53 GMT  
		Size: 53.8 MB (53835608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975396f61c24e5ee1274056200b0f15893c0e6e0aaaecb6ae175983941b5f117`  
		Last Modified: Tue, 02 Sep 2025 07:44:25 GMT  
		Size: 71.8 MB (71803892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c05d2fc5f503ee466ad95b528a6c079321867f6838e6d1f6bb7a64d14f637a3`  
		Last Modified: Tue, 02 Sep 2025 07:44:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c8b210ac48bfb5a63ae2e2faccadbac0f0d671bbdaa09a7bb794e44ee4df164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2246edccd9a33b1597f50d6a1f56eb0ba1fe28a6a44c1b60bc3a132781e12aa9`

```dockerfile
```

-	Layers:
	-	`sha256:e382b88ce54f331f6ec78851cd10750aae5c528582f355d2b51745bf01a710ca`  
		Last Modified: Tue, 02 Sep 2025 09:46:09 GMT  
		Size: 5.4 MB (5383314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184f98d80c6cb1e122adcc2ee9ec92a6d1862e78861ddfa6d5328b95a4690ab8`  
		Last Modified: Tue, 02 Sep 2025 09:46:10 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cf6d7d056f456daccb4279699e0a1504bb4d702367894192c1a84795f45e3534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163148985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c2c6a8e8012ecfb23e171665304a078e61cda426577c6d5ece568cb6b2cbf6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b86b85d8e463227af39e173e64af903231b80321ea222465ddb24d5db1019a`  
		Last Modified: Tue, 02 Sep 2025 07:58:44 GMT  
		Size: 52.2 MB (52165455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f2490f5b0023a1fe4f541e09ce0ef61092086b8cb469e3f6009905babdd56c`  
		Last Modified: Tue, 02 Sep 2025 08:08:23 GMT  
		Size: 77.4 MB (77388670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c979b7b162b609a4fa6d1b97765189a44accb6b94113ff08179702a0d556d5`  
		Last Modified: Tue, 02 Sep 2025 08:55:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:931312eef923a5730b5a83a9a35620501768172dd5de274ab39730a7ecbde764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f70aa4e3b870d09b120329af9670bbe47795f760cdba061188be932bb8a075f`

```dockerfile
```

-	Layers:
	-	`sha256:2c98164b781ff58d49d3c6d4bdea2b37c913cf89ba494388b38a6f85cfb2aa70`  
		Last Modified: Tue, 02 Sep 2025 09:46:15 GMT  
		Size: 5.4 MB (5381811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08da4cfcb53e12aa43d29f83d49c76b887ef60fa0cfc56e7fb434cb9fb1018c1`  
		Last Modified: Tue, 02 Sep 2025 09:46:16 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
