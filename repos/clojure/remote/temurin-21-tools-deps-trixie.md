## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:3aa7bf260f6f6b763679b1c546fa7a647f4aedd48c9d448dd5818ccd41ccb4a0
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

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:cd6b842f3b8ac2a1eee6e7eb1834f6f669b9325359a78b0031b97f43b8e4b413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292658285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b086b170970cc5dd5e8b3e8868b80d7231c6b01b0b7440754f12cd3668da292`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:55:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:55:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:55:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:55:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:55:28 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:55:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:55:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:55:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:55:45 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:55:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7634d88edc0e8fc40f68f03a0e9c9ea4a1e29bcf57dc2431f789e5d5f8c5d02e`  
		Last Modified: Mon, 08 Dec 2025 23:56:36 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b4a57a83c2a4790a645f72a1601c0e4e89ba723da7af5bf1d460357e2db30b`  
		Last Modified: Mon, 08 Dec 2025 23:56:22 GMT  
		Size: 85.5 MB (85541695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471dca180a7bc395276808bd7c86c2ba72a479dcb484cf10ba0b976749659c88`  
		Last Modified: Mon, 08 Dec 2025 23:56:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20f0116f0ff8a483e3511622f9b1371031735f1301836118b66daa3545f6302`  
		Last Modified: Mon, 08 Dec 2025 23:56:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:36369c44ff4e2da7cf2208bcefc1484a5216252d33f266905333943701a5e7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bf1ef722d332c8c4ea5f7860c6696caeead3057f4eedef223e003e4d26f937`

```dockerfile
```

