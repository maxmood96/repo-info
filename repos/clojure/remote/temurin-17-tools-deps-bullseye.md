## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:59952a6794b3a7377745ecbbb4ad56453068535720cb9f3784f8997a2ff81240
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:658b741b46f63e20ae0620716d329de893ae9e0f871ff945e7bd1bbbeecf4105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268979447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34ef72254bce63bea497690c831cc4a00cf7fe5406696bd6a1f290b661fb03d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:58:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:58:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:58:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:58:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:58:29 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:58:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:58:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:58:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:58:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:58:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9930bbcbf917d8b65a26e2f4c9b13daf95382413834495c7f164d931dd8112b`  
		Last Modified: Tue, 17 Mar 2026 02:59:07 GMT  
		Size: 145.6 MB (145628435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d6daf3e6a1b732d736b1ca4bc906a52f26bc18028502c69843115c5c06bf14`  
		Last Modified: Tue, 17 Mar 2026 02:59:05 GMT  
		Size: 69.6 MB (69587494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e70c7ef66b1db436eaa76c4b86c55c044236c33d6929fc04bd7db04a30197a`  
		Last Modified: Tue, 17 Mar 2026 02:59:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a17687ce193b72b0f7ed34dcebae6ae0db1ebf81d996673fd041b772877cd34`  
		Last Modified: Tue, 17 Mar 2026 02:59:03 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b68de466e83b0279ccee4c5c4f1bd9c38b347373834c2c123a4acaf3907a2c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528cf599f8ccd721cddd6e9212f332faf109f554ca8e489f9d190d127544ac28`

```dockerfile
```

-	Layers:
	-	`sha256:193024b34950ad186b115e75df960a06b3d2df5f881eb4a12240c077f497f9a8`  
		Last Modified: Tue, 17 Mar 2026 02:59:03 GMT  
		Size: 7.4 MB (7407653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99e9cbaf0600a79dd90f79fe8139749c8ebd6350c346c2818cccf7fddb6ff82`  
		Last Modified: Tue, 17 Mar 2026 02:59:03 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a30606a922010f348500ed0b13cc3cce6735330f0c9c18eeb6a286ea7c7491fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266412481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76d74eded312d04653f651839d1c689aba759c23c91c347da000f4864bdcff8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:03:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:03:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:03:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:03:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:03:12 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:03:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:03:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:03:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:03:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:03:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c71dd7ee77e5c4c5af33e305a31612759cdd5424841d57ea90b3524fad65734`  
		Last Modified: Tue, 17 Mar 2026 03:03:49 GMT  
		Size: 144.4 MB (144436241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f124e9f2366ac73bd6c3cd137aece1cc9461dd26bed4a4a214c5fca7fb246425`  
		Last Modified: Tue, 17 Mar 2026 03:03:48 GMT  
		Size: 69.7 MB (69727950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bfbbae5d8f89171b6f2b049ad3032d6618a74c7ade6038393f5df38d83bb83`  
		Last Modified: Tue, 17 Mar 2026 03:03:45 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd5c775772c0527309e20d7899cae3deea585280de2c54f8bda6dced89fa636`  
		Last Modified: Tue, 17 Mar 2026 03:03:45 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7eb1419cd222fe5f8f24f25aeb666c1af19739945328dcd2d1588baa240a0529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779266d7d8f967751e09980ba0d2fd8f17d4eb6d2c3f1f1491ce2cf2d0d168be`

```dockerfile
```

-	Layers:
	-	`sha256:a450f6372e0dabd84f4553f509ef76e42c3b1d77522100b1819e9fff6730c19e`  
		Last Modified: Tue, 17 Mar 2026 03:03:45 GMT  
		Size: 7.4 MB (7412752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19b704136e5d98c20445b58c32e45960073d4ededa0c8c12e3293fbafba53cd`  
		Last Modified: Tue, 17 Mar 2026 03:03:45 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json
