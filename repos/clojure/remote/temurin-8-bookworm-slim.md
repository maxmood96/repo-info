## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:98ab3cab3b957c616f3ecb5c1be6efb7bfe1feca1d8e5a11fc158dd1746de803
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4302dea7284f1e0f3a73627962bc662f46935e32552ed91a098cec61005667ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152496614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b845d5704a6bc1b1b62fe021ad0c8dd1ebb556b97ec92f90671d9a492180fbd2`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1a77b343c70e92295408fcc55140d7bc7e5bf0d687702b7daa8267c27fe40d`  
		Last Modified: Tue, 12 Aug 2025 21:34:43 GMT  
		Size: 54.7 MB (54731352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5ac765832f17eb48d93a40ff39b19c08ccdf7f59336bf2ca737e82926f5f7b`  
		Last Modified: Tue, 12 Aug 2025 21:34:42 GMT  
		Size: 69.5 MB (69534363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5668aa7d7307ebdd80b8b362a217489c02e4f0c67cad58cd1826ac7dcb3f1c59`  
		Last Modified: Tue, 12 Aug 2025 21:34:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b20560b97f90429bc89bd9b40e4fdcac7624442465ee5b899a0b19fc5dbf5fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3484944198ad7cfe760775152803918dbd6084eab3f02689069058eb3fe3b6d`

```dockerfile
```

-	Layers:
	-	`sha256:fea2ab9ccf48c0dc80b69cb7fc727e84c64bece69420274bed21a9059e8762b5`  
		Last Modified: Wed, 13 Aug 2025 00:41:35 GMT  
		Size: 5.2 MB (5232854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fbc21f3cf25ebc671a94a09fad5f2bdfe231bc702213f9d415622c37fe8bf8`  
		Last Modified: Wed, 13 Aug 2025 00:41:36 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1c2e1b740e0d797bbca402122629b9b89e9ec8fcbcca0e4e3fcd63d86144d820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151323283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841177eca9d59cf6960ab14b2b43435a780c9a61aad0aed03ebdb602cb82a0ab`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0fff8509b02636af604683211237b72e62bdacf78ce575598074ac13b3a0d1`  
		Last Modified: Wed, 13 Aug 2025 14:01:49 GMT  
		Size: 53.8 MB (53835638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cef506d5ddfdf9cb8df75e3e9102671129f8c3c0889b5ce73050958af76f11`  
		Last Modified: Wed, 13 Aug 2025 14:06:45 GMT  
		Size: 69.4 MB (69405000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d273464c9916a3c22ec96c185b56fa1aee066f89880c081bfd86ed38c8aed668`  
		Last Modified: Wed, 13 Aug 2025 14:20:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7520f6f9ca12ef946dd85cb1856f12901d263596b8bb9f48c44ceb37a46e8f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e1adaf81f680e61785da189ec663bcf93af13e54bb1ebae598cc88b44e22bf`

```dockerfile
```

-	Layers:
	-	`sha256:39297222c3b1ac1e38b03a00f60a9297171881542aafbe333d01ebb5ac994432`  
		Last Modified: Wed, 13 Aug 2025 15:42:12 GMT  
		Size: 5.2 MB (5239313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80934af3f327dcc5e0f96890fccc9f052abfbb6c4181e9bd8917a37ba716a09`  
		Last Modified: Wed, 13 Aug 2025 15:42:13 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d410b5e36565d6105aa23d6758fe936cd0224a33e05c7e88dc1f60bf4a27f0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159601513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45c5b9a6bc5862919d0f98f73862fa8a644aea1039a21210afd387be28cd788`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906fe8e3d88098947ce766d06d6b97288acba0a9b017b385a6599208fc09bf46`  
		Last Modified: Wed, 13 Aug 2025 19:18:51 GMT  
		Size: 52.2 MB (52165436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dbf0d00a915dac4ec0ef876cc0a6be1498f8e829db2d064f2329dcf023ab2b`  
		Last Modified: Wed, 13 Aug 2025 19:26:56 GMT  
		Size: 75.4 MB (75362011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05c72f3f1aca78404ebc2fb6ee6d69054e638d2d74f314765faa0689749ba90`  
		Last Modified: Wed, 13 Aug 2025 19:26:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:936cbaf98c9622f7cabefeac4d87a83360c721d21f9ca6a7378cf6c89f5c3402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b29f7a7b46e08fb1910c907e1e866d3ffaf4fe5e66afe07cf50f4fe7c6a8cd2`

```dockerfile
```

-	Layers:
	-	`sha256:7304059451cf22a193679b538a21a17379468a0024eb71608d51040e81a50176`  
		Last Modified: Wed, 13 Aug 2025 21:40:29 GMT  
		Size: 5.2 MB (5238605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fec4f134417ea61dff8d6ad26ba888a2774fa959931a85f079b95527569943`  
		Last Modified: Wed, 13 Aug 2025 21:40:30 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
