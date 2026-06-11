## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:972cb94d76028953cd79421076ed21daaa5d3300eac9c8d93f7cf5834da8a8ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

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

### `clojure:temurin-8-trixie-slim` - unknown; unknown

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

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-trixie-slim` - unknown; unknown

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

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:286d201e43f3a44432a501a17fde5a6a8b3575eb6e155e0f73903c60b6e612bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160644722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586a28005be935cf08ca161e40c31d45579199a4aaa043ac9015a238520aba89`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 09:17:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:17:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:17:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:17:46 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:17:46 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:21:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:21:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:21:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0dafcdb584c250d4f51034e4989e39dcd0d589f7a229452a6c4e6b6bc95ab7`  
		Last Modified: Thu, 11 Jun 2026 09:18:52 GMT  
		Size: 52.7 MB (52669138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfac144f5b168d0cf9aa7dbf694430fe3f77d709c5dfb18a2722fa352465665`  
		Last Modified: Thu, 11 Jun 2026 09:21:44 GMT  
		Size: 74.4 MB (74368600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b067a6d9eada3428866e7fa7591a1ae5fa03b178338297168a4c78e52e13a`  
		Last Modified: Thu, 11 Jun 2026 09:21:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:290eb25c48215548391813a476f7d06abea7d236bec56d129bb9143fe4c1bb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc8b103f6cc319cb3598e7caa0963a6e7f0f2373cbff69981a7764a994731cb`

```dockerfile
```

-	Layers:
	-	`sha256:ae543fbe626d3f72321445348a83ca4b8032c1680ecdca67a294b36e4da3f892`  
		Last Modified: Thu, 11 Jun 2026 09:21:42 GMT  
		Size: 5.4 MB (5382568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20163c3efed31c68d337ee75ac8105a13553b735b0731b1c51e4f66c4dbb592a`  
		Last Modified: Thu, 11 Jun 2026 09:21:41 GMT  
		Size: 13.5 KB (13476 bytes)  
		MIME: application/vnd.in-toto+json
