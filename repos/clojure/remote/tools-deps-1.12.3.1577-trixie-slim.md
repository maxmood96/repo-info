## `clojure:tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:f607eda241469d3c1de1133f55a7d4d405dab98c7fc9d0e13de1a7ecb72ac1db
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

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:57fae00f615e5e3e12b01c1afa7a6bc3f8f5af5362c4347230addeecfc81cb31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193809881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a36bbc1e76768c2f2cf3f84be3ec45a49034fe6a30a344f803eb25250bccd5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702edf5d3cb7972e67b788dbf401153dbceb2945a95d9d668009a8176118fe83`  
		Last Modified: Tue, 21 Oct 2025 12:26:35 GMT  
		Size: 92.0 MB (92036032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bf3ea196a721ada033cbe2c148e9d8ebeb638147f94e81f0ed5dd50b0f4187`  
		Last Modified: Tue, 21 Oct 2025 12:26:33 GMT  
		Size: 72.0 MB (71994887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3112c96b3bfd79f3918d177653ed24b73043a0b8347461628ecc7323a23346`  
		Last Modified: Tue, 21 Oct 2025 03:12:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b5b942a12b7922e6ef639a25868f161370680c13cfa65f5e232dfc446fae82`  
		Last Modified: Tue, 21 Oct 2025 03:12:43 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e98d4ee8bef30467f40150b05b2f09030076171e1fc19aa74ce24b8a95685614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd64583224d9956b8784b964bd111f96a9c0b1a80d42b8294f5035fa9ef7cbe`

```dockerfile
```

-	Layers:
	-	`sha256:8a827c1ab7382c5b44f40bcdc9bc3d03a07c104cbcdf366cd5f7f3fd593e442e`  
		Last Modified: Tue, 21 Oct 2025 09:45:34 GMT  
		Size: 5.2 MB (5207505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85513f0123c32f8b429ee478f1ee3fc9d483ba0903e3b02b9e7e7574a65e0a3a`  
		Last Modified: Tue, 21 Oct 2025 09:45:35 GMT  
		Size: 16.5 KB (16535 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a765d377c5f1d5fed2bbb9575ba19bef5818e782155eb9ec8be9ee357ae3e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192996758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c2e26b1618089813daca54887658c67b1b8a40c5aa9a71e9bea6128d60418`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14a1c351e842604951597002745a987731ca761743a4f9c6166233489b739eb`  
		Last Modified: Tue, 21 Oct 2025 02:30:34 GMT  
		Size: 91.0 MB (91045273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b07606de4ba9b71519b5bdc555a555b30376f09b73ade7468743ff1defe58`  
		Last Modified: Tue, 21 Oct 2025 02:30:29 GMT  
		Size: 71.8 MB (71808319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b38e91d0a44a2711ef41184409c5ff2f6afeb35c886e3f6e6cdb2139c053ff`  
		Last Modified: Tue, 21 Oct 2025 02:30:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f73bc9f10fe3e00b2cdf3a6b3f2871bb8cf8ac769ddd72e94e755f67a70918a`  
		Last Modified: Tue, 21 Oct 2025 02:30:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:17040935296cade31fee2e424c7487ab847dd772bb9b3576d5477914e79499ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4baa54b7d0928aa467969b67a3eeecd9dfeed730c77235bc6ba05d0577dc26`

```dockerfile
```

-	Layers:
	-	`sha256:e121a2bc64b03c8c7646eda58cdf428836c718fdaa1cc044aaae2aafaec4da62`  
		Last Modified: Tue, 21 Oct 2025 09:45:41 GMT  
		Size: 5.2 MB (5213295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:076af747c59d415e8b95e94954fe9c42c7f4432f2ed0b7e0394e5df8fe014a95`  
		Last Modified: Tue, 21 Oct 2025 09:45:42 GMT  
		Size: 16.7 KB (16677 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:08914256cfd1dbf2626eb3d93a29be066cf9e8a6c34165725f0a480899362f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202595406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58cebb9282c344bb09e246a0e13a135477807903f9244033c8e50652faff151`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673d315aed8718d3c9a70f343a38b3eaf84c29764337879eea3fcbfeccc112a2`  
		Last Modified: Tue, 21 Oct 2025 16:21:40 GMT  
		Size: 91.6 MB (91601696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db47e5443dffcad53e863401182e3a1e1c119f9403c542ffb57118a18931ff4b`  
		Last Modified: Tue, 21 Oct 2025 16:28:58 GMT  
		Size: 77.4 MB (77394152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36ecda0d65946ce30e3772af6337323fe50e82e055257b430ae77f1d23d9e6`  
		Last Modified: Tue, 21 Oct 2025 16:28:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940734b0e9409244da0825349969fe52698b7a77b2076407798db1ae8c315724`  
		Last Modified: Tue, 21 Oct 2025 16:28:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:35bc2e7f1defb2b15ab2a76f9e65b63dc514baa26fc3e1163565fa152a900bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8652b24ff765791563d7c6af09ebd5b97b0055132a9866b10ab278eaee71e98d`

```dockerfile
```

-	Layers:
	-	`sha256:4eef40ed6e07086544cbf2998cebc6410e8e4e6272a9bf9fa77b1b0740db8b45`  
		Last Modified: Tue, 21 Oct 2025 18:41:32 GMT  
		Size: 5.2 MB (5213186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc089c8e43149ca55bf1ed6aa19d7faa88aed276cbab762df706cdcd9b66026`  
		Last Modified: Tue, 21 Oct 2025 18:41:33 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:5b62dfec7812e1fa49ec685fb5f6afa1f3b508fe071954e6c51193c21437931e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192517489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238d268723368a6afc72e59054470b1936188bf2001108839034bb70b37f81f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e79c438abc7d333e712a0bd587c84f6fc3311ddd7d7911438fb6932d59c8e2`  
		Last Modified: Thu, 16 Oct 2025 08:58:29 GMT  
		Size: 90.8 MB (90752401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832afb67bfce080fcbde81a133f68034515dec6c6a5196ddfc46bc6a2b98345c`  
		Last Modified: Thu, 16 Oct 2025 09:19:28 GMT  
		Size: 73.5 MB (73488543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fa4d6ca0494de1558960b80303a693a2a243912927ac35e4444b49eef2a396`  
		Last Modified: Thu, 16 Oct 2025 09:19:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a527a95a8206623f32ac7d62d98b769d8ed4369a8ce66c9b92b42fa6068dccf`  
		Last Modified: Thu, 16 Oct 2025 09:19:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b6386f137516c338ce6ebc6fc134650251e1bf64ba16e824febe52ae2afeaaa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e176873f73d1a3a25f5983d992b9bae5d046a89fc7eea66a7f4b6e932efa59cf`

```dockerfile
```

-	Layers:
	-	`sha256:6d04a5ea74004ab77610638757e0e1d275ea11f59c01b88f92cc57548815725f`  
		Last Modified: Thu, 16 Oct 2025 12:36:51 GMT  
		Size: 5.2 MB (5196978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b31c5739f7e2d88da3058e8db6f5e0355fb2b9f64cffa20d853232d5059d527`  
		Last Modified: Thu, 16 Oct 2025 12:36:52 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:33a4dc9b7c97797793862a1607edb20e13b9b660395076b039cca42f77b899ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (190998182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1527b5f05ca0006996d308a72f6dd06d706b96f84bb8c7cc9e715587b1f754`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29722a94c5326270eeba3670d3d5df4e7037067570c7bfae78a5379a8a598fd1`  
		Last Modified: Tue, 21 Oct 2025 22:44:56 GMT  
		Size: 88.2 MB (88206399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe37c950714791ee06c1390847a6fe128cef11316cb96a5e0fe39483055f1bbf`  
		Last Modified: Tue, 21 Oct 2025 22:49:28 GMT  
		Size: 73.0 MB (72953485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76169bb5b949a6c3dc0c33af9825ad5dad8bad22d6939e3bc1ed2eb5b290a156`  
		Last Modified: Tue, 21 Oct 2025 22:49:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3312ce13b7c6a9655b9f315af1ebfe5047e31bd1829537200d5b69079b57cb9`  
		Last Modified: Tue, 21 Oct 2025 22:49:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e74c940923f6d7a6ca6b9e1ce7150ea17658c320bb8e082e1393278a8907742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0fd367f39ad55d28725c3e0e149a21d7509517de68c18a6ccd6408d603f733`

```dockerfile
```

-	Layers:
	-	`sha256:f5f49008ddaf2a1f7d300135b40f2eb237fb78a7e483b6f764f08fffadde8abe`  
		Last Modified: Wed, 22 Oct 2025 00:41:24 GMT  
		Size: 5.2 MB (5205977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8ee1d1e5593df43ea59ff318bab15ecf71df80847a471d9e0fcd9a988e5675b`  
		Last Modified: Wed, 22 Oct 2025 00:41:25 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json
