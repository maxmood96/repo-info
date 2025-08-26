## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:56610871254eb5f2db60e732cd17ca4d732c54af5b1559d65d95bdd28108edc0
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e32b12e3aeea91a514497d7a3b73201894fbcc9ef4c618bb58023c2aa4675e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242600915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8f84915100bbfe62d621ce6b384d180e0c3cc1b2a0c79026dd7a56036a9b82`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df5f9a37b869e6e5edb32c69390f77a97be2d72f920fc00fbaba6de99abcde`  
		Last Modified: Tue, 26 Aug 2025 22:18:05 GMT  
		Size: 144.7 MB (144693303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ae8566bf64043a2e89478483549445d7a7daf9818ae5b5088f3a0cf7efc715`  
		Last Modified: Tue, 26 Aug 2025 22:23:06 GMT  
		Size: 69.7 MB (69676315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae4816ba59ddb2304a9f5f9aae5a22c0d20858856f74bdfbd681612b5863d75`  
		Last Modified: Tue, 26 Aug 2025 18:58:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4c23cf781a957760fde19159ddde8eb07bbaa4a75485397d83de3d1c546fab`  
		Last Modified: Tue, 26 Aug 2025 18:58:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:54327557f4e8eab2cc1d1e60490bf87255a46ac32e19e4e8b2f91cf1dc2fcac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5127152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961dc82ae998cce0008252c1c33c86b1b4117927517ee6900521e477d01a7e17`

```dockerfile
```

-	Layers:
	-	`sha256:2a58befb67abca4013fbf7b7cb3b045f037d022f672c5e3ed5985eda01b0f5a0`  
		Last Modified: Tue, 26 Aug 2025 18:37:32 GMT  
		Size: 5.1 MB (5111273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9add60e2f11996cf028bc66fecaf3583cc0158f094f5ae82712a09be9cc2967`  
		Last Modified: Tue, 26 Aug 2025 18:37:33 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bdc77610da2246224ef5bc642a302e0a71aba2d5e35e9b8f699597e68c7cc220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241174665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f583c23296dfbcdbd65d28fa8dcd86aecfb0e74d0ae201e5bec05d9b5f02445`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5cf058475776582e9e64a646c76b474fe20722c0592878e59918c738320dbf`  
		Last Modified: Tue, 19 Aug 2025 03:50:35 GMT  
		Size: 143.5 MB (143542112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f07b2e01a24e9ce321e14aa2cc745a4b094f44cd1bcda6ade0454b8985b97e0`  
		Last Modified: Tue, 26 Aug 2025 17:42:09 GMT  
		Size: 69.5 MB (69549509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5467f4a4094cfbee234aa6efe4267f6c20e9cf235f42884f1d93366b3d43f2f`  
		Last Modified: Tue, 26 Aug 2025 17:42:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d247203cd97295ecfc33cdb2fca70890563e824572b2582fd24412ec1a1e5887`  
		Last Modified: Tue, 26 Aug 2025 17:42:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1c1fc7e9e5ba0a791197213a6fb262f2306cec7c476e1acb710c126228e33841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c518025ba8375354d7a139f4aecb23e677da33c024c0e267bd76512c3aa3cd6`

```dockerfile
```

-	Layers:
	-	`sha256:da1587e21988dcd8eb85a5d559c4def87e3ddb3a9958c093133f02895f705e40`  
		Last Modified: Tue, 26 Aug 2025 18:37:39 GMT  
		Size: 5.1 MB (5117034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a8e9ddac51fa831263ea1846643ea3d30b2283c849ab9c10ad8753a290f97c`  
		Last Modified: Tue, 26 Aug 2025 18:37:40 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8684f72bd27c34396b8bb7e27057d9ab70207fa5b0f022dd85f939c4b5173e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251951368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5682560b647549c4b2fa3641438c9fecdd8eaa2f61083372b115ee7847acb4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f775e155906486b3af9c87541a33fa50508312260cb346dd22a54dd5f4b81a2`  
		Last Modified: Sun, 24 Aug 2025 06:13:53 GMT  
		Size: 144.4 MB (144372832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9934c6c89352d393c8067e20c792bb57995ec4decbb3759b67aac8b6ede12763`  
		Last Modified: Tue, 26 Aug 2025 17:55:34 GMT  
		Size: 75.5 MB (75504071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a405f98e3eaf7a14cffd9cd50c9dde522175604fa74342d3b825ed8dbf3e1`  
		Last Modified: Tue, 26 Aug 2025 17:55:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31502d7e7e82ebe7c54518978a151a432e76efc324527de7a8fab8031c1b526`  
		Last Modified: Tue, 26 Aug 2025 17:55:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0281f6d8114155016e6ff5aa69bb4cce2e853e54bc8c53cd7d456c1ed1ce908e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedc8651844b1bccb3ce6005dbe3289d14ab7545310f70eab66c43e99d71bfb0`

```dockerfile
```

-	Layers:
	-	`sha256:781e1e480ac4658c761a51ca523dd91000b69ad46459d90f2d82d4bc3a478b3d`  
		Last Modified: Tue, 26 Aug 2025 18:37:45 GMT  
		Size: 5.1 MB (5116431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f890ba8f220f31cbbc785f80861df8cb9d330273cce1dcc20d64b8c990e5ab`  
		Last Modified: Tue, 26 Aug 2025 18:37:46 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:803877e69c97f8bf8b1c0bf6ec1215a22d8e4ad4dd08a9d792d8ec816d6b11ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230097752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c948b23d17dcc29599346a2339baa5f349966ec2faed830821754529ae4016b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5827a26ead12b66a1ef4f4d0246902cd46ee903e980906b81bf18663ea811b`  
		Last Modified: Sun, 24 Aug 2025 06:14:14 GMT  
		Size: 134.7 MB (134724369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0611a438c7433758a2cc12f52bb2a5ba4410d4071ec68c6eaecb0df0cc111274`  
		Last Modified: Tue, 26 Aug 2025 18:09:17 GMT  
		Size: 68.5 MB (68484501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28580afe42a4e92042f4000638625aef9635cb1bb42b2f86096dc4e7237d8260`  
		Last Modified: Tue, 26 Aug 2025 18:09:12 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f52d1e677af3d1a6aa6136444d830f2347d54df64857f525952622810acd7`  
		Last Modified: Tue, 26 Aug 2025 18:09:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b835119d63d8e2e67c32a4eeee23b89cceb20441063fdfb324eed4e24549da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5118473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3002f5aad4a3c3f14932c61051d063c240ff98866dffb900d14073b2f3fd281`

```dockerfile
```

-	Layers:
	-	`sha256:dc20429d7df4ab5e7ee45e93da3ceefdbc88698ea3072453b13b393b58a6ef3b`  
		Last Modified: Tue, 26 Aug 2025 21:35:26 GMT  
		Size: 5.1 MB (5102594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e33117fd33bb4d8d2c6ddc4af9f8c99fbffd553415d1524f572e1a0c0888078`  
		Last Modified: Tue, 26 Aug 2025 21:35:27 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
