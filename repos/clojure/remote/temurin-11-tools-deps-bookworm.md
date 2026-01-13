## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:f6852208b6ea82e809e59ee2ca38dc079c6cfb5adf83d6000a5150bb58f7970f
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

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

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

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

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

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

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

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
