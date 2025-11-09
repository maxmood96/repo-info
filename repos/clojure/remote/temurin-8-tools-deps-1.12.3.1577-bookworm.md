## `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:33641942ded0789e9d672bc757dfc3d89f939671320679abfef68867e137431b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3b2edce1ba6e6a4892f3ea7b374180252785a9d447d017ce8e8a516ce8fadedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184362777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e50d46e3ed4e19266a04fc22e011d99b5387b50b75d11f7cbe86bc861d0e837`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:04:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:04:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:04:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:04:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:04:15 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:04:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:04:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:04:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6f0a62d2627d070b81f8ce8f2568511c8a25c37c457133fda50072866b059a`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 54.7 MB (54733360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315bf4e878a447919c3c5fd760727588c8730afd3c26d9f238bb69dab8b0f70c`  
		Last Modified: Sat, 08 Nov 2025 18:05:05 GMT  
		Size: 81.1 MB (81147715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2dd23dcee09f23dc099062a56523fb34ed5272240cc2d19dc209cd227b31ae`  
		Last Modified: Sat, 08 Nov 2025 18:04:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:11973a1914a9c4d3e49025f779511fc0b02bd59502f9dc5af0092cc6688ff739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc5760bacf6db5970330a9cad43bc7a4235e152803aa1b0c717b79e0110868d`

```dockerfile
```

-	Layers:
	-	`sha256:c90ee0d3099074da4e73662574a10f42f781450093c6e0131e4ab1bed96dafee`  
		Last Modified: Sat, 08 Nov 2025 19:37:36 GMT  
		Size: 7.5 MB (7496500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8df40904b33324254e1c5437b57ceea29fb84aa7d35617435ac05b5292b9217`  
		Last Modified: Sat, 08 Nov 2025 19:37:37 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8c22ceb8e3f0b74b63bbdd99f8f9056fe82b8ac9c2f6454a98be6264c1225ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183206284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0aaf28d0d67c525af8ecf08c24cd7404bfb5876c1d9e46f421f00ee2430660`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:03:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:03:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:03:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:03:28 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:03:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:03:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:03:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d65e2c645922bca495cc09b41e5fb6607a461cc075f841130727e1fe1abad97`  
		Last Modified: Sat, 08 Nov 2025 18:04:25 GMT  
		Size: 53.8 MB (53815043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f91976142da690d48e2759b697107c085275a632caae6714757632d8b69369d`  
		Last Modified: Sat, 08 Nov 2025 18:04:12 GMT  
		Size: 81.0 MB (81031117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bd79543eea0be5fa29d81e8abb22af7755b0570ffbc30a5eb091dcfb15e570`  
		Last Modified: Sat, 08 Nov 2025 18:04:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fc0cdd40733ff1537888288e74e9a2d1df6d790acf88fa1e46a46f834ebcaf9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0d90b5fb2ba12377f337ee8e452f1fc076f509b02c54656a429c4424b1bc75`

```dockerfile
```

-	Layers:
	-	`sha256:8abf0991d0519e8656df2a791dba1633464ca97cb6d79881d6be320de350c2d1`  
		Last Modified: Sat, 08 Nov 2025 19:37:43 GMT  
		Size: 7.5 MB (7502961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63529da63af3f266faebe419fe23be0fccedf3edf9b2896bd67faa448173c84f`  
		Last Modified: Sat, 08 Nov 2025 19:37:44 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:13f07fac92a870a34bebfb576a27c23e146aa2d940fd65c636716fa8d2c62f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191489083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa7726e0afd58efc0c8a1e2e245a20f394fb75dbe23ee9d4cea8aa2ab1eb70f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:07:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:07:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:07:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:07:13 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:07:13 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:15:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:15:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:15:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d32be4fa3f3f6cb4472d405863e8c9515baaef78e3e54ebe7c4f01ced5fc4d`  
		Last Modified: Sat, 08 Nov 2025 19:16:12 GMT  
		Size: 52.2 MB (52175124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65204b4ead1c81678cd2d4ff6ec14d8aca8ffcf14189cc01065d3bd28178562b`  
		Last Modified: Sat, 08 Nov 2025 19:16:15 GMT  
		Size: 87.0 MB (86986035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4485a3f68c0cd7527310704381bb1b915f1eb1fdcec8c157a2f2ec85fa84502`  
		Last Modified: Sat, 08 Nov 2025 19:16:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fd43419ff2ba6dade51691877641305d2fb87af8fd0c846a9c46694caf2ab58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215573f3571c4c6e3dae64c2c0cad0b292440a06dd2f95e96d2069ff4f1381d3`

```dockerfile
```

-	Layers:
	-	`sha256:ab684f0ce3ac36bcd680b0a9ca0cba2d2919216629fdd31e4966b2ca08a971f7`  
		Last Modified: Sat, 08 Nov 2025 22:54:09 GMT  
		Size: 7.5 MB (7502307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b1e9d35799d6d837878d2ae4f3e7d2e7da5f4755ef7b4020e2ec5281137edd`  
		Last Modified: Sat, 08 Nov 2025 22:54:10 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
