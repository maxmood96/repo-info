## `clojure:temurin-25-bullseye`

```console
$ docker pull clojure@sha256:ecc86708e02e2c63672706158fdefc4c1fa0988f662ad566982d8ce3243af36a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3515508b9d591c1f9365241ff7a692f5b7138523bc8d9b44ebcd63c6ebe58e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215364224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb50c1c2a924e8956c11e561ba95a3ec6b8ff20330ab4c09298b12cde680ff1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:56:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:23 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:23 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:56:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:56:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa7251cf4bc9092743f68c7cdfbc15de4931aa2d983fc67e1e4af18fe2fe3fc`  
		Last Modified: Fri, 14 Nov 2025 00:57:18 GMT  
		Size: 92.0 MB (92045287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4089a1aa2d4f05ba44fa53733d3534ea24480031825949bf7485b2408484d0fe`  
		Last Modified: Fri, 14 Nov 2025 00:57:14 GMT  
		Size: 69.6 MB (69561204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222ed7fa0ad0b0ab3985a222232ab9d67663d97714da4f88e5b93dea5d0a6647`  
		Last Modified: Fri, 14 Nov 2025 00:57:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fff2261218bd37a8f22eed094f972831d4a52046b564447e8948b3e5b8b44f2`  
		Last Modified: Fri, 14 Nov 2025 00:57:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ef8094cfabeb89d07f5174e0c219b3e21678aec113ea24f21a8e830be8ba3b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473fa6271011cb2780529751e2a173cd6640f83d14d31add374bde5b9f502a04`

```dockerfile
```

-	Layers:
	-	`sha256:7d2b7c102e107dd86e56065d5da672d9e1d633e97dd035cfb0a405079412b102`  
		Last Modified: Fri, 14 Nov 2025 01:48:10 GMT  
		Size: 7.3 MB (7347007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b4646eeea0a50dc655b0ba3e84f6245b493faae04047c1b7962b71ba650622c`  
		Last Modified: Fri, 14 Nov 2025 01:48:11 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:25f86623d4e11ed00c315c86257714286d275f0d9e924ac4a2e9b0646a5817e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212999904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdc0ee7d4e735f623a4c7411162b3eb8661042f6f80516401dba2fe08eb2e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:45:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:44 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:45:44 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:45:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:45:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:57 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfbcbc7b509bf0ecbeed57138f4131fd53b82f2e100c24d267c3ff9050d7442`  
		Last Modified: Sat, 08 Nov 2025 19:56:07 GMT  
		Size: 91.1 MB (91052503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff80785714e75b1a84cacf5d13b78b1b5d506fb1c926b2b73d9790a00e238fa`  
		Last Modified: Sat, 08 Nov 2025 19:56:08 GMT  
		Size: 69.7 MB (69688389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43e6eefd8919e9bbfa47f1c1956c207b23c81fb21b4bdf9ff26cdd668514067`  
		Last Modified: Sat, 08 Nov 2025 19:07:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6517a9bcf6f5791067d085a08074bd3f1f1c8bdfc0e5a94269264dfec89057e4`  
		Last Modified: Sat, 08 Nov 2025 19:07:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:95a76e7ea54fee91bddd468d42be766b080dafa1303e6552ed03062be63fdca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8a2a7d8e008934f9e9632a61c1387a36753486eb4ce48cb9e8ae8e4d9eeb14`

```dockerfile
```

-	Layers:
	-	`sha256:1608c3b946ed357b97a407f555599abce2e7c2209b4e78666605c174c939588b`  
		Last Modified: Sat, 08 Nov 2025 22:51:26 GMT  
		Size: 7.4 MB (7352127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6d91bba50683fab420bef283417761004eefd77ae01fbbf0339c4d07de59a6b`  
		Last Modified: Sat, 08 Nov 2025 22:51:47 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
