## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:69aa9abca13e402b27b0e60a2472d063a73f43e43867876a51af07e7a37e1032
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
$ docker pull clojure@sha256:113b677ccf163065627a5dbed7cb26b6ec409323085a4fbb765786431f76684f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275462741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae950a1a45014354a1c012888b92648145ce555f9d87771cb61b05f5d038f17`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:02:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:02:45 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:03:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:03:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c235822ae767753eebfd96dc8d59127c8d2e59a178619638fd31ba2c99d190b`  
		Last Modified: Wed, 15 Apr 2026 22:03:25 GMT  
		Size: 145.8 MB (145806843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c31c4c1df7078dd3469b1e4fc4a7571ff99287eeadcb592bdbd4b87d2578657`  
		Last Modified: Wed, 15 Apr 2026 22:03:23 GMT  
		Size: 81.2 MB (81166429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd957e555ab780843d42e5b83488bbaa85a948be4457cf946c1b9f5a2b2e3afb`  
		Last Modified: Wed, 15 Apr 2026 22:03:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:578ca7e43510d2e21279b0e6175be267aaf7cb472728171f542de5c30e9b56c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758f62132fa18e2bc9ba4b573aeb5274b0aec890bebf9feaeb958448a6fd5e30`

```dockerfile
```

-	Layers:
	-	`sha256:c0604cadb063d86185f6456ad2c4af88afdaef94cf4708f9a118303794edfd1e`  
		Last Modified: Wed, 15 Apr 2026 22:03:20 GMT  
		Size: 7.4 MB (7398443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae0f9ca311ae29552a7e0c25edd411ce2c23ec178061889af56df6c16d94f6f`  
		Last Modified: Wed, 15 Apr 2026 22:03:19 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:66919ef577e15a2cd2db787bc3c4bce5cee0b7a8aabf3fcff4e306a933389fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272047908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdee531008f8dfffe87366ed8757f801161210f389fdaa2b7584c3b6c24f7f8e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:14:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:14:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:14:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:14:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:14:14 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:14:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:14:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:14:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6aa79f57b851025158debdf90f9d6e55c9fee8567c556437a946a1bacb1ba7`  
		Last Modified: Wed, 15 Apr 2026 22:14:55 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e84a7969a7c95dde95f68f91536a404d1fba4502a2fab4bc77054110b211503`  
		Last Modified: Wed, 15 Apr 2026 22:14:53 GMT  
		Size: 81.2 MB (81173197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2947df0b639883eee8a14ad2e4531c680b57f37aa914b9951d53bad9ecafee`  
		Last Modified: Wed, 15 Apr 2026 22:14:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:21a8713341422fa8ac9f858249e9f387d3c1975d1b9de42eaf51f02994797d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5bf2bf9fdce81efedff6ca14cfba2c496e308a830179afebaa5188fb1ef8cd`

```dockerfile
```

-	Layers:
	-	`sha256:12e0cb883c0e4c7705be7f2490141cd7ecd7b07d05a8ba547f1ddd263192a0c0`  
		Last Modified: Wed, 15 Apr 2026 22:14:50 GMT  
		Size: 7.4 MB (7404824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eed08268fe775e28d602a1fae97cc1e223ee41337731b891ad30c507bcdb422`  
		Last Modified: Wed, 15 Apr 2026 22:14:49 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:74b1ab5ffc0316d198fc39cf5fa369fa60cc65aace2d9a5330f824a90f1919d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272335305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c3b6a21c4a412594da932ad1e4be4e3e28947127b4d3e70307fc4493f999ce`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:28:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:28:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:28:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:28:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:28:31 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:33:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:33:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:33:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1061aa781fb4b7c36cdecd69fd6ed87373d79e2a52e43dd17a688e779d38977c`  
		Last Modified: Tue, 07 Apr 2026 14:30:00 GMT  
		Size: 133.0 MB (132997676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f35aa7019b6ef25665b7677d66d2178bb40ee2a24d59861551e387c9e4d72b`  
		Last Modified: Tue, 07 Apr 2026 14:34:28 GMT  
		Size: 87.0 MB (87000045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba52bef27f7a82455b6f78de17e478edb5f73febcc2cf4603058f7bf778cdd4`  
		Last Modified: Tue, 07 Apr 2026 14:34:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8489737b693ab6f1976a5347b4af0243252672169be18568aa0a465b68582f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a98c92404dae1194d21f1068c1f24ed8d14c1eb8ad6d98341c7982ba12bc385`

```dockerfile
```

-	Layers:
	-	`sha256:d9ea4bbdc3b3882abab527a1ceeeee7cb82edb50a529c23323613f7a0f0120e2`  
		Last Modified: Tue, 07 Apr 2026 14:34:22 GMT  
		Size: 7.4 MB (7403044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d83e21c07ef3a327238a0d841e2ab10aac8e4fc1e13e688e5999a6a74c872ee`  
		Last Modified: Tue, 07 Apr 2026 14:34:22 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:885addda74201b1f06c262da677d9300b23004e93a14048f697782c670bddaed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253698678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178fa9095d9a446892a4dcbceacd88d56a9859ef3d0849e11731290731cc8e1a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:40:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:40:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:40:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:40:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:40:08 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:40:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:40:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:40:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cbf6ffc38d826dee06273c7ef7b49d6253b226b4fd09999f110e03545066ff`  
		Last Modified: Tue, 07 Apr 2026 05:40:51 GMT  
		Size: 126.6 MB (126562219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcf6b342e10a8b2e1fce7bb6bfeadd0e0e9370158e708eb04906b5b344c1cff`  
		Last Modified: Tue, 07 Apr 2026 05:40:51 GMT  
		Size: 80.0 MB (79987728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2a01aa53cd7980f006f601ad8d3ee9a4192900b64c7f58d39ae362b5feaf07`  
		Last Modified: Tue, 07 Apr 2026 05:40:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:46401c905fbe8eae63ca0cc0adb6e3528583d95774b81198fba3490ae25cfbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3eadfa87710b435bb220c1ed68b5dfbab15e90fe38690cc72a62dc62c68e53`

```dockerfile
```

-	Layers:
	-	`sha256:e9b9d43002641857b5012bf77823c46911a08ec84948c9dd84abce916d2d0b2c`  
		Last Modified: Tue, 07 Apr 2026 05:40:49 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ef1e06e39e152805c6c31d5f2684798cd0c0347f5b200a98732cf9a5dc02c4`  
		Last Modified: Tue, 07 Apr 2026 05:40:48 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
