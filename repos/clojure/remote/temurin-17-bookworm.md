## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:176397cfdec536a31e5a099fd68a996579042382020efd5cd1b64e17afda9f18
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

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:47940e166a5bb469ae7a0afd456a0654b5bc438f02c92e7941930bfe3b913e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272533470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75b9e1a9fab50fc5fefabd0f5b5c4b28a7f200a2adb7583c76ba74c4a861320`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:18:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:18:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:18:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:18:44 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:18:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:18:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:18:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:18:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c218ed03ec7171324179ef6495b62c61c21692fde82ac0e398781618297cc5`  
		Last Modified: Thu, 11 Jun 2026 01:19:20 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b535c906b47b567948088a8904d1e841848083d94083052af21894f78a3acb`  
		Last Modified: Thu, 11 Jun 2026 01:19:18 GMT  
		Size: 78.1 MB (78124939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bb23b132e43b3074ef9471c86ebb66e83ca3db3901baf09782a97ae862dd8c`  
		Last Modified: Thu, 11 Jun 2026 01:19:15 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de49395fd0b680cecd84a6e3946f231096c090dfdd5183562e39bcb6e60541b`  
		Last Modified: Thu, 11 Jun 2026 01:19:15 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8d58081816d3007de355aa0a0a0fed7dc23c3d0849166555fc1f59c619e0cc60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384d549d980a9cee2b41b4436b4f60671e9cfd6bc026f285304af648e20b69fc`

```dockerfile
```

-	Layers:
	-	`sha256:9b7689750f6bad00449bc3492c4c6157a7c2486b10e4dff152ef22f2272137e7`  
		Last Modified: Thu, 11 Jun 2026 01:19:15 GMT  
		Size: 7.4 MB (7376134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7aed0f995660a0c377db190b5873dbb822314d772459a1a290ec0c5133cf8f`  
		Last Modified: Thu, 11 Jun 2026 01:19:15 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1919548bed7dd998a0b94a99759c91b36fe82e350884d08933bca8572f7f0fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271243774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c20c0e04544c35dd8971e704e6fade2096844464df621151988633fecc9fad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:22:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:22:47 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:23:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:23:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:23:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:23:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:23:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830bc4413373a9ec92f3016dcca6740b73dba7d2181fc7a16d88332a921e1aac`  
		Last Modified: Thu, 11 Jun 2026 01:23:24 GMT  
		Size: 144.7 MB (144724335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fa7aaa40239148a2414d74e4d7e6ec77778055a51734184564320b10d0e7cf`  
		Last Modified: Thu, 11 Jun 2026 01:23:23 GMT  
		Size: 78.1 MB (78129383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8ff801415c58afa925191d9470613821f0a470667f33e4eaca39577de10570`  
		Last Modified: Thu, 11 Jun 2026 01:23:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a888c0af3b988c1923fedc65371fee171133eacbfc15ea79da0cf4cdfb16d717`  
		Last Modified: Thu, 11 Jun 2026 01:23:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7e5baced8d01df2a952d9f85c01e039c7bdf459e2bd8286bf3efbb2b59a07343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad778a6b35d740ef7c2ecd249847e0f5c624dfa834db206f1709e065bcbadaf`

```dockerfile
```

-	Layers:
	-	`sha256:cc2d2182a438c9902f3418f850a9a57718619cfea3eedb29d56197a69dae82d3`  
		Last Modified: Thu, 11 Jun 2026 01:23:20 GMT  
		Size: 7.4 MB (7381897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:028b6aa03971d183d8e4f732dd347d481cf8f22a772666b6c5a1e4b479757b15`  
		Last Modified: Thu, 11 Jun 2026 01:23:20 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:7991d378f0bb7734351c6f7bff45d0c5424ec3c022f2eab95f357b82b9e09a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282072743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7ff48e3e72937c3db87b123017a9a707daf75ea3f815d90da0aa4fda19cb1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:29:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:29:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:29:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:29:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:29:27 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:34:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:34:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:34:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:34:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:34:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bab2c1eb2f066d3ff6bab086dbc5fafbc50c746db8da2cc3d2b22fadc81c442`  
		Last Modified: Thu, 11 Jun 2026 09:30:52 GMT  
		Size: 145.8 MB (145766120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72966509623c726b4cba9fe43a46dd2b325f91e2741977b28e5ad24a3d72ea9c`  
		Last Modified: Thu, 11 Jun 2026 09:34:47 GMT  
		Size: 84.0 MB (83958913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76184b2bae89cdc3732d9fbdfb39e3cdfe5b1ee957b0f397dac74f533f79d8ef`  
		Last Modified: Thu, 11 Jun 2026 09:34:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa913b4b701cdf0e57cfb16ff4bf784ff9b8fbee3c81a4092371efa61ceebe39`  
		Last Modified: Thu, 11 Jun 2026 09:34:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fcf9fce5c050da0d19f070b0a66fee689eee856e1e9a94a3804311d2d1688b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998d12ddd4757509c31290cc3f70842109cf0817b4aa3291603cc073309dcb7d`

```dockerfile
```

-	Layers:
	-	`sha256:b1df60d5d5d01fa9d1eebc49b31625396396ac42274f4b7c2d93810784b69e39`  
		Last Modified: Thu, 11 Jun 2026 09:34:45 GMT  
		Size: 7.4 MB (7381350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a59bd49328d83a5761dadd27a72ede7bfb0a21d5536bf6f4c6337e510671301`  
		Last Modified: Thu, 11 Jun 2026 09:34:45 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:da156d9c55590af4186c6b4b3ca469039eb32a7b3be015a07cb1c79a225817c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260002457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d15f3d3cbd401dbeb8a1adaf213cee2276afe664760eb44a3e981d515ce91b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:08:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:08:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:08:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:08:43 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:08:43 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:10:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:10:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:10:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:10:07 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:10:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926c439affe882834bbc28f308a8c4852fa7e61999319fb64f635b6bec189cb`  
		Last Modified: Thu, 11 Jun 2026 03:09:33 GMT  
		Size: 135.9 MB (135910383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d6863637b3769a103d9239b2723812af3a6eb870193d3ee3c1d30eb4684acc`  
		Last Modified: Thu, 11 Jun 2026 03:10:37 GMT  
		Size: 76.9 MB (76929536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fabce59524b2e3d6b2064cde87e779b945fd390173b32d8a3514efa75f8103d`  
		Last Modified: Thu, 11 Jun 2026 03:10:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a4a238ca1ab6fec6f16fa86354d737db0f8438ba75341dfb7fb8485f371531`  
		Last Modified: Thu, 11 Jun 2026 03:10:34 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:86ecb5f302a8e807e7ad4eca583e25d1d09efdb27f43165232b20d070f5459f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7383385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5888cb62fa1e7cbf6f1ca0fa1a6ce459e3eac9ebfcf05c554d7f349c202c40`

```dockerfile
```

-	Layers:
	-	`sha256:2352f73a7537b8c844172d03648ae5e9ff9957b6183e707071e1293da37fa719`  
		Last Modified: Thu, 11 Jun 2026 03:10:35 GMT  
		Size: 7.4 MB (7367453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df04611adb4ec2f843891950ecbd8ab3cb371a5b336422313f5f22aeaa53719a`  
		Last Modified: Thu, 11 Jun 2026 03:10:34 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
