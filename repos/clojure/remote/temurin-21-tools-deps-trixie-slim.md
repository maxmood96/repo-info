## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:ab1b1d6c9599e20df3e5fb7d436b238c424783fe1a8ae29fd6b1cafde9679b7a
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bd4e86609c18f1fba11e1676df305dd57708788e63d7c044d16161b28e67ebbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256905197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf315be983c807b8935ff08b8cb9344fc4905f04c0edba73b0411a4d28e9485`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:19:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:19:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:19:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:19:27 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:19:27 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:19:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:19:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c19fabebb47ce7445db546d6e3679747e4940e0d58ccc72c61a5798b0ee5cc7`  
		Last Modified: Fri, 19 Jun 2026 02:20:06 GMT  
		Size: 158.2 MB (158166940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38390ab111e03c20143964db73ebcc03ad6ae87531f91e9f33b492e87dc7f059`  
		Last Modified: Fri, 19 Jun 2026 02:20:05 GMT  
		Size: 69.0 MB (68951807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d89fd347067ec43cd052637336ae39b4e8e564878e0df7f4a35885aadd19a7b`  
		Last Modified: Fri, 19 Jun 2026 02:20:02 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7f67e3faf51dff3ab4d17dc27f9a88d7901f5a32cd833d8d0f28b0bb6081f0`  
		Last Modified: Fri, 19 Jun 2026 02:20:02 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:934e876dbfe843a48739a8b4d4d73b764270a1097051102d8bce48256d916062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b278f7afdc6ef97e525ad372f786a4a760e974b413ca202f5715beb4410fa02`

```dockerfile
```

-	Layers:
	-	`sha256:b7c1771ab373d6f765f86bbaf935bf5a654c03ad0f11dc0f304563bd8d1fe463`  
		Last Modified: Fri, 19 Jun 2026 02:20:02 GMT  
		Size: 5.3 MB (5259094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b7d8bb7fb21e72fe0b8e76e497b24d6904a11a5970b744b3e9cbc63eb0d26a`  
		Last Modified: Fri, 19 Jun 2026 02:20:02 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b9d444b20606bd7350c05ee1a8d264b30db339368742184d2b1c936a26f47929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255388256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa240c46e33e6b207af743e6fb9f321a009431be00da569023a701f0406760bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:19:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:19:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:19:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:19:56 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:19:56 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:13 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1258dcdc09250812fec6c8457e41fe27305280ce68f40315cb9b63434ab43f32`  
		Last Modified: Fri, 19 Jun 2026 02:20:38 GMT  
		Size: 156.5 MB (156461328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d901949f1650a97ef37c4911cd64f89b7bbb661f2f60eee3d7a733dfe57a132`  
		Last Modified: Fri, 19 Jun 2026 02:20:35 GMT  
		Size: 68.8 MB (68777359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f520a5181c670acd51374ca130616dbc1f168d76b7edc59ee2756b3823047`  
		Last Modified: Fri, 19 Jun 2026 02:20:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acd51d39ad1ab2a6160ddb3e821c6f5b911caee4605c2c0a5cf8dd79b5831e1`  
		Last Modified: Fri, 19 Jun 2026 02:20:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8ae5ea6238428ad858786dfa6a1a9ac1109e447d76bf9550ee7dc84072a0b7f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06031ba7258749d0e5e2bdf6eaac8ccd9a88a2c10ce4c5c343252f27a26ffe52`

```dockerfile
```

-	Layers:
	-	`sha256:e5ab7a5d625cc8790d90d1415d3f22939980053d7e26d6ef8136166b0f9155c6`  
		Last Modified: Fri, 19 Jun 2026 02:20:32 GMT  
		Size: 5.3 MB (5264855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dc8f424cdbcf10ce61b80a95e5df2e793b9b785468cea08b4adca93a1cb30d0`  
		Last Modified: Fri, 19 Jun 2026 02:20:32 GMT  
		Size: 16.1 KB (16082 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:98dbad28194b5c1dc49c1c994e920e6c69a3253e30424189c77245886c1aebdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266319613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c6f6e0af28e581deec2e6f3c056a085f1daba082840150abf74526fea58784`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:00:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:00:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:00:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:00:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:00:47 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:52:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:52:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:52:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:52:48 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:52:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae30f60cd0ec6ba95234bc9baf8b715de9cca5a8c7483a3f4eebc08e9456b2`  
		Last Modified: Wed, 17 Jun 2026 00:04:10 GMT  
		Size: 158.3 MB (158343250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b753e509813b5da0784e09192f88d44be4eb601939e4e1e92ae2a7bfe2807ef2`  
		Last Modified: Fri, 19 Jun 2026 02:53:31 GMT  
		Size: 74.4 MB (74368982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f03630a7625027a52de38c886736d882b9ee9f2353b130f21ba2e93ac19e26`  
		Last Modified: Fri, 19 Jun 2026 02:53:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13c2f0daa46626cf969c25c6b5b65fdd8695968c193dde01657490e8064a5f9`  
		Last Modified: Fri, 19 Jun 2026 02:53:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7fbc71449b0ce33b7a15ac3b48901aaea7c04f8d62ec252cc9d7ab08de866a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f05dbc13098a353e0aa60d8589ea3474cac180ff2bc6802ff51e602ebec860`

```dockerfile
```

-	Layers:
	-	`sha256:d26427d2b89539e3f08a5c363b42ed14f523a38dc6ef6c08577eda5a765a4eb4`  
		Last Modified: Fri, 19 Jun 2026 02:53:29 GMT  
		Size: 5.3 MB (5263465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262bf4d8c59525d4506b9d47f912696ccf66a436e973dc1c00cf90a0d7405dba`  
		Last Modified: Fri, 19 Jun 2026 02:53:29 GMT  
		Size: 16.0 KB (16014 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6f3d7abe3a7d48351857adac329d3ce77ab244640602a0188f5cfde37a554e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247172992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a5fadfd4a95b7833bb1022d1524767959fb451c79f1c3603d95dd8ef93c644`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:38:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:51 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:38:51 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66d9375a62e658d5255a5581f80c6f86b82e7d20e6a5c6878c2e0220d54700`  
		Last Modified: Tue, 16 Jun 2026 23:40:34 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8873b5073dfb09961cb9fdc4799046ffa622a660b5ec06c489d3bcd771fcedd1`  
		Last Modified: Fri, 19 Jun 2026 02:21:02 GMT  
		Size: 69.9 MB (69932261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba40f26856d04085a549908e68588ba6df3e6c7ce48107dd5fe1f3c4be7bbe29`  
		Last Modified: Fri, 19 Jun 2026 02:21:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a69d25719d57cdd705d178d215b15ecba4c4d3f7470a1d219c721fffe8daa7`  
		Last Modified: Fri, 19 Jun 2026 02:21:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8378a9c28c434a61154fe4842fd8cd8d00207ae5c4795b116b4ee54c761ae5d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140acb1d947d90aca076cb824bbbe3e532ff91fe4a05f68e086a67b25698e205`

```dockerfile
```

-	Layers:
	-	`sha256:73f19e89a5ac6f02fd3f56ee45ed6f6c992771e44fb8b520b0031fa5a8fbd9d5`  
		Last Modified: Fri, 19 Jun 2026 02:21:00 GMT  
		Size: 5.3 MB (5255018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2577131e446d3a309dff704e75d932811379876d97707d605edf9860ee49f778`  
		Last Modified: Fri, 19 Jun 2026 02:21:00 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json
