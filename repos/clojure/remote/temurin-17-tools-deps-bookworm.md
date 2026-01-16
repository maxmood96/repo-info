## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:719d9d1a3c2f884316e4f076db4fd1fd2d6817191dd72df8a92839f3f890d1dc
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
$ docker pull clojure@sha256:0be6c50ca5c5cd481d67ea26460711cf9365a65611eba148fd34560082befb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274476579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2a1dee7f5b568ecfc1bf7b7bc77cdffc8cc7a3d33a1eef13ec0ef018e0f487`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:31:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:31:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:31:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:31:16 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:31:16 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:31:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:31:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:31:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:31:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:31:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e7b113b5fe251cfedeffd7d223488e388944c52dc7b1786324c5a3784dc1ac`  
		Last Modified: Wed, 14 Jan 2026 07:43:52 GMT  
		Size: 144.8 MB (144847974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9a8ad28ddcd2e4d2956f48b0cb270cfb3a889c32a94de57ab30c334a61d8ae`  
		Last Modified: Tue, 13 Jan 2026 03:32:06 GMT  
		Size: 81.1 MB (81145945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcf41ba736d7eb447f2c8ef3a9c78825c04a7604298fe9e0e81a8e8bcb57e26`  
		Last Modified: Tue, 13 Jan 2026 03:32:00 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca245ac4bf4a51f7a23d31f014e5488fa243110f5d9f82b81410f3050e03f7e`  
		Last Modified: Tue, 13 Jan 2026 03:32:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4bb3744ebdb2dd9ea8241da87f4ee04b245597d2ac378793638206938b571718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d873d4e7b1394d3f3904ed4552b7198eb1ac351a83e04bf852d1e8f9c71b3f5`

```dockerfile
```

-	Layers:
	-	`sha256:e02889650ce99e3a5502edf6b83c0a582d2a6a8dd0246f9d77a62c962412edc0`  
		Last Modified: Tue, 13 Jan 2026 07:39:18 GMT  
		Size: 7.4 MB (7375535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89bcd5ddf76aea7c6e471b732ad57f351fb9f188e19961e3a807ef6f781e63b`  
		Last Modified: Tue, 13 Jan 2026 07:39:19 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dfaeb232d41af11b441d651203f40a718702e9634ebd5a3809ec228dd1f8e433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.2 MB (273186091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b8b50008cf25421e518b8e3079cacf0dadcc14b09ffeffb4270b876e4aa53d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:34:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:34:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:34:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:34:56 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:34:56 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:35:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:35:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:35:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:35:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:35:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9e499a794c15a07626a606f04b7db6ef8b8166a5812e8cc79eaecf666139f3`  
		Last Modified: Tue, 13 Jan 2026 03:36:05 GMT  
		Size: 143.7 MB (143679916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7798a0bf919636926ca2d0c77c362cb523549c254df08909fa33754ecdea8b`  
		Last Modified: Tue, 13 Jan 2026 03:35:51 GMT  
		Size: 81.1 MB (81139068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee45c6354547a6a1e7560dbad955dfcd26225c1a38f39fcf091f3254c81ceeb`  
		Last Modified: Tue, 13 Jan 2026 03:35:40 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d25f1e6d4756c9a3d786954f2791a644d8bc942b0048015c9e86e186698522`  
		Last Modified: Tue, 13 Jan 2026 03:35:40 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5dc198025461ce1d89692acf5a262d91fa788a4a3e0ab74a3ab6f971346a024f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a707be9419ffb645cf6f2b1c1e02e02b218c2f159e828f0bd610c8e261d8bcce`

```dockerfile
```

-	Layers:
	-	`sha256:d657fb6d4cd07cfa46c37c3585c04f0f468667f3b209dadd53c30c7c6c806d0d`  
		Last Modified: Tue, 13 Jan 2026 07:39:25 GMT  
		Size: 7.4 MB (7381298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019d3cebef139c917b639334f4967b15e607bdb13c1d29d857a8eb5d1b933673`  
		Last Modified: Tue, 13 Jan 2026 07:39:26 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:7fbc49333dd263eb4b909f7aaa452d4793ee6977baf547f12b7a2c0ba9c004e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283840077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4056e30b6193c28d3cdabe515af8f71e5f7d4041005cc668ac6c93f22dcf33`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 05:40:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:40:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:40:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:40:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 05:40:50 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:43:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 05:43:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 05:43:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 05:43:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 05:43:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3caecfdd7b6952c5561a9744f7d3d4cbbf3ec2c42a80cea345e4dce59f22b`  
		Last Modified: Tue, 13 Jan 2026 05:42:17 GMT  
		Size: 144.5 MB (144525182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c15f0c4fdbbe745847ac3cf1c2fdd3fe239b87624156b2090be12b56122b1f`  
		Last Modified: Tue, 13 Jan 2026 05:44:47 GMT  
		Size: 87.0 MB (86986476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f92ec3cb45208264828b3e8ae1f0cac24e20d7ab5ee2ca8366f14de0e1d652`  
		Last Modified: Tue, 13 Jan 2026 05:44:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e47ebac2758f3d7b6cb59464335edf9932211f22fda6cbc2ef611db6768b576`  
		Last Modified: Tue, 13 Jan 2026 05:44:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9963db5b217816396a8e71fb84c41f6a6ea85385b6d631808be250cd0e920259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896fefe1e2ab918f5d939b2e6fd8a9af49a6a6a0644f2b81c279b17b11ac3829`

```dockerfile
```

-	Layers:
	-	`sha256:8aa2f961506a21ec8687043667fbf879e61617b812fc78744bf6916798c9ad48`  
		Last Modified: Tue, 13 Jan 2026 07:39:33 GMT  
		Size: 7.4 MB (7380751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60c50d3ca3f1c70f7752b937db06569df858f71c1252da05311c14e98b4854b`  
		Last Modified: Tue, 13 Jan 2026 07:39:34 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:168ed1e1bb5a9ed76067d1d325853beca3e68d3c1bd16aa9bc487f0df7d34fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261958515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d866db024a81c97be0e2cbda1c027bf7e91f5f34846ee6ebe87f180476045a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:15:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:15:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:15:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:15:50 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:15:50 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:16:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:16:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:16:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:16:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:16:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a4e65f91bf8fabfb37d94cb2c3f8147c2abb08a57ec48a145b2bddba56b56d`  
		Last Modified: Thu, 15 Jan 2026 23:17:00 GMT  
		Size: 134.9 MB (134859767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377e17a49b03202ef7a5ba5e9248ec99fe2ad4613f7e0ff512b00dfedc07b8af`  
		Last Modified: Thu, 15 Jan 2026 23:16:49 GMT  
		Size: 80.0 MB (79959275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1855b225fb62fdd93c5384f76dcedeb1dbe44cc82db97777350f5a110b9685f0`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398b7bb38f97c5859ad6d607f908fe8d7a125b01c1e8b3c66f32cae675ce512b`  
		Last Modified: Thu, 15 Jan 2026 23:16:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e86cbc011f2a45038648fd0b668291ae765b9be6f9aa0f717feef5d9aadc461a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ceb08baaa67ba8f690b6a3f6de76bca67ea307b5ca0f1177bee9ac357d58b0`

```dockerfile
```

-	Layers:
	-	`sha256:3b6764de5e8f4fcd545697bcf38196cad2eb25e06a9c4d773108affe305181ab`  
		Last Modified: Fri, 16 Jan 2026 01:39:03 GMT  
		Size: 7.4 MB (7366854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee4572293d593f4ab2a8c4269c6ceddf8c1db909d163c15076a1a1c225311a1`  
		Last Modified: Fri, 16 Jan 2026 01:39:04 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
