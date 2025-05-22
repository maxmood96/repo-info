## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:4cdbb01a4d1bc8850b1d5519db5251cf043b78020d0d36f091b4d56811f7ec68
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ee87eb7f7db0a2356a024dc6b9795adbb28997d9bcdfbbb51c80090ad5926cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280142599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4455177f29ec89b130f48dd4e9f1b225e01084b21f279d9950d28e4acaf262`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d38bbd6b3bfeb82bdca2f48d6b3cce15fa7f70a9df67b07f66e4f17f1559a95`  
		Last Modified: Wed, 21 May 2025 23:32:48 GMT  
		Size: 145.6 MB (145635724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34ec304e46c8f96b60d58ef9bee541f1c1e9674f6eba591f019cbc77dff181a`  
		Last Modified: Wed, 21 May 2025 23:32:47 GMT  
		Size: 85.3 MB (85259322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6c0bf4cd58ce1cad411e41f57232b074f42217aa91f2ae5c7ad2eb6b42b715`  
		Last Modified: Wed, 21 May 2025 23:32:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:594434b90bc2f73d637d1bf0f604cf3b969c87e1f713bdc39ab1ea232c824591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a537a6db587795fec5f2b87eb5f7991b054adaf4597078a21dcda451dd43132f`

```dockerfile
```

-	Layers:
	-	`sha256:e52e6d10ae041cfa3434450b216afb553d5fe811c799da6db7105469031ea292`  
		Last Modified: Wed, 21 May 2025 23:32:45 GMT  
		Size: 7.3 MB (7338557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfef2bc01bff8ed4b2f05ec951a7046a1abcd588dcc42ed833998b691613eb67`  
		Last Modified: Wed, 21 May 2025 23:32:44 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8063b461d0c82e859eee6e8aa32e9e816747bac83e8fcbfda8bdfd1e50a2f812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277214897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab516b07f20ac5f880a3e584de5d419778eabd1d01d257342603648ed4a5af04`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Wed, 21 May 2025 22:31:07 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fb27b90b3828e5b95e6f507607ede8d9b516d361aa57b7d7bd47780cf9df52`  
		Last Modified: Thu, 22 May 2025 08:12:56 GMT  
		Size: 142.4 MB (142420737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b4c740d481bc7cf1d2cb962ab1228a851ed52db212c6b162a8fc0bcfcc0f0f`  
		Last Modified: Thu, 22 May 2025 08:17:22 GMT  
		Size: 85.2 MB (85175221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae5bf51efa6465c109a8e640cd5b844c50c521b6cabeefa4fb68eb4ee32d1c1`  
		Last Modified: Thu, 22 May 2025 08:17:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4521315609bf18b024f34d086171b3646c4ab03318d73b9a81a110989dde4251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fb8b5536537dfae29558ae169d24a01308968d61774191a9c03bdd669e067`

```dockerfile
```

-	Layers:
	-	`sha256:f60439b48bfe0d296ee6f517c2940d9d6138f434533bc312b3ad8a8927172737`  
		Last Modified: Thu, 22 May 2025 08:17:20 GMT  
		Size: 7.3 MB (7346205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f1128932af124ca833671175b8c6f9d6d09def700e5b45930e591149c26415`  
		Last Modified: Thu, 22 May 2025 08:17:19 GMT  
		Size: 14.3 KB (14345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b43e41fd20d93fd9553a9ffce9dc3c758205843841709d0da2a204d785b517d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276642764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56dad017c916e24aeeae55bae02d17c99b630e3d746857f49d42b914a89a525`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Wed, 21 May 2025 22:32:01 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17462e0f35311ccfe3eef0a2080d12ea66d12c8bc6ac23c78f9944f10acfc784`  
		Last Modified: Thu, 22 May 2025 11:03:11 GMT  
		Size: 132.8 MB (132809860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc03d193c9fd60856d0483c8594d77bce6741e79707c9ced1b81213f4a60d58`  
		Last Modified: Thu, 22 May 2025 11:10:47 GMT  
		Size: 90.8 MB (90751715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9361528a909b2ff18f5f58c92f3b7187c3ffd0178260657287a13074ad107`  
		Last Modified: Thu, 22 May 2025 11:10:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:702bd6a9de26246611694fa345ade9341a48513be2e13daeef25319d716ca337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7356635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0b9310ac617f7642e41c7b407f108d0167114609eb6fecca6e3c7c9bc68039`

```dockerfile
```

-	Layers:
	-	`sha256:2a4750d3381f8b3dd377584ba682336f38494b9157679337e3c4d4e392789421`  
		Last Modified: Thu, 22 May 2025 11:10:43 GMT  
		Size: 7.3 MB (7342359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dccd68dbb04f637e2d93fed27d8f0b72395aac3e517f36d5884d9756387d865`  
		Last Modified: Thu, 22 May 2025 11:10:43 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e777e484952a32c3670d6c00687688134ab8e1e02f01f8ee3988612998894e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261248907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf5d42726ce13fec5b3e75d16bab4ccbf864f294255c8887556ea867313b373`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Wed, 21 May 2025 22:31:46 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5926ae25fe9817c3fc9b51b369a326f72c3940aeb3cce1e885d54af89199e4`  
		Last Modified: Thu, 22 May 2025 03:40:46 GMT  
		Size: 125.6 MB (125585847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcc4c4268d75c982cc486b7d2a7f07c3b38f0755bbf2b729776ea25c4baca6c`  
		Last Modified: Thu, 22 May 2025 03:47:35 GMT  
		Size: 86.3 MB (86340189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eda0053602dc5511a5df0f305b5a0ceedcbc03f034a7a2c3f4792b180678b1`  
		Last Modified: Thu, 22 May 2025 03:47:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:61feb061ea5122402b4357afa3b5496cc54aaa7dea1b9e1d717d69178d8e8f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcbe049491254670257644a4c491cbdc8058858dd1c7b870dd36eb7196da582`

```dockerfile
```

-	Layers:
	-	`sha256:c4f41ca92f3d1dcd3ca17b2aab51e36a37b123264e95b75abf19391151fa58c7`  
		Last Modified: Thu, 22 May 2025 03:47:34 GMT  
		Size: 7.3 MB (7334483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55a380d81f2f2090e844f652621ac744231db8ada122e5fe8062ce1bbdd41f8b`  
		Last Modified: Thu, 22 May 2025 03:47:34 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
