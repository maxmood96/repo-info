## `clojure:tools-deps-trixie`

```console
$ docker pull clojure@sha256:540b2471a32076a9613a2a6351d7fca810579e856b4685fe884509f3baeefda0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3b907140f9d0599041b8a4b77ddd1d925a26800cd08d2ce0f21dc2c8e51bd249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226881754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38abaade06f8bc073a459deafa8bf58e069fbccf060dfc00504312350664e001`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:23:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:12 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:12 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524dbeffba95db33e7103389d24b642e57761d3e0e8f12a61dd6d7d75397dc04`  
		Last Modified: Tue, 03 Feb 2026 03:23:50 GMT  
		Size: 92.0 MB (92045330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730b4add08637eac5d318fbab04c3afd8f5bf4bc42fa1c8612340393073dfaf1`  
		Last Modified: Tue, 03 Feb 2026 03:23:50 GMT  
		Size: 85.5 MB (85542430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d849ed9048fbbde4420377df224933bd2eb547000a8f05d24a40550e4e750b48`  
		Last Modified: Tue, 03 Feb 2026 03:23:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea62353e009119bacaca51437ac5bd35ac47588fd56fa4500c9d2fa8c293e994`  
		Last Modified: Tue, 03 Feb 2026 03:23:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:aeb41fce28fd8bdf335374f219fa13a9ebabd82ab3e67072f7c18aaaaf2be77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac60ae00f0ee64f9d504d0d2c212009cdb12ef946951b6497b51bf4353eeea3`

```dockerfile
```

-	Layers:
	-	`sha256:d826d9ad013e5b296bd32ba602f8acfb22af06883b536e5c817f5e848807c811`  
		Last Modified: Tue, 03 Feb 2026 03:23:47 GMT  
		Size: 7.4 MB (7419158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cecfea8bb43eb0728617d3f841c7f5f18e6fc48baab14680306852f6e2ac5e66`  
		Last Modified: Tue, 03 Feb 2026 03:23:47 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a038e13b4a4951bdff7834e60e9f9af9a1c34d36e3b7763e90ef03c226e5666c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226066869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872d457b9534257b1ecacf63c13e8ddfd6510da1d74aad5eceefba1f056ae7da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:25:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:25:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:25:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:25:41 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:25:41 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:26:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:26:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:26:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:26:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:26:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34b547d96db252f97cad4b67c1b1dbac2d1f553c03aeaf5a4a27eb7cae5c81a`  
		Last Modified: Tue, 03 Feb 2026 03:26:22 GMT  
		Size: 91.1 MB (91052482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b088a1d5c6ac0a54b42e31c52259d67d2b202624d8a826880731b8fb24719814`  
		Last Modified: Tue, 03 Feb 2026 03:26:22 GMT  
		Size: 85.4 MB (85361327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7211c8fe3a4fb1cb22866ec210f56efd751cf59a60393814d430c5ef48af9f7f`  
		Last Modified: Tue, 03 Feb 2026 03:26:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e43baec7dfacee2f99bc375820c839f5929335f3599cf400dba56f2fb01e21`  
		Last Modified: Tue, 03 Feb 2026 03:26:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:afe609172072118aca717853678ff879ffb2329e9e57d3e3cd4b7c84fed25b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0392259b825834d0a2aa67d387fe4cf25d5e5c7391b41dac56b5309baa8b45e7`

```dockerfile
```

-	Layers:
	-	`sha256:d84496e3cb090fbeeb7f76f4026770a07b6b9895f50311995e7592deb2a54f82`  
		Last Modified: Tue, 03 Feb 2026 03:26:19 GMT  
		Size: 7.4 MB (7426209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66dbee5931ac0570357ef591200d56287758970477131745bd6975642cfb183b`  
		Last Modified: Tue, 03 Feb 2026 03:26:18 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e90e333af2d8bb29a4392488ca5878ea2aedca38b7b5b8c4c3ecd9e9110e0ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235671498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c93259db317581758bf20ea693377dd14a254ef24086798e46cc8aafc75dcc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:53:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:53:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:53:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:53:45 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:53:45 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:57:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:57:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:57:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:57:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:57:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10e5aa8395183e2062d241448e3330aae274c98e53b0e8f60cc593e6ecb6bb0`  
		Last Modified: Tue, 03 Feb 2026 09:55:09 GMT  
		Size: 91.6 MB (91610746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be2f6fefef7e5c5dd30a5d860640eb7d2bc18f44650b6e221051450896a1398`  
		Last Modified: Tue, 03 Feb 2026 09:58:36 GMT  
		Size: 90.9 MB (90947594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf37a78f34e6d7c103d8c1270675984b77104c2d3f98e891cbd9808183c53ded`  
		Last Modified: Tue, 03 Feb 2026 09:58:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d707a75676cecc3f6c865f5bb6a895aa35f9c39395c7473e09fccc68244d6e`  
		Last Modified: Tue, 03 Feb 2026 09:58:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e012a750cfd38d94d33bcdae4770819f63848e4208aaacdc578f98f8422f2f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f362e65abee37bd11659db6f688eafae0bb869d8c0d874afbf73c8298cefe9f0`

```dockerfile
```

-	Layers:
	-	`sha256:89e137a048a562bd312bcf56808fb7720e16a0abf905f0d5aa169801412b50dd`  
		Last Modified: Tue, 03 Feb 2026 09:58:33 GMT  
		Size: 7.4 MB (7424889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18fa211ff908b5655575f9990d8b52775e849e10ccb0646be059e68d6139c873`  
		Last Modified: Tue, 03 Feb 2026 09:58:33 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:5c219ee045fc260defd373e8529b67844e1d227eb6a172fbca4c9309cc5bee72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222955849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a556ebc1d5ffcefa7699fa85eb9fa8d923a1c33ec8bb18b8592cfbaf98456a20`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 21:12:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 21:12:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 21:12:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 21:12:22 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 21:12:22 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 21:27:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 21:27:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 21:27:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 21:27:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 21:27:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fe598f31566ea16873e9a3c5986699f1d21dbe097ec6c69f669dc2451a4a6d`  
		Last Modified: Thu, 05 Feb 2026 21:18:03 GMT  
		Size: 90.8 MB (90752897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10be60d230f5c519ec8ea1f0d7030ade80016821267158b8f61b606db21d88e7`  
		Last Modified: Thu, 05 Feb 2026 21:31:29 GMT  
		Size: 84.4 MB (84425145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cb9e92ecc49cddf2bf183307e29f8731156f1971bc60140bdfcaefddd9c748`  
		Last Modified: Thu, 05 Feb 2026 21:31:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cf36d9abf94ededf1d6024b3edc28c9fcfd4da6bb8e80ae50988f43631edd8`  
		Last Modified: Thu, 05 Feb 2026 21:31:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:986f45307916db81ef97dd7abb9a9e2622e8e9bfe5d6cb1a83042e9776b5168a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ba0d015d0a10cdb6dbb93687f8102a9b3de4f517b7d9854a6aec362abd0d68`

```dockerfile
```

-	Layers:
	-	`sha256:1b9f2f1b00a69f7d2f6a416e16424d1e07369580fb3f93441fa5cabead90f2db`  
		Last Modified: Thu, 05 Feb 2026 21:31:16 GMT  
		Size: 7.4 MB (7407082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cafddf9ddacbee4832764d15c4cee57d7962e42a61153eb32ce2752138a7b5c2`  
		Last Modified: Thu, 05 Feb 2026 21:31:14 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:7617a5c4728b44e3e0e8ec993b6322b182a2f88964b0e09084de58608a95fdf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224077934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccff479f715783634f8cab9f252212cc1c0c28ff27a88c337f1151769fdec25`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:06:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:06:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:06:03 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:06:03 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:07:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:07:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:07:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:07:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:07:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44692e8f5993370045053829da7afee7b337c7a2e81c01f2c2132ff813e3d17b`  
		Last Modified: Tue, 03 Feb 2026 05:06:43 GMT  
		Size: 88.2 MB (88210678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6497f3ea6d2dced8b79feb0ff9a23e9f2298da6f59184ca7e1eb2be4fb106ea6`  
		Last Modified: Tue, 03 Feb 2026 05:07:42 GMT  
		Size: 86.5 MB (86511836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6884644b9e159a4c02ad6b2c457d24c4ab343f4b5e1924b5a234a5dd9477d728`  
		Last Modified: Tue, 03 Feb 2026 05:07:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1366c6d353cb270a428d1a4e0d4eaa1e33f425b151cd061dd28427272f2bc0`  
		Last Modified: Tue, 03 Feb 2026 05:07:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:227785a489f773b8d04b176962a49c1b91c4f6a24e5450e99f2b7683ef9bb77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea385fbddd27d64ff086bbe643cfc5ecce2660561e23ecffb9971d469372ff2e`

```dockerfile
```

-	Layers:
	-	`sha256:66c76ec815003727947688c14f5daf506b3f3c40545e19691463a1001dc6ea12`  
		Last Modified: Tue, 03 Feb 2026 05:07:41 GMT  
		Size: 7.4 MB (7417628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:497c28d7b42fbd4d38dda52c1016314742b10a999be5a11780a141f1bb68e779`  
		Last Modified: Tue, 03 Feb 2026 05:07:41 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
