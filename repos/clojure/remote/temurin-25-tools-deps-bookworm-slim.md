## `clojure:temurin-25-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:bf6c33a86e3f3972a3c0a03beec5fc396c9d516861e5f02102e44df6a59975a3
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

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:03f882e8c641c342e72b221cd028a8722b8b769b828cc51fbe32cc7193943af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189954120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb96f520afaed248019751dfae6d61dcad689fa0c03ea743d4a2f4f1e5ddb4a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:55:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:57 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:55:57 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:56:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:56:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ab3ac0e7973c78d10dd30ec97f0a0bb9f6e0192b1a6a3f90a7d4cbc1ed084`  
		Last Modified: Fri, 14 Nov 2025 00:56:47 GMT  
		Size: 92.0 MB (92045298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3042fe6c43bd82aeb81e9acba48b90241f6857506362213ffa2e92d625c17062`  
		Last Modified: Fri, 14 Nov 2025 00:56:46 GMT  
		Size: 69.7 MB (69679212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deacab916454e363ada76679dc33cb790bac24fd6eaf10f7be463cb1c24c71c2`  
		Last Modified: Fri, 14 Nov 2025 00:56:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18999fa4a4df9bc11191134714c6d834b627e6e48f249efd47f5d731cb453ff`  
		Last Modified: Fri, 14 Nov 2025 00:56:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:28f9b36e01a420cf4e6e69d4e1d5f2f5e22306b86d5d462c615be82c18ffd241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae2918f3ba5d1624798eefc89a5b4f04c67343f7671e89c89b8e35667dedba7`

```dockerfile
```

-	Layers:
	-	`sha256:dced3d26c19bbf8a519589e0031eeda34b5bbbde1a55bf8c891b6758670305b9`  
		Last Modified: Fri, 14 Nov 2025 01:46:08 GMT  
		Size: 5.1 MB (5064748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9cefffac9fc5ef0954c6e4e070e7352f3f4dbcb94562af9d4018099b392acb1`  
		Last Modified: Fri, 14 Nov 2025 01:46:09 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8c575edaec40f6d6d752665b486d9a990e0ab48b6aad38dc05d0bc732e2a2c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188716264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb44df878c5a08778ebeb48482e5e763c8b49fc5e4406644ee0ad484d970251`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:58:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:58:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:58:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:58:09 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:58:10 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:58:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:58:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:58:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:58:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:58:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93277903c5f55039a9466dbe00fe90af47c94c9afb3298c4857d978ff9ca3676`  
		Last Modified: Fri, 14 Nov 2025 00:59:05 GMT  
		Size: 91.1 MB (91052514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b9fd5ebce38df2590f321a5bc1e4e35f8f08d4a48091a82c58333001f040bf`  
		Last Modified: Fri, 14 Nov 2025 00:59:04 GMT  
		Size: 69.6 MB (69560331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857fd39aa089d99d257a86df085b85bab9fc7fc1a3cd15b8ba20a83b7da097d4`  
		Last Modified: Fri, 14 Nov 2025 00:58:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb964eae213a63a7828a944a634a3b94aa0dded979bc4eaf9bee95414ceb7c3`  
		Last Modified: Fri, 14 Nov 2025 00:58:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31bcc8929827b34cd53ddca7881db2a12399f96b41a13aa0d0b5527839cf05f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e5e5699306126c4d872069b8bcf9917cf27a9f423edee32b9cc1f5ef8d47f2`

```dockerfile
```

-	Layers:
	-	`sha256:14f5187af74ec522c61cbbcab07f647dda59a219c58a9d44640b47390c8dd438`  
		Last Modified: Fri, 14 Nov 2025 01:46:14 GMT  
		Size: 5.1 MB (5070530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46df3a0a8c11ea6cf61962c30bbbaab9ae0e11fae973a5193b2920baa32c16f5`  
		Last Modified: Fri, 14 Nov 2025 01:46:15 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:53b11285a375cb3f009dd56f174dc9c577b161475b60521307ef6b503302b733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199194052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ebea39ae746c133b338e45e757cfa080c594317c5f61ba9ff9e546510ac779`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:46:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:46:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:46:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:46:54 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:46:54 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:54:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:54:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:54:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:54:44 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:54:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965d7bccb021209291d1051f699e8f11ed0f5b51517e9c23eee8d574faad746`  
		Last Modified: Sat, 08 Nov 2025 21:48:12 GMT  
		Size: 91.6 MB (91610745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0054dcc07af215c789b54b91a914591512e44f11fbe1fb171b22a622fbb3d3d`  
		Last Modified: Sat, 08 Nov 2025 21:55:33 GMT  
		Size: 75.5 MB (75513353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e931568892ad7177dcea52886b4258175619fa6863d0434664394cb2f9e7d8fb`  
		Last Modified: Sat, 08 Nov 2025 21:55:26 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198fee14b0ba56095850b7a029e17583f64fc8cb096e3fac0c9b1fc8782be8ec`  
		Last Modified: Sat, 08 Nov 2025 21:55:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9a5cb72a1a3fb1b96338c7487b92d0981c3425e8f42344d8068e5a74f0823012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8828f38dafd927f9f2b399c9b9d56b8abf33de24c01fbf1982cc7c78f2a7d6`

```dockerfile
```

-	Layers:
	-	`sha256:b403d526d9b37b73b7fa9503a39923da3b6ec9dd6595751d1e13111363e5efb9`  
		Last Modified: Sat, 08 Nov 2025 22:51:19 GMT  
		Size: 5.1 MB (5071216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc432a3e6368455bce06a7d0c599832c0995663f2a3dc34d891679fddbe5eeda`  
		Last Modified: Sat, 08 Nov 2025 22:51:20 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:222e0099308789cbb4724a1b02316801a014b8138dc40468af51fa8d6bef2db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183587008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db21fa256340cf90467fd7cbc5c2e4dc441571f86de93512e55556e62c86b490`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 01:03:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:03:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:03:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:03:04 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 01:03:04 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:04:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 01:04:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 01:04:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:04:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:04:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde265baf46f3c8b33742759c5fa64bad12a3b3dd450ba515f29cda2827e7aab`  
		Last Modified: Fri, 14 Nov 2025 01:03:57 GMT  
		Size: 88.2 MB (88210714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31b5dcaa6a12819352961736da5fff6cfa0b66cf81a42518ed89fd426c94ef4`  
		Last Modified: Fri, 14 Nov 2025 01:05:19 GMT  
		Size: 68.5 MB (68490702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953fa9d5362cea568f8be016b84dbc717525723c14278d2a61bb46be498f4578`  
		Last Modified: Fri, 14 Nov 2025 01:05:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0aa35ce56f8570a36c037298ac62ec197859609577e74ba4bfb59dfd6f959b`  
		Last Modified: Fri, 14 Nov 2025 01:05:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:17f47c130a0b070a0f9007f068d3ffe1c7215eef949cdf871417fa42fa39fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304dbcff64a4549e0efec3b66bdec833e3ea2c274845aac3666ccdf85f7206bb`

```dockerfile
```

-	Layers:
	-	`sha256:1cde5d93a495757ba96fe556bb9c0169a9d90fef76005c8bef01548f3f9b1d49`  
		Last Modified: Fri, 14 Nov 2025 01:46:27 GMT  
		Size: 5.1 MB (5058617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b492d0ca2ce5e8b848b8a5ddf89416ca0082a7848758a4d8fc87977bcdb5bf4a`  
		Last Modified: Fri, 14 Nov 2025 01:46:27 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
