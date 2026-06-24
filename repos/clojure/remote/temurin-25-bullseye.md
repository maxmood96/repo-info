## `clojure:temurin-25-bullseye`

```console
$ docker pull clojure@sha256:e9b40f081f4c2cbf6f343a2d1c289f325f55003b61188b842270a1330159f5ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:df45536409fce8d6ed9053300ba07cbcb433900072232841fd6b630f7e0b5610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212861552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc717cfbf88607c4cb1b8adb76487f3c0968099fb40e6eed7ec578076cae19b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:21:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:21:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:21:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:21:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:21:22 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:21:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:21:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:21:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:21:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:21:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62879ccc16204396734f6afda741c59657fac3795c4dd2c47e0e8c7788336955`  
		Last Modified: Wed, 24 Jun 2026 02:21:58 GMT  
		Size: 92.6 MB (92574611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624a453da5e10d4464e677969720d5e40ad9b32593980951e210beabae1aea1f`  
		Last Modified: Wed, 24 Jun 2026 02:21:57 GMT  
		Size: 66.5 MB (66512891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b799c7d5693cbe3b28794f74a5ff564f6e089173d57aa1cd4f7b3d06e6dd1c7`  
		Last Modified: Wed, 24 Jun 2026 02:21:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff691ef9976dcf0d3b594f0e3f543c5d8f88fc2af216ba04cd8217beab5c060`  
		Last Modified: Wed, 24 Jun 2026 02:21:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f403a5616ae99fe609e0b627311f61c5a3366f1f51b4148313f7332ed52de4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af68f0b48ef994c0e08ef2b054b315d828ba1e14f8c933ce915b9d4b29b9a556`

```dockerfile
```

-	Layers:
	-	`sha256:29e3f2ccc2264b9f8e6cccbeb428b87a21d03d1854f4269e0b6fa8892796177d`  
		Last Modified: Wed, 24 Jun 2026 02:21:55 GMT  
		Size: 7.4 MB (7373519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f64ead90dd607a19a80ac94af1c540ac3cda293e48d35717a1de99ca38dab8a`  
		Last Modified: Wed, 24 Jun 2026 02:21:54 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5b786fd1c7cf4890a4fe5df26b3c96755adcb09c912d3e4a1ca597088428f95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210478501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1cb0527c652e63dbdcf59b9b69f1b2df8821407426325e92587583d91d3783`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:28:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:28:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:28:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:28:02 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:28:02 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:28:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:28:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:28:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:28:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:28:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a2a70d5ee2dbf3513e92299cea63b95e5cf802cd7fd022b31d58b47285e5fd`  
		Last Modified: Wed, 24 Jun 2026 02:28:39 GMT  
		Size: 91.5 MB (91542238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b062c8bc946e3c47c410128e3b678cd9a73e14cbb840699d18033067e6e6ae`  
		Last Modified: Wed, 24 Jun 2026 02:28:39 GMT  
		Size: 66.7 MB (66678003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4437a6adaa828059748e2adbcb8418e114e5fed8a9e8fa2ddd8a4a704a59603d`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b488b4fbe523ae8d8bdd170448ea032fa16daa2868349d4a45f65debef11e`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4ed70aec00a3c823505d3f01023aa59451913a4062d9ec262ecdddf0af895403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b63b1e46960eac09e112d4273882890680c4e7591dcba192c6ef4df2e80e0d`

```dockerfile
```

-	Layers:
	-	`sha256:b97fef62a844a766b487a192deea4826eb5d62f7f38684066d4d1506e73ab6c4`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 7.4 MB (7378639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3cac9e52a466fb149b1c57ee269bb9ac448993faa92e0db3f8c17b814a2d22c`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 16.7 KB (16743 bytes)  
		MIME: application/vnd.in-toto+json
