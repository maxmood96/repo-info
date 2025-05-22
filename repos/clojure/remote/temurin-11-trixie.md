## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:87056b5b669fab794c9040f547f08c874b9cb09070555c467588bead8555edb4
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

### `clojure:temurin-11-trixie` - linux; amd64

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

### `clojure:temurin-11-trixie` - unknown; unknown

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

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-11-trixie` - unknown; unknown

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

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8d9c795b6ddf59e3f14ab303a01085b2064c4c2d0439bf9b91004e87e24afc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276625493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05e66f4bbeb22cd90af6b0e7c392876347a8a12b77b2d121540fc6c16096281`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
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
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cae647bc37778358b907d22b7bf35eb9da015bfb7b8a8800a879a20173b410d`  
		Last Modified: Tue, 13 May 2025 18:34:18 GMT  
		Size: 132.8 MB (132809833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b624595fee2e9c5cc6b200917de575903a351bb8e157dcadbe4de1187bbdff09`  
		Last Modified: Tue, 13 May 2025 18:44:17 GMT  
		Size: 90.7 MB (90742462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925061405230820572745f5e9add62419103ce912ea4d03f2429ab40f50fd1dd`  
		Last Modified: Tue, 13 May 2025 18:44:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2e25556fa9b99226ae87a3699376870f257f994dcb44815e60a7a916cd15d787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7307222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdf1c46dacc1f7419752ae8dc0d0a0ac0a4b0d058f9232c1991bf9e2f07253d`

```dockerfile
```

-	Layers:
	-	`sha256:89bf8735cbb7ec79f59d5c2784b047b0e0b6143b0b9834e39b233158644a617a`  
		Last Modified: Tue, 13 May 2025 18:44:15 GMT  
		Size: 7.3 MB (7292948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe57ed7bac4d6542d792b35caebf8e6e858666d1f9617b237bc739c6be84fb0a`  
		Last Modified: Tue, 13 May 2025 18:44:14 GMT  
		Size: 14.3 KB (14274 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

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

### `clojure:temurin-11-trixie` - unknown; unknown

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
