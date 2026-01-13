## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:1d0acae132571dd87af950d4d93abaa24e126f2a4c0a79e3847fbb6f057c33a4
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
$ docker pull clojure@sha256:d6696a734c72ce61ab5c565643e02c8dca8c183e7af4ab1ae7f4720607c02cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274476669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c59e9c3b42e54007a6ce79d07bf02a810f0599acf4b9462237dee903fa730ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:57:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:57:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:57:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:57:43 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:57:43 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:59:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:59:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:59:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 00:59:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 00:59:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b646c925f63f627dc99a80f05c6e0dac0bfae2a4777f9319eed952d4efd04492`  
		Last Modified: Tue, 30 Dec 2025 00:58:42 GMT  
		Size: 144.8 MB (144847922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fce30e725e05991432d539f08801ca10bd5d4560ec22cc035c33602b6b35558`  
		Last Modified: Tue, 30 Dec 2025 00:59:51 GMT  
		Size: 81.1 MB (81146913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974700e179cde53866ba69acd01fb48c9add628bbefccecac7da0622f197b7e3`  
		Last Modified: Tue, 30 Dec 2025 00:59:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa275f8f63bb4ae38569ea109d317bae01bf21cfe6a70ae238483a104b56497f`  
		Last Modified: Tue, 30 Dec 2025 00:59:43 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f527809e7e66e818111c1862ea38385f194596959ae7f9963518eb4f13923067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac2fa33cf25324d72d56e95bf3703b1e9c089d4db455e8d2ce7c4d267f595d1`

```dockerfile
```

-	Layers:
	-	`sha256:4403ba67b0ebdca6f0d7db8a22ad5b4196b5b47a7f0f43e3b21bb7beeb8ebfb5`  
		Last Modified: Tue, 30 Dec 2025 04:39:21 GMT  
		Size: 7.4 MB (7374892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de93a107ec3210d5b8aa0af153dbe1cebaebcf296f2a4f37de14a2f525fb1e1`  
		Last Modified: Tue, 30 Dec 2025 04:39:22 GMT  
		Size: 15.0 KB (14977 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c250d95651735d4cd1dba8cdbc694a0390ace0784a672b5c174ca72710f4429c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273065646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69cfecb3ff829a4930e78aec6a060831b49e94bc913054bf8e5118df50b2cd0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:00:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:00:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:00:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:00:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:00:25 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:00:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:00:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:00:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:00:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:00:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0442df99e77dda685f39c2a8361d0772b7e8a3de8d586d393f385ed1b658d38d`  
		Last Modified: Thu, 01 Jan 2026 05:46:21 GMT  
		Size: 143.7 MB (143679913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d892408578fe9e0b1a6eee679de2e495116d3bca01bf792e005eacdbef091f`  
		Last Modified: Tue, 30 Dec 2025 01:01:20 GMT  
		Size: 81.0 MB (81025548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1a1bed5af49e458e913141a67612d0518b9de6aea2057e1fed62145071602c`  
		Last Modified: Tue, 30 Dec 2025 01:01:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464179c3537a2e1e12fd3cf8f81b12ad73752940fde9d8c84fa99ec387d7ed1e`  
		Last Modified: Tue, 30 Dec 2025 01:01:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:98b008fd3de42d2b859cdb63c48be00ca43697cf820c0fe2cb523ed1473e76ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2638494ac09ea423255cd83a1bdbd0e366de0876e466b8b4a1eb4da79550a8`

```dockerfile
```

-	Layers:
	-	`sha256:0e08573de9b3030d33d2bc94c0c8e426eb10c634cd88a369e855a48a49c6f645`  
		Last Modified: Tue, 30 Dec 2025 04:39:28 GMT  
		Size: 7.4 MB (7380655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5adf49fd20d2e0ef080fa316e6de96ff6428a9e09c50f12d2e62bfa54f3e9e7a`  
		Last Modified: Tue, 30 Dec 2025 04:39:28 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:25515eb80cb8abb47f96f78c173904b1dd10bfb4cbf559fb6490bd0bbcdfe3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283835433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6454e63d5e8e8d598a5768492011a145cf8470691483764351205c7f58350a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:41:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:41:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:41:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:41:39 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:41:39 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:44:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:44:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:44:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:44:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:44:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7a8066a3d82608858f32fca639475eb98fdc4539bc7abe179d1e9964bf731f`  
		Last Modified: Tue, 30 Dec 2025 01:43:10 GMT  
		Size: 144.5 MB (144525257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f8401b2dbcb1e6c6af0101a69a9dc37f770b13d156685421d290df86327ce5`  
		Last Modified: Tue, 30 Dec 2025 01:45:39 GMT  
		Size: 87.0 MB (86982138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96620a083c2b525d05f9b77192032e8ec9b502b2b383a06ad196e0876fe470df`  
		Last Modified: Tue, 30 Dec 2025 01:45:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96157b2b5733202babadbfd5bf21d8cf457e7b4d1d155a2279a642fe859de448`  
		Last Modified: Tue, 30 Dec 2025 01:45:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4aa445855ee50926d318198f5579225ac16ee579f0c5bb540f6fbe289eba378f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cd333607c95b433fc0cb1dc2730ac16fea502847b22d0cd3a88c17be3197b2`

```dockerfile
```

-	Layers:
	-	`sha256:445347edbe6c872cf49e42855ea541357de26fab0d46016d95cadab7bc8c6b1e`  
		Last Modified: Tue, 30 Dec 2025 04:39:34 GMT  
		Size: 7.4 MB (7380106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f733a04de43f91f8e030bc0eff9b692fb14ca12897c46a85a86af454015ca6e`  
		Last Modified: Tue, 30 Dec 2025 04:39:35 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:dd374ca7af31baec435b2abcf55d642523cf8db082d45646c52d6246e8e67ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261957716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b692d10263025573f23fd63302f39fb62aabaff5a3dc14aeac874bdece473f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:03:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:03:41 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:03:41 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:03:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:03:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:03:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:03:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:03:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fd087cd33abb835a3d928d9f2e0a964896748847afaf3e2058ca1eb9f5d830`  
		Last Modified: Tue, 13 Jan 2026 03:04:37 GMT  
		Size: 134.9 MB (134859046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defdb509a2ede5f443a29d03f57f0710512dde28ec0ce27969b1c9fbcd807039`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 80.0 MB (79959202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9360226d790c8df59d556955578b48d53acf61987d232fafff2e523021f9701e`  
		Last Modified: Tue, 13 Jan 2026 03:04:28 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649d11114450695f87373c983f6753f50f13a0470d40e99a104d8cebce5a1560`  
		Last Modified: Tue, 13 Jan 2026 03:04:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2d803acbef18d9450f7c2ae6b1bcde849522ebbbff7c789578bc73890cd5058b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b5ad336864c54a3a4c12e232058da060a83584c0bbfe919667e7d6c94381ab`

```dockerfile
```

-	Layers:
	-	`sha256:a45a005254e8afb4d4a606e8c21169597cd2126d34ee2dc7fd6df596dfc2a4df`  
		Last Modified: Tue, 13 Jan 2026 04:37:21 GMT  
		Size: 7.4 MB (7366854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b25960c55794f823009151d1417b7f45689e3e1ace5b4922bda25fbb42ac432`  
		Last Modified: Tue, 13 Jan 2026 04:37:22 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
