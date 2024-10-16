## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:6446958d116ccce7a7815a5520134bd7ec72f5755346e059c570277f35346ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3228c0a24cf3d93ecf41d0c34c32e7a1a52f5f79196fb4d82df34dc62e97bf53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228027679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bd41d418a0920376be16c1f68efdc0758265da9adddf737eee05716a5e7dd9`
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
	-	`sha256:cc9351e80f31bea3a461840a7aeb12991531811348299d2686f6d1f58bf8f539`  
		Last Modified: Sat, 12 Oct 2024 00:53:37 GMT  
		Size: 103.6 MB (103611879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da70117c9c9ea2d4367f83a14732b89f6cdb12ff8a9be6e1d28e6c1b798ff4`  
		Last Modified: Sat, 12 Oct 2024 00:53:37 GMT  
		Size: 69.3 MB (69333767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b8123e9fc78a49b7c5cc5bd5ed9410c8b8c2794011bb1d78d090be18f3a4d4`  
		Last Modified: Sat, 12 Oct 2024 00:53:35 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:acb8a0edecdd5dcc3df278164e2d772c221b4bbf4eea2ba500cb0e61782e7481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7326058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31516d197555f473a315a339ae75455b65279c98c4dd8f2fdadd41b04b941de3`

```dockerfile
```

-	Layers:
	-	`sha256:10c17c1560bb23b0fda2980cdfc9e9ab8ef91cf4cd25cacad63ad59a4db2ed53`  
		Last Modified: Sat, 12 Oct 2024 00:53:35 GMT  
		Size: 7.3 MB (7312169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0335bb32021eef0411061e1a058a9d2b412db6a6375cca85578c4fbdb4ce6585`  
		Last Modified: Sat, 12 Oct 2024 00:53:35 GMT  
		Size: 13.9 KB (13889 bytes)  
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
