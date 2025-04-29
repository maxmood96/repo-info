## `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:b4959fc210f88f3d634c9f583d7ab951c6c0560d198ae49fe97b88227f4e73d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:db8fcb7256b7399cc618abdbf275107c229eddf6876d996d4d7f08b6cab88f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213096179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e074dcb820ebb3112fc39e232c25d9ab32fb1a3249922ad2fd87f3ce6d2c20ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9422688b73396143d24133eac30773a2e9e6f4d221585795e30d37d25fbf1ee`  
		Last Modified: Mon, 28 Apr 2025 22:08:12 GMT  
		Size: 90.0 MB (89951979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a64b5e2c1a776b4472aa40a0830147b612722e2bb7fa4c221efd3cc2441259`  
		Last Modified: Mon, 28 Apr 2025 22:08:13 GMT  
		Size: 69.4 MB (69395423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bef49c7acdb6cce5ea5ea312d4d0cd0495ce9b207020a32e0e63f5e1460d33`  
		Last Modified: Mon, 28 Apr 2025 22:08:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefd71d4293a37ebbf0dcdfb8ee78c2ef7a53bc28d66265e95d383c74932f7c2`  
		Last Modified: Mon, 28 Apr 2025 22:08:11 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:01399991634a0068ecc741092a40eacf2b6d7fe0ed1ee4e80e5e30d4ccdf3a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7173015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb29250f54ca57d71da0483a5ce27ed4cc0bc86173819668c298640988b23ed8`

```dockerfile
```

-	Layers:
	-	`sha256:81d5529fc2ffbb2850f340b8ebd62e7a5ca2a548d4cdfb7784d962c54a313756`  
		Last Modified: Mon, 28 Apr 2025 22:08:12 GMT  
		Size: 7.2 MB (7157201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:453d46342066fd4d828264acaafc68739d5f55c6f9357610ea266574f012ef00`  
		Last Modified: Mon, 28 Apr 2025 22:08:12 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f22e1bb25c078c9483d71c996108b2df9d72d8d4fb3b918469047d351b101c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210875748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36cd6d1236856d1a317119c3d2394cc9f66a0330fb7e1bc4643b3e2cf7e710a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5aaf2cfcd971df2d03428ee5ee76c3c86e096ad694169897b6600599fa86690`  
		Last Modified: Wed, 23 Apr 2025 20:04:34 GMT  
		Size: 89.1 MB (89091269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66b0fe0a561496071832a1114e4f93cab7b74b4a6a0186734843db320c895a`  
		Last Modified: Wed, 23 Apr 2025 20:08:19 GMT  
		Size: 69.5 MB (69529212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96157ff52cd459477c5557eac0b7a3a77a2f93652ec7e0541fb6b53bbb71191`  
		Last Modified: Wed, 23 Apr 2025 20:08:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b073a7aae2cc032759f84335f97e241af101c25c02e0103271a71c01db78253`  
		Last Modified: Wed, 23 Apr 2025 20:08:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3816240f696e7a4d184d3c0919613920721a0779e5bd13ec6bd1460b3d255b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b661dbdbdff3842f78f38bc7242b42337db67f1372050929b8e2308271dacf7`

```dockerfile
```

-	Layers:
	-	`sha256:0798eba8d4ffed5ca334d0d7c840779492dba4e9891e6921b9d0110e072ff728`  
		Last Modified: Wed, 23 Apr 2025 20:08:16 GMT  
		Size: 7.2 MB (7162243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28c8e097960b644c89c5595ed2d034f9c14bc168022d5e69410d2b1407c13a2`  
		Last Modified: Wed, 23 Apr 2025 20:08:15 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
