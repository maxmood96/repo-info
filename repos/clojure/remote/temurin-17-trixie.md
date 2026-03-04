## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:d202e3ab94fdf8523aff21b2e0a7b489a87ee71c1017169fb7e902dd1a3aff09
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

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ca8c20e27a6c158491d4ee66182ec06e7aa13fd6b56bff35c695733697553665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280490076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6310f70e1047dcbf28a72a96fb4cefc7547b3f4e78c49177da1de71349de414a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:50:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:24 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:24 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8da55beef3d67028eec21992f2d6c46db468b4002e35e92d79a4684691d4cae`  
		Last Modified: Wed, 04 Mar 2026 17:51:04 GMT  
		Size: 145.6 MB (145628711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d383dfb753ff86d338fc9edefeeaf237c9c1e30b87b12a1e87c12d8121d9298`  
		Last Modified: Wed, 04 Mar 2026 17:51:07 GMT  
		Size: 85.6 MB (85567202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446a2cd9e80561c212b25cddf1cd7ba3122de1dded8a8c61a46b8f841f377b7`  
		Last Modified: Wed, 04 Mar 2026 17:50:59 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4fd80cc20b3654b74eb6d5b446a0690a6ebb0070357f1bd3f804f1aa9b0712`  
		Last Modified: Wed, 04 Mar 2026 17:50:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:20491d34f577de0db655a658bd89fa2483f9b390b5bcc6214db524ab0a63b878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66d88a96585e4e4e30b685053a9ff69fbcda956c1e732b8099cc6a9d3cbb31d`

```dockerfile
```

-	Layers:
	-	`sha256:c385955330a045fc9805cce54f1fe2b9593a7b8ce2a6fe7b1d50e476391f7b72`  
		Last Modified: Wed, 04 Mar 2026 17:51:00 GMT  
		Size: 7.5 MB (7470593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:621a3aab8a6d9fbcaba034d7bbe16dd7299775b9485f996c377b6e8fa303371f`  
		Last Modified: Wed, 04 Mar 2026 17:50:59 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c571748cf7ffce7316af81659e58369d353757664dcdd0c25ec406d2a73b8451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279472225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd14108e3d73525232b367ff339486a1e63cab23388cffcd1e1c198a8ebf8cab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:49:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:49 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:49 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360982e010405d53b72d6dc4d8059ad7d81c35614b335aa4a12268267214c1f1`  
		Last Modified: Wed, 04 Mar 2026 17:50:33 GMT  
		Size: 144.4 MB (144436197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1a91fc7564a0fe2a2f0d70c7f8d53fc6bbf7d03e43c452812b0aa55f317827`  
		Last Modified: Wed, 04 Mar 2026 17:50:31 GMT  
		Size: 85.4 MB (85382817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91643fe676a308f81f1f168616306575163961ca62372fdc9ef65c2a0a3fe9c`  
		Last Modified: Wed, 04 Mar 2026 17:50:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e8564e83f6c5e09ab0b59159c925f1292a8e8de7e17c49943b55c70584bf49`  
		Last Modified: Wed, 04 Mar 2026 17:50:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:28878bc5283c909baa1ab1fa550fbdc9b19ff9e618a37609642f0d726f67e160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7d8e03a83db16e38213a51a03943dbe42b21fcb8a2c979e9c9d6e2db543ae7`

```dockerfile
```

-	Layers:
	-	`sha256:2de11fd1d1bae043771c6f7b023bbb8bb7979e6b2ebfb8dfa7113cd775f213ae`  
		Last Modified: Wed, 04 Mar 2026 17:50:28 GMT  
		Size: 7.5 MB (7477623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8831a432bd4f89470193fd3db4cd8b7517821086ffb316aa4e57d1ae0b0d032`  
		Last Modified: Wed, 04 Mar 2026 17:50:27 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7b9fa3101eb448117f50926e022023380687f9911178ffb3dd9931f39f1a59e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289527882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c3be22a6a0b8518082e6a804093937879433d263bd3bfef8ed7484362acd10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 18:01:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 18:01:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 18:01:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 18:01:16 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 18:01:16 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 18:02:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 18:02:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 18:02:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 18:02:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 18:02:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2355bf75a71029ff93e07fffbb393969b2f288ffdd38f12d08439208decbc9a0`  
		Last Modified: Wed, 04 Mar 2026 18:02:57 GMT  
		Size: 145.4 MB (145438252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499915723f766d8151ad823d2f1897a273a32c7aabe788083d8ea0e6e29a882`  
		Last Modified: Wed, 04 Mar 2026 18:02:56 GMT  
		Size: 91.0 MB (90976325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c02427da69c14166969a8ac578e6f917ae32d2725f22c8540916948c811f51`  
		Last Modified: Wed, 04 Mar 2026 18:02:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db1065cd9ab2be064e6ff2e3716323ce7c274dd031b1d790b3f6f46d5c469f1`  
		Last Modified: Wed, 04 Mar 2026 18:02:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:919885301cd81b5ef83705636c9846d06496e2bf6c5ec7fb255c146d1242d441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710e5fe937885a2b88eb3dfc7de54f56229e860a9be1b43c69e6a99dab804de1`

```dockerfile
```

-	Layers:
	-	`sha256:a649a07406d47eeb3cb31764cdef2d3b7589b57e49e160a08820c9e6ef40798e`  
		Last Modified: Wed, 04 Mar 2026 18:02:53 GMT  
		Size: 7.5 MB (7475014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15f6b592f2a2b0954b94f195e819d48d0bcb694f2b02465880b171ff8150713`  
		Last Modified: Wed, 04 Mar 2026 18:02:53 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:2181b3b385599c7cf87b92c044f50715e74b0e22e7cc112f67d77d5efeb5e5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274880714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7610ac4451a4a727071d9e56d858a12cd817e12102e539652e1ef63005fb53cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 10:51:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 10:51:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 10:51:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 10:51:35 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Wed, 04 Mar 2026 10:51:35 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 10:54:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 10:54:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 10:54:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 10:54:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 10:54:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db99fe8e9aa791e3b0fe2b096e079a262bb09902b5d09c2085e34c6f29398e4a`  
		Last Modified: Wed, 04 Mar 2026 10:59:51 GMT  
		Size: 142.7 MB (142662998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4b8f0a23724cf8c6ead37582d4e0cb1f3383aeabe6eed6712cfcfaec15d026`  
		Last Modified: Wed, 04 Mar 2026 10:59:40 GMT  
		Size: 84.4 MB (84439738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eeb521fdf83ff6e146419994d6909bc576614fdbd8d1aaa9e14d01324fbad7`  
		Last Modified: Wed, 04 Mar 2026 10:59:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de82ca7c25a767f0e7357e3c95514a6e4e54287e198a2a89048055e2414f5d3`  
		Last Modified: Wed, 04 Mar 2026 10:59:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:53b8f3633812233699984521b27bc580f9016a963c12f3e6c53613d1d60a34bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7472391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e69a9e075729ec124b6a04e98fc30f49a28cd8763ccf6243f28654dcf62b4f7`

```dockerfile
```

-	Layers:
	-	`sha256:e76c6e9514e56eb87bd706000e05753e334d7184cbf20d31732a2e005126079b`  
		Last Modified: Wed, 04 Mar 2026 10:59:16 GMT  
		Size: 7.5 MB (7456589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:920772677d70c530777738391be919d43c20023ce0faf89eaecb3f1931a01d5d`  
		Last Modified: Wed, 04 Mar 2026 10:59:13 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:7d0781620a6457c0ca07c2d89a6204d63c42b50b85ebf0bc7df89f81b424556d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271512516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1bc1394b11dec12f69e3e49c720b75717cca22feeeede1ee6da35cb34f935e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:49:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:15 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:15 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:49:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:49:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb908934144b1126e1ccdbf4b1fa1fe673d980c88d80d25018cad0ff60a3211`  
		Last Modified: Wed, 04 Mar 2026 17:50:05 GMT  
		Size: 135.6 MB (135627121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a968e5b5dadd828f4a0e45812436136d4b0ebe02e568f811bf7c58ff8eeef058`  
		Last Modified: Wed, 04 Mar 2026 17:50:05 GMT  
		Size: 86.5 MB (86529820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d42a0c13c4b14752b37e32852474afc81f6920f8ccfc87539c3b5106b311fdd`  
		Last Modified: Wed, 04 Mar 2026 17:50:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a44485278f79b1c38af87555f59bc434a910e9634a3f7fe71421490400ec74`  
		Last Modified: Wed, 04 Mar 2026 17:50:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5d553fac32a3c03a26af6e8af90a60579e1e242f3cb1878898cc3639a4725c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900aa72d472a1311b675443f44c5d683bcf849485d3af7c21e8294bcce8f7531`

```dockerfile
```

-	Layers:
	-	`sha256:d54c277a698be98a321b7ce844503f5fdc6bfd63b019cae04775ccf58e3f9bbc`  
		Last Modified: Wed, 04 Mar 2026 17:50:03 GMT  
		Size: 7.5 MB (7466515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b54d0d2f1f37fa9cb03b149830642e17fb097e24cc541c4f687f8d1c551d9e`  
		Last Modified: Wed, 04 Mar 2026 17:50:02 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json
