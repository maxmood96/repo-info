## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:57f19344282fae07296056e91c06334ac2208a52d426fa7305887339748b9ccd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5e5b130aeb8075e0233418b03633a2d091fa6ccc8e2ee04966c66fb541ca82a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228026915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e81838eaaf0b78de8090490865b9c38cb011aa648fa75213f3bdfdaaf7a18b4`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f0c9de5c0464a7016be502647b786c714fdc66534ff48040eee36e4fd6d19`  
		Last Modified: Thu, 17 Oct 2024 01:13:27 GMT  
		Size: 103.6 MB (103611915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6620a3ba902d08aa2b7d54920ed08d376b06ce3544d6e20dd13f6629a99f25ac`  
		Last Modified: Thu, 17 Oct 2024 01:13:29 GMT  
		Size: 69.3 MB (69333746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0ab7aa6f14a2a759e45f186667aac5c9dbf5449addaeb7a16c2db3d88b506a`  
		Last Modified: Thu, 17 Oct 2024 01:13:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c6cec573f34e453033b0ef24d05c87e9733337165d48ca40b8ab660ba66333cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7326149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81bf056dcf7838ee118073f2d54e450d2d878868492b89ebb341f705f2036c92`

```dockerfile
```

-	Layers:
	-	`sha256:24850f67ab82a066253b132bec863445f7823ec68f0babeb03407f4eaf0ae32b`  
		Last Modified: Thu, 17 Oct 2024 01:13:24 GMT  
		Size: 7.3 MB (7312259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d96161fb2fb9b73623799d8c23ffad52bdddfc608c28a022434695452ddaab`  
		Last Modified: Thu, 17 Oct 2024 01:13:24 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7714aff454a1fc300d0c4ef5486e381a61e7d3ea49a8496fdc23ddbea9b5749a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225930794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7424fc31fa2e1ca635bcb2495019252c5219b7c4fa6cea4e80aebb6ebd6bce1`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafa242c12920bdd16205ec39134ee4ed313e2b2a934188963705bd5a12f044`  
		Last Modified: Sat, 12 Oct 2024 00:57:42 GMT  
		Size: 102.7 MB (102729221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cc2abbd20a029ecbd733c52e7c5ebb95f6fbc9e7801b43ee513384cf7a5240`  
		Last Modified: Sat, 12 Oct 2024 01:02:09 GMT  
		Size: 69.5 MB (69467063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98d74b18536187313fde8447ffe22349bf8104ad14faf0300c5f8d0a2572809`  
		Last Modified: Sat, 12 Oct 2024 01:02:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3463e7033b2993f2652249a4c058394c06269aca312f780e7f6d27eab2efbe55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7331967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973cdbfb1ef3fac417c924c2eed2955b128be88a33d95ea9a6d8a95b21f4917c`

```dockerfile
```

-	Layers:
	-	`sha256:3ff440d4141de92d39ce8cd0d52e17413fa0cf9fa946caa727492992e619158f`  
		Last Modified: Wed, 16 Oct 2024 02:08:48 GMT  
		Size: 7.3 MB (7317971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b09f47bc3df6f3af1060c5d8ca0486f996370f0a20b920646f05e0b21328c6`  
		Last Modified: Wed, 16 Oct 2024 02:08:47 GMT  
		Size: 14.0 KB (13996 bytes)  
		MIME: application/vnd.in-toto+json
