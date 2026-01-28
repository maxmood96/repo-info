## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:4180e1092ae2fa151984ea3c27bb46882f0b77c3038731d95fc171de72aaafa8
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
$ docker pull clojure@sha256:de4cf3148cdbe1e0033bdd1a08cc3a3b4d85adb86d55a0c62c87f8d35c4f750e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274480725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2511211907db04bb603eb25585495a4c1e47484a0fb49cbfa99386c225950ee9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:41 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:41 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:03:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:03:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9299eff324167ca01a454ed75a81ea770c381579ff4f31b848e45372a43be61`  
		Last Modified: Wed, 28 Jan 2026 18:04:17 GMT  
		Size: 144.8 MB (144847906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeb918214ceaf98bde03856cf817e6b8cde2c870fbe407914efd2b403e07917`  
		Last Modified: Wed, 28 Jan 2026 18:04:16 GMT  
		Size: 81.2 MB (81150155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc1fb169c475fd1bb1b82049d24d24077a02c8d4a994f5418867be4b942339`  
		Last Modified: Wed, 28 Jan 2026 18:04:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7b46dfcae5d9b21d867bc42886b5157423178995fc1883aae29e1e5d236d48`  
		Last Modified: Wed, 28 Jan 2026 18:04:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c8a26e2778d775fb4c8a5929205a89537cbd76b7b31647b850708577aeb29564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a0ff57ed9d001f0f69ec726216b62628f987b772bcf8c21c5054f8aaadcf78`

```dockerfile
```

-	Layers:
	-	`sha256:284305b1751a7294e0a37e93f8e8b35c0570562fc1ad00eb889f439e5ed38e25`  
		Last Modified: Wed, 28 Jan 2026 18:04:13 GMT  
		Size: 7.4 MB (7375537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6512b044c00b8b4d147d4a4b973c72df6a55c7c9145f620ca0568a9ad3d1b214`  
		Last Modified: Wed, 28 Jan 2026 18:04:12 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:693eb869feee3da0a0b7278bc3a37faa82f1db34531c51c1c0d031073f0ba6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.2 MB (273185568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94996fc142a00f3b9e36540eb3fb1883db311200be86589e16478301ee737211`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:03:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:43 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:43 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:03:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:03:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd93e5e5bae506da5d6b3f05f40a1abeae84e13385397ba27989fa078a1a6a1c`  
		Last Modified: Wed, 28 Jan 2026 18:04:22 GMT  
		Size: 143.7 MB (143679942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7d4a0149a93b90061d460d05f15541951224cc55998b8ec3864b9c6526c900`  
		Last Modified: Wed, 28 Jan 2026 18:04:21 GMT  
		Size: 81.1 MB (81138511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d0be0dcf340774dbba2369c1d35e323130f1c8f9fe944fc6c7b5c5046014b4`  
		Last Modified: Wed, 28 Jan 2026 18:04:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f62916eb568aa8e876cb0c04f53993192b5c3b7f0221a9f4954f3f16ec72f13`  
		Last Modified: Wed, 28 Jan 2026 18:04:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e484c6faafce1a3d257b32d27291eaaf160cb0e1acd9fa0e059b50fc5c79812c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1417eb6e770b59b9c08f038bcfb0bedd5c90ff60ff5606390b3b6260288f42cb`

```dockerfile
```

-	Layers:
	-	`sha256:6be47b44907249f4bb5ea64f5609a1f79d9a2a0ea557803293d37041feaca9c1`  
		Last Modified: Wed, 28 Jan 2026 18:04:18 GMT  
		Size: 7.4 MB (7381300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa84b34a3ade87e951e848fea268648f691b22a2f53d500e539567c99cee83d`  
		Last Modified: Wed, 28 Jan 2026 18:04:17 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:4931bf0ab59fcefacfce0f0325d84ded5722232f48cd4bfda9025663a1ee05c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283840639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c4b330d37d4b6e1e8e346b48b8425e2d98a696e80c063ec88564bcb8782fab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:22:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:22:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:22:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:22:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:22:08 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:22:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:22:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:22:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:22:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:22:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fbee1bb403f77f615e65138a7f3f83ebbdd41dcc148d0618e1d492d141013`  
		Last Modified: Wed, 28 Jan 2026 18:23:34 GMT  
		Size: 144.5 MB (144524725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aed2772937e06ef8ad39137131fa3872ce25c75f49b5977e65da267f08ef80f`  
		Last Modified: Wed, 28 Jan 2026 18:23:32 GMT  
		Size: 87.0 MB (86987498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a860611d7ed451d3edd579af643b62cf4bbe7f573a9c5c36804d279ed3f796b`  
		Last Modified: Wed, 28 Jan 2026 18:23:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cb8035565c9b7c6a8165cf7239ee5b8e88ea6890360e2607bc7a22fe83c746`  
		Last Modified: Wed, 28 Jan 2026 18:23:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2a04516cd2b4c5dacd45c2727d90ae1ffa4776e83e568a1a997e3b2e82ad4934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4adcc959e422be2d619ee4225a8a8ce65bb8455a51e12154dce34ca7b6cedc95`

```dockerfile
```

-	Layers:
	-	`sha256:992114c1b48c4f07a1f1766cd318b11db77b9ba6f24b3b4200e8622c634848c9`  
		Last Modified: Wed, 28 Jan 2026 18:23:29 GMT  
		Size: 7.4 MB (7380753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf79b47b14cacff4a373bf59288bc60783cb151aaa677d7f5a5307d73a14ae98`  
		Last Modified: Wed, 28 Jan 2026 18:23:28 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:c23139f5d1115df1b7173218089c3c109dda12fc2e50de5ee9586bd50d977478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261962586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c46be1baf80a264ba45d8781cce5e837827f241b598d83fbe037768850e003`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:13:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:13:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:13:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:13:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:13:37 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:03:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:03:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac3b1f7ccd0fe409a1e257a52e40422d728bbba127f4f188372cdba4f17bb4c`  
		Last Modified: Thu, 15 Jan 2026 23:14:16 GMT  
		Size: 134.9 MB (134859770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125cc54f4e4ce11e5f0466b30ce1f5c34ec80149e852b51378f91c67bb18cf2`  
		Last Modified: Wed, 28 Jan 2026 18:04:13 GMT  
		Size: 80.0 MB (79963345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831906a2cd7b07f1d2261df90dfef734e4924f5b5aba6be5e30db4e97f9a107e`  
		Last Modified: Wed, 28 Jan 2026 18:04:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3db99bce17d32ddc834b9db320547dffe732ece7cdf6b3115c9592d696384bf`  
		Last Modified: Wed, 28 Jan 2026 18:04:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:75029672f362fc841d7543649f41f6a539d6b58be9dd8619f28e928334b699db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba7ad2ec646b72a5630a874eb811f0395639867bd458a650a15be819667f3bd`

```dockerfile
```

-	Layers:
	-	`sha256:831ba5d6eb3db950f80c99e42c2f22e4e8271c8c5c4d794bb5713bb1e089dc1d`  
		Last Modified: Wed, 28 Jan 2026 18:04:12 GMT  
		Size: 7.4 MB (7366856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c4ba5aee14a977df9e036fea327f145e9b16f866f83f31c54c24ad1187ddadd`  
		Last Modified: Wed, 28 Jan 2026 18:04:12 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json
