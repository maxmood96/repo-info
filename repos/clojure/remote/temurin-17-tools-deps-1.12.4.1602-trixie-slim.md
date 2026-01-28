## `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:282b0eb6fcf93d7d4ffaf641ce74f795e0401574430001d68696807cc9b5486c
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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2e8f7c8d0ccc30b2d2a28bce9eabe665a9579cf213a0be1d9b03698bcab5a60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249567206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96306b142592beb43396d45bbe894fbe8f53304e58da6e5526ee52ed970f5c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:05:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:05:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:05:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:05:17 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:17 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:05:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:05:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:05:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:05:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:05:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4089e0f991dc4e8ce14be18f139d9eecf3f20eb4d04c5236ed77279a49eb2bf0`  
		Last Modified: Wed, 28 Jan 2026 18:05:58 GMT  
		Size: 144.8 MB (144847905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77ae2465c317cc4424bbd786e7486fcc8f556ef9a7aa9c5c7c53f05c34257fa`  
		Last Modified: Wed, 28 Jan 2026 18:05:56 GMT  
		Size: 74.9 MB (74944574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4f39d081a5b581188ec654dc495f8e9ad44706a75a1801ff0e615b8a6ab8a5`  
		Last Modified: Wed, 28 Jan 2026 18:05:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94106ceaa00bd3437330c8d29f7251510166d1b14f6f3ab47df21f72e2112c30`  
		Last Modified: Wed, 28 Jan 2026 18:05:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:85036c23b1dd50c8eb520a3643d9e51933cdfb9b6810ef7107062600ba8aa1be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6bb87b7759435fabf0b2d5cd9a0abf61de27338b9b069f10feaf27edd4fab7`

```dockerfile
```

-	Layers:
	-	`sha256:d31d9dab9e659a89c4e21680e994de151d280b98701f3639cdffce6837ce7e4c`  
		Last Modified: Wed, 28 Jan 2026 18:05:53 GMT  
		Size: 5.3 MB (5256299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:214e90c1eaea3616d4b71247b57097b5beb2038da2884374d72447815d90ecf6`  
		Last Modified: Wed, 28 Jan 2026 18:05:53 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b26ea8626cbc5f8173511af4001c9487909328efffa995cefb6e095dcaed2f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248936752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7276112972551e77c35b6d6f16b905dd30bdf367504cdbb141c6abaf2a07e4b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:04:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:04:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:04:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:04:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:16 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:04:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:04:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:04:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b540c0925610289c92c3fd81f1c6a5b297d5e9ed40106fb0cc3c479446bc01`  
		Last Modified: Wed, 28 Jan 2026 18:04:59 GMT  
		Size: 143.7 MB (143679942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6fab64570805500a4dfd7899786e0df32a1b002a9aa89d48eb0b107bdf0d0b`  
		Last Modified: Wed, 28 Jan 2026 18:04:58 GMT  
		Size: 75.1 MB (75121727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5417f90145ca326fefee38717fc2728288f7535c596fcdfc88a343c2d1d4ee2`  
		Last Modified: Wed, 28 Jan 2026 18:04:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402ea3f61b738ecd21441ad88e13151e510d6615a8c938314b0255207d146555`  
		Last Modified: Wed, 28 Jan 2026 18:04:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a362509d4fc1f5e19e1c52d325f85cc4a10b5ac1bd042bf6caee31294ac8c0f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5302c32946ecad0e8535cd86518e765381eb1a82de22e6d28958e1352ae245cf`

```dockerfile
```

-	Layers:
	-	`sha256:211301e1c239ce6f444f49440d26e27a48654334a63683996bffe1822d07514b`  
		Last Modified: Wed, 28 Jan 2026 18:04:55 GMT  
		Size: 5.3 MB (5262068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee4d3eca607e8f9e467fb9107b2115c6e287080ee5ebf54d8eb0eae93730bfe`  
		Last Modified: Wed, 28 Jan 2026 18:04:54 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:073215bc499ea8db419f891e8e564462e4346dc6b66e838c98b18e7ef0b59827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258712013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d04a8846aa3e01c2bb14dfcf43a25ab9a34d819025130b9e2eaf760fbebcd23`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:26:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:26:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:26:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:26:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:26:07 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:26:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:26:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:26:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:26:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:26:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7f3b48545bb26df22f8fc2393ea26e698fcaf9b03a0325d1f54c82ad63d640`  
		Last Modified: Wed, 28 Jan 2026 18:27:38 GMT  
		Size: 144.5 MB (144524726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4371e7d439aaeee5763724cfe6ca662ba97c39273e7a322c77140016ba94997`  
		Last Modified: Wed, 28 Jan 2026 18:27:37 GMT  
		Size: 80.6 MB (80590643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318373384cd2854e885994cdf90a78546a366b51f43278ea2d1216910580612`  
		Last Modified: Wed, 28 Jan 2026 18:27:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41afa899bcea092352d79e4473b3f2a4607fe60ab567fbd9bf0940e02dd79d79`  
		Last Modified: Wed, 28 Jan 2026 18:27:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cf60d51b876dd3f0fe33c3bbef4d0d5376bffa7bb4fc55a93c2a5712c065091b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7869ac237e0088480d2cee86ad5e59d8400d30aed2d8782a4f94c772cf8446ff`

```dockerfile
```

-	Layers:
	-	`sha256:91d1ceca2a2410d4db48665ec082794279c5920d673b6f4e3c1255b64c01879a`  
		Last Modified: Wed, 28 Jan 2026 18:27:34 GMT  
		Size: 5.3 MB (5260670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330cb8ff7feaf0eca2842c20ef2f55bed2c55757ced61171c1f46257f3488eae`  
		Last Modified: Wed, 28 Jan 2026 18:27:33 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6865bee3e4a224e873621287e09109180e2a0105660b5f3845526dd9fceb0ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240261812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f067134ea048c4935008f27f7ee775aefb02b219fe9aadb8130668cf0678ed03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:15:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:15:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:15:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:15:43 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:15:43 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:09:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:09:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:09:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:09:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:09:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee861ab10085b97ec9d76bda4b5655283ef0733479ff9f05457f5ce5423d4a64`  
		Last Modified: Thu, 15 Jan 2026 23:16:23 GMT  
		Size: 134.9 MB (134859759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec84d75678561fd0966eb79d590e8933e04983f520c146ac811d88e69b29019`  
		Last Modified: Wed, 28 Jan 2026 18:10:02 GMT  
		Size: 75.6 MB (75567603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912cad2c15c506f7057e9f938a12aff238d040c3a759b47ff7096d30737cad91`  
		Last Modified: Wed, 28 Jan 2026 18:10:00 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64b5fc24666d174c4fb84ab41324003dee78e7d522f3db97164df31d477b6f2`  
		Last Modified: Wed, 28 Jan 2026 18:10:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:992b219841efc3cfe11653807acb2e7a4032820d0ec3bfb534736a1d4b0b5f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d514e8c95bd88b32f5f9ebb4a41a8daad7284439185fa5bf78fcae4fba0ca5a4`

```dockerfile
```

-	Layers:
	-	`sha256:5844082b103acd4473a206715f374f79b652bc4a198576fd7caf178f2e9873e3`  
		Last Modified: Wed, 28 Jan 2026 18:10:00 GMT  
		Size: 5.3 MB (5252223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270805744741de4e4b6a511385618da4dac6030d59db446701225414ae322bd1`  
		Last Modified: Wed, 28 Jan 2026 18:10:00 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
