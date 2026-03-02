## `clojure:temurin-11-tools-deps-1.12.4.1607-bullseye`

```console
$ docker pull clojure@sha256:7410fc9d1c7f8ebdfe439d43e10eed4767a1589cfdebc2b1c311102596fbb511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1607-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1f7fac8f3ed875b8696da0a0db21a901030a882e01d5dbd690fef0d83401a995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269148597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6483e707f3f6802971e6c1fcb8e16946ca788cbceef0bab8edff8cdd4331e8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:45:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:58 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:58 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486ef9736b485fa7bb372a458a6d548853d9202bc7857419cf5b19336c7d1717`  
		Last Modified: Mon, 02 Mar 2026 19:46:36 GMT  
		Size: 145.8 MB (145806702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab827e8ec02fcd634fe405a8696eb31fcaaee132cc58ba97cb3e61ecf5fdee0b`  
		Last Modified: Mon, 02 Mar 2026 19:46:34 GMT  
		Size: 69.6 MB (69584816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bc769d4402edc0377c9cc708db2ec5a9d070277a9fa0cba53add168429a5d4`  
		Last Modified: Mon, 02 Mar 2026 19:46:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1607-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:742077a387d0811a33fce23a923b7103ad1d2f527fcb6329118a2c4a85817ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7443627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0d685a43cc8043075537142eac2839dfd0819e17a7aa0377fdc51beab72474`

```dockerfile
```

-	Layers:
	-	`sha256:9b677cc37e5db4a3a6cf2d98d50a51717de2eff21063b352660e1a6a61c011e6`  
		Last Modified: Mon, 02 Mar 2026 19:46:32 GMT  
		Size: 7.4 MB (7429418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0a4665616429008d709e21f78a9d3a4c179c8dbfe6aa66eb9b4d6d86e5bd46`  
		Last Modified: Mon, 02 Mar 2026 19:46:32 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1607-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c74b6b066b75ad618eb9dc47b1c64c24c12f8e180550ee555a334fc8b2d4d19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264486148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076656742d7531370aa021b1e617925108657df87771456bcdb797cd5050461b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:45:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:51 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:51 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf58f32357d9e093d84c8e6928d37a32b366685d7e38803e8426f4435dd789a`  
		Last Modified: Mon, 02 Mar 2026 19:46:28 GMT  
		Size: 142.5 MB (142501424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9b4649dda672688bee31f85f494af44a39ffd60d5f653151376e10264d79d3`  
		Last Modified: Mon, 02 Mar 2026 19:46:27 GMT  
		Size: 69.7 MB (69725686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab8008d4b538a3affe89d71719438bbe7ef0e709dbf0a17afb8b58a13845a74`  
		Last Modified: Mon, 02 Mar 2026 19:46:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1607-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:baba1b48582738414bc38e18bfae49c4e0c744ba789fa8541ba302214f98ccd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7449462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a252e094df5691aebecc9909a83473402cdc7df639680555579c0c92ca2351`

```dockerfile
```

-	Layers:
	-	`sha256:5984d3f69b31eb046fdc8a06d1609970562d67813114f0590af36f6234b9ed0f`  
		Last Modified: Mon, 02 Mar 2026 19:46:24 GMT  
		Size: 7.4 MB (7435135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afb9a0f0dd2cae770cbe610549b4491ae49b0d06ff8ba22b339072aff721bd9`  
		Last Modified: Mon, 02 Mar 2026 19:46:24 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
