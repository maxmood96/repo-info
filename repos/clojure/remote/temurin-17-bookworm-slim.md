## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:01e296a9a29cb27199a265d68486ea213c336f1d61f670634536f7be837141a1
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

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

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:30d9983bdc20202ae719fa6dcd06a5f796a479020dede874d8db53981bb482af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253051192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aded77c21e021bd395eec2f06e4d44086f109e7cf9ba4b304ae3c3ab698d1c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:51:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:51:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:51:19 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:51:19 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:51:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:51:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:52:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:52:00 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:52:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6794dc00bb6fdaf8b962c369d15f7405aaac04411e7ecbf15a73162317f234`  
		Last Modified: Mon, 09 Mar 2026 20:52:43 GMT  
		Size: 145.4 MB (145438252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f3fa96ed675b2ab57a6ecb8140b534cc08c38e180234f852af24cc6d7d2840`  
		Last Modified: Mon, 09 Mar 2026 20:52:42 GMT  
		Size: 75.5 MB (75533565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3444ef8f59d8f20914dabcb494989e1bb0af6fb800e3ee6ce47d96a97352f`  
		Last Modified: Mon, 09 Mar 2026 20:52:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efd6a5511cecdd7de6eea91e65a2c3dd215e09eb46f497968117ab7177c128a`  
		Last Modified: Mon, 09 Mar 2026 20:52:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1241f1163c2ed8294176ce200955b618309047860fdf256bb2c4bc81a4019b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95eb210026311a594b5c842dc833dda5d5d504b5d3e63d4ff52321d5fe58634`

```dockerfile
```

-	Layers:
	-	`sha256:ff995c05a137f472ebc202f19bbc8fb16d0eb40a83c0792dd052f126d7fc5a05`  
		Last Modified: Mon, 09 Mar 2026 20:52:38 GMT  
		Size: 5.1 MB (5121325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbca8c53941da4d1bf1327e172bb9a15af6344b9f3d3205aaafec8f0c18ba83`  
		Last Modified: Mon, 09 Mar 2026 20:52:38 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b5b699b11ef7ae74de1443d6a4972bcb62eb136d0040096e7c9aad524636c6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231033295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdcfd68c0a1081ee128cdf9b0784ae174ae8120f21417d77df5bda8d77f2ccc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:34:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:30 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:34:43 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:34:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f40c4812b116e842a7e8b49a607546c096afccd07515ec218a2c1c1b134c70`  
		Last Modified: Mon, 09 Mar 2026 20:35:31 GMT  
		Size: 135.6 MB (135627122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e082bac5656d89924b39f248a9952dcd65c6fbce5970886773d39b42494eee`  
		Last Modified: Mon, 09 Mar 2026 20:35:24 GMT  
		Size: 68.5 MB (68513605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fcc257504af90e3fec67362890273dcdd07f91b4e1e83a80849f43e2dde75e`  
		Last Modified: Mon, 09 Mar 2026 20:35:08 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8be159411fb84168e8209c3b04cd90654f23993262ab9aa807211150b5a5ed`  
		Last Modified: Mon, 09 Mar 2026 20:35:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b3d4899ac9d7a300c1d2050068186be213168f042e7a0e83fd398240806bb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1459b5022c00262892c6fc15729004d37b553c3fccaabdb9a38b3a91ad304926`

```dockerfile
```

-	Layers:
	-	`sha256:58ce1fe3b8f11a4ff8be4804f70d21988a82811e418ecf9ca5270dac75347443`  
		Last Modified: Mon, 09 Mar 2026 20:35:09 GMT  
		Size: 5.1 MB (5107488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42668d5126143b31aa145ca4b473b929cfeef87a5bb75dadc9cc3355a41ea34`  
		Last Modified: Mon, 09 Mar 2026 20:35:08 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
