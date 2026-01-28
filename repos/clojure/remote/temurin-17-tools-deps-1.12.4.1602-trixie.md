## `clojure:temurin-17-tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:ea3279799907987bfa85a12abd2d41101a70a2e0ea9ca033da1017d85b309b46
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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:65219f153bc3ff4b4c31c184b6dbeebc742b1c4562a1c4f96e4315f2fe01cf83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282647488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddd867099e5e17876d8639c23b9360827bfa43ebb866556ccd5175e4dc27954`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:05:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:05:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:05:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:05:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:07 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:05:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:05:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:05:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:05:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:05:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d54c1c4cd42173acc01f56e11427fec13b70ae322ae740f6e5af1ebf4740aac`  
		Last Modified: Wed, 28 Jan 2026 18:05:46 GMT  
		Size: 144.8 MB (144847923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859a3eb74523e08a84f29a9db1fa8306ed6d40e54ab313616100da087dc6b400`  
		Last Modified: Wed, 28 Jan 2026 18:05:45 GMT  
		Size: 88.5 MB (88512907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cd311facec41e73b5a6cd50972d6b8bffb553fd08cad43c7e5babed18bd31a`  
		Last Modified: Wed, 28 Jan 2026 18:05:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bd75e0a9300882bed8f9e614e75bd2fbbb9de6cfe1c0c364d3f4b84e50ee40`  
		Last Modified: Wed, 28 Jan 2026 18:05:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:92f2b473d0d871376cf96ae8362fe69b724e3f455f33f1b506fa06323a637838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483044e8c2146a166fa2c2ad0933ca2056e72473c6e0f3a657374379e6064850`

```dockerfile
```

-	Layers:
	-	`sha256:c068cea88f6af522b019f12b04112ebf9cf689188167f218462556101b0783b3`  
		Last Modified: Wed, 28 Jan 2026 18:05:42 GMT  
		Size: 7.5 MB (7467828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c2a94edf66da0d3e4086561c048abc4c3fb06e7af9649f3d724d5ae7c36c737`  
		Last Modified: Wed, 28 Jan 2026 18:05:41 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:30cb1963dc38f93a4dff889579e0f147f96594f8e55d3e7040d22ca50ddf70ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.0 MB (282021413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c89ad1bb0de2ba8cfc3f16c66d3733d8b0a9a4e81fbbda7405018caef756094`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:04:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:04:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:04:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:04:15 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:15 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:04:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:04:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:04:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bd383b92dc3a5ad6e303f259e027f5de3c5d2399df069006d0fc711d466a4f`  
		Last Modified: Wed, 28 Jan 2026 18:04:51 GMT  
		Size: 143.7 MB (143679942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa30af03cc394e3ae7fb08571c7a195d520bbc85100fbdecf21b7ba398331054`  
		Last Modified: Wed, 28 Jan 2026 18:04:56 GMT  
		Size: 88.7 MB (88692347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce161caf061e7aad8edc6a3223a55830a04e6a66c0e30d70521b843bf4edf9c`  
		Last Modified: Wed, 28 Jan 2026 18:04:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e4587e0bee042c1906707c653ee93fd9c53a0ac6dbe049bdbf97da6740ad4c`  
		Last Modified: Wed, 28 Jan 2026 18:04:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2eb19c73ba20d07a3528b23cd89c829729a3af6d4dbf1ca06f2b71124e3db082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303d15e9af08ea3767530dc2476f7b3b9200094c7bb8b1ad976d84c6ea66b067`

```dockerfile
```

-	Layers:
	-	`sha256:db87564dd3a70fd2e0d1ef050924bb293a8307109b8cc9c5193020bf89610540`  
		Last Modified: Wed, 28 Jan 2026 18:04:54 GMT  
		Size: 7.5 MB (7474858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fee35d2f1d2208e35ae26ae084df0e8e90c885d9003998cc3fb36c687416e69`  
		Last Modified: Wed, 28 Jan 2026 18:04:53 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:214c9c825ff0da8d7de5f0dc917afaf764938bf35b9ed0ddc166d2105db226b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291785545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41928f8e026bcc166b185c34e4e4e0af57ef5f8b73a6fe69af951d532052db7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:25:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:25:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:25:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:25:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:25:12 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:25:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:25:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:25:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:25:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:25:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1018c3460cf258236be180731a45a091aeea7a0b3099f92e9bfa486fa3b9252a`  
		Last Modified: Wed, 28 Jan 2026 18:26:43 GMT  
		Size: 144.5 MB (144524726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8ef909c30e213ea4306a50a74e64036751ffba5581dac282f8c22a46a94804`  
		Last Modified: Wed, 28 Jan 2026 18:26:42 GMT  
		Size: 94.2 MB (94152815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abcce7df5dae969bcb0e81d99bccba0e847d817aee4af55b99dbf882a34b275`  
		Last Modified: Wed, 28 Jan 2026 18:26:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829aca8d3d201a504f4efe367658360a58e65c8fdd41fe21cef7173451a3b187`  
		Last Modified: Wed, 28 Jan 2026 18:26:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:da86331e6713db46463c301a4488b04b05b06a3e9e80ce5e87259d4721fba7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6549593d80e2c1eedeb05c10b8a03c1453c3803653e34ff25c92143592f8ca36`

```dockerfile
```

-	Layers:
	-	`sha256:7e64b9ff682544ff2635b1dfd50388b5953e3580b13dcc32a84fbab85eefc92d`  
		Last Modified: Wed, 28 Jan 2026 18:26:37 GMT  
		Size: 7.5 MB (7472249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbf198f1b7b0eb1894bce0252727e6c55cb3fea409fbeee03b2186a27c77919a`  
		Last Modified: Wed, 28 Jan 2026 18:26:37 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:bb4cda7e93c53e03da6ae5c0940e63bf121df58cbae52b321066d527ec19b20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273341114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b162f2c6562989735327f708b082a33a645b5322827fcc838f99cd1b68695451`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:08:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:08:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:08:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:08:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:08:07 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:08:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:08:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:08:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:08:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:08:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b69fb4ef87a8cfaae07e66b78eb1c45148ce37788b4c6d5e7cc201f8ae0950`  
		Last Modified: Wed, 28 Jan 2026 18:08:56 GMT  
		Size: 134.9 MB (134859775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e01cc0f71a7f35943a9424f8da59eaf8016993885298bb36d0aec42aa7886a`  
		Last Modified: Wed, 28 Jan 2026 18:08:55 GMT  
		Size: 89.1 MB (89131594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13746c0b39e393d5c207c33af8553aa8d2288a29b5acedc33d96735cd2c09c3e`  
		Last Modified: Wed, 28 Jan 2026 18:08:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37ead2ff5ca0c21a67bcc95c7501de242f99979fa8299ad4f13e7e82007154d`  
		Last Modified: Wed, 28 Jan 2026 18:08:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0b958abc2c09e7b5e098065dc70e0e904c3a2c745080ced8471f3d51187f5d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd16f01fbb4376efc25a346d8bb8c16418ebcd851690f5350b8c439a592b0989`

```dockerfile
```

-	Layers:
	-	`sha256:19ac926e098c0a8647bad0b0386d9069e1291f8166390b865a9b8f68383ff6e9`  
		Last Modified: Wed, 28 Jan 2026 18:08:53 GMT  
		Size: 7.5 MB (7463750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8375d0dcd5b0bb31c90b0feae61348f47b4e0d6e3548da9fdfd30abfbc0e4520`  
		Last Modified: Wed, 28 Jan 2026 18:08:53 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
