## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:912394a746d4e8eb6e85dedcf992bb37a7ec70c0a37e6de9b3aa4782ac6bee2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bebb25b7c971efc7307c5de337762d95f8ecbea6ee782aa2b8eada074182fe69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153936423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ce319875112d2b7443ba83e0784d32de45a51fb200c5b05e76f703b497d0d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:16:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:16:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:16:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:16:01 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:16:01 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:17:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:17:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:17:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fe6547f42a64279074ac2ff0a6bdfb75cc700d15c0212ef99de77ce645184e`  
		Last Modified: Thu, 11 Jun 2026 01:16:37 GMT  
		Size: 55.2 MB (55198725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e35fd553aea2f40257fdb66509752c8d2663dd69f17b2702dfdbd7fcba4db91`  
		Last Modified: Thu, 11 Jun 2026 01:17:26 GMT  
		Size: 69.0 MB (68951641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d602b554c47af56492be54ab7006242c7157e2009a2d788875dfdeb3f12b92f`  
		Last Modified: Thu, 11 Jun 2026 01:17:25 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e3dd7c67dd801a2e1296892c849b492159ca26101d17a693130bf87a52713907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3991f48f3a1898cf41dd3aaf0921c4e08d9b1cc5cbe2db35729e4a7553f2d3f`

```dockerfile
```

-	Layers:
	-	`sha256:841713ef82564d18ed0b13707b55f768440466090c5dcad6ebfb7acdcb3b2955`  
		Last Modified: Thu, 11 Jun 2026 01:17:25 GMT  
		Size: 5.4 MB (5377602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43ceb441284d3821e00a561c9dc927e7ec690aeb4701592f2d37b3bbad3b04d5`  
		Last Modified: Thu, 11 Jun 2026 01:17:24 GMT  
		Size: 13.4 KB (13428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8a407842a723e946f06c71308c18ac914cab805a4922ca283cc3fb785ece4847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153199585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a233f44cb9364c5f6e5c65b03e0139a08f636a904006dd016313df2809abf0e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:20:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:02 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:20:02 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:20:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:20:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f46937d4c333cac54de2b567124c6611ca0cd80e3e0875d3a5b27805ea807`  
		Last Modified: Thu, 11 Jun 2026 01:20:34 GMT  
		Size: 54.3 MB (54272936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ee85b3f052bd06e3a96a22befa7d3118419f87798e3141754fe60c71a10516`  
		Last Modified: Thu, 11 Jun 2026 01:21:16 GMT  
		Size: 68.8 MB (68777474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b715c66f1dfebdd6b711f6356786df82abde7ed67e95e1fcf2b81a51eaae4285`  
		Last Modified: Thu, 11 Jun 2026 01:21:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d5f6a240d7d91d06efb5c8309fdca95f66a0350acf6208bfbdd6d6aaec28b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dff884b96b243bda680116899bb39f873167f6b2f18a36419797be8c0b7a8f`

```dockerfile
```

-	Layers:
	-	`sha256:ca99b527a81472d3f38e994db8dc4fd57216f3d3da9f75b73133f645332bc60e`  
		Last Modified: Thu, 11 Jun 2026 01:21:14 GMT  
		Size: 5.4 MB (5384063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0c262fbc2024acee1ed720a93e631d7afd5e16a07c7d96a3b225dfcb6d98768`  
		Last Modified: Thu, 11 Jun 2026 01:21:14 GMT  
		Size: 14.5 KB (14498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3ed3c23397ec1909bde667891acd31f75b89766ce3747189bf6fc0337a13a7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160639350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609a0f7feb19dc5ef7e9c0e441152cd2e6b255673e394f186471657b97c1160c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:45:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:56 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:56 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7961f98cc972c19f52c3da7f9574fdbd686cce1a2ba4e6c10d8ccc0f8c2c5c`  
		Last Modified: Thu, 04 Jun 2026 17:47:34 GMT  
		Size: 52.7 MB (52669122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fb51d82d4f82f7c9b0cb2393b13b569b19effd49b6f8cfaf7cafebd6330c22`  
		Last Modified: Thu, 04 Jun 2026 17:47:34 GMT  
		Size: 74.4 MB (74369128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d615f2c88d65683aef13b230568eec639f487e8f0e3647d8a02db789d7703d19`  
		Last Modified: Thu, 04 Jun 2026 17:47:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:24ff5af648ad466f0663fb4cd90290b3cc63f9dd08900e5284e0631c99e67361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3760cbff6c8e9f378f5a8b94ced1b246ddf750d26f21c45511170440fd667a3`

```dockerfile
```

-	Layers:
	-	`sha256:1838536e4d318280af607eda166a3d14956e7a460ee5f3d50a409f053ad3656e`  
		Last Modified: Thu, 04 Jun 2026 17:47:32 GMT  
		Size: 5.4 MB (5382568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e3902f501ad845d13568cbceb6458daa325a82b4c949bcf1d3f5c39def83191`  
		Last Modified: Thu, 04 Jun 2026 17:47:31 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json
