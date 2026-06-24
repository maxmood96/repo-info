## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:34c2f2c29fb18ab29dd18078c76692a006096d2352e7d4867f70bb3552081454
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
$ docker pull clojure@sha256:97af586c2f446e4571c97d57df2b4b95ad22b4f9f3424c839901db84c45b2997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256905022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09a20a49ba08591ce4439b8f729d872f435ed10165639a71077ee710222b6f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:43:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 01:43:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 01:43:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:43:37 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:20:33 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:20:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:20:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:20:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:20:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd9c01fcd53c66a79850bb146e9cb313e088b65a3481a04ca2984714b2c4fa5`  
		Last Modified: Wed, 24 Jun 2026 01:44:21 GMT  
		Size: 158.2 MB (158166944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525bd1f0aef4c74e21bef0e42606cb522edf6941db206c7e9539e07121a73bf5`  
		Last Modified: Wed, 24 Jun 2026 02:21:08 GMT  
		Size: 69.0 MB (68951619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058fa1f17f9bba898b092b14bc361ba88a1b235241c9d93721a50e402668bfc9`  
		Last Modified: Wed, 24 Jun 2026 02:21:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e0abdcec93dbe1bfda4c5608ff5bb2fd81dc1f4d98b9bc52fdb53c4d657d21`  
		Last Modified: Wed, 24 Jun 2026 02:21:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:76bece5cf5a628a392ad776f22623f455839962bc61e42290b070efd13aaf4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2328fbd68671e0ab8973af1a43ebcb35cc74242e399e29a446224c4717dd60`

```dockerfile
```

-	Layers:
	-	`sha256:9c7ebef9cc2731c41645d2a9665d0d12edd8cbaa96e1e50c531fda3451257df1`  
		Last Modified: Wed, 24 Jun 2026 02:21:06 GMT  
		Size: 5.3 MB (5259094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a006e6c02e7b1e5a94312e5739ebcdb100809eebf1c9d0629d1c742d9582cc8`  
		Last Modified: Wed, 24 Jun 2026 02:21:05 GMT  
		Size: 15.0 KB (15011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e020ac0fe767d5fa530782248b23a65f8636198a002801404cf3f00dbed992aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255388367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d87fbb143d1e667e7572af1f2c4650a4877fb4b5e0dfccf67d98794bad42c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:26:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:26:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:26:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:26:46 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:26:46 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:27:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:27:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:27:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:27:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:27:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e8c630980f139c7b859459e6ecfe1e9db0e96c89e5cad993c8b7ad5b0dc0a4`  
		Last Modified: Wed, 24 Jun 2026 02:27:29 GMT  
		Size: 156.5 MB (156461252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf100942ed145e979a7e24b12336a5d71ac9d6e4102d915362d29dd9bc9e334`  
		Last Modified: Wed, 24 Jun 2026 02:27:27 GMT  
		Size: 68.8 MB (68777524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4e58c6bfd1204b042002ba48aed3bef14063429ddc6218286c65de93b8df66`  
		Last Modified: Wed, 24 Jun 2026 02:27:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd6666e00d974aa11a05611d69f58c35558bcccf9beac9b694373fe44a0bf26`  
		Last Modified: Wed, 24 Jun 2026 02:27:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c23e8a3e7ccaa529ca65c36ca1ef634249708ed36ba93c0262a6c2ffd8ba5576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d6c4189829f34bfdefe5cd5e7b22e8f537383cf5a8d67afa3432a7c5a0e935`

```dockerfile
```

-	Layers:
	-	`sha256:04f015386467bee360d44ef1e3e3dca68470e523ec5da48009c9510d6ebed751`  
		Last Modified: Wed, 24 Jun 2026 02:27:24 GMT  
		Size: 5.3 MB (5264855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26497fe0be1285e8e0ee0cd344cc7a2dc79f1db9a6b18b7c0bd72aeee443983a`  
		Last Modified: Wed, 24 Jun 2026 02:27:24 GMT  
		Size: 16.1 KB (16084 bytes)  
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
