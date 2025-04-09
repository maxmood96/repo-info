## `clojure:temurin-24-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:ebaa021fdcc32df1f6364d320950a0c372709d18e7246719ea3c5d3061eb0b75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c8df81dd4865831f8d7ea71203d6f54aad6666c734bf83e0a9014a4f86d51543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187705754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a5fedb483a748ad400b6f143f0900a4538c9eb7cf0ee5852603d1554e892e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fc9975e7fad3704a55fdf6228e858326023062a058bb7a21c728ea0a2963ce`  
		Last Modified: Wed, 09 Apr 2025 02:19:34 GMT  
		Size: 89.9 MB (89949048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59f9cfc8574e19c854e35cd4ed1dd5b251ffbad6403fb502c2a4a7c6f96d3cb`  
		Last Modified: Wed, 09 Apr 2025 02:19:34 GMT  
		Size: 69.5 MB (69528408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d275276ea4a71de1e63bd564ad6224bc3b8b66555fe6ed53cd95b46634ddbde`  
		Last Modified: Wed, 09 Apr 2025 02:19:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2c7dc6b18248ea62414881195358023ad48e6740d295a3441cdb33ef12c022`  
		Last Modified: Wed, 09 Apr 2025 02:19:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:78fc938b5eae3b26323c27e5ba73b32b5cc62e3d289770ffe513289f23d90272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a57c1aaa9a62faa0a89de749ef57cf86dc930aeeb3ec01056ce74452cc58b6e`

```dockerfile
```

-	Layers:
	-	`sha256:abcd8792187cae0796e9d148432b608b358f095866651b5b1e94e5a2775513df`  
		Last Modified: Wed, 09 Apr 2025 02:19:32 GMT  
		Size: 4.9 MB (4864597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8bff64013ff04ed64c702d64aabb9c88ef1426638e9bc36031ad995c434d0e`  
		Last Modified: Wed, 09 Apr 2025 02:19:31 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:40040e733821c2b256ad5ef2af5f1380d1acf5561e9c62eb7423ac4d7e86f3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186537959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6065f68a17cc4752653e6e56f965a88cd78f2fdb3788496da453fd80170090ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e18d2baa19d8ecbec452c63857469775a49da49a6ee666e57c904c334e09651`  
		Last Modified: Tue, 08 Apr 2025 11:37:59 GMT  
		Size: 89.1 MB (89092706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8b72610d2e24e47ea16af34788db18c5f97f49058558de1c29ee337e209be1`  
		Last Modified: Tue, 08 Apr 2025 11:41:00 GMT  
		Size: 69.4 MB (69377892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a07018a3c75cbf8ea9f5cfd09ba3fea6edb6b5118709b1e295bbb8229a4f22`  
		Last Modified: Tue, 08 Apr 2025 11:40:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95eb54552fa92d97cc71cfa2f7299852941f06e387988b412875ef3e0fab6cb`  
		Last Modified: Tue, 08 Apr 2025 11:40:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c138311dfa9d48bad946d9ad48526fd1040c9b57354439d560e74b26c5e6911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4886345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314b34c555019f89dbce7c66b51d38cf384d8219f66562ae62615ed371cd676`

```dockerfile
```

-	Layers:
	-	`sha256:4b53d5a1cf6d1c9f10cdafc33e97a1d2af8eedacc0174513f63569a15fc2f82e`  
		Last Modified: Tue, 08 Apr 2025 11:40:58 GMT  
		Size: 4.9 MB (4870355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444cafef7da568f8a6a77469d4c7b32774a68a6726a2aa3f45e8c77e2fb77826`  
		Last Modified: Tue, 08 Apr 2025 11:40:58 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
