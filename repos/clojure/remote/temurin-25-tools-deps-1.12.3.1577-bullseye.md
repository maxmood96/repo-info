## `clojure:temurin-25-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:ae6c370e57f804b92565a339f2608baf489f34c7f227d9a192670678f03d7d57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.3.1577-bullseye` - linux; amd64

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

### `clojure:temurin-25-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f684494a11599a35276a7af9eace9a601d7dab4488a945add125d74370b6766b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212999860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058374c63f46e881df622866af1ee2b19ca4b2b0ef7e26dc11f27043730242ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:58:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:58:27 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:58:27 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:58:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:58:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:58:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:58:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:58:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd70e546029fbf17e337f919437c1c08492e7037f5da834949fcaab929c253c`  
		Last Modified: Fri, 14 Nov 2025 00:59:19 GMT  
		Size: 91.1 MB (91052530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adda11e9a277c2e278aadfa7e91c7457ca8cac97759863de8a6217639c7a1ab1`  
		Last Modified: Fri, 14 Nov 2025 00:59:21 GMT  
		Size: 69.7 MB (69688320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced4bfde0decf14524be2dda262ff152b4c321839ba69bf534cb5e1b0bc7aee`  
		Last Modified: Fri, 14 Nov 2025 00:59:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b496328bde2a4e51e2324fed7b3242c6172c700a8ebac545605998eaa50060a1`  
		Last Modified: Fri, 14 Nov 2025 00:59:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4769ec5c608404771134f01fbc31db5e1fb6ce30a187b0cd6cc585601b2cdee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1dd48ec9d52fd2aba7e5c2404818c8cfabec9d79f3a9321a6a0ee194af584d`

```dockerfile
```

-	Layers:
	-	`sha256:37589c3534ed1a0deea7886f8751d21893a078994b98259190c1cdedb710f9bf`  
		Last Modified: Fri, 14 Nov 2025 01:48:17 GMT  
		Size: 7.4 MB (7352127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5375ed30f208b3ae3f1b03ea4e4e99f4309baf6127103223132b4b3d7d58383`  
		Last Modified: Fri, 14 Nov 2025 01:48:18 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
