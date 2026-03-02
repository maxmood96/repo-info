## `clojure:temurin-25-trixie`

```console
$ docker pull clojure@sha256:ddb8f8eaf784ab324a4e59b8cb463fd77ed56c98dd1b0db527bb09ba7d08c0d0
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

### `clojure:temurin-25-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:8226db19d3e1aa5aae4adbf60a762601b3d60da4f6d95820f26d7f364b1fadb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227105112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc88e024b9711eedea9d3f8a098703bdc8f3619921b937f20113e887fecf4c6f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:48:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:27 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:27 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:45 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd9ecb2f2cb912fd0910ee3e757c808dd1bbf0d08dbbc0631ecf6074a0b5bef`  
		Last Modified: Mon, 02 Mar 2026 19:49:08 GMT  
		Size: 92.3 MB (92256298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55093c28cc2786e8af680f015ed5b5bcb8eddf853c6f500f715bd7f224cb6164`  
		Last Modified: Mon, 02 Mar 2026 19:49:08 GMT  
		Size: 85.6 MB (85554648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b2bbac322132f7797cd463627c26fd913c05a289dd6ab8b862afc344ca3d24`  
		Last Modified: Mon, 02 Mar 2026 19:49:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03c4a52b4768fc0394fa376c145f5da3c5e40f12e655a2d66f4a92c5a34dc07`  
		Last Modified: Mon, 02 Mar 2026 19:49:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:84d88d0d7a8cae907dbf8c69698c3fc536a36c1d62d64ae9bc872268cf2a3545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1ae8fe67c371927e40762120c40185e0b05b894e73182b86c88d0b0915b67`

```dockerfile
```

-	Layers:
	-	`sha256:8c95e886645de3d6d64839ec013c0b329994e179500d7d47cd3d77e90a0b1853`  
		Last Modified: Mon, 02 Mar 2026 19:49:04 GMT  
		Size: 7.4 MB (7438659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a022ae78840c80828e407929317d9d0abfb701889853898fd54be80b4a8b7d3`  
		Last Modified: Mon, 02 Mar 2026 19:49:04 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7420b6bd8681567eb896c621c87c106fc68131993576103b0edd89f2eb576907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226319849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e37746b010d7b9b42528e3671d0a175d977cb434278ab1a7b59de85cbfafbe9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:39 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:39 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:57 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b658a6a5494619daba51dcc0afcc317eaa9860c6a25358609b78cafdc8c1d544`  
		Last Modified: Mon, 02 Mar 2026 19:49:20 GMT  
		Size: 91.3 MB (91288264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9547363607f027862960151ccfb52f8560ea833f4d57c13af5ce9c4b6cb20dc7`  
		Last Modified: Mon, 02 Mar 2026 19:49:20 GMT  
		Size: 85.4 MB (85378374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be67b8a6e673fb0b85902b353214d95ed5ff8273906596097ef3cafc5499488`  
		Last Modified: Mon, 02 Mar 2026 19:49:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dda5a3e8b36913894954fba029f01db4937fcc6a9cd12510e42a0b46133b284`  
		Last Modified: Mon, 02 Mar 2026 19:49:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:291a8217b25ee85d59baf3d4030830bdfc75837411bea004e6b9b3edad50b404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97604374d930521e5819768a7652efd3071523d814ee8663561294c75e14119`

```dockerfile
```

-	Layers:
	-	`sha256:26fe98d724f4c3d01506098a02aa5b63d859458bda965a23f73afca4fa1b6a1a`  
		Last Modified: Mon, 02 Mar 2026 19:49:17 GMT  
		Size: 7.4 MB (7445710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e4f4b204684d36f38592cd43232231a0e8abaec40657c089c17aea8bbe0dd3c`  
		Last Modified: Mon, 02 Mar 2026 19:49:16 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:af2a86a89d9fe491a4a090029a2db4f562052c9b8ac6cdc9f0940b39ff3c94cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235702769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddd10d69d533a8c624ebad8093fa9de4b08c777f078941cccb12cbd8ee1b612`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 02:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:14:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:14:50 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 02:14:50 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:19:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 02:19:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 02:19:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:19:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:19:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898bd9db475a819ec030b333968ed33ad54a305029d5289784462edd831f227f`  
		Last Modified: Wed, 25 Feb 2026 02:16:20 GMT  
		Size: 91.6 MB (91632903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546efa00bb9dea82d6a9c931ac2e95c22934b0f3a9f50f9b99a7adf1282e279c`  
		Last Modified: Wed, 25 Feb 2026 02:19:44 GMT  
		Size: 91.0 MB (90956561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7e32b1c2312dfd7c935fcbebb08755f65b6ad7764a99802991022a38a37e17`  
		Last Modified: Wed, 25 Feb 2026 02:19:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9f9c7446291662a229068687acff115bc1bbef7f94d5293cefe06ad47d101a`  
		Last Modified: Wed, 25 Feb 2026 02:19:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:723fc5f0d1302482ea252d8af78b7147873be66a00c5bf9925019d8a9767afc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ad571c5eb9f7468687949e575e9b92bba5d57029ff3ab85c2451e3beac52ba`

```dockerfile
```

-	Layers:
	-	`sha256:44f6adb064c534a0a4493322b76bb45ea4319a69d643a74244d3ef90a7749108`  
		Last Modified: Wed, 25 Feb 2026 02:19:41 GMT  
		Size: 7.4 MB (7424891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb3485489930beb1d91f268c64e4ccf43059e1204336ce4cd894ebaee078c8b`  
		Last Modified: Wed, 25 Feb 2026 02:19:41 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d7f761fefa4a3cfc27f3b554046cc31e566a70d7bcd21a47e39bd1350644d1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222975671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22c7cceff86edb4a9f70c5b3e2960309fc1f9bc79adb6647a05119c8127f5ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 27 Feb 2026 22:16:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Feb 2026 22:16:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 27 Feb 2026 22:16:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 22:16:31 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 27 Feb 2026 22:16:31 GMT
WORKDIR /tmp
# Fri, 27 Feb 2026 22:31:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 27 Feb 2026 22:31:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 27 Feb 2026 22:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 27 Feb 2026 22:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 27 Feb 2026 22:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573ae1dfa5ac3e612d691341ceea58307500dd6a6a8d2971335cac8b5c5296cc`  
		Last Modified: Fri, 27 Feb 2026 22:22:12 GMT  
		Size: 90.8 MB (90773425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1776edc5ee38340b1a3e147091bea6beda68c8955cad17b3f00c64ee8d0954d1`  
		Last Modified: Fri, 27 Feb 2026 22:35:39 GMT  
		Size: 84.4 MB (84424267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb6a2e97e5ad32c75b8a8cca8ce9e5724a709be6eeafe7a28bcf621a96dc2a6`  
		Last Modified: Fri, 27 Feb 2026 22:35:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1147b7daacd21825d7169985a5fa7e6da50267370ab4b024cf2c8adccab948`  
		Last Modified: Fri, 27 Feb 2026 22:35:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:89f346b64866a992149776cd516c2ea00321dc44b11b728458d73c0587956c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165cf0a2e6ec6c9d3aadf41129785a3703fea595c9e4c87c10e78b10acc29e90`

```dockerfile
```

-	Layers:
	-	`sha256:6ef5c0e0f5308ee5904f0c43930d41af168cece07984187e882ebb743c526572`  
		Last Modified: Fri, 27 Feb 2026 22:35:28 GMT  
		Size: 7.4 MB (7407084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b95980a81a9ebf191f57454a0e0e367ec6bc5e32f395f7b865ed2bfd1194c42b`  
		Last Modified: Fri, 27 Feb 2026 22:35:26 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ceca3e7f23741414152342d5aaf56a24ecb855a2766f88611dc7c876da2e1b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224120335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7bbca8c8038abf7ca591893d02b1111caab6f4b3f8dcd0fede8c60bb9270ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:49:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:49:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:49:24 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:49:24 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:49:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:49:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:49:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:49:41 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:49:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99619b629997e7e2d7c147c45be51691baf65f5fc75a6f4dd6e47ed8d9af9e47`  
		Last Modified: Mon, 02 Mar 2026 19:50:13 GMT  
		Size: 88.2 MB (88233824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a16180236f3bbbe1224b3e86f99f6713be13f440d4fc01f9d1b2fd21574fdb9`  
		Last Modified: Mon, 02 Mar 2026 19:50:13 GMT  
		Size: 86.5 MB (86530933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9be2eb5e8b58399a49a32b9b5b10376aba529c56204e413195ed7cb54baed4c`  
		Last Modified: Mon, 02 Mar 2026 19:50:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa483ca28cdc05e4da0f1d2a1bd1b9a3288beace1df9558096f874624dc6ec5`  
		Last Modified: Mon, 02 Mar 2026 19:50:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f2d3aa8b34c700fe8ee915c5bba29d326db23ca59118ad75e2cd23e6ee7e67a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a1219edefb88444f37fe5a6f855ee0842b7d0f3f954e42386a03ecc0e87457`

```dockerfile
```

-	Layers:
	-	`sha256:4ab57e0699140e2a649d6f8a864b0a72b1c333222aea1bd04b7f4930d362fe66`  
		Last Modified: Mon, 02 Mar 2026 19:50:11 GMT  
		Size: 7.4 MB (7419143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd014b61dea7bb88777730f065865b3c860aecb6b3431a39c94ce7e029046582`  
		Last Modified: Mon, 02 Mar 2026 19:50:10 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
