## `clojure:tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:ee99cfa02d6a59c41533abcfff57eb998c744013c0a60ad6cddbd9f62e709289
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

### `clojure:tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9b16585b400f72d1e951d1c872e94020f675fb44d0063e1258be4ece02e0835e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221923729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a09109be376a2e4856526d2bc128973afd4b1badf3211ec428220e81941771`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:36:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:23 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:38 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f435583340862428d577712313640fec3b6f70a11311d895be15fda348097e`  
		Last Modified: Mon, 09 Mar 2026 20:37:00 GMT  
		Size: 92.3 MB (92256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb577e31f357a6e9e08f51c106118aa35282c39dd1489ab2bbb9f265aeacf39`  
		Last Modified: Mon, 09 Mar 2026 20:37:00 GMT  
		Size: 81.2 MB (81177609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ae13e47410701368df71c8425a2409dd7585c48df590697f4f3d5a9ab0bc87`  
		Last Modified: Mon, 09 Mar 2026 20:36:57 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733bab1b3ff1b62d211fdfced50e819f26a8628cf4ed1ebea4d73026612947a3`  
		Last Modified: Mon, 09 Mar 2026 20:36:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8c7832e23d8b292dc92f3c81a696258521a48f34be41bcc8ba03f7869e21c7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7365471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f853f375a16455014a94254191cb8c7b5611f6e2788f76f0bdc8a4fd5851b4`

```dockerfile
```

-	Layers:
	-	`sha256:5de5b4eedd13aa0c5c2e4aad4d971e2ff424f1af33551a8bfe215ce1a4404b84`  
		Last Modified: Mon, 09 Mar 2026 20:36:57 GMT  
		Size: 7.3 MB (7347700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d1da5629458b5851c2e6e6738363a90e18f9dfc18da25c5a1077d0041d1f5a`  
		Last Modified: Mon, 09 Mar 2026 20:36:57 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:808d8836d689825dc9b29b73defe4c6942577966d2a96afdc6d761097a408d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220820827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fbc4cc05a12eaecc3d7cdd4be6499671b1ca09d9df351bf69f0f3c13e66155`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:36:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:24 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:39 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edd46fe068e1b415bea38a9f7cfbbe59e553c1f22908740d8eb83bb50a5770b`  
		Last Modified: Mon, 09 Mar 2026 20:37:02 GMT  
		Size: 91.3 MB (91288290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b04215323220fd3d77497088933d3e8c77280e869a9ddecaa0765749b06f4d0`  
		Last Modified: Mon, 09 Mar 2026 20:37:02 GMT  
		Size: 81.2 MB (81158284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90746158aa87e2ff37637cc596cfcad1a34b8c07186045fa750d9fd54877e304`  
		Last Modified: Mon, 09 Mar 2026 20:36:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedd87bbde4e578cb0f78023dad18bdfa2b30ed07a3dca033f4ca0e0e6dde5d7`  
		Last Modified: Mon, 09 Mar 2026 20:36:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:373f1347629cba0d50e951e4c3f17522c274c57a98ee12aee341c867c7410f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73928f93f5f256eb1e28452978f2a00eefdd81e2bfd0cb3912c5eff66617de59`

```dockerfile
```

-	Layers:
	-	`sha256:216def05398c23aa510425c90738adca52fa237fd36e2f163ae83184f07ec6d2`  
		Last Modified: Mon, 09 Mar 2026 20:36:59 GMT  
		Size: 7.4 MB (7353532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57faafb882875baa5b9fadc5e06521affed5ec695d0faadc10ce11cd0cc09519`  
		Last Modified: Mon, 09 Mar 2026 20:36:58 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:b7beffc34bfe40cc153a4e4cc2d9a072b7001ba0dce35f5841dc9660b041b7d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230971108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c124f6cd051a9cc23cc1bbc0f29a4e2588fc69ad6a3c3f237cdaaaf48dc82f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:39:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:39:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:39:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:39:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:39:48 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 21:07:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 21:07:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 21:07:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 21:07:37 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 21:07:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375aa8eacf526a2bf938fbc2d4fee75e90900d45e6476502c1338fa7b89cf807`  
		Last Modified: Mon, 09 Mar 2026 20:41:55 GMT  
		Size: 91.6 MB (91632879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b74684bf768b85dd03b2869338cf265c00fe52c2802044a317223ccf95415`  
		Last Modified: Mon, 09 Mar 2026 21:08:35 GMT  
		Size: 87.0 MB (87000387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27af2fe9a8693464f1749e9cffb5797698e2cebd0280fe8626cbbc3ff2c7f6d9`  
		Last Modified: Mon, 09 Mar 2026 21:08:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1695a85255f1960a495b9651b168179b99d25e95e7bce9cc63ea93d17f77837c`  
		Last Modified: Mon, 09 Mar 2026 21:08:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:608872de3d3c76f3429a5523bc09c90deee5563e8c9d648482122451fa6e57f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7353320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989e5d9fc90f87c30e41e0a4ab70c7f5106216d1ace61308dda80eb965fc805e`

```dockerfile
```

-	Layers:
	-	`sha256:615c84c2f8401a1d933a8d3cf270ebe889751db9804bdf5f1d421b0045f381c3`  
		Last Modified: Mon, 09 Mar 2026 21:08:33 GMT  
		Size: 7.3 MB (7336264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e25ce4234c1fe1865f967b9ccc63606b675ad43aad06e9551698a1ebe073ca9`  
		Last Modified: Mon, 09 Mar 2026 21:08:33 GMT  
		Size: 17.1 KB (17056 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:7494f7c0260f82f93f5a0cef16218e318eb29a2302506b0277dd3b6a9fd39a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215371510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1aa003477d69b0e3a1cb06db519efe888cb0fa203ccedd8f7e12e61f99cd52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:32:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:32:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:32:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:32:15 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:32:16 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:37:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:37:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:37:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:37:05 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:37:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090c1a93b6afd53923a7febafaf7e1aa30c3499c036618702ec7c47bcc97854`  
		Last Modified: Mon, 09 Mar 2026 20:33:13 GMT  
		Size: 88.2 MB (88233824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee82ccbfdc1572f8f3ca195e24c15c0e239a5208718e1b323db4e769f81b717`  
		Last Modified: Mon, 09 Mar 2026 20:37:31 GMT  
		Size: 80.0 MB (79988555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b997dc3571e47c528d7606b4195499606111d658975769d1235c5f4ed3dc35`  
		Last Modified: Mon, 09 Mar 2026 20:37:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16154ce6de44b6d19f5356b2e54b7a51d0c25059aaa570c1d5c1f100b5cedbb2`  
		Last Modified: Mon, 09 Mar 2026 20:37:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5aa025df8359e2b0ec3b121c6345c9ee867fbc978281d0238e5b840e4cd8d334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f211df827767706727f06ff6db7c49dd6b5cd838f0be9a3c99a785a74165182e`

```dockerfile
```

-	Layers:
	-	`sha256:309685e9f1b2e6d7afeca6f1b932c8f4d623162f43b5fcbc936e324617c0d41f`  
		Last Modified: Mon, 09 Mar 2026 20:37:29 GMT  
		Size: 7.3 MB (7323581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01e0b432a8712902a5ce2d87d992e86866be60980382836d440059f9d143cfd`  
		Last Modified: Mon, 09 Mar 2026 20:37:28 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
