## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:449ecab4880a0e118d54463b402dfbea6d58fcadbfeec96c1246194a3bca29c1
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4e5fbfae80ea63de84591c1101ee2da5901f93cfd20b2585a6b1b1aa5c45a12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250560806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3cc777137fbd9c151eb50f8150b0ea652b13420a5c6722e04d12b0890300f5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:03:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:03:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:03:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:03:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:03:08 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:03:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:03:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2370006d61322e9317a583479da6057565d4805d8e5a6c756d42dc6815f6f610`  
		Last Modified: Wed, 15 Apr 2026 22:03:46 GMT  
		Size: 145.8 MB (145806793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf02e5524e7655e67c73f2cad45b86c8cddba7247e2e31be77a1a837a4da7f5`  
		Last Modified: Wed, 15 Apr 2026 22:03:45 GMT  
		Size: 75.0 MB (74977726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e64c32e43ce3545230fbf90d844745f407d22198fb2d8fdc65c33677b8a7d9`  
		Last Modified: Wed, 15 Apr 2026 22:03:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:371c078080ba426f30fceeaa0699e38013a523e1e49c8aac46a875f755562b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aabe48b70ce77b2b1eeb724d30d5dd8a3c13e4f3d85113ec4c2de8aed88cec`

```dockerfile
```

-	Layers:
	-	`sha256:5e629beef0a7f756910d9f64dbc22a7ae194dcb589a5a365e6cb902b37c02530`  
		Last Modified: Wed, 15 Apr 2026 22:03:41 GMT  
		Size: 5.3 MB (5279279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389751c6fdedc8842888bc6614ac037ebf2108e857679303a9213613806c5812`  
		Last Modified: Wed, 15 Apr 2026 22:03:41 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:39fa476023cf7167b9824f2a66c8a55201eec9e17a188ad038e4fa1995c5b6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244475856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927ec28d57a10136d17d6636202d91480db064c6d559a090cdcdee3bcadacbf6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:20:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190a74c976dc2438d09255b2962f7eb86d09cc2d8561ac235b8194f95326fa14`  
		Last Modified: Wed, 22 Apr 2026 02:21:31 GMT  
		Size: 142.5 MB (142500802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23551bc95003a80fbd24948fae8a57fe08d1f46234610449ed77798451ccce17`  
		Last Modified: Wed, 22 Apr 2026 02:21:29 GMT  
		Size: 71.8 MB (71830804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d23dd77094b844d2e8efb0e95cb108e500ea1b4aa13bab6c7accb0bcb9cee5`  
		Last Modified: Wed, 22 Apr 2026 02:21:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8067264e0e60779d22ef64678c2a7a9cf4e057e47123081a895521f6a278448a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83fe0dae605e61dcec575bde7316577a6c4057f6f1a3e4a64879941dcae7287`

```dockerfile
```

-	Layers:
	-	`sha256:2cfb6a1639a0fe71b02ac59203d4b0309525b0a24512e291a3ac3733af5c3114`  
		Last Modified: Wed, 22 Apr 2026 02:21:27 GMT  
		Size: 5.3 MB (5285720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b91f7dac3392f4a6c5d50dc518d20704b09b0fe493a1b8328e5efc763c894d`  
		Last Modified: Wed, 22 Apr 2026 02:21:26 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3522fc4d9cef901496ad7504b5a738d81ba876e42a8a43ecf13c623facd2ee67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247201387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d092cfeb83996b1209a4fa5e39d0aa65be3f07660952d1df91b15671494e009`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:42:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:42:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:42:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:42:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:42:14 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:48:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:48:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:48:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76042bd72cd27c05c77d44bd98d120db7be804788d7f01116ecc64346fb992b6`  
		Last Modified: Thu, 16 Apr 2026 02:43:49 GMT  
		Size: 133.0 MB (132997414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f654998ceab4a801a39fade9f3743f1efe6e5172d489c2c6cbd8c6fed240b3`  
		Last Modified: Thu, 16 Apr 2026 02:48:47 GMT  
		Size: 80.6 MB (80610309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6086fa06102084aa8ec5e00e7262867ff3567ad9c96ee6ddc33d0f7226dcd7a`  
		Last Modified: Thu, 16 Apr 2026 02:48:45 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9eb1c37a17b60da98c1f4f33830f84fd03ac98e3f823589e645a8afaf62c37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4830f54a59a5f58c87c71420f2674d67ecfc377099c3f7b5d337fc446b163f41`

```dockerfile
```

-	Layers:
	-	`sha256:dd6ca91153023e2a8128e59f52dec1d9dd53a7e8844236678229039c04948bd2`  
		Last Modified: Thu, 16 Apr 2026 02:48:46 GMT  
		Size: 5.3 MB (5283035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f296a7684a405afb228344d31f81a1462f76a9e7f3ed1d4fe4d1f2b8928aa4f`  
		Last Modified: Thu, 16 Apr 2026 02:48:45 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3a9e490aa14fa4fce0703558966d1dd804cba580d2046dcccfaddb02da835144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231996748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deac4cfb687175f1dff99a96c673a17fa15bd595c563af7094bf1be22c80ce0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:37:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:37:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:37:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:37:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:37:29 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:37:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:37:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:37:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a32edf2f71f415e4d0f760b85f158bab54c5b1f8d9904e205dd9e0e8af61bc`  
		Last Modified: Thu, 16 Apr 2026 00:38:15 GMT  
		Size: 126.6 MB (126562154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7e94bf3e4c836af7a06b169ba8fb598e3184172389c78cfce40eb6171351b3`  
		Last Modified: Thu, 16 Apr 2026 00:38:14 GMT  
		Size: 75.6 MB (75598531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e769b3dd39de11ec4ca1192329addd78ccce45c4e43cab3bc9195f54896cba82`  
		Last Modified: Thu, 16 Apr 2026 00:38:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec5cf6b599fdac4970e6ce39e192f8edc8299c841ab33a3102e11298e4540635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8012488230b97ceaba38a625d170a8f8dfef7088a252144ff1ef0e8808322562`

```dockerfile
```

-	Layers:
	-	`sha256:02c13f83332601b1f343d6c322d94e9cb815dd703fd99ffa2c82783484335da9`  
		Last Modified: Thu, 16 Apr 2026 00:38:12 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf1c5f1ad5d52f237ac30256528855dda50edc5ffef0525f463144cc5a7a4fe`  
		Last Modified: Thu, 16 Apr 2026 00:38:12 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
