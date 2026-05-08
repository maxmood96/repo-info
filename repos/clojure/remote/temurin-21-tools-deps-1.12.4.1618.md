## `clojure:temurin-21-tools-deps-1.12.4.1618`

```console
$ docker pull clojure@sha256:1e752d447cc7c0ed634ac48cd23f5ae2e45abb7ff346df6be46af8f5cadaca7f
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

### `clojure:temurin-21-tools-deps-1.12.4.1618` - linux; amd64

```console
$ docker pull clojure@sha256:14f1d037ddb9c1feb332036dcff572f1733888b526f752cfea1ea377a6ddcd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287513099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef198425e0182deb4d7189225b9fa4d304851e23fc675b91282a3cebf1ffb72`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:19:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:52 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d481bac3cb68cfc946c2db6bf5993730fcd8837abe8b8587304aa8c4462fddc3`  
		Last Modified: Wed, 22 Apr 2026 02:20:29 GMT  
		Size: 157.9 MB (157857071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a8c4ecdce35666780600c1912c6bab3605f04440387debf4c1991adbaa67dc`  
		Last Modified: Wed, 22 Apr 2026 02:20:27 GMT  
		Size: 81.2 MB (81166362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a07c42df665f9c134169f47847a94b9000ee25fe7188764cbce1587068b3df4`  
		Last Modified: Wed, 22 Apr 2026 02:20:23 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5118e3e77b5f20161b657a69c0d4c9679dc1f09c93d4850eaff4f120a5a19c35`  
		Last Modified: Wed, 22 Apr 2026 02:20:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:c2067ea7cbb520288e673f099150d85bec27c6e373b95488ce5d6bf13d170b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b887bdd37980619ccc077dda715047edaf5abb5f098ec33ba46810c43fad80`

```dockerfile
```

-	Layers:
	-	`sha256:b1465063a9e188e674420014b1cca076f330139449856aff113c167c9a8cbef1`  
		Last Modified: Wed, 22 Apr 2026 02:20:24 GMT  
		Size: 7.4 MB (7380838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7288a0c8fc7fbbba0e42a1ccade98dd189edefb48a9d45fa1c3fee75ab5fbecb`  
		Last Modified: Wed, 22 Apr 2026 02:20:23 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:48afeba190e141f638bb70cb2f483377051bd8840858b99cd66c6cf8d241550d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286009435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777297f834e608b34fe43fc4eb3f485be470dcf1e00b29919debe45f2bac6bc4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:26:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:26:14 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:26:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:26:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a14438b793e27c7006f5f44a3ae858cd4a17fd25d3dc6d60e2305e2a40fa93`  
		Last Modified: Fri, 08 May 2026 00:26:55 GMT  
		Size: 156.5 MB (156461247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908331de17f4004f0f57da24523131bbde1b195fe327576c07d46336f63e2f0a`  
		Last Modified: Fri, 08 May 2026 00:26:53 GMT  
		Size: 81.2 MB (81174077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d9e7f67666aaf8b0a64a05ca1631ce89810d6876cc10619948a8c990da2d28`  
		Last Modified: Fri, 08 May 2026 00:26:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ffff3d7b0f2297f9bc1c8f2dfd900b4a0b16d3a3bb90e24b2632fb5b79f46f`  
		Last Modified: Fri, 08 May 2026 00:26:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:84cb2ff8a850fc0162bab41b83f17d9f759981bc90922e7c14ddcef54413fd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7404010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beefd63dfa62866c228282b7ee4124f923be2c745e2a6539a6a06a9bf8886005`

```dockerfile
```

-	Layers:
	-	`sha256:a8dcf5811c913247fb49aeca8a18bd540dd07ed902aeb40ec23fe0a63cc6942a`  
		Last Modified: Fri, 08 May 2026 00:26:50 GMT  
		Size: 7.4 MB (7387252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dfefad745d4ba85f83212dc4fc8fd98f1d807b572311a72d6e7a3beec3e7f3c`  
		Last Modified: Fri, 08 May 2026 00:26:50 GMT  
		Size: 16.8 KB (16758 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618` - linux; ppc64le

```console
$ docker pull clojure@sha256:9d1c66697ec608f07ea28dcced3045b4e24468a5feba842de0ab2546b20dd58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297685170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14f542482474e69fbd70c6af86a045b26cefce486e81d67d0b62423a405da85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:35:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:35:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:35:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:35:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:35:27 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:40:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:40:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:40:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:40:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:40:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0398f5f2459bce57485cbf20c7c00c0cc4acd23743ed54d0ac36f4b1a739a3a`  
		Last Modified: Fri, 08 May 2026 01:36:55 GMT  
		Size: 158.3 MB (158343239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8e0b4789351557860694b46272535c93117f7a4691328b094ce2686e9cf5a4`  
		Last Modified: Fri, 08 May 2026 01:40:43 GMT  
		Size: 87.0 MB (87004156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaba1804922b140c687efd6ac4549912e9bd9bc330683f54b12c24909bb597d`  
		Last Modified: Fri, 08 May 2026 01:40:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d0ecef2f15021651346f5987602abf46f737c2ec4425f7706698f9b793427e`  
		Last Modified: Fri, 08 May 2026 01:40:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:227679f74ffb57a162228e77838bb7c4b11215233033c07053046c5c2f9ca280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651970740fc77dfc0ac1c0090a9d4f5d185e143094a1444327c233b0d4e00902`

```dockerfile
```

-	Layers:
	-	`sha256:d0c209e45ae75c7b9991561c4472184b0cd6a9fd0946437638689394730fd0a1`  
		Last Modified: Fri, 08 May 2026 01:40:41 GMT  
		Size: 7.4 MB (7386693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e361a8246910435e103755fa5cbf2158ee2c284078498cbef639e138d42b3a20`  
		Last Modified: Fri, 08 May 2026 01:40:40 GMT  
		Size: 16.7 KB (16676 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618` - linux; s390x

```console
$ docker pull clojure@sha256:001f4ccee57ca38eebaa835e27d8cb1ad2e7e3877ee039efd21814a1415ca153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274234018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad45bbd309a2b88aa114b612718ac5a7fbf072b8c94e7d3cfbbff8da46876104`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:02:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:02:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:02:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:02:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:02:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:04:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:04:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:04:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:04:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:04:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823a94a034a486e2e5ad070f6a03cf5992927682e92a4d8ac4bb69d1ed8dc2bb`  
		Last Modified: Wed, 22 Apr 2026 04:03:34 GMT  
		Size: 147.1 MB (147105251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aebb546e2f387a309f6a68b4fd8ba56b7cc10be20933a9f675624598b7adac6`  
		Last Modified: Wed, 22 Apr 2026 04:04:32 GMT  
		Size: 80.0 MB (79979758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4140d0b1dfa405bc46b45e731cc6579693be9f9027e042f28d3b92910fbbe380`  
		Last Modified: Wed, 22 Apr 2026 04:04:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d63b4fe7ec385b141b782f5a781be94af52353d834d6dbf34763c3c515b6a2`  
		Last Modified: Wed, 22 Apr 2026 04:04:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:1b925f66140c899296ef697ac6592077943e244ce5eef30a00f8b84708d12e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94b9bc0fae2fb53712b01bf011468d33dccded7b504dbeece6e8ad1e873953f`

```dockerfile
```

-	Layers:
	-	`sha256:8f2de666a2a170cb1cd7d9e27260b182085dc33f82fb5b0b8afb6891c849ab88`  
		Last Modified: Wed, 22 Apr 2026 04:04:30 GMT  
		Size: 7.4 MB (7372157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c5bb700f1e1b8df6c632d5c47b2fe8a3da9b6c222472b6515639bbfefb52d6a`  
		Last Modified: Wed, 22 Apr 2026 04:04:30 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
