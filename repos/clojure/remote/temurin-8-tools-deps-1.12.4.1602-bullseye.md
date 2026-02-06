## `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye`

```console
$ docker pull clojure@sha256:3882d865b57f5569a298124858640f4cbe721c68916d91f773370f6d3884a9cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:95fe659b90eef48e4b361d8a103c0914af3b858d6edd88739f52b66183ecbc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178468721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2299bdf512673731f03365d0064cc3b13b9087965fb8643bfd4959408ce1b2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:01:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:01:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:01:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:01:28 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:01:28 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:01:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:01:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:01:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6455c4980b161b45fefd1d902421a3c1c773c376a97da0240629392e9afc6966`  
		Last Modified: Thu, 05 Feb 2026 23:02:01 GMT  
		Size: 55.2 MB (55170164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4394766335f1a2ce5e408a9559ccb84420cd5cd145be5ede1c8ff5bf45e5ae0f`  
		Last Modified: Thu, 05 Feb 2026 23:02:02 GMT  
		Size: 69.5 MB (69541653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27994d97025e6738c1dd9c5fc44594de75f95991588ff87cfaa25c8b88d6f374`  
		Last Modified: Thu, 05 Feb 2026 23:01:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:28ad3815ebbf58d8ed615e40f67a3d539adc1de12f1813b83e6c916099a1e7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7532900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ebb80e3700f1a27b4597a31f567082a5fa876adcbd8c5d949336887ba2c5a0`

```dockerfile
```

-	Layers:
	-	`sha256:bb6ceddd08eefb7c0632b707d3b4ab7da6aad44c1afc21ec828eee512f757c38`  
		Last Modified: Thu, 05 Feb 2026 23:01:59 GMT  
		Size: 7.5 MB (7518707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6dad894261cdc52147a453e3d7517b4d30bc016ddfbdc1d16ae33ee1e75c2c`  
		Last Modified: Thu, 05 Feb 2026 23:01:59 GMT  
		Size: 14.2 KB (14193 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0c355d504d4f7cfbc3f67da4cee9f147f8ef20cc39f336893bdaaab29c53e7a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176203969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96523577ca13cd55467a7e5bf0d7466b00904c5352a4c641070387b81f9f2bbc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:02:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:02:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:02:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:02:22 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:02:22 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:02:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:02:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:02:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9f37b75522971662718f7a463425d9152d5462a579ff84ab85d7b5eee98f3b`  
		Last Modified: Thu, 05 Feb 2026 23:02:56 GMT  
		Size: 54.3 MB (54251630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34966d1b6e9ef06cce724b01867db6c2c418de2bfcf139d8ac3875ecfd46fd0`  
		Last Modified: Thu, 05 Feb 2026 23:02:57 GMT  
		Size: 69.7 MB (69693374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c95615eb72bb177ccb55dd44a3315e24a06df49ccb69d26e44d39a7fb2c174`  
		Last Modified: Thu, 05 Feb 2026 23:02:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ab51fd5eed72c0c285f9a4ad095d6be5be4525018c2a30ddc144e71dc22d556e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7538817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0b3017360d9c68db3d6f34764980c1de9e7762d6162ab5446598d95f9d4952`

```dockerfile
```

-	Layers:
	-	`sha256:504325782a9d9667bb39f031cd917fe397364c796dcda72114231186c23cda01`  
		Last Modified: Thu, 05 Feb 2026 23:02:54 GMT  
		Size: 7.5 MB (7524506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c228f80008a70460f1898073535a3bba5f6b0269500a261e50e45adf2b7696c`  
		Last Modified: Thu, 05 Feb 2026 23:02:54 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json
