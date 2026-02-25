## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:9732e23a308246141e7fcddb187d2743f786b249330c90f4bd527519ea4277b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9931d6c5edba829d3879ccaf21b18ee1fbf7739f75a8e260e18409e0159093fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190003881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2ef4739ac0740c66bd978e4090e19600410c25e73dceae0bb3166590b0ab42`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:52:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:23 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:52:23 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b748e78e7b88335045a7938572d023d71fe0f01480d555a0534a19c0f0ba5b`  
		Last Modified: Tue, 24 Feb 2026 19:52:53 GMT  
		Size: 55.2 MB (55170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1f4f076d7d5698338e0e4ab23199e469d1255df3b33f32be57f9ffe1f2ee45`  
		Last Modified: Tue, 24 Feb 2026 19:53:41 GMT  
		Size: 85.5 MB (85540044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c14137f11425a83d19191736ec7e35df487c976574528c7a3acf4808a72f2a`  
		Last Modified: Tue, 24 Feb 2026 19:53:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b96d5ef3e6c575112664f61efb3bd8f3907a6ccc4141c2629a63a3d87a067b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7604237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d278617cf9d8d91580c705135496b0cb9a6b82cf238a3381678ce32c49878425`

```dockerfile
```

-	Layers:
	-	`sha256:a55847d8942e75ceacf75c62eff9e27fb4eadd7e4792be18ba0d8bcca4bcfab4`  
		Last Modified: Tue, 24 Feb 2026 19:53:37 GMT  
		Size: 7.6 MB (7590067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58bba47d2c53220adee7344e664b531099a890dc03c5fe1432541dfbf190a2e`  
		Last Modified: Tue, 24 Feb 2026 19:53:37 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23081d5e7f2696df193ba8d5b5482c9697d20772c833e6b0446c8fe700adf1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189269237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555b12397e69d9d7ea915a3f860fc30fc18ff288296b2e41c7a8b3b6e38b8a5e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:03:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:03:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:03:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:03:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:03:54 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:04:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:04:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:04:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffea5bc637380019ebfcf1c2986b05e95a9345882ceef7187b8a6e659a3d421`  
		Last Modified: Tue, 24 Feb 2026 20:04:35 GMT  
		Size: 54.3 MB (54251622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c51f0da78c920ccc7b606244a9873c2d06bf2f9ad888be02b6f2e17ab514a07`  
		Last Modified: Tue, 24 Feb 2026 20:04:35 GMT  
		Size: 85.4 MB (85364804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3df6554104c992dcfd07f78edb745d1709a7d5f2aa21ffca6f3aa51d06c532`  
		Last Modified: Tue, 24 Feb 2026 20:04:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:92a6bc4f230253d3c59baa1d67695ccc4ef25fbd134fd9c402c42ec332ae747c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7612085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a3fe78552ffc11fb353ce33217a7b4f87a448e5ff4e38b2670734271b7cb17`

```dockerfile
```

-	Layers:
	-	`sha256:b199765e3ec0a4d129c61daf425f30a9b537e2d241d1c2f058b4b4a7e90c8bae`  
		Last Modified: Tue, 24 Feb 2026 20:04:32 GMT  
		Size: 7.6 MB (7597797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8b542e985e245ccedc374eb54c9373658d1828f72e45dded230190a36a5d59`  
		Last Modified: Tue, 24 Feb 2026 20:04:32 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:32afe9fdbfe890de2347b9c0878e163b4e226dfccbb0958926a24e227ff49ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196720186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b627a34f3fbe71649c48a3732790d5cb34f1b00dec6dd6209bd3497b7ba05a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:43:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:43:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:43:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:43:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:43:24 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:47:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 01:47:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 01:47:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdef948f7a075c7ba090915db8bdf444c4fd6f03737e0d659d8563f21b69755`  
		Last Modified: Wed, 25 Feb 2026 01:44:45 GMT  
		Size: 52.7 MB (52650395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaddea7d6325dfa3cf92c7dab4509689725e7a42b4ea0626ecaa348487e2328`  
		Last Modified: Wed, 25 Feb 2026 01:48:38 GMT  
		Size: 91.0 MB (90956883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace16c6e95b88964ddf774f873fcddcb84bc480986f07123b6a2c82ce31c1fe`  
		Last Modified: Wed, 25 Feb 2026 01:48:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5cac2f8985feb23e248eb6dcae044e9357a87a267aabf0e3ae8c890d38e90cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7609301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e10498d904824dc1f04ac0330584a55fb927f25c211e6cd20d09284573e57d`

```dockerfile
```

-	Layers:
	-	`sha256:9d76ffe91861126289d78d45fa25e524579e5929c8d75b6b57b64aa6fa82f1b8`  
		Last Modified: Wed, 25 Feb 2026 01:48:36 GMT  
		Size: 7.6 MB (7595083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2afc78bf6378513a7309a122d00416e2acf435620ce14531791161d78d37d6`  
		Last Modified: Wed, 25 Feb 2026 01:48:35 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
