## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:5f2c42a92496cffe30488b1d907c954cf58ca87d18f3c628b3a5410be3b77073
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5c00e6efd1e21dc6ee848bbf91b19040c30546db253aee6f4f5c405c57378320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269270090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce0b948738379e0308383580048c25fb4868809ad213dde3b620da5f16213d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e001ad7ae096669b6d88ee4d504f40adffadab88e8b6a298aee5ecc73d6d720c`  
		Last Modified: Tue, 23 Jul 2024 02:01:06 GMT  
		Size: 145.2 MB (145166521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9941c44d06d067f6654174b5e85cca5bcfcfb89aaabb7e24e42145c875c8dde3`  
		Last Modified: Tue, 23 Jul 2024 02:01:06 GMT  
		Size: 69.0 MB (69021165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d8d94b1502c35cc971b05968e968f4cec95dfd823c7525403f586b37b515b7`  
		Last Modified: Tue, 23 Jul 2024 02:01:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc175d3a275aaad307f202cad865065bf7a6e8d948f9fc937e9434ec826e6e6b`  
		Last Modified: Tue, 23 Jul 2024 02:01:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9bbbad953b6dd6cf4625a06a473aa1ed75976131a29a81fd27a31e4f11c8ac0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8876783e1ea1bfb60dc1966bc6af7408c9a8a1e2ff934ba199558110db728465`

```dockerfile
```

-	Layers:
	-	`sha256:96e4555336d0b0832dfba6b8f259c8ebfc4e96ec51fa8a849ac69b6af18ca584`  
		Last Modified: Tue, 23 Jul 2024 02:01:05 GMT  
		Size: 7.0 MB (7040344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c3efebeaca283d2def2abf520803cc9208ced15274a9033ee2317d8b664d604`  
		Last Modified: Tue, 23 Jul 2024 02:01:05 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b3cd9bf4993c3bb7b8f589cf6d0f9389e1a0670cda2a027383a8e0c7c288a14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266749269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5547bd1d1c892130007bba1e46ecf1a12d3937b695679d46e36cccf0da86b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accd4022fd10bdf90d9867428728c11f63914bb907fb3d33669e944f902b3c49`  
		Last Modified: Tue, 02 Jul 2024 09:29:36 GMT  
		Size: 143.9 MB (143892757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12016a3d6377ce756a293000d43146da9853346d22b3c8dfb5dfd300e55c77b9`  
		Last Modified: Tue, 02 Jul 2024 09:33:56 GMT  
		Size: 69.1 MB (69133819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baec2ce90d4b77e36e1d96b640452090dfde07305f0d881a73e966bcc5e1919a`  
		Last Modified: Tue, 02 Jul 2024 09:33:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e83f46dd527d6d2e7bb5e5247728074e2fd1be571f2f1f4adb6bf2e2ec88ad`  
		Last Modified: Tue, 02 Jul 2024 09:33:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3c59e1a6ff9db4b47f37d6aba3cd58c7d0812728f99fca4ef4a76ac6ca6b39b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870a7934015f2fdd95171c9b09eba4fa97f9fde042a5e5d975a6dd376f75765a`

```dockerfile
```

-	Layers:
	-	`sha256:465d17598c0f7fdd0a5c9f68b9bcb3132637e77f1ddb6e267c4a69f1b10f1e4a`  
		Last Modified: Tue, 02 Jul 2024 09:33:54 GMT  
		Size: 7.0 MB (7005512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df45b66314009052b48161c3adcb1cde720f2967d79d464325ba41638dbd27c6`  
		Last Modified: Tue, 02 Jul 2024 09:33:54 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json
