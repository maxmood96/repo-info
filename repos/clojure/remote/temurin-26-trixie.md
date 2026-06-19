## `clojure:temurin-26-trixie`

```console
$ docker pull clojure@sha256:0f7997a166522bb68789e11f0915860d0ceb788b65a447f9f2f0c10022330acf
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

### `clojure:temurin-26-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f562d4d8b16db4d8177ff4416228a8215d5c6dc5bdf282ad8af0c2df988bfcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226362079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194d2ac489e1bc0a39db58cc2d9989b06470c0981d14f6d648868d1912702939`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:22:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:22:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:22:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:22:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:22:33 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cb909c75ba9829eecc9fd391dc43919b246630784f35a98bbebe27cbebb23`  
		Last Modified: Fri, 19 Jun 2026 02:23:13 GMT  
		Size: 94.5 MB (94524388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001d94f9be88c568d5f2aa8169744ce435341a59ffbea9dfb1228d4f7735012`  
		Last Modified: Fri, 19 Jun 2026 02:23:13 GMT  
		Size: 82.5 MB (82519528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8568296b76d566cb8c6f62672cbfc829b2b518f77d040e5c2cc882994b1d8aa7`  
		Last Modified: Fri, 19 Jun 2026 02:23:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908fab673a046780b8d3c796f9895873510e41c5c492d201920b3ca3af443063`  
		Last Modified: Fri, 19 Jun 2026 02:23:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:00c10f106b4a75302cba570847194bda156c3c5cee91e0f8f31b7b251b6d6bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7449561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ab7abfa0111def3b7b06372eb10a33e5daf29e7602ee902454a9b37eccccf`

```dockerfile
```

-	Layers:
	-	`sha256:cc5e8905766658c9762dfcb9a8bfa8286de6a3cc82daf9b7e4d3f095357afbb0`  
		Last Modified: Fri, 19 Jun 2026 02:23:10 GMT  
		Size: 7.4 MB (7433662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13730e5935ad6fc7168e4b2388dea6e5510dd3ec9811431c796413013e11298a`  
		Last Modified: Fri, 19 Jun 2026 02:23:10 GMT  
		Size: 15.9 KB (15899 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:791bb098c2eb41cbfe7dd0f180bc71e968b47cae58e230eca5f6afd88f519eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.5 MB (225522309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766b48226d62676d778a24a5c75c3b33bde3f5c4357d14cf3592db0af3008ca0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:22:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:22:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:22:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:22:41 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:22:41 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:58 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7019fc85a3331738e55d0d1db2a3e23f77811989acf20ae0e069643ac79105d4`  
		Last Modified: Fri, 19 Jun 2026 02:23:20 GMT  
		Size: 93.5 MB (93504354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649693d9cb53bcae5f79d5a4048e2af2b0330f62ab0258e93687b953180abab2`  
		Last Modified: Fri, 19 Jun 2026 02:23:21 GMT  
		Size: 82.3 MB (82338742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80f5fdab89d36dc689264c6c2b50e5fe1981f9e3d2cf3c0c0cbb95b49ce4a39`  
		Last Modified: Fri, 19 Jun 2026 02:23:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4d980e3acfc148b7a3dae4aee3a182aefa4c14d5c46ebe0b086918bb82dcc6`  
		Last Modified: Fri, 19 Jun 2026 02:23:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dda3d0509bef1713dab190b6eac5e2cd63202a2e9d31333929caff415aa7fc91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7456070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1ccc4b4ec8495ff1ba98fafa284a6083376ba6ef1a31a855a8c997d4c9de8e`

```dockerfile
```

-	Layers:
	-	`sha256:bcfab811e652e2f9503032433447293628e687326ef1279148d5b332fc707cae`  
		Last Modified: Fri, 19 Jun 2026 02:23:17 GMT  
		Size: 7.4 MB (7440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a08c0fa95b7aae880ea3ee87e8c1c82079154d63f4dc320e8a0b609748be5c7`  
		Last Modified: Fri, 19 Jun 2026 02:23:17 GMT  
		Size: 16.0 KB (16018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b1fbff283e4e78142341de318e3c3db317ee3101696727785d3921fcf54b7253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234979734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8905fac51090fa8d1f83a7b4e6f07f3a57726bc0c2db65f96d1f5541a046d69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:14:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:14:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:14:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:14:41 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:14:42 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 03:02:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 03:02:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 03:02:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 03:02:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 03:02:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328775c3b052bb498a48836eab308724b02180a01e1a5397b2235df60a8765bf`  
		Last Modified: Wed, 17 Jun 2026 00:18:19 GMT  
		Size: 93.9 MB (93902081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856bbc9642d3749f9fafd01caa9367cf6d7cc51aeeda7b5534fec5814a5b6493`  
		Last Modified: Fri, 19 Jun 2026 03:02:51 GMT  
		Size: 87.9 MB (87938672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3aa4058e871053c8acf129884e52b6071d6c57b4fb83fe7c36b5e10416deca2`  
		Last Modified: Fri, 19 Jun 2026 03:02:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9d92cdb44a87d393de81d7cc542d6777b26204448c78557dae01fa7fa11b88`  
		Last Modified: Fri, 19 Jun 2026 03:02:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:380469a20c70685d24bc6c6d29f8fd664bae04f451d9d1d1c38843b953445e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7437968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3236d55dbc39d0524264f553b836537057cccc07bd5473b17f536ceebf2f97f`

```dockerfile
```

-	Layers:
	-	`sha256:3164a02a32f2e0a9199fc150a484ac04f8ea7b090c60c8528fed27f3b742bf85`  
		Last Modified: Fri, 19 Jun 2026 03:02:49 GMT  
		Size: 7.4 MB (7422019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a73fcad800e3be57a1e8524158b865a7e8d8d83306dce121dd2e1b5052bc804`  
		Last Modified: Fri, 19 Jun 2026 03:02:48 GMT  
		Size: 15.9 KB (15949 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:d3d762231d55da365de8efde60c6cd3984fafbc34ead3fd14c9fcb68661f9825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223425843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f24692733f6555c76407a013383bb6a357ccd9717c2bc749d9624e6820aa30`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:43:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:43:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:43:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:43:17 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:43:17 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:25:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:25:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:25:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:25:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:25:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4fe075b6dd2f22b2b5ed10e7aa905d6a156ebcea02659f73eed01d90f3f8b4`  
		Last Modified: Tue, 16 Jun 2026 23:50:05 GMT  
		Size: 90.5 MB (90537002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897cd6b9010dacd89ef872b1d7087ae9bd2fc9a41e5da3a2ceff4f88de2f8cc1`  
		Last Modified: Fri, 19 Jun 2026 02:25:37 GMT  
		Size: 83.5 MB (83501906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d09a072d9d3ebec870eda4d7a24ed9b1ba8a57e7a6ab86c1e8be489ec233cc2`  
		Last Modified: Fri, 19 Jun 2026 02:25:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d6bd630fe96cc323810ebb6e757f52bf064a046b03c22d05401b3a6c571c22`  
		Last Modified: Fri, 19 Jun 2026 02:25:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4d4a43f01ff5138ec01d0d290880bc7f98a5c1273f2155475687a493e321030e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09a5c1209cbbbf3fdbd66b2921c2191f35feb1acdb66972b9699d2ffa7653ca`

```dockerfile
```

-	Layers:
	-	`sha256:8e2aa403d18e3a8fac76d90c3ab8529386588684cf3accd817572068cfbdeee6`  
		Last Modified: Fri, 19 Jun 2026 02:25:35 GMT  
		Size: 7.4 MB (7414770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28b840baa6674e934c8303f07012b329ef7a64d40a79eecae70a2048f3471679`  
		Last Modified: Fri, 19 Jun 2026 02:25:35 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json
