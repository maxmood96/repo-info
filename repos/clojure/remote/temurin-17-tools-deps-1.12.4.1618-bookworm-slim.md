## `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:be496f0e568a5cd03aafe05c55f444b5caf1ca1408cefc2d317dd4e7cd00b547
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b5552d06e4d916432f1ef5d3972bbabc1ae38cf4286ebda936729f62605fc3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243567490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ddf8e329b968b50922393cf3f3e20f5a1273dae78f926baef1735942ea234f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:58:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:58:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:58:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:58:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:58:36 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:58:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:58:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:58:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:58:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:58:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037f7eebaaf9115b14d0d10d8a79bcae530674da0889f5a45a3fd2c7f63a2142`  
		Last Modified: Tue, 17 Mar 2026 02:59:13 GMT  
		Size: 145.6 MB (145628486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eb6ca4f462335fcd1eea1fac0da34e0bce85a2eaec47e2e7271d677e497d0b`  
		Last Modified: Tue, 17 Mar 2026 02:59:12 GMT  
		Size: 69.7 MB (69701742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60924bba1264bd013295ce2a270c9efc940ca6334339b134749805286bd222`  
		Last Modified: Tue, 17 Mar 2026 02:59:09 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ccd6c0702f31150360a4a0db5a80a80bc2760146753054d78e3b445cee4eab`  
		Last Modified: Tue, 17 Mar 2026 02:59:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1138f12eeeb7bfb43139d57799cb8e69eb7f8940cf974b0c255abbd3754c8a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f5ac38be5929becc18f928207f4ce3e8ac6c1669be25ffeee619b093a1bbfc`

```dockerfile
```

-	Layers:
	-	`sha256:8d36ee8cbaae2048ddd6396bd923e823a4402946ce2d018aa168ce0e18460c45`  
		Last Modified: Tue, 17 Mar 2026 02:59:09 GMT  
		Size: 5.1 MB (5116167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:305be86d88cc6d32707cf48976318b372dd03d8dec3f4db1c5566c70bb9bac41`  
		Last Modified: Tue, 17 Mar 2026 02:59:09 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0236a52158363d9271b2709602e2c316ee232187235950970e307f942cd7ac5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242242350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3529ccb4a0d15ba0d2ee258d2064901cb87b1286d491a83348b2583d0941697e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:02:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:02:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:02:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:02:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:02:17 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:03:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:03:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:03:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:03:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:03:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa62dc66a526d723e5c9e288d76268601c2dd64c33a54d5a5e67e537eafdb01`  
		Last Modified: Tue, 17 Mar 2026 03:02:57 GMT  
		Size: 144.4 MB (144436241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f4777d10d05bcaaca291b8a0cfbc2a0d6d0bae2d5b3aefb21f1775b109a421`  
		Last Modified: Tue, 17 Mar 2026 03:03:35 GMT  
		Size: 69.7 MB (69689004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3b6acb3b92dd64b2e308f4875a4661a0ef73b80c1c894ec307eddedb0c881a`  
		Last Modified: Tue, 17 Mar 2026 03:03:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8d1583dc45df2bcfa27df8fc09379e927e34b5fcdf40bf472d9e936ce13beb`  
		Last Modified: Tue, 17 Mar 2026 03:03:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0f7bfb443e57515adae1e904c015fe0f5836ec005900af6422df75f16f6a422b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ea1745dd7c3dc2b38f54aec034a436caa18a13e0bb755630b260f1acca5855`

```dockerfile
```

-	Layers:
	-	`sha256:92e62c4712193bd8d93ef309f981160049e747a98467f2d987136ad3eddc0f6b`  
		Last Modified: Tue, 17 Mar 2026 03:03:33 GMT  
		Size: 5.1 MB (5121928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7962bd7bad4c3ad3ac1ce356c7bc9263fa25f50e03b55afc58d0d3db2f62e298`  
		Last Modified: Tue, 17 Mar 2026 03:03:33 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d988d98f63bfd22aa78defd80d9e19c48844c6f08b33c176903388371236cd25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253051041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854d213d8c4ed3d51742997cb3fe9cf3144e28baf13642a43d4a71661302d2a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:24:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:24:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:24:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:24:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:24:42 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:30:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:30:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:30:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:30:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:30:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705c24a18f6ee8e217698c94ce8917cf545ab215e1af2f67054b8aadf8bc4a9`  
		Last Modified: Tue, 17 Mar 2026 18:25:57 GMT  
		Size: 145.4 MB (145438266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0405cf48aacfe852792e8db2dd763330f6a73ae6f1750d26a1d2c03d07c6687a`  
		Last Modified: Tue, 17 Mar 2026 18:30:56 GMT  
		Size: 75.5 MB (75533368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1db6b7fac07fec680ca092b5be38f1d8b2374f355e66445f9da98cf57505b4c`  
		Last Modified: Tue, 17 Mar 2026 18:30:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f562593312ad2a3a137ba4daba01aa5abe410fafcea2686e6069e54c6e5240d`  
		Last Modified: Tue, 17 Mar 2026 18:30:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:327a23e7af8c65c21cdd4fd31d50ad87765e9ca203dd39734283e9ae03ce7576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac8883797b91f362e3d4867817ca8a4f7ebaa5916da127f13d51310f67d8575`

```dockerfile
```

-	Layers:
	-	`sha256:a811c24b7a1ef409414d416fbe0a955a65ab0fc6fcb7a4a7db79b28f126ecf6d`  
		Last Modified: Tue, 17 Mar 2026 18:30:54 GMT  
		Size: 5.1 MB (5121325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7918962a5b756198bddc41ccd09a696b4903794c303126115565fa8ef67fd770`  
		Last Modified: Tue, 17 Mar 2026 18:30:54 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9d40ad87a708dc8df76ae681a98d1de6d5c2a52eaff3362ae6de9e1e466b7b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231033292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbacf0317fda269eba42b53debfd07c38654bc0c30164ff5125ef1140f2162e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:35:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:35:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:35:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:35:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:35:59 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:36:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:36:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:36:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:36:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:36:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90333c0ee269ff313cb16815a9366978962cdd272d8a7bba08017c7887643d2e`  
		Last Modified: Tue, 17 Mar 2026 11:37:40 GMT  
		Size: 135.6 MB (135626810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1933c6783ddbee86a116e3c855007a4df62904afb5c53f5a9b146f2889099085`  
		Last Modified: Tue, 17 Mar 2026 11:37:39 GMT  
		Size: 68.5 MB (68513925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963200d6c04a4b4ea556dfa3e51cb0e6a1275371dbc03c38dbd29bffcc421ac2`  
		Last Modified: Tue, 17 Mar 2026 11:37:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e224738114c8ab04685d2672733b2edef961a087fa2f4a56a51480bb253137d`  
		Last Modified: Tue, 17 Mar 2026 11:37:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e3990400eddcab9a39ac3e3c546e46ea8fa05a7afdb258f665cc148a63430ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee80df7f963f4370c242aab5fde2e8342fc0e07a4ac8d27459e3a655cabd629b`

```dockerfile
```

-	Layers:
	-	`sha256:31b34e6e42a62b61b65938432d60119006e58111c50fddfee852b5730d27c010`  
		Last Modified: Tue, 17 Mar 2026 11:37:36 GMT  
		Size: 5.1 MB (5107488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1cadff5bb513f7b37e724e7758b7bd686e68de9468e011073fc7b78c45c59f0`  
		Last Modified: Tue, 17 Mar 2026 11:37:36 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
