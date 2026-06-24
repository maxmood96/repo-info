## `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim`

```console
$ docker pull clojure@sha256:861fc3bc908149f18d6348287a68f1e3745b3fdc55a2f705167b8d44a6a71fb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:63fc4de0ff1a620aee013f7fc90a93ff6a5a693ff699b4b36ec99cd43fca2b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153936791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16c24d9218938cd0c54164d96db95b5f68d0e1dc47b9c1e14f131a3d2cbd7a5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:15:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:15:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:15:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:15:00 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:15:00 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:15:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:15:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:15:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674efba2372c86122c2dbee84663590d78042a1b54d6aff689593cf0824d4f0c`  
		Last Modified: Wed, 24 Jun 2026 02:15:36 GMT  
		Size: 55.2 MB (55198699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd2f72341efec9285e89ccfd8bc3629e99d2a468030407d1e4a94839b885ce7`  
		Last Modified: Wed, 24 Jun 2026 02:15:36 GMT  
		Size: 69.0 MB (68952028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34c05d014b8247b8afc30e5dc766203c1dc97e87a7c6d695d7baf73ec6fa48d`  
		Last Modified: Wed, 24 Jun 2026 02:15:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:162942dfca9ba68d4494607c56dae0b7e12fa5e020a488f91b2bc0d7ba170f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c9ebce5309d572093b50a39defff1c24ce6db2d0158dd35663fd808d692bed`

```dockerfile
```

-	Layers:
	-	`sha256:1caca2130b6409ec7434c35bbf3543ad07837be83f4c18af7efc228ac9afc231`  
		Last Modified: Wed, 24 Jun 2026 02:15:33 GMT  
		Size: 5.4 MB (5377602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a841254f1ce51e74db3897d28e5f6720a3755a90e758edca20904cb84a981e2`  
		Last Modified: Wed, 24 Jun 2026 02:15:33 GMT  
		Size: 14.4 KB (14381 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e03e96e4cc4c649eef68b5c8bd8f01e3ef63b1d4f0c4accb68f16e42a6ceeb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153199666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7590e2c7bf61460c377464194bb31d9794df2a130aefd96a94f5fec849b5733`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:21:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:21:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:21:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:21:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:21:33 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:21:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:21:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:21:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df556439df195577d320bde207d9851aa4c8d39d30e6e28c28c873b1b365de1d`  
		Last Modified: Wed, 24 Jun 2026 02:22:09 GMT  
		Size: 54.3 MB (54272901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d076a6bfe25ed2d76e9fb04fcb98b195ae995b5d93cde64d97e88749eee934b`  
		Last Modified: Wed, 24 Jun 2026 02:22:10 GMT  
		Size: 68.8 MB (68777569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca873ae3d058a453a75872d65cc11445fc875b398c4ad127ca501a1f4da7f9`  
		Last Modified: Wed, 24 Jun 2026 02:22:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31df66b373db4f51afbb45c003f48ea59b253bf5d812cbe153108a5c1de80740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8aa1f17a82a809eac299d92fd735680902877d296a0876ba032f6ca9ea0584`

```dockerfile
```

-	Layers:
	-	`sha256:abccc49eb867e68a2fdeb77a79e2c5507d10184e5648035431c63d48442c723e`  
		Last Modified: Wed, 24 Jun 2026 02:22:07 GMT  
		Size: 5.4 MB (5384063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8a7e1b4fa0bdfb7b7147a7c82bb1f50f1fec34e30989b803b3361b25c04bad1`  
		Last Modified: Wed, 24 Jun 2026 02:22:07 GMT  
		Size: 14.5 KB (14499 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e086500e11a6ece399254c06205bec3b649df0fbb56c80d5d2ab43aeefb6931e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160645043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b5b29388c465461dee0562b6f1276bead3693d350f2cb9b3a49e5c0c68ce75`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 07:51:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:51:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:51:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:51:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 07:51:11 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 07:51:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 07:51:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 07:51:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0904cc4fd2cb228e5d922464c3722785790eea034f950339bcb8e8d40a05723f`  
		Last Modified: Wed, 24 Jun 2026 07:52:26 GMT  
		Size: 52.7 MB (52669122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80a3126fec7da016238e8afd478cbf3a294aac95f9fb45f27c3e44e7ced7ba0`  
		Last Modified: Wed, 24 Jun 2026 07:52:27 GMT  
		Size: 74.4 MB (74368888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec0a275a2cd295c1445bade1953bfd78d470d7a7787c5bc916ecbf93663b6d`  
		Last Modified: Wed, 24 Jun 2026 07:52:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02052d10dbe2f9c0a074bfaec347bcbd9b19660d85060ae80fec6b3f5eed09eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c86946aa2eb01d803be5c4c099789de90765d40b5e939b61ef9ac4f7d62af82`

```dockerfile
```

-	Layers:
	-	`sha256:ab6284161a246b339197d88ad9752275e0d954b52ee565074c1de8a71a301dd8`  
		Last Modified: Wed, 24 Jun 2026 07:52:24 GMT  
		Size: 5.4 MB (5382568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fde15c4b025564c644bb7f4177e32359ac289d1cd7a46b38009a76bd2565ac7`  
		Last Modified: Wed, 24 Jun 2026 07:52:23 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json
