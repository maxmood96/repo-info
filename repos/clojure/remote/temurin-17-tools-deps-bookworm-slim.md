## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:9fb75e76c83d2238d3f13075d4ba0c8c8f104770e2f629f4a90d5c4689b3dc89
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2fe3bd0a2459bc632edbea3eaea0cb709960c70b4cbfd46006b0bbeee3e3af9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242754442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5721bc2be137e3b78effd2b7b1a1c4591a33ea2fd409e941cba9b27595043ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:54:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:54:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:54:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:54:43 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:54:43 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:54:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:54:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:54:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:54:57 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:54:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3789c028cdaa9631727628c673bb60537cc9b61a194c369ea45a52e0abb76ca`  
		Last Modified: Fri, 16 Jan 2026 01:55:18 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4652d108bf79e80819fc95d24aedf9a84fc74668663c6d520d05964aa303ac0d`  
		Last Modified: Fri, 16 Jan 2026 01:55:16 GMT  
		Size: 69.7 MB (69676884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6d2043c747b2e6e7adcc05e724c32f1c6100780222cc39cb4d199118014fc9`  
		Last Modified: Fri, 16 Jan 2026 01:55:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45cd510d996276c8c569d3735f94634d2ba0a3f2559ff7b46a0d52c27c924cc`  
		Last Modified: Fri, 16 Jan 2026 01:55:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ed7a1f8a2acca06b3a2fa03f50ec6d5ea1175a47bd7ff30c228fa217ac1f136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5508ecb57f569a4b0aa86be4004042b9f5041b5e9e12cc97c6bb1d0acee63e67`

```dockerfile
```

-	Layers:
	-	`sha256:abdeb28c4e6b4146d4aee99606eb95be8f4b6fb480154b662187aca3aa04755b`  
		Last Modified: Fri, 16 Jan 2026 01:55:14 GMT  
		Size: 5.1 MB (5113400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89ef7f662e1283c5847a1a027e8968c01d5da377dc36ecc3059225c073753af9`  
		Last Modified: Fri, 16 Jan 2026 01:55:13 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2ceea4a341805113c33117c4276e346b4704c3054f1870b2aeaba91922f10f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241461463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769a819ef8e3b43c2acaaba157e53a08d6de0616acfba23a9f8d2476e648aedb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:58:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:58:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:58:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:58:38 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:58:38 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:58:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:58:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:58:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:58:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:58:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f6bc05c68c69be12e1034738b0bbb6cdd6107d7f32d2d21280a82671ae520a`  
		Last Modified: Fri, 16 Jan 2026 01:59:17 GMT  
		Size: 143.7 MB (143679919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f87b39a5fe1523e1bd0e288d9a4257385811f7cf41c7b8deb07ef37532ec9a`  
		Last Modified: Fri, 16 Jan 2026 01:59:29 GMT  
		Size: 69.7 MB (69672614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981e05ac78cc92d8b9a4584c2ed8e050649185b12ed2fd2102034a3091c38020`  
		Last Modified: Fri, 16 Jan 2026 01:59:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858a3c8abe9d1976b1785c66d31b803c02e7409eaddc14213031b13cf6d6e593`  
		Last Modified: Fri, 16 Jan 2026 01:59:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ce8d72fbb7cd1d3f2b0afb150d31f015186cf933fa7ff231f48e26d338a3405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7107a2a0612dc13de164967afc713b9fbe39e508c6bd351bd71eeb34031afcd`

```dockerfile
```

-	Layers:
	-	`sha256:2f193dd8825202d37c59d06998dd46a48dced4223dd85d105b47c0d214c21710`  
		Last Modified: Fri, 16 Jan 2026 01:59:11 GMT  
		Size: 5.1 MB (5119161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ce58e239d62aa020b538051f3c63d18ba91d6053bfececbbaf6251abdce15c`  
		Last Modified: Fri, 16 Jan 2026 04:40:58 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0e870e006c1231a00f123ca7ab83c1e008a8d443852a54fe9aa035511f437bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252107155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f895a2f91872a6342b6dd3139bf55af2cb2d8fe0981214cf4b839210297320`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:12:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:12:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:12:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:12:14 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:12:15 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:20:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:20:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:20:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:20:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:20:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59571788fceb185f89ae2134067b41fea4b2a91989cd4404e661c3dd827195b9`  
		Last Modified: Fri, 16 Jan 2026 03:14:22 GMT  
		Size: 144.5 MB (144524717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116cfc5a042e1608b7b47ed47b0a3d8438ea294ccb0b77ae2f38567baaca2607`  
		Last Modified: Fri, 16 Jan 2026 03:21:35 GMT  
		Size: 75.5 MB (75512686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43923da7126e89fa19470146d5a908310fe126b086eff16c23ab977c772ec7b2`  
		Last Modified: Fri, 16 Jan 2026 03:20:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7835984fb368304728f89b804420da19de603f1024765638a29a71785a0492`  
		Last Modified: Fri, 16 Jan 2026 03:21:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:91232cad3c143259712c726bcfda8ba289f9e9e9eb8b595e3c7b0ddded1fd230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25f1ff0dfbd79236793e3c097328d667b809fd295121b1a78e72061cb59ee45`

```dockerfile
```

-	Layers:
	-	`sha256:36a99dc3ad2b17e1b42b0e4f269c3f327f92ffd012f8fc51a437f20e97ab431d`  
		Last Modified: Fri, 16 Jan 2026 03:21:00 GMT  
		Size: 5.1 MB (5118558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e543c939c4ea350e9f38fa1a6e619c2d4837facf699b6ec8efed939d73931525`  
		Last Modified: Fri, 16 Jan 2026 04:41:10 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d1b33fcdf6a165f76cbdbdb04186c7031f52ed256002cddab06e111d19de452e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230233920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ff33a70d1008b2de4421767688434ece1e57c03766279714a1f5de15909368`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:16:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:16:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:16:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:16:04 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:16:04 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:16:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:16:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:16:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:16:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:16:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:08 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aab18a387fc18c5b933990f24aae256bef846e7ea7b8f21dfcc273a36931821`  
		Last Modified: Thu, 15 Jan 2026 23:17:11 GMT  
		Size: 134.9 MB (134859759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a977f7e9bd4b1c33865a53bdc34245ec4bdd6cabd4672876e5cad38f7b4178`  
		Last Modified: Thu, 15 Jan 2026 23:16:46 GMT  
		Size: 68.5 MB (68488703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c650ee5b9a379f2ec8d2fd833492b4102d05ed49ad036b806244326863108066`  
		Last Modified: Thu, 15 Jan 2026 23:16:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dba86eb4686f786f75464d09d1641ec66fe83756c1fb285d9dd52c006c87f1`  
		Last Modified: Thu, 15 Jan 2026 23:16:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2bff09fe07642b10beb3aeff3ce13acfd4b5ca85fa4f644fdbd09b3c84cbd2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7f6a4229e39128720654e270c21cf325b41b94cbb3077a71d0918b12ff7bac`

```dockerfile
```

-	Layers:
	-	`sha256:0045b175db66e763168c38f2d0bf9cb6b5040e7bd0649999e5bd81a9801ceee3`  
		Last Modified: Fri, 16 Jan 2026 01:39:03 GMT  
		Size: 5.1 MB (5104721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d3aecb7a9007e4523d1ebfb546953ec9a675a52d1316fd3d3bf08c6ad89ceb1`  
		Last Modified: Fri, 16 Jan 2026 01:39:05 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
