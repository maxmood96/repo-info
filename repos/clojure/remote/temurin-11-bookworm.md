## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:9fe7543c16fbdcdd7f6e3691d8113de94d3d8716444e80580a0d2a422533a30e
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
$ docker pull clojure@sha256:7ea0cc767f938f7f591bd50c39c98e2c774e12484942c3ea258d1778617846db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275276905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e23d82a83214084d6c8fcba6e8f2286cbcf23ed98c575c974efe3472fc6455`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0edad6df57e5676247c3077d7469cf5fb4e8a0f589854b1f4a37944e37fcdf`  
		Last Modified: Mon, 15 Sep 2025 23:25:20 GMT  
		Size: 145.7 MB (145658268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4148f1e403796a0ac292af0fcf5eb9431c1365222de3dd04547c0dad107ea4d5`  
		Last Modified: Mon, 15 Sep 2025 23:26:03 GMT  
		Size: 81.1 MB (81137383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ef375f5e85406b46fb2b307b3bdd4427c6604489e0def662aee376faf73306`  
		Last Modified: Mon, 15 Sep 2025 23:25:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:543fb0379b387b442f2c0f302b5752b2a0a08e25828c72b3c9376b6c4e54a39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf8ee185c713560ec33098e4dde33e9ee8ff51bdaef05a018774a721cf158ed`

```dockerfile
```

-	Layers:
	-	`sha256:8fab288a2b97cd4b90c0ba25b0a53c1f75fcc343ac27ebf3c958f003b29a460e`  
		Last Modified: Tue, 16 Sep 2025 00:35:27 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df0c8e3bcf065e50f1e29f2dd2ac6b02b75ab5d779a3dbcdade0fdeaa6f61762`  
		Last Modified: Tue, 16 Sep 2025 00:35:28 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b96013b3f699beb198d97e1c3cd44227d19c9f47f8e825b7a4fc567654de4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271844060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60f9433dbca9d518788f88721fc4eaabec44694d7e369c6282ffc5e314e99ae`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e9b0bc27cde01cf2a6a897c5f9a783cbd14ca466dd7a6ff08a204102ee72be`  
		Last Modified: Mon, 15 Sep 2025 23:25:34 GMT  
		Size: 142.5 MB (142458730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e924a9cf1eca6dbb8661a41a89654bff4e01fc2f50af721249dc0aac8b63c37`  
		Last Modified: Mon, 15 Sep 2025 23:26:01 GMT  
		Size: 81.0 MB (81025666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b85a73764a699e41ceb58643fd82871232503df1c9ebfce912378cf7e76964`  
		Last Modified: Mon, 15 Sep 2025 23:25:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:80de509cadd2254f272f488902cbade18aaf37ae041de9a5e090260f9287ad33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6027a29e00107386bb5dabf6f9deab76f864856994bfb7b76e927aa8f60f9c7`

```dockerfile
```

-	Layers:
	-	`sha256:21ddfdc7972c6dc23e67c2c89f1181dae85bcb3f468339f23e13ae7cb38fec86`  
		Last Modified: Tue, 16 Sep 2025 00:37:37 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c23fdbca79f4cefc247dfae544b39f9654bef18f257acb131f270798808a3ee`  
		Last Modified: Tue, 16 Sep 2025 00:37:38 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:500db7e964b750f54a7e021310cb01ec833c9bba076ca47f7b32b7da5a13b943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272158884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8491804f21e783e17269d68beadabb5190ae7c9d898948d59ed2025d64b8b6b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef13c4ba7a52133e1454df897daa22c7439b0df6eb204c60e2ecd3e616796b9`  
		Last Modified: Tue, 16 Sep 2025 00:41:48 GMT  
		Size: 132.9 MB (132852835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba69bf298e8dac3c2c2b7d324a7c623855f61c9a91633bca6620fbaf4b271ef4`  
		Last Modified: Tue, 16 Sep 2025 00:51:48 GMT  
		Size: 87.0 MB (86978584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a257b209955dfb8fa851a3d3da913f5dc56db4a04413c88347018dadbbd2028b`  
		Last Modified: Tue, 16 Sep 2025 00:51:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:67f720f7e75c2f051ea5c304168aafafaeb28cf52517bcf813d14804b94a72a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b75db20a64ad62e54672af356d9007ab596ec03f036d1db7c2288899a5fd6d`

```dockerfile
```

-	Layers:
	-	`sha256:b155d414c0bdc333a6d9a9ac428dbfd43c66c4d82ba719b746f8797dabbbd871`  
		Last Modified: Tue, 16 Sep 2025 03:35:24 GMT  
		Size: 7.4 MB (7399630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a6c4eec9cbe658b72fdeadfa085b86b60025a824ceb486997663951e5d7eb11`  
		Last Modified: Tue, 16 Sep 2025 03:35:25 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:c21705da5d6e4357270f197b400f1742522d9023f55c61686d1c63034ff795f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252711815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c41e4741fb6b099b31ae3f58570d83b85c936faf1eff923ed18566af0004e6f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72069f8f4220851a584759cf319dda1df252a01a6128f74b28d99dcc4423cd99`  
		Last Modified: Tue, 16 Sep 2025 00:16:15 GMT  
		Size: 125.6 MB (125622201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d510cb90dad435ad6e1b28a0e99305fc2c39d71d31c47eb3cd6ef18ca978b0`  
		Last Modified: Tue, 16 Sep 2025 00:21:56 GMT  
		Size: 80.0 MB (79951430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e62c21b4e2b305c22ead7531266dae8876e690573124b8a01d7384a0d7b5e0`  
		Last Modified: Tue, 16 Sep 2025 01:06:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3a6ffaaf0237bb8ddf90342e900942c44910992c239a428d4f4ba595a3a525f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fbde6c24dc77616cdc628f34474d304345e24fe6f4444fa32d71e627f87711`

```dockerfile
```

-	Layers:
	-	`sha256:c4af70b90f593b277778574253290f0ce09315adf4f72f1eb50730882caf6f60`  
		Last Modified: Tue, 16 Sep 2025 03:35:30 GMT  
		Size: 7.4 MB (7386354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cae79612240a822e4dc2266fb10be90c9a44b80281c08af2aacb57109035012`  
		Last Modified: Tue, 16 Sep 2025 03:35:32 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json
