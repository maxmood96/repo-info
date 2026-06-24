## `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm`

```console
$ docker pull clojure@sha256:649ab212fb42b33cf483978d7324ef3d192fb4db42416113e890183767d72dc7
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

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3bac6649e0e7cee5d2ce720ab7dae834f3442364f5cc9ee88a98ee777e33920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272533665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f34defae16abb861eedf350a32d4a92fb44908e2796693ad833c3b9bc1e036`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:17:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:17:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:17:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:17:56 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:17:56 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:18:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:18:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:18:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:18:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:18:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc50e56031389fa858a3f35aa0daebd0cbd73820b3f44c4575945a7e6923f4c`  
		Last Modified: Wed, 24 Jun 2026 02:18:33 GMT  
		Size: 145.9 MB (145905427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd6a08e2e1d6d62722c90fb54d4cff772dc2efb4007b75c37530a2c160c831a`  
		Last Modified: Wed, 24 Jun 2026 02:18:32 GMT  
		Size: 78.1 MB (78124988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cadc8ece6c1931d134c920925c7cc8f570138d907bf1639ee06fe606983832a`  
		Last Modified: Wed, 24 Jun 2026 02:18:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8486c70916201ab12902b23bf3db7fdec9ba8201445f178859ff6b7bee55f67a`  
		Last Modified: Wed, 24 Jun 2026 02:18:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a15fbc6b6ad4fc1ad0dafb1b6922f9d4247155a0b0024f275e4d779207b76b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e57a48ddcd0635cad1f9009f24fd89ea20640cf8abb7b9b59001839c8fdcc80`

```dockerfile
```

-	Layers:
	-	`sha256:d4de576948065b6b926a5bf176f83473076d7b3158ef8998cb21e46e9bdb36f2`  
		Last Modified: Wed, 24 Jun 2026 02:18:29 GMT  
		Size: 7.4 MB (7376134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea722844c4ea45ab5249c462ab99f9adcbbe8c60eaf05f0e90fe8234bb138278`  
		Last Modified: Wed, 24 Jun 2026 02:18:29 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6217c4849a2d9e9598bb4aa7c6ef9f4dbec4794544f6d71999adee4616a7ebe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271244129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83bf33ad1b13be97c91baae1c1f38cd5ba64efcea4f7951ea5d941b5c07d3ee2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:24:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:24:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:24:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:24:15 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:24:15 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:24:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:24:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:24:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:24:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:24:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9d82d6d7555817100ec4456b8ef081a1268c7a3cb676ba767e887f3b82db78`  
		Last Modified: Wed, 24 Jun 2026 02:24:55 GMT  
		Size: 144.7 MB (144724321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46bafa5d03598a64c51b88450b56ca54ca76144d05ee36a096aebe229c80e22`  
		Last Modified: Wed, 24 Jun 2026 02:24:54 GMT  
		Size: 78.1 MB (78129568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1741ffcd04c56e75d651902dadefb068df3689b98ae1b223d5abf443a5b1b7d4`  
		Last Modified: Wed, 24 Jun 2026 02:24:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be798f1e09d0b66a8c0cb7e22234b5e5817361d56a593176cc2436c809e79fa`  
		Last Modified: Wed, 24 Jun 2026 02:24:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5f48bcdadf35b78715a37c343dd730380aa9a19ba8cfd6373b02bdd32a612f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc721b441221aea25bb4da2b7aac6df7ccb1d33b75521b173106b1ee99659fda`

```dockerfile
```

-	Layers:
	-	`sha256:c06714521db44756f2847149c1b0bc30b2f8931e4ed50adc310ffa75652ead6b`  
		Last Modified: Wed, 24 Jun 2026 02:24:51 GMT  
		Size: 7.4 MB (7381897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fdbad351caa3ff348137e9ea8f047d7a36dc4f51409b5a4084a22fea9f58e23`  
		Last Modified: Wed, 24 Jun 2026 02:24:50 GMT  
		Size: 16.0 KB (16049 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:c366b62d622f5e12e8172306261b56ce5bd1ba7157acfc283e45f91f2895d124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282072663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd975e8f7186a6875fec7af2c1cff0618bf3b47ac1c5541d8a4b21a8b0705f6b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 08:01:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:01:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:01:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:01:31 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 08:01:32 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:09:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:09:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:09:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:09:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:09:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc3303405f604b9119feae76c1964b8d7cd671be00851817c5db88d3df2f4fe`  
		Last Modified: Wed, 24 Jun 2026 08:04:41 GMT  
		Size: 145.8 MB (145766195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d30949bf48c5bdef4f641231c25b795d35f04eed5c15651fb06b21d23f6af22`  
		Last Modified: Wed, 24 Jun 2026 08:09:46 GMT  
		Size: 84.0 MB (83958579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7825172d01d5a0ca52821c8d7b50eaaaf4c05320739f333c8282beafb3876`  
		Last Modified: Wed, 24 Jun 2026 08:09:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f3afbf22ae92a6f88b9398dd5ebbffe1d79cccc6879d7230fdcc7182593a6d`  
		Last Modified: Wed, 24 Jun 2026 08:09:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9fba8b1792c80fcff1b2e31254dae7390f41000c7e0e0491fdce7e0be71b856b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f263685f4eb9ba3471f03c91b549eaabddb80ed1eb4dfb6bece7e20fc15ea5`

```dockerfile
```

-	Layers:
	-	`sha256:5b2f44fe19edd6d216234793c6f74566c93a880b7373cddd70a697c697cc0102`  
		Last Modified: Wed, 24 Jun 2026 08:09:43 GMT  
		Size: 7.4 MB (7381350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a377f189e80738c41a781e202a82782cf2b49f434a89a3f08ccd1cbf0652341`  
		Last Modified: Wed, 24 Jun 2026 08:09:43 GMT  
		Size: 16.0 KB (15980 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:b0bac98f1f87594be2ca5afe4040c0ead34256a4b8a9a5efe5db895f88a26175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260002910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70868a17311977113488d612e31e4a8f94abcdd137a9e6eea3cb8bf2b21c7c29`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:11:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:11:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:11:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:11:02 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:11:02 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:13:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:13:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:13:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:13:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:13:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163a00859d47f645890acf4472c5048a743eac0767215dce1944e4a6c0c32b13`  
		Last Modified: Wed, 24 Jun 2026 04:12:35 GMT  
		Size: 135.9 MB (135910426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a5b9e693c04af9c33174bca304ca1e02710c81e80e9903e5e895be75b15ff7`  
		Last Modified: Wed, 24 Jun 2026 04:13:34 GMT  
		Size: 76.9 MB (76929767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaeef40976bdc39e0dd9c2f30d8453116f53e1872aba5aaa776e7aaf21e9dafb`  
		Last Modified: Wed, 24 Jun 2026 04:13:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1eb5ff0252c1ffde6b47771df19070471be6aa8d480a31b3760327464e633f8`  
		Last Modified: Wed, 24 Jun 2026 04:13:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c99081e9c632e8de935116efced15ddf1fdac38423430f4d1f8a38990dd63b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7383385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3238e2a0d8fda8a7ec54a801f4357d9ebb0ccd3b73709f3a33e8fad07c11e596`

```dockerfile
```

-	Layers:
	-	`sha256:d81decafa935d0c02125271351d3e0266ea7ab9b592c8bd03e2798ad4fdb8401`  
		Last Modified: Wed, 24 Jun 2026 04:13:32 GMT  
		Size: 7.4 MB (7367453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae0cba17843b234d44eeae113a2fb9395c3303903c654e56c0cac5c1b2d34d6`  
		Last Modified: Wed, 24 Jun 2026 04:13:32 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
