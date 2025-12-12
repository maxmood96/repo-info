## `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye`

```console
$ docker pull clojure@sha256:1e1060b7ba4f1f797b9372585b390cc04e3d8f113cf032c705175c4554734ceb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b083ceb30caf8441ce16d17097a303ceb2627a3653157f79d435e76e9eac82bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268162320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c40266213669b4edf2bceacf4350b4b001622a096e0229a413e70ba20809548`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:39:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:22 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:22 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e7a6d7e10fc8f1a18e936a13baa40b5b5a2fba407af1a51207223697993e44`  
		Last Modified: Thu, 11 Dec 2025 22:39:58 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154a37e976fd170093278543d705a1aca48d97ed2921ff802afc207cade73eee`  
		Last Modified: Thu, 11 Dec 2025 22:40:08 GMT  
		Size: 69.6 MB (69556920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2814acc425f33757d205baa6d995f83dce1caf535c19ba689b216c071e8485`  
		Last Modified: Thu, 11 Dec 2025 22:40:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e0280e7e4bc9d55d36e0b6d768109e310d1ecd7d7955e5ee84797476bcd924`  
		Last Modified: Thu, 11 Dec 2025 22:40:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c342cc310b63ee12014fb614b4b060bcaf01a60fe9f0ec4edc61d8e8ff9407c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1468ff2f44de02f3f5158161bbaa028e42b0fd9d40afd821610c31b988f8f4`

```dockerfile
```

-	Layers:
	-	`sha256:e57474228987c1e43d58c6fd92d643ac1998245e16f619df159145ed256da128`  
		Last Modified: Fri, 12 Dec 2025 01:38:04 GMT  
		Size: 7.4 MB (7395669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8579971271345891ff35707ea7e404c11027eede0bc0b27e6096104ec35bf8c`  
		Last Modified: Fri, 12 Dec 2025 01:38:05 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:887b1dd1e61fea8b21b89055c0a98ff4341c8b17f96b921499ca9f5eee277dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265625829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659d952ea412a9fe19c426026ed88e641ad5972a2af8fd92b62f0bf166cf60d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:39:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:14 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:14 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136b0ca6be80c6ee28769db2ee15dd28adab23e15693101158aeb8db3bc07d18`  
		Last Modified: Thu, 11 Dec 2025 22:39:50 GMT  
		Size: 143.7 MB (143679919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeb3889b36266523112fdd4337f92a89fa13c6763425787ceb5809174ca40cf`  
		Last Modified: Thu, 11 Dec 2025 22:40:02 GMT  
		Size: 69.7 MB (69687160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30712c0c9e57510fccebdd310ca19de498330c994afab7eba5b3ff0fb6afd627`  
		Last Modified: Thu, 11 Dec 2025 22:39:53 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a407922dcdfcc4145fe926f67fa7a6d24a025296da3d74429aab0ed19ebd3ccc`  
		Last Modified: Thu, 11 Dec 2025 22:39:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:420677cebe2a784b8a3ca72b0c88573f683e46b2c82f96d5ca2d4ae2012f30b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7356f7f46c81a3d6130a43891146db8e50c2e382d2a4149f0479301bb75f98ff`

```dockerfile
```

-	Layers:
	-	`sha256:f4457c439dede2fdbed4273b110cef3e6b231a8577162926e4b1410f47c3b05f`  
		Last Modified: Fri, 12 Dec 2025 01:38:11 GMT  
		Size: 7.4 MB (7400768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be360d5c9a9357ab47cab685cfbbcd18b89133d7d9df1c7fc9ffa77485e28a4`  
		Last Modified: Fri, 12 Dec 2025 01:38:12 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
