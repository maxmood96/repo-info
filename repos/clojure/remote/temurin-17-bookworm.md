## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:a0df47def64c7b0f683898c53a1b18b82a481fea35c9f86f1bcd15e6abeb2fde
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

### `clojure:temurin-17-bookworm` - linux; amd64

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

### `clojure:temurin-17-bookworm` - unknown; unknown

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

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-17-bookworm` - unknown; unknown

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

### `clojure:temurin-17-bookworm` - linux; ppc64le

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

### `clojure:temurin-17-bookworm` - unknown; unknown

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

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:dd374ca7af31baec435b2abcf55d642523cf8db082d45646c52d6246e8e67ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261957716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b692d10263025573f23fd63302f39fb62aabaff5a3dc14aeac874bdece473f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:03:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:03:41 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:03:41 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:03:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:03:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:03:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:03:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:03:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fd087cd33abb835a3d928d9f2e0a964896748847afaf3e2058ca1eb9f5d830`  
		Last Modified: Tue, 13 Jan 2026 03:04:37 GMT  
		Size: 134.9 MB (134859046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defdb509a2ede5f443a29d03f57f0710512dde28ec0ce27969b1c9fbcd807039`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 80.0 MB (79959202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9360226d790c8df59d556955578b48d53acf61987d232fafff2e523021f9701e`  
		Last Modified: Tue, 13 Jan 2026 03:04:28 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649d11114450695f87373c983f6753f50f13a0470d40e99a104d8cebce5a1560`  
		Last Modified: Tue, 13 Jan 2026 03:04:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2d803acbef18d9450f7c2ae6b1bcde849522ebbbff7c789578bc73890cd5058b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b5ad336864c54a3a4c12e232058da060a83584c0bbfe919667e7d6c94381ab`

```dockerfile
```

-	Layers:
	-	`sha256:a45a005254e8afb4d4a606e8c21169597cd2126d34ee2dc7fd6df596dfc2a4df`  
		Last Modified: Tue, 13 Jan 2026 04:37:21 GMT  
		Size: 7.4 MB (7366854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b25960c55794f823009151d1417b7f45689e3e1ace5b4922bda25fbb42ac432`  
		Last Modified: Tue, 13 Jan 2026 04:37:22 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
