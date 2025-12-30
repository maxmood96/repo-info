## `clojure:temurin-11-tools-deps-1.12.4.1582-bookworm`

```console
$ docker pull clojure@sha256:5506ef2a5eeab4bc25b98e61b640d81ff671df4f7e79db8331b9440aec29d005
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

### `clojure:temurin-11-tools-deps-1.12.4.1582-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5c934cdb3574f65fee4cbe2309dfc883468ddcff49f8cc4952f99b887056edbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274595080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe147b39bc72b55187dd3c67c6a6a97de1c670770ee14f98db2cf073600aa7c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:55:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:55:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:55:29 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:55:29 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:55:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:55:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:55:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d9c435ceb7ef96a7ff57d1b256c4ef1c6879b0f30d8c8b3a48a3db55066983`  
		Last Modified: Tue, 30 Dec 2025 00:56:27 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de65452aaaabb35bc365bc6b2a2f97dde811adca5f65f7ca11cdb33a268b020f`  
		Last Modified: Tue, 30 Dec 2025 00:56:19 GMT  
		Size: 81.1 MB (81146987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355596e6dbe3c5013799f29cd5542e51b392104fb37b6f89e0502e281c7e8c97`  
		Last Modified: Tue, 30 Dec 2025 00:56:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6afa40a9be758f504a4b3c9dded49ad846e8a28cbbf9610c9d29abd36ee36189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c750563700543827adc525e531048d3ac9357f24b8aa045361e5e1cc22958e`

```dockerfile
```

-	Layers:
	-	`sha256:569ab168174175541023bbac82eeeb849b8cefee303131fe8a25e9810216ff63`  
		Last Modified: Tue, 30 Dec 2025 04:36:27 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c807edc0628de735fbd27b8ec4063b9f8d822eaaba46baef5024f92fb3b9c2`  
		Last Modified: Tue, 30 Dec 2025 04:36:27 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0475e969c8debb97463aec4e844a6e3194e1f8baddf525f2d52718a2ef6e4dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.1 MB (271116915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ad38bb117e5b6511ae439ba059f75da90e5e7b3a8be7d8dcc09515d57028d8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:56:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:56:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:56:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:56:35 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:56:35 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:56:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:56:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:56:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fb26c3fd4471bd4bbb27e524bd96bb89890333d14ed5f022d507b47550ce7b`  
		Last Modified: Tue, 30 Dec 2025 00:57:25 GMT  
		Size: 141.7 MB (141731574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e8eb8e909ec96225d10c26c914b6d83850075f06ef5bd0ec5f975df2e1bb`  
		Last Modified: Tue, 30 Dec 2025 00:57:27 GMT  
		Size: 81.0 MB (81025549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86afe717592014a38cd49125f5424479ef4f4fa8e106f61a05f9d84ecacc2811`  
		Last Modified: Tue, 30 Dec 2025 00:57:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d8e17bb711794cee8e690081772eb1221aa03d4126bb9d878b27f0b8ef1c740e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd4d9ca665f36645a87bac2ddaf1b7dc0276ea596abba50f2b8beb94580b986`

```dockerfile
```

-	Layers:
	-	`sha256:6f2b247a9d565463a5515bf0955a631823368b88972e230ca9052542cf5f3017`  
		Last Modified: Tue, 30 Dec 2025 04:36:33 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935048d191a4d7b9b5d877fc1d2a8cfd8e9db4da2b3e9db075fe7a92e38610c5`  
		Last Modified: Tue, 30 Dec 2025 04:36:34 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:aff198fb73443ea7f3b38850b924871a1f96aa297d172f0c72f3946a04629072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271391814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc055a842436bcf31ac781f0c7e11eed18f39591ac353b818828c9196865b4e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:39:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:39:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:39:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:39:29 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:39:30 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:42:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:42:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:42:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5312618fdbb21b19cb36fc288a3ca1e6e644df592e19b679ae56dfaa229bf80e`  
		Last Modified: Tue, 30 Dec 2025 01:41:15 GMT  
		Size: 132.1 MB (132081932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbecfef354c7b62ad92279dae7403bebba3580d2c2c618c8b151a341af1de08`  
		Last Modified: Tue, 30 Dec 2025 01:43:20 GMT  
		Size: 87.0 MB (86982240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab16b2a5cafa91d9fe42e5a16f65b4fed08447faa94aada364d54674eca4ac47`  
		Last Modified: Tue, 30 Dec 2025 01:43:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:028f5a13768aa843c573aaa97eaabc32375df6410c42f495d23197dbb38d46fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4b0b50985efeb7f7ac104a9913b8274578ade8f122903ced69f1cbf85ea1a2`

```dockerfile
```

-	Layers:
	-	`sha256:48b24da8ba77123623c02a6ed28cb51118fcf689e03a2cb0c3bfa6dc5d54d456`  
		Last Modified: Tue, 30 Dec 2025 04:36:41 GMT  
		Size: 7.4 MB (7399630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68409213a550e1828a940586d2339910208bcfa3250311236216ccb120ac852`  
		Last Modified: Tue, 30 Dec 2025 04:36:41 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:1466fc1f675afc4841b9263525ac3dbf99dcd9df0e2f65350a3227c993deeb54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252787721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d61b6003148d4281f85cd8da2c8eac83a6fffcf21d6754e57e60c71cb24ba4b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 02:00:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:00:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:00:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:00:48 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 02:00:48 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:01:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 02:01:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 02:01:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ce8a6983b315f7ccc96b582192afffde7bfdc0a45f357f2cd098b4f88aab2be4`  
		Last Modified: Mon, 29 Dec 2025 22:25:37 GMT  
		Size: 47.1 MB (47137727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229b218e921c120f98aba19421a93b00de9976ceb5c36fb717d0f777015f1e5`  
		Last Modified: Tue, 30 Dec 2025 02:01:48 GMT  
		Size: 125.7 MB (125694401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c07e41cc05c76351eb8d960f5fd397064c37bb3098709cc309629e8a3b5091`  
		Last Modified: Tue, 30 Dec 2025 02:01:41 GMT  
		Size: 80.0 MB (79954949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71b452969276ee7808d577efc5522133432d4f6927cd04a334c1747e125fe79`  
		Last Modified: Tue, 30 Dec 2025 02:01:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:522ee10b5ad64234a855393eeafb43788769ae3755cde4467168e46d74dc3f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95235ae722530710652d9c8f9a80638e6a06083663772de262b3a4bc82aa6011`

```dockerfile
```

-	Layers:
	-	`sha256:2d640c47274f555520354b0c2c083731cce255473334d2385d32e7d298047b07`  
		Last Modified: Tue, 30 Dec 2025 04:36:47 GMT  
		Size: 7.4 MB (7386354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae35e3f1edf7a83befe97736569e638a12f2149cadbd5e380dac80a4244b34cf`  
		Last Modified: Tue, 30 Dec 2025 04:36:48 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
