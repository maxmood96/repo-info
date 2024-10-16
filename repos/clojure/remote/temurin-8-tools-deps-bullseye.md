## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:8a131ee4de93ddab33cf56b10b84e2fe2dda79d02399d2344e8f1143d8674b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8cd6dfe7a2b52aa53f49166b17c171a454e3b3c371439099412602fac8ddfa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228027517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e175caaf2768f83cadb8fb24cb6032146c0dcbff9657fde6365e18369d33c0`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b970b06ef27b03bec53abc38ea79675e6c703380afbd3896ceb96b3c32644e`  
		Last Modified: Wed, 16 Oct 2024 16:12:52 GMT  
		Size: 103.6 MB (103611915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187b9e8cf80ff7c1a97ae22a32eea30fc671fac4698caa947ebd17da23a065aa`  
		Last Modified: Wed, 16 Oct 2024 16:12:51 GMT  
		Size: 69.3 MB (69333565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e564ca06c75e92d1783f20dbe78d68439a8afaa1ca80a49aff6e37138c29e3da`  
		Last Modified: Wed, 16 Oct 2024 16:12:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c7bc26b6fa88946ee085955fe3195758188d0f2b5f46c0fb858885440052abb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7326059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32f0cac4a2a30b7a11f6ceb2fdefb9b0d3db1f35e22b059673a6ab20b4afe0`

```dockerfile
```

-	Layers:
	-	`sha256:a0c6ba3a4204fcdf9ecefcb92d7ae116477adaa59fb0a5e70cf4bf235f03f914`  
		Last Modified: Wed, 16 Oct 2024 16:12:50 GMT  
		Size: 7.3 MB (7312169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de6f58e66611fab63ae2453165fb0df7bea67ad4ed6dd7c37fd68e87cf0d9d23`  
		Last Modified: Wed, 16 Oct 2024 16:12:50 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

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
