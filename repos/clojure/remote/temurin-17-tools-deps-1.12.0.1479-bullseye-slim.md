## `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:5114cfbe7dc44fdfc7169a796acac98da3e9dcfb6edd7635bd1ad6753d90ba94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4eea9b48dd5693ea6fb3f3705b9d19a5e6006ff1b01b7de179a39e562fed904b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233546543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52de18e022f93f7ad04313d880cf1ef18ecb4325848f49cf621e60babdf0475f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e81c45a1381f1b13fb99721e6135efc8f438bb50685df2541797ed6845134bc`  
		Last Modified: Tue, 24 Dec 2024 22:38:13 GMT  
		Size: 144.5 MB (144536674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc96d6f9c57489ff28e14b6a46439f321fa65238d876f8366bfdc83d63f45e`  
		Last Modified: Tue, 24 Dec 2024 22:38:11 GMT  
		Size: 58.8 MB (58756188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825ecdfbf9d9c6575d4461be5b2bec318cc6ac09e5065b986fa2204b30257b56`  
		Last Modified: Tue, 24 Dec 2024 22:38:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4985d479ff3fdbe74c080d082abc04f93197455711ffc11023e5672f86272d`  
		Last Modified: Tue, 24 Dec 2024 22:38:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6ac91f1d5e6056963d0f6e11e8a85cbd9d4380165183200c0c8f3344b4ce47de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6aaff449e92038ccce35ffc4c218fabed2ba426792f42e2979e8675f3131f8`

```dockerfile
```

-	Layers:
	-	`sha256:eca6f1363ee2dc80ba0905e208c17b19b9ccc20b90bc37302cce21f4fbf578cc`  
		Last Modified: Tue, 24 Dec 2024 22:38:11 GMT  
		Size: 5.1 MB (5117007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:557add435ba0713900cd90d8dbeaa4ace8c415ede99ffbcd7386da2acf97c4e9`  
		Last Modified: Tue, 24 Dec 2024 22:38:11 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8197d9f02f3774a1a2de446ca17546d961ca36381b5693d3a9ecf19bb10d575b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230987204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64182b68d86a9b57d4684e9459f0fd1153df4f1585e634f7e6860775b4d7963c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bfdadce1216dd298f1b476897a36dc506dec08d9613ab2d5e49cd1a5534d6d`  
		Last Modified: Wed, 25 Dec 2024 02:14:36 GMT  
		Size: 143.4 MB (143361000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc70f5e65c7d14963fb350cfec6100cae3213af050782e048165f1abc0f3bcf6`  
		Size: 58.9 MB (58880317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34acee8102ec9c7252114405637ffc7e78ee780083b78f246dddca0d05f0ef7`  
		Last Modified: Wed, 25 Dec 2024 07:29:57 GMT  
		Size: 608.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9579391e6c143448c201923dcfb04f32552131511c800dfb54987689e3ae58e`  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:76d3de87845e2c8b7df26468b2f2e6c1391bbe115c7afffe45b1ea0312412d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2284c444648f0a98d8f27d65ae4a85f27cf899a48effa1268c77c104f894b61`

```dockerfile
```

-	Layers:
	-	`sha256:0074147d316be56a207c9ca36067e2ea5e51c0dde95d103377dcd7968383acfa`  
		Last Modified: Wed, 25 Dec 2024 07:29:57 GMT  
		Size: 5.1 MB (5122739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30941fc487e89be0b377df714a2d9bf3054d47d3fcc48db368ffc3e3d44c6a95`  
		Last Modified: Wed, 25 Dec 2024 07:29:57 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
