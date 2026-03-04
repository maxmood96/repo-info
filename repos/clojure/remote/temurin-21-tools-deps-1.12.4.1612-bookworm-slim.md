## `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm-slim`

```console
$ docker pull clojure@sha256:751a79f4a6467b59f7bc35fab5a4d443b3fce8160cd15f56879c7204aec1f800
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

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4c77bae7b4b5cac1f48620e5b6691ecee5240a5bb99abbb6ceeff408112f5590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255795895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a56714562a4edd518426d439cbdbcc69ff762949f83f09ee04e20110b08247`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:50:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:44 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:44 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9b29a46f257203aff88cd140e72a0e13b275a8cb671f8a5fc0ca262fb9c6a4`  
		Last Modified: Wed, 04 Mar 2026 17:51:18 GMT  
		Size: 157.9 MB (157857099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e7af4ec886da31c27c47b02b651e86102f056b8e6a5c541024a54e38e82d08`  
		Last Modified: Wed, 04 Mar 2026 17:51:17 GMT  
		Size: 69.7 MB (69701473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365c6a12bc504c8848f95362dddf6d1a04e1dab6ad6141832eb0c08cf1e8773a`  
		Last Modified: Wed, 04 Mar 2026 17:51:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8208a19571be3a4e9b4c2c8828ce7ab91da23d41ca889b1aad9115e652f23fab`  
		Last Modified: Wed, 04 Mar 2026 17:51:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9965640aa1b9865c6b3f5a117e6f7ec300b6e1d61b6d4b7201cc12621f0605f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795a247e31ceef696a0632f0d9042f929e49e409936354d6eb78ef45e63ef321`

```dockerfile
```

-	Layers:
	-	`sha256:d45c53930e9945cb0add0aabd644cc9df531c362a458b95d1cc7aff09c9b43f9`  
		Last Modified: Wed, 04 Mar 2026 17:51:14 GMT  
		Size: 5.1 MB (5118019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9967980143571014d94e7ee07d632116e972ddaba059b8861888ee3a1c7532e9`  
		Last Modified: Wed, 04 Mar 2026 17:51:14 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:810dea5518f065e6d93bdca1e7d2810b7bf5d740af8d7e5ebc91efc8064318bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253938784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2316088c70def581d8e0affb825e000265600feb49ebc001fdc41c41d2c235`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:50:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:24 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:24 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16de3644e584cdca97b6a3d77eb27fdfacd5ef6eff2504b0bafed355f26a956d`  
		Last Modified: Wed, 04 Mar 2026 17:51:03 GMT  
		Size: 156.1 MB (156133092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94fb4b9745d0944d58e7e1cfb89663db8a7b726e79da9cacbc2b952d23e7d28`  
		Last Modified: Wed, 04 Mar 2026 17:51:01 GMT  
		Size: 69.7 MB (69688572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df67367702e5109268f0717067936c755e944bfbb6e31d6aa3833b038915666`  
		Last Modified: Wed, 04 Mar 2026 17:50:59 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98145811ef30f24797a4e4624b66b5467e35120d47a2f214fe7d8f3fe5f3fac`  
		Last Modified: Wed, 04 Mar 2026 17:50:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1224d05a41dcff34a3c8dac12be35ab17fa8786efc892f647a8fbd329eb654bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4764f2e1510ef54c2b6b6bc6b0b06b68aa67a438cefdac42e84c679bf848d41`

```dockerfile
```

-	Layers:
	-	`sha256:dca272c171a264bac069bd003be4db931be58d5e24f0191e7d7f53fa56a10234`  
		Last Modified: Wed, 04 Mar 2026 17:50:59 GMT  
		Size: 5.1 MB (5123780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85f829bcb8cbb143b4ec98402a64c316ffd99e99ca2cd675bdd2ff0311d360ee`  
		Last Modified: Wed, 04 Mar 2026 17:50:58 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:09e2d9027b8a1081f0da97439c71bbd29ff8fe060cca78693d2a214de0768fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265590030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445898b86f45da88819365d1989d97c2d3cba65665a58be5d0dcbebbff1c29cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 18:03:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 18:03:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 18:03:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 18:03:19 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 18:03:20 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 18:04:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 18:04:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 18:04:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 18:04:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 18:04:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b2f86062ce2ece30a39cca84be6bee97c4ef36f623592a4e3d6b23cbc744d`  
		Last Modified: Wed, 04 Mar 2026 18:04:53 GMT  
		Size: 158.0 MB (157977551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457c32aee901b0bb7767e4d25c1739c98b3f2162cb62978f07315dbecd4e3ebc`  
		Last Modified: Wed, 04 Mar 2026 18:04:51 GMT  
		Size: 75.5 MB (75533100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec75cecd9cffafadd798b5bfe04913187d674885093a7fa52d153f68b586e9b`  
		Last Modified: Wed, 04 Mar 2026 18:04:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafea2df7277cd3ac9d43c574f887e97ebac8bf590a3d330c8eacce62e6ab807`  
		Last Modified: Wed, 04 Mar 2026 18:04:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8087170a44a87626e3d9f1090a1e19f87a5adc6a37ee94087f7d02391427df2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533a2d3bf734756f4c6ae84b0ea4adcf927c411145cc29c3dfde211669584762`

```dockerfile
```

-	Layers:
	-	`sha256:40abe7491507734335f3ca055469a0c98eb8f5be0780518b14a17bed92721e6a`  
		Last Modified: Wed, 04 Mar 2026 18:04:47 GMT  
		Size: 5.1 MB (5123177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed340129176cc5498db86598946ccbc01cafce6ea4014498c9ca5aea9200e18`  
		Last Modified: Wed, 04 Mar 2026 18:04:47 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a46d3f556e24a235097e94ccd29aa105d5dbdf4ce135b3c043545dd69e0200a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242511271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf8a7cc049ede2e210841d47d740f87c5654ec4793cea4e8502a3980407c41a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:50:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:20 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:20 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a684129a82f26a3c08ae976a299ba50684f9c07f32b2cfbb3669438689e45`  
		Last Modified: Wed, 04 Mar 2026 17:51:06 GMT  
		Size: 147.1 MB (147105251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c3f66cb2e2454122ccc97fe4c70589afa0846e0cde041a8c62763983d23422`  
		Last Modified: Wed, 04 Mar 2026 17:51:05 GMT  
		Size: 68.5 MB (68513454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2256085fe65e2a3176f692ef202d13714b9433ac6bc980a090430e8a909b9c33`  
		Last Modified: Wed, 04 Mar 2026 17:51:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420d2479b99319f16feb6aa7f85effff91f17e158bb55341b4ee237d15c01ce5`  
		Last Modified: Wed, 04 Mar 2026 17:51:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec9f988b0dac9ab5e4ee3badd9158cc66e5e7766278e9ac622467c9951e20423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8322f5149d50558e23acb000ee087ce8491dc962b8dc9a5e11708b26e0b2660b`

```dockerfile
```

-	Layers:
	-	`sha256:8f4e55e68f5219776515aa222e609207881bd367cb758428464bb6ad30a9204f`  
		Last Modified: Wed, 04 Mar 2026 17:51:03 GMT  
		Size: 5.1 MB (5109340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f45ba89d7a3f872373755b8ea30a439f72ce01f416492760948a6af26c179fe`  
		Last Modified: Wed, 04 Mar 2026 17:51:02 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
