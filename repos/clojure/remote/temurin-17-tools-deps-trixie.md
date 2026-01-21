## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:63d45540862be1added54074e85a9f751a4dd096b29c939f149d6d02cdaf0959
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:8310879cd8137f836a187987c704f1915752ad8dacfddee6db5e47a9460134a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279677925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb48cb3e7986e1aa7807094e73303b8c8dfc48f9e63f4f3ed4dcb61264c45013`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:56:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:56:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:56:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:56:38 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:56:38 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:56:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:56:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:56:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:56:54 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:56:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d45bfbf016ce8f64d1785100ccafb78a1e3850cae14315038c036dcb578ce4`  
		Last Modified: Fri, 16 Jan 2026 06:10:45 GMT  
		Size: 144.8 MB (144847942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164e6e92744f4d8aa7ef4996600cfea3950f74c4ee4762c64c3a285bf3d812`  
		Last Modified: Fri, 16 Jan 2026 01:57:16 GMT  
		Size: 85.5 MB (85543322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564f22dd36433375dee469749df4c0fef86715f19c3d3d0036c239f3c634126e`  
		Last Modified: Fri, 16 Jan 2026 01:57:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8767622eefc3c1a75d59e702cd0a405ea4ac887e42c67bbb0bba36d6b3c406`  
		Last Modified: Fri, 16 Jan 2026 01:57:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e6a20b35f1cd38e71209dc5d41d78d99133a1528792e8598d6f449a0915ddc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f5e4adf569827b579a5d3bf4ee71f39883c5ba5a22cd1a2b1bbe3fe40e1745`

```dockerfile
```

-	Layers:
	-	`sha256:335e02027b7b11b6957eb6bb836e84f6de2fbdd8cc87a3a611a3b5e36c684b74`  
		Last Modified: Fri, 16 Jan 2026 01:57:13 GMT  
		Size: 7.5 MB (7467826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ddfcfe5f30f57e9e12ddd6d81edc3bb1e71c8033708dfbc17d41a2c655a4ee`  
		Last Modified: Fri, 16 Jan 2026 04:44:11 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e0a67dfcd826443b77473c4b68fdfb5bdd3fe5a1f6e83be52faf7f88aaf31022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278690258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540d28f5c82995cc258f274606bc6ee89b1c059ac41fb0c5052b0bcd2d276701`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:00:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:00:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:00:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:00:16 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:00:16 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:00:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:00:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:00:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:00:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:00:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a867f6fe6564505762121d677ee0b0c36d5be20f23ecd1f54419fa593aaffe23`  
		Last Modified: Fri, 16 Jan 2026 02:00:58 GMT  
		Size: 143.7 MB (143680025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862173e9821c5a6563b4ff7affb528fdad2a3cfce44dcd761e1abbfa91d63c4`  
		Last Modified: Fri, 16 Jan 2026 02:01:14 GMT  
		Size: 85.4 MB (85361107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db677592d26826135def2bc8bc4d9c84864d2014ab829d1c595fbc7eabc06d1d`  
		Last Modified: Fri, 16 Jan 2026 02:00:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b604ef521976512a1fd6eb7c7c1c84b7a1702978fbcaa09425fc25aa054317a`  
		Last Modified: Fri, 16 Jan 2026 02:01:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9a8307123bf7308209098873f886ab5c7a9d044a49cf04ebc986a9e247c52a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a057afbc5ff20ccbc77c98c1dc33e94b2fdc1ac528562eacfaa12c5ce14f9188`

```dockerfile
```

-	Layers:
	-	`sha256:fe9ab784e190e97f7ce5721eb3e300f80a2c70354a280df5b542c3bdbbc29ad4`  
		Last Modified: Fri, 16 Jan 2026 02:00:54 GMT  
		Size: 7.5 MB (7474856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f296b92ad370a4f10f20b3bba77bfb67788f45ebb343ff9061bde05228974cb`  
		Last Modified: Fri, 16 Jan 2026 02:00:55 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:bb7bf69b97bf6ce26cca654997abd89dfe011fda0e208251c13048ad8d284140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288581128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099258659f609e2b1fe9d51491f0bccee461e623ea0b5441f9beb1ad4b897761`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:16:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:16:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:16:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:16:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:16:28 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:25:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:25:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:25:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:25:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:25:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6bf15ee3631779c5e8a10fa679c64130a5b54ad0969e061ffe1b160beac0d5`  
		Last Modified: Fri, 16 Jan 2026 03:18:34 GMT  
		Size: 144.5 MB (144524715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7b94d4c5d77f3f93586a3fac5c3ed7b6496b45e74f6b93016fcc9d69aa4d8f`  
		Last Modified: Fri, 16 Jan 2026 03:26:48 GMT  
		Size: 90.9 MB (90948406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1f914461ea8aa5c8074b67ea456204aa6537b1b3c47040a701098c2c740a3d`  
		Last Modified: Fri, 16 Jan 2026 03:26:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4996ea0c1cee34ea0c043dae0744db1631af907a49cb14e0fbb72852e35ddb1`  
		Last Modified: Fri, 16 Jan 2026 03:26:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7e3866afd4a83363865754b57a9cf562a590d0c077e35a481e2a6f3ce0fe5ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0703db25d58e353047233d03af9d37be1438458ed8e8d6a95e8a0d82363a2897`

```dockerfile
```

-	Layers:
	-	`sha256:a264b642b8876f6e76b1ce4053cc875dbab969fdb2d311e871e6c2535d0e76ff`  
		Last Modified: Fri, 16 Jan 2026 03:26:22 GMT  
		Size: 7.5 MB (7472247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca4b86f2f6ef5f4b5449cc0fe63feb7e6fd5f36e1dfd4c281a09aa4db3843b0c`  
		Last Modified: Fri, 16 Jan 2026 04:44:27 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:86f8146d2e01ee383bd6b377c29ce9a6ab4c9458cc80d61b7237bbf0d0856e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274085747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d966d9c09d600be3ca31b96547dcc51fa639b079b6a1578d256e51af28846a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 06:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 06:28:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 06:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 06:28:31 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 01 Jan 2026 06:28:31 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 06:43:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 01 Jan 2026 06:43:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 01 Jan 2026 06:43:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 06:43:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 06:43:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84137287e78b3f369929e5abc1e6ea708f5c823ab4a3f6ddfafc4335289f5a85`  
		Last Modified: Thu, 01 Jan 2026 06:34:32 GMT  
		Size: 141.9 MB (141889568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2608f484a88cf2b41c5ac45bcdf6d3677bfddbcb2c786c407abb3c6da4ccc1a4`  
		Last Modified: Thu, 01 Jan 2026 06:48:38 GMT  
		Size: 84.4 MB (84423985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2330be42cc0e1c84411574e5559c5ee864268f7c2803ed41a11e074c5724cc23`  
		Last Modified: Thu, 01 Jan 2026 06:48:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95763ecb571a2d2b763c2dc2ee12d735f043cd1b1e0cbe4e9d5183e31f9708be`  
		Last Modified: Thu, 01 Jan 2026 06:48:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d419860cf53d3e4528a964baef45da3426d53496110e5810315062bb9e0ed518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c692e0b6e75397e81446a2aaa3ca7ca8b52a6ee172f5bf9f0554a41c4d6787e`

```dockerfile
```

-	Layers:
	-	`sha256:1b353703cbf097c86bda64ee499a2fe02033a987eb2416ccac7550d1449d1829`  
		Last Modified: Thu, 01 Jan 2026 06:48:13 GMT  
		Size: 7.5 MB (7452925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3785a0050307df368a9cd3ac290758867a3092c4844e242566f8c18fbc2ee4fa`  
		Last Modified: Thu, 01 Jan 2026 07:36:03 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:f578300f3bde7cb23681f1320fb379ce4196b387af8c00cc540d436aa0510e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270718684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31c7fa4d2d30462203d0c6fe022ef658ee439a5e2c8189863c976f72138ffa2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:14:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:14:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:14:51 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:14:51 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:17:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:17:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:17:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:17:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:17:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08054f6039e2280b26ac40e203037cfb04df46b507fd01341e85a498b8db938`  
		Last Modified: Thu, 15 Jan 2026 23:15:54 GMT  
		Size: 134.9 MB (134859759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c7e0bb012d5611126d0ae0863e25d8af4cf42e92c2f82fc883577d908e18fd`  
		Last Modified: Thu, 15 Jan 2026 23:18:34 GMT  
		Size: 86.5 MB (86509180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b322e2b33b4e061a0898b556f39068155c74ef71fa3d90b59bd71adeee98718`  
		Last Modified: Thu, 15 Jan 2026 23:18:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeeb695e0a8b1f09bac38fb0ec4671d1d81ab329f9c20856d38001a53d17caa`  
		Last Modified: Thu, 15 Jan 2026 23:18:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:238ba223212377d78f672115e7391341d0600ffa3b4a8f2de4dcb86ee533b636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b043cc60f52a997e7ff2af512e2f935a3f30d1ee6405b550609414c92f72f357`

```dockerfile
```

-	Layers:
	-	`sha256:82ddfe2c81a1b9c481b7c73685bd7b6e5cac7c80e54701e34dd0a8f6b9e4c93a`  
		Last Modified: Thu, 15 Jan 2026 23:18:14 GMT  
		Size: 7.5 MB (7463748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8ccee7ecec99111558eff1c1f1f651d0455beb8b8e5ecad8102cf35a90434f`  
		Last Modified: Thu, 15 Jan 2026 23:18:13 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