-	Layers:
	-	`sha256:4a460825e36def4bd4f64840ee1c8478d5cf92e5a35fffcee2845c9349813970`  
		Last Modified: Tue, 09 Dec 2025 04:44:42 GMT  
		Size: 7.5 MB (7470033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4a6a231e37b67d35822fa54015f30b9a61759b01127f9dc9ca305958e4dcf2a`  
		Last Modified: Tue, 09 Dec 2025 04:44:43 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:46c0ebea7eb5bdff994a9392e5d6f4fcf7c1e7278da910b14e45ac65af051560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291124029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ffe69bf24ec2b0099ee1ac78559ecd4361a914597bfb13ac70596db01e21fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:02:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:02:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:02:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:02:39 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:02:39 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:02:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:02:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:02:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:02:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:02:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cf29c6ea9574837c785b6419e44eb6a4c4f58667bbfb78db9ea4112abcc09d`  
		Last Modified: Tue, 09 Dec 2025 00:03:44 GMT  
		Size: 156.1 MB (156107650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7abfcce45aed0126ce97ceebf0dccbdee1ebe31c679cbbeb4bb8d1a3a5976f`  
		Last Modified: Tue, 09 Dec 2025 00:03:40 GMT  
		Size: 85.4 MB (85365113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a6279ca79a8a8f3427aa1f35580c151f677a8a2a0e7b760ccc2e94efc3656`  
		Last Modified: Tue, 09 Dec 2025 00:03:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dda81e8f8bc9d5c10eff467974cbbd1350d2535fd5a802331da1275d34bee1b`  
		Last Modified: Tue, 09 Dec 2025 00:03:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:de8103e2c8e63cb519397dcf6c114e578f7a9ec2ee976eabfec683ceeb91df08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c398f29978b6fc1fe07887880f8c6fb840ba3ea37907ec733df0147df922f6c`

```dockerfile
```

-	Layers:
	-	`sha256:2f2b076a92fbf5ef45c6581b80f33fbb4d5404e9d33190dbf0aa85154d66fef5`  
		Last Modified: Tue, 09 Dec 2025 04:45:19 GMT  
		Size: 7.5 MB (7477063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3697b26d97cf9b97df9eafb1293fa8b7e09f22ffb2394f705b45b1c4501fd427`  
		Last Modified: Tue, 09 Dec 2025 04:45:20 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c3432d4bb18b208d48377758da24311ff2fe0b71586e685ba35523ee014acb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301999971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f014f8f92068aaceae3747cdae80cfeb4c2e0be95ff2d5a9a3eb954cd74f2da1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:29:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:29:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:29:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:29:48 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:29:49 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:30:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:30:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:30:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:30:40 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:30:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6a2ef35163b9d4f6648137cf0019838288c6072622a6112548fb68bfe52e18`  
		Last Modified: Mon, 08 Dec 2025 23:35:07 GMT  
		Size: 157.9 MB (157942951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366e13381937c669010653d4da5ccec593043394a6b706c2995dd3f968853e38`  
		Last Modified: Mon, 08 Dec 2025 23:31:42 GMT  
		Size: 90.9 MB (90947501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daef7c06cd8d6e32f8571d5913b0ce6745a9ae2796c4ccd635435956b5b1dfd`  
		Last Modified: Mon, 08 Dec 2025 23:31:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95600155ba5b9e5a1632136cdde89056e2608ec567154b20c2cce625d003fe26`  
		Last Modified: Mon, 08 Dec 2025 23:31:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a98fed7e23d1227ca73d5cd779496618e5620d24ee18fc676709df0ff25e11c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64895f5bcbd9a44ad919bbc49a670b1aa3aebf96e14c2c6ed9a2249bcb137ce`

```dockerfile
```

-	Layers:
	-	`sha256:c108e31cc8198ebf2d06afdf4fc77b1912afe2c645465d80df58e94f595a52e6`  
		Last Modified: Tue, 09 Dec 2025 01:38:28 GMT  
		Size: 7.5 MB (7474452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:458c0ced43d2ee8499fbc5b657dbbf57c8dbbc23b3daee154942f76d35e3ac58`  
		Last Modified: Tue, 09 Dec 2025 01:38:29 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:fe818d5cbf1f07d5689a07d8550187fef5f993bc18c8aaab33c528694acc5740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289392999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6022d64abdeca198fbff87174f36826d9e9b6714e1bc993288ecba9052bf4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 18:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 18:20:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 18:20:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 18:20:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Thu, 20 Nov 2025 18:20:05 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 18:36:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 20 Nov 2025 18:36:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 20 Nov 2025 18:36:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 18:36:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 18:36:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9510e39712dd763e37991974565f84df07e5754bd9efcade332f8c04005a4403`  
		Last Modified: Thu, 20 Nov 2025 18:38:42 GMT  
		Size: 157.2 MB (157194242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a0579df77c747c2a8c3bc55bf9d5d4e13de4f00e9be47ba33d3534531a8e94`  
		Last Modified: Thu, 20 Nov 2025 18:40:49 GMT  
		Size: 84.4 MB (84426521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9f24b9b7df127d57f113d2a8d2e41763bd0a4211a05b4a6b0bf84c4d0e4f8f`  
		Last Modified: Thu, 20 Nov 2025 18:40:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97db8818b672928861d749f862df5a4771f2ccb89f472f5aee852c693633b4c5`  
		Last Modified: Thu, 20 Nov 2025 18:40:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f50c8d80d9c69e669c12c3da7a1ce5fd30d20732e2f03e6e41da7cca8d30276e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469dddb5fa20b43fec4f2b57e70dff7248743222ba3141f23cddecd8dcd4ef5d`

```dockerfile
```

-	Layers:
	-	`sha256:6bebe4a4131ba6e0e093cfeabec26b3f03c8046997570f2d9c534faa66aa824e`  
		Last Modified: Thu, 20 Nov 2025 19:37:27 GMT  
		Size: 7.5 MB (7457946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae2929afb545f8eb7491aad0cb2ad0a46fe776f2e89075a88febc9d5b38fdf3b`  
		Last Modified: Thu, 20 Nov 2025 19:37:28 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:72c9a1c8bb8282484cccd5629d06c43dd0a93916a2a92c88695f438c9ed63971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282927985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4643a84ff8ee006fce25870ea470367757e8b5386cdb6a67641b7245cc21ea`
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
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ad8af80bd1fca505a458dadc68d16da2d131f0ace69cc71fe587e4b3a2a78d`  
		Last Modified: Tue, 09 Dec 2025 01:31:58 GMT  
		Size: 147.1 MB (147069847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ae6372ea09379c1a8bb5215b1d8d5bd3fd9e6bf168db96964f7c58a98e077`  
		Last Modified: Tue, 09 Dec 2025 01:33:29 GMT  
		Size: 86.5 MB (86511192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7b5cc2cf174f3eb7fd34a921acbee9d9067e896b4858481e426778a7fab03`  
		Last Modified: Tue, 09 Dec 2025 01:33:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4182603ed3d5cb5eabbc46c801f10f720d7ef77241dbab5490b6aa5c1135ca8b`  
		Last Modified: Tue, 09 Dec 2025 01:33:11 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:28a22f29f1befdea9ab086821d035b2ee80cf740e84010eb7f1cee5d0fe31e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aad8f5c0ef9fdd68a0298a6dded6f94122ddcdea01c5d37b26fead1e54b943`

```dockerfile
```

-	Layers:
	-	`sha256:b78ec6fd2aeadf194b518bdc0be1e715d9f116c3258f8f073d1676a28937386e`  
		Last Modified: Tue, 09 Dec 2025 04:45:34 GMT  
		Size: 7.5 MB (7465955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70f047055f5e329505bd02e6d9c007f1fec59f03f94044a5fc452eaceb1818e0`  
		Last Modified: Tue, 09 Dec 2025 04:45:35 GMT  
		Size: 15.0 KB (14952 bytes)  
		MIME: application/vnd.in-toto+json
