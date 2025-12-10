## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:3fefefa3203d302ff5e33e3249e473a9dcdbe101c2c71bc2a241bc91fd64529e
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:03ec35ba08b127c9cbc8d49403bbd79106f8bddab659d2c87cfd2d06a386b00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259599787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919a94a79f73989073aa7b499b00bb127c6097bdce1f5bc17707c156e94a6f9d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:55:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:55:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:55:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:55:27 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:55:27 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:55:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:55:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:55:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:55:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:55:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7634d88edc0e8fc40f68f03a0e9c9ea4a1e29bcf57dc2431f789e5d5f8c5d02e`  
		Last Modified: Mon, 08 Dec 2025 23:56:36 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e860319d28e5bc459bb734d18d65966dd1b4526828e9ffa29741f2e9b329891`  
		Last Modified: Mon, 08 Dec 2025 23:56:22 GMT  
		Size: 72.0 MB (71996220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471dca180a7bc395276808bd7c86c2ba72a479dcb484cf10ba0b976749659c88`  
		Last Modified: Mon, 08 Dec 2025 23:56:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20707c1677e0caef99f26ff9c197cdd83d930903ec78c3fc4641c9f5a02e7ddd`  
		Last Modified: Mon, 08 Dec 2025 23:56:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0b945e089c2fb891beac5e7415a37f6cb3e9e10ccfff4358c06769a4b1e41a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01a611c800efda766d961e1018e01de1f6d3db1c93c8d1021b996c853cfb92e`

```dockerfile
```

-	Layers:
	-	`sha256:877271bda88b61fb5f2c2f66107f7c313669928448ab6f5b92559a96f0d06298`  
		Last Modified: Tue, 09 Dec 2025 04:45:12 GMT  
		Size: 5.3 MB (5259301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f373f4823d7dfc4afecbf9bafa7df5dc3e4fbf4dbe8c7d9b871922b8e20e7a`  
		Last Modified: Tue, 09 Dec 2025 04:45:13 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c8e2ee14b6f082bed2233718522a1e6ec1b6aa21f9711c35795bcd6e895aa26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258055815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc2a368ffd16aae272da018a92627fd2f3796605b5b1a86af91491d726a1384`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:02:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:02:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:02:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:02:38 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:02:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:02:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:02:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:02:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:02:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873736c4017f43817a44968c596f23bd7e67ec53ded41c421dcef8fad1a6e121`  
		Last Modified: Tue, 09 Dec 2025 00:03:44 GMT  
		Size: 156.1 MB (156107651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475ed19fd84563895789f5fa396eea64c11d16c13eb903d8fc5403d362be94ec`  
		Last Modified: Tue, 09 Dec 2025 00:03:29 GMT  
		Size: 71.8 MB (71808496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7ce0f6d743887540aa7b106e1d011d151e2adf8dd20c6405194169c6a56b3a`  
		Last Modified: Tue, 09 Dec 2025 00:03:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57dc1d263206b10b02ccea14dac5d5991fe2365802bcce877acfacd4adeca27`  
		Last Modified: Tue, 09 Dec 2025 00:03:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:42855112fc3d7326e7a496e66147fb3885b2dd9e8ddfb3cec6287601e2bee6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e25c4d2b0d5c350ecd438660f04f85f49f74ca25dc293049a6c044b4141cb0c`

```dockerfile
```

-	Layers:
	-	`sha256:dddd806bf8821b193560940dc0db53fd9f54d6230bdab7ca80debe0d123ffbbb`  
		Last Modified: Tue, 09 Dec 2025 04:45:18 GMT  
		Size: 5.3 MB (5265070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:089831de7605fe0d61c993c66fbe4770a61080e6fd66cd1c1aaadc956cc3244d`  
		Last Modified: Tue, 09 Dec 2025 04:45:19 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a9a2930c3c3ce02efc557d1fd0cabf301940c1dbb244fd11fe30956675342d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268930996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80769c3a3e7e07e4cc82fd81e43bcb3fca5827f955a7ba0c299d2b9df31e4034`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:53:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:53:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:53:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:53:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 03:53:31 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 03:54:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 03:54:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 03:54:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 03:54:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 03:54:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1738f5a3e98755bfb9425681189b2a44278e8171bee65caa143a42717b2cfb8e`  
		Last Modified: Tue, 09 Dec 2025 03:55:01 GMT  
		Size: 157.9 MB (157942950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd3f7f03dcf2e9b0e1fdfffec0288ad2b51c90a1ce0b519cf6c1378bc728f76`  
		Last Modified: Tue, 09 Dec 2025 03:55:24 GMT  
		Size: 77.4 MB (77390118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b4681dab0914df4f4bed5558f111c87a5b561d9decc692b5af95f50f5d285b`  
		Last Modified: Tue, 09 Dec 2025 03:55:21 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a569c1d9d190cd446b183e2ff5101b3a93e65d411540519ab2434ae6dbac15`  
		Last Modified: Tue, 09 Dec 2025 03:55:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0e653dd1fe0f65c390a4cd59d8d11e9751a65dee69a375ca4a7ea9d2fae224ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41258be86f014b202ab51fa8ed2f818401ee396efcc90c926a2d8b473912b9ba`

```dockerfile
```

-	Layers:
	-	`sha256:b8e7aaf0a9ff3aeea40311d6e4d99246847793ea09075e404d5072cb3728825e`  
		Last Modified: Tue, 09 Dec 2025 04:45:23 GMT  
		Size: 5.3 MB (5263672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9e203764e967f22b6c6122f1a2e4e15832aee05adafe60a7b9c804ca2160c12`  
		Last Modified: Tue, 09 Dec 2025 04:45:24 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:ed8c33c48120465ac77ccd2ea4c74ebc0dfa70b333f31a6946f32a904ca7cdfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256348991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff130125c8828d429c506c8a3eee9e11c95fc856ec9c51b3195b40325fe5989`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 18:27:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 18:27:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 18:27:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 18:27:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Thu, 20 Nov 2025 18:27:05 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 18:43:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 20 Nov 2025 18:43:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 20 Nov 2025 18:43:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 18:43:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 18:43:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516f07972228dcbc55c70b87824ef60b8072c90f8a8787a93b8e4054d62735df`  
		Last Modified: Thu, 20 Nov 2025 18:32:59 GMT  
		Size: 157.2 MB (157194320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01afe0e6f99f498246c4bf39f4339fa16957e9fd851cd63ef2c95b93b254ac6`  
		Last Modified: Thu, 20 Nov 2025 18:47:48 GMT  
		Size: 70.9 MB (70880504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456d5648f503859cd3ff3658f8fc69adb73868fb84beaae7fdb205ac32f59eb7`  
		Last Modified: Thu, 20 Nov 2025 18:47:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc3659a9d5a68ffb91a8e9b1f902404f839b2eb82b8e4eb29c5c70a8d1d6ae6`  
		Last Modified: Thu, 20 Nov 2025 18:47:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33b783f8928005e18eadf143c3f7db0270e1d13ffdd979ac1934682909c95b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed760e517e8b5a13be723cd282af13e8a2f438a56aec4d1bec71c9cbfb5d171`

```dockerfile
```

-	Layers:
	-	`sha256:f4cf391357ec690ce00b6d71dd029c8128c9dfe9c17b253311e3bbc60ff43124`  
		Last Modified: Thu, 20 Nov 2025 19:37:28 GMT  
		Size: 5.2 MB (5248765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25035b68b126b2e1b4a2f81116f1c8889bbc153fcb95fab217f3ec5842ca4471`  
		Last Modified: Thu, 20 Nov 2025 19:37:29 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d81b81975ba0d71293ff1767c194c4a4b91fb789e44c7c39181cef613ea914f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249858704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50fb6cd4d2272f84897fc3df9e1d0d2593a98a389e2f01c5992ed9639e03c1a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:31:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:31:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:31:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:31:13 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:31:13 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:32:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:32:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:32:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:32:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:32:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ad8af80bd1fca505a458dadc68d16da2d131f0ace69cc71fe587e4b3a2a78d`  
		Last Modified: Tue, 09 Dec 2025 01:31:58 GMT  
		Size: 147.1 MB (147069847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88aa6cd3ed5549d98df7f8570d46934e56fafec42077e76d2f561f126b0580`  
		Last Modified: Tue, 09 Dec 2025 01:33:18 GMT  
		Size: 73.0 MB (72953419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7b5cc2cf174f3eb7fd34a921acbee9d9067e896b4858481e426778a7fab03`  
		Last Modified: Tue, 09 Dec 2025 01:33:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4182603ed3d5cb5eabbc46c801f10f720d7ef77241dbab5490b6aa5c1135ca8b`  
		Last Modified: Tue, 09 Dec 2025 01:33:11 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:264915a624eed4edd6c796f26430ab05f003794af83c0e0ca84363c3a8bb545c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7114b0889e30eccd25369c392a115712b0c9994590788911e856d55832867c2f`

```dockerfile
```

-	Layers:
	-	`sha256:103f33968d3dfb0204d1ecca1a580bb1c81893136ff70a400719a53710bfe69f`  
		Last Modified: Tue, 09 Dec 2025 04:45:33 GMT  
		Size: 5.3 MB (5255225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8623ca6f1e888d19f696c6edddd1b3f5e2fe66d12b2d7399e58eeda41fdd457`  
		Last Modified: Tue, 09 Dec 2025 04:45:34 GMT  
		Size: 15.0 KB (15011 bytes)  
		MIME: application/vnd.in-toto+json
