## `clojure:temurin-26-trixie-slim`

```console
$ docker pull clojure@sha256:ae6df80486160de43275212ac03cc2baf5004b1f2f45446f83d1cc12e19c1798
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

### `clojure:temurin-26-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:305dcec4dcff098939783dc791471d23098b6bd0ce55e1f7970b0bb6392f8290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196353224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770dec1e87e0818d42ed7449841d934f4449f7223174427d0828feb34cfe48b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:02:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:51 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:02:51 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:03:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:03:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:03:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:03:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:03:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24a8e21c69b3af1d7a485eb2aec3bc805f3d247fde1173dc91f705055ab5f0e`  
		Last Modified: Wed, 20 May 2026 00:03:27 GMT  
		Size: 94.5 MB (94524344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b77aab4a3322a27c5d77944ef483d1242b684fa49ccb2cfb200c78c653bc4b1`  
		Last Modified: Wed, 20 May 2026 00:03:27 GMT  
		Size: 72.0 MB (72047913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5934524b8e1b4872d9dde8bceed59d451b2fa813486424454d87033ea95254e1`  
		Last Modified: Wed, 20 May 2026 00:03:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c96a0ea1cfe40289df0728ade302899e8d603718017235b8e39d2de6a5a05e`  
		Last Modified: Wed, 20 May 2026 00:03:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee0424bc8b42a7095ab0b0ec886de7f7fc89fc6ad49aa83ed14c751695f57c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8483e3206e26455ed5b25083894160fb6b5430829c516d23dfe7df903cadd4b1`

```dockerfile
```

-	Layers:
	-	`sha256:e5b63884c309575a4b97c1c67401d070435987004f5a0bca0519d3bd7101f4f5`  
		Last Modified: Wed, 20 May 2026 00:03:24 GMT  
		Size: 5.2 MB (5224858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9d55af2ea85d2583b864f40b1ecc5db2704e9a844251480eace69c95808d5ee`  
		Last Modified: Wed, 20 May 2026 00:03:24 GMT  
		Size: 16.0 KB (15958 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:12fea82b7e271f51802b2d32eabb043ee52f9c48456bb224dd9a20403b9bd0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195519380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4528fdbb71674de4e0e081b3fc059d4cdc0e43cb3c9bc27cdea8d522d3a7138`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:09:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:09:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:09:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:09:39 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:09:39 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:09:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:09:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:09:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:09:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:09:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80cbfdbf332678d68e9f50c7dc2913246ac2df517a03f27cfcdc053abb146bf`  
		Last Modified: Wed, 20 May 2026 00:10:19 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1911aad669681aabd7a50917008724b65828fc668c4c1585f2c06567e84d1119`  
		Last Modified: Wed, 20 May 2026 00:10:19 GMT  
		Size: 71.9 MB (71872083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03861512190f50c321c3e41e25bf180e6cbd96895857ba0c2c4cb7a954ceb76`  
		Last Modified: Wed, 20 May 2026 00:10:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8d7689f23072c4b79412b5b786a0f91dd01a453534773ad00c2ae7fade1e2a`  
		Last Modified: Wed, 20 May 2026 00:10:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a3faca0a24eadd70675958065237530fc16afe2dc16a5d082edf355a43225984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8b9181ffa38d3f1fc12da2ec3d1c14de661e44baddea32e7155b7bd29daed5`

```dockerfile
```

-	Layers:
	-	`sha256:d4f1801aed88075a64f12baa2f9b5ddcafffcd8f07964defbd333f946372aff2`  
		Last Modified: Wed, 20 May 2026 00:10:16 GMT  
		Size: 5.2 MB (5230616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564a5d17a0b56617557768037d0d184d3ba7d0f25f1bca3f8b9c1513af7dff67`  
		Last Modified: Wed, 20 May 2026 00:10:16 GMT  
		Size: 16.1 KB (16077 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:480f8256eb9098359d4bf381aa1650a11e721458a494aae3bb31c40c32fffafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204969657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33658b4fdd44888b2a46433dacf7b1fc23f452ce00e24ef4123303a4fa9fdbd8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 06:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:12:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:12:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:12:19 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 06:12:19 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:15:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 06:15:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 06:15:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:15:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:15:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2942d8be338199c26e34e214469a511179af7962dd2c53cc0d1e7902697a70`  
		Last Modified: Wed, 20 May 2026 06:13:33 GMT  
		Size: 93.9 MB (93902068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9cd1cc67b6b32f5ab8de346adb4bc5e81cdb70df5e14f9a556c4b85416c5aa`  
		Last Modified: Wed, 20 May 2026 06:16:30 GMT  
		Size: 77.5 MB (77466093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b3fec4645ad511d427536fefc796a46bf09ba108b2bf6ba9ece2dfc6736244`  
		Last Modified: Wed, 20 May 2026 06:16:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661999c488e41f46ba3b51cd94db3e69b74f176dad205ed2b1f218beb11125d8`  
		Last Modified: Wed, 20 May 2026 06:16:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8831d985ea32c2e99dcabdac0d200599d1e0173b56b849012a30bf8b996a5ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf3923cacfbdc88d7137308974c19780bd6c91753f8bc59fd084dce337d8826`

```dockerfile
```

-	Layers:
	-	`sha256:75acc576495b30a2bbad3edb97610be05284bb19259b2638aa92843e0c6b75eb`  
		Last Modified: Wed, 20 May 2026 06:16:27 GMT  
		Size: 5.2 MB (5213165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d373fbb7b9723a869090534f01a86c15c25f414dc649a514cff3070fd8447bed`  
		Last Modified: Wed, 20 May 2026 06:16:27 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:368b064267a76e1466d9a1c03fbed21ea7767e48a2a94ba5df747fd176eba64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193413369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732334d004618e533dadb140f4f9f2ac1317c5f440880aea1762760e65c62422`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:49:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:49:23 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:49:23 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:50:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:50:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:50:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:50:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:50:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f28ec650cc3670cf225cb9ba6ae9fc5cb2ad7e45efa2a6c00995e79e4c5ae07`  
		Last Modified: Wed, 20 May 2026 01:50:04 GMT  
		Size: 90.5 MB (90536967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c2e1a948cdddbfb36636088148b96c1e27b4b5212c0e9588f8d2d3518d4cb1`  
		Last Modified: Wed, 20 May 2026 01:51:02 GMT  
		Size: 73.0 MB (73029442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514d51a519815e4d2971eb52e2f7faca948d44b190d180c86182b78b6efed93b`  
		Last Modified: Wed, 20 May 2026 01:51:00 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e025dd0f501ce596c01c2a2c58101148a2379e6d3b85359a3bd92e9f757ec4`  
		Last Modified: Wed, 20 May 2026 01:51:00 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f30ba445f176c4e85ccc53fdfab88ea1dc3844d938d040032d6c9b712c4ea8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7be96e9daf622f06828cc559e252c552b3b0b483f8a4046eae69455fd397f2`

```dockerfile
```

-	Layers:
	-	`sha256:e4d1699eadc042432181840be0e5ca397de17363c4d61276f3b228c247a3449b`  
		Last Modified: Wed, 20 May 2026 01:51:00 GMT  
		Size: 5.2 MB (5205968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a827253ecb02bb6192e0ca8f7079683a0308244ad23444586df07e0afb9c943`  
		Last Modified: Wed, 20 May 2026 01:51:00 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json
