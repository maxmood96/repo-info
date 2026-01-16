## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:829a67bced04fbe00c384254204ebd72c179ae9c62f3a5a9a30d5ffbbc71a724
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6630fcc42317aeaedc5a3a3958ec3e9e2f4ed53ed0afff621137770db63ed652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274595093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71931436f6eb92bdf149e787dbeadc2a00112df67f173255c6d8b16bf5f36d4f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:23:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:23:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:23:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:23:00 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:23:00 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:26:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:26:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:26:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2b2540b9d0847be9dbb4faf0972c1e6ce6f44bcc50210c3fe218d19943fb15`  
		Last Modified: Tue, 13 Jan 2026 09:49:19 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe95b68fbc6d51643f8c1f091f6cc7d932fafb08af85919b6432c108d6d4b163`  
		Last Modified: Tue, 13 Jan 2026 03:27:10 GMT  
		Size: 81.1 MB (81146174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d390235ade5bd5b48103ac6f4b9a2948f5f3d480f2abd49da207f93adfd60114`  
		Last Modified: Tue, 13 Jan 2026 03:27:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:37e7369c9bc14d1dab75010b4fde1ed035adfd9e9468081010edb39892454a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9660d5df0f89240757d7f036e9adbd43f978718f518e72c76d70d8092de6403e`

```dockerfile
```

-	Layers:
	-	`sha256:297df11ec921be656e599c50663fa83475478fa083a838cfd3d7a53a1d560efe`  
		Last Modified: Tue, 13 Jan 2026 07:36:38 GMT  
		Size: 7.4 MB (7395674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efc8b33581f0f0b620bd51dadb3ab170b5651db825cb36b0cb61bbdce820b4f7`  
		Last Modified: Tue, 13 Jan 2026 07:36:39 GMT  
		Size: 13.4 KB (13408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78ca6a4c5206a6b683f5cb4b3dd7614ff807bdad504e3004418c34dd87a9529b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271237363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075d62d0b4acc448891a613cd465bd7eb80156b4087bccb7c06b3ee128c49b0a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:30:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:30:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:30:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:30:55 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:30:55 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:31:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:31:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:31:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6f262a3c2189b9cd0384a932e6767d2852f8794e1b6f1112dc289767526e4d`  
		Last Modified: Tue, 13 Jan 2026 03:47:51 GMT  
		Size: 141.7 MB (141731561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ee9b9f92a9554da4e9c14e1c989f164af848bef769ec161a9676b73d6c533a`  
		Last Modified: Tue, 13 Jan 2026 03:31:49 GMT  
		Size: 81.1 MB (81139087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e34a468eb1cd1d4bb9323d8092d5ca8142dc98ddaa6e86a6bf9238c46a4b7db`  
		Last Modified: Tue, 13 Jan 2026 03:31:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:be3f4e5f008738df081184eb2e8f3de7d3ef2a7f9d3a0751285ff2ec36bb9bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802612c89b4cd39304af10a414b54d6d6d534751a40670d8ac966d40ad6e3cd3`

```dockerfile
```

-	Layers:
	-	`sha256:5be5c59e01aceb8e0284898be8ba8f1de60f7149b04cf777f267a326323cbdf0`  
		Last Modified: Tue, 13 Jan 2026 07:36:45 GMT  
		Size: 7.4 MB (7402055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d63575659ff91d2865fb0f4362b52abf00c84e20d6a14f3f27cca2721c713b04`  
		Last Modified: Tue, 13 Jan 2026 07:36:46 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:bae8b5a863a3e116890f7c0041902e15b69cf432d1edb534b08294f758065d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271396639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a896c4b027ec9714cbe1b236bec2e881962909c86d4d80b56b995ae350ee7e9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 05:35:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:35:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:35:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:35:58 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 05:35:58 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:38:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 05:38:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 05:38:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05ee15f4f80900e39229320dc4a18f31e5467836d53d8648177af2819a8867`  
		Last Modified: Wed, 14 Jan 2026 13:17:59 GMT  
		Size: 132.1 MB (132081995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7354ec8d35a01da51c5c7bde89f230a9ea4888db6096c6fef02bb3e50aeaf0a`  
		Last Modified: Tue, 13 Jan 2026 05:40:00 GMT  
		Size: 87.0 MB (86986625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae1e38f5f6360dfe9cbec6d4e5309223f893b0ab212d02898fe3e47a263bcc2`  
		Last Modified: Tue, 13 Jan 2026 05:39:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ef7e362e6ed6279884b2bd3e9e7de66904e8f4634ebb775423735a139dbcee07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2bc5875ea1f1f52780b0fd0903435b9a75ac16e76a3566b185645f8bd7a7c2`

```dockerfile
```

-	Layers:
	-	`sha256:5b0cedd1796ce370349d243765d063823d2f7748072eefa4f199e2316e373ab7`  
		Last Modified: Tue, 13 Jan 2026 07:36:56 GMT  
		Size: 7.4 MB (7400275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1bb16c8893c9ab8fbf4dfc91f77e1cdbdd730f5068424e0a3f4b592d022f8e`  
		Last Modified: Tue, 13 Jan 2026 07:36:57 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:9933f081272dc2a1bef7012ba339ae1efea10bd2923bb2b1e668380cdf498376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252793009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e852e584a9944e1fe04768f90f30b1af5346c83952dbe7270308519f7b12e2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:01:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:01:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:01:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:01:11 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:01:11 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:01:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:01:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:01:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0169d7f6ed0ff6b49090b395a9f093c75bb5dccf62b26b86f3da77036d9696ad`  
		Last Modified: Tue, 13 Jan 2026 03:02:07 GMT  
		Size: 125.7 MB (125694399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d88795a3b9e0539eb3bced6bfc4589b314d1885d6aa7086d60c159fd964112`  
		Last Modified: Tue, 13 Jan 2026 03:02:13 GMT  
		Size: 80.0 MB (79959536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edc61ba4e94246bef354642900b01635764d9ba60152e64fece65c90d30b9c`  
		Last Modified: Tue, 13 Jan 2026 03:01:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:de98dac18ff9dfa5b6005b39fbeff98a4640089fca5bb3eb65d120802d8adfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dbac0b5645b6c33016675f0f4c734d9ed0317194a73879122b09feb3fb877d`

```dockerfile
```

-	Layers:
	-	`sha256:d21fa6ceeff0abebfe9ba74b13eaee07c7b4d17cbf21f5929d055cb491d4b06b`  
		Last Modified: Tue, 13 Jan 2026 04:36:03 GMT  
		Size: 7.4 MB (7386997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abaa15d6f4f20b66292485b18c03988e561a809d2c24bea84ebf4635675698ff`  
		Last Modified: Tue, 13 Jan 2026 04:36:04 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json
