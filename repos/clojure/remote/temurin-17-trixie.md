## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:369e3e9e52d117c2c15cf14a52f72195e820441bda8aafcd40ed81b6b0b6b348
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

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f718f5273dbcefe96b8c9f3cae78ed79b10ba102f10ab40f4196a712d4931e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282477464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a433c33ad6ba8d5193ed2d60e67dcf2089df31e69af32d1887a888277c4c7a12`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f468d8f3423213f3894fece5d145d047cfaa51db26ba948678536c902df5358`  
		Last Modified: Thu, 02 Oct 2025 08:59:09 GMT  
		Size: 144.7 MB (144693589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78f0ff8e60155359cb4913921dd9df80f803fe7e72f3e101c8755142154a574`  
		Last Modified: Thu, 02 Oct 2025 08:59:33 GMT  
		Size: 88.5 MB (88498207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7de4c5377f888f6ce494e486d1dd6a72acf47fe034fa651d06aed06850cbba5`  
		Last Modified: Thu, 02 Oct 2025 08:59:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57011202db2686e0c6e9e6c0993cda3e3dda50c594ef586bf9d571d5d0c7d35e`  
		Last Modified: Thu, 02 Oct 2025 08:59:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e7b7ff51df7aba47666ec93d23ee8c27a26f20f8f58b4239fce3bf97759e79d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a9824449f04b7ebef3155ed6a8b802ba462e91ec496bd8738f63c2c697c246`

```dockerfile
```

-	Layers:
	-	`sha256:c6f67e0a4db7ba485ba1214e7939047fc610c5fd6cc3d840d166405b4f69939b`  
		Last Modified: Thu, 02 Oct 2025 12:39:48 GMT  
		Size: 7.5 MB (7466899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b52388052c71a4a1b0d4d3c0336e81a60dc8e64847656b4fa4d855e65c7c8ab`  
		Last Modified: Thu, 02 Oct 2025 12:39:49 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:573a5faab0035044199dca839c5bb9a7de700fb0e8cbe9e06b2bfd96b051e0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281882368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d000f54b3ceef1a61c3f1999d63b35207471c98a7dfa265be0bf7f2cec866888`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e38d1930ae6419042590ec372f58de328029c453483a34de0f7aec09ae1d90`  
		Last Modified: Thu, 02 Oct 2025 09:50:44 GMT  
		Size: 143.5 MB (143542162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20eee459f214dcb00cab6b3e37eab4cab9fbada6298a9925772e59eae9b3c6e`  
		Last Modified: Thu, 02 Oct 2025 02:45:12 GMT  
		Size: 88.7 MB (88690471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70cd19b21ca60f8d92ffc23246a95023104813083f6047ec393830842c1e18d`  
		Last Modified: Thu, 02 Oct 2025 02:44:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e083e3bb26f263ed75fc982cf17706428be528212f095cfe28b9130f2e2d8d`  
		Last Modified: Thu, 02 Oct 2025 02:44:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:beba15af84640c90a6d415f1ec482696e322ef89eef45918f19b9eac8f9e21a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aba33ba73ce5ae95c03c3104abc620378c65500f8682cd567fcd18994de95b`

```dockerfile
```

-	Layers:
	-	`sha256:208ed3b9615042adb2b7e6959ad7d45f6ec1e6dd46a796c373b86891e60eb48a`  
		Last Modified: Thu, 02 Oct 2025 06:41:47 GMT  
		Size: 7.5 MB (7473929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:963418b40bd8f8c4db8913ab8ce7e26b3a082d07bdb1acc0f65f989d5bfd1927`  
		Last Modified: Thu, 02 Oct 2025 06:41:48 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d5c760569575f93338f806cac5a1dde0d357a7b6e5419a3bd99fab27be6eac3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 MB (291634920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c6800abafd91524b19454a9d47d4e3229ae410c8ac3d52e3129700338e13fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147ef3ed9bf7756639cb71fcdd41937a73c6b055157e28fe7fd302fcde2df556`  
		Last Modified: Thu, 02 Oct 2025 08:49:19 GMT  
		Size: 144.4 MB (144372680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf10802a773fda7593bb49abed7c460aad147da319a57ea50fb0c9ce9891e2`  
		Last Modified: Thu, 02 Oct 2025 09:04:59 GMT  
		Size: 94.2 MB (94151982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6151cfc513dad6f69929deb25ab217689426f08ea36da5737f1c33f75c0cac`  
		Last Modified: Thu, 02 Oct 2025 09:05:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11017b87687d1b8bacbe65685826963fbe47a3dc664594a72a68315959aa5cbf`  
		Last Modified: Thu, 02 Oct 2025 09:05:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2eb691efdc9e62b8a3afe2d6980c51689e4578165cc392fdbe0269d7e54b09a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcee001209e5ee16b6958050421e5e554fb7b05bbfbe8bfcf5083dcd6b955d4`

```dockerfile
```

-	Layers:
	-	`sha256:58c2841c5e1e2acc572bb056bddc6b97512f19ce84e647332fbf1b22f8114f06`  
		Last Modified: Thu, 02 Oct 2025 09:39:06 GMT  
		Size: 7.5 MB (7471318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa34fea284deb499d67b59d81a634e62abdf9eddc7efc1585a78916940c6f56`  
		Last Modified: Thu, 02 Oct 2025 09:39:07 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:9bef743fe826cb5bcb13d748e5d0cbf6a40528600ab1f0dec963ae10fc6c1278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270769519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7dabbfba138a493d060fdd1ba681d7f3d6dd39c9f1764af79175266e281a5b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3ae21fa5b4d30371a66ca687e7c73e5de6887104c1d0ede9bca919214a08b0`  
		Last Modified: Thu, 18 Sep 2025 19:48:28 GMT  
		Size: 138.6 MB (138575662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75f3c1334ec9f5f2fd36b054d78ebc20154407af3e5f7d2d694d051b451cb90`  
		Last Modified: Sat, 27 Sep 2025 00:08:18 GMT  
		Size: 84.4 MB (84427371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc550d8cc9780fceb69b83065ad0643609f80310df572d392679e711672e617f`  
		Last Modified: Sat, 27 Sep 2025 00:08:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa7381e608293db80205c25fa3a086d8b9613bcc5bddfbb12262ef50b5f912`  
		Last Modified: Sat, 27 Sep 2025 00:08:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:878a81d52588ddd33519f1ea681d295c39d8d30a11b18afda8870c983439b1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25855f9b085ff99342363ded60e25af798b7b906755f8cda680dd7c976be13da`

```dockerfile
```

-	Layers:
	-	`sha256:b9139750f527c5e80450cef0e47808390171aa75940a4c8fa6cf344640d58876`  
		Last Modified: Sat, 27 Sep 2025 03:35:44 GMT  
		Size: 7.5 MB (7452839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aef6cfcf647a05cbc192a7d513e9d1d0d9e2469118a02046e61c08a131b7995`  
		Last Modified: Sat, 27 Sep 2025 03:35:45 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:12c5364f19cd72cffd39806a7e5693caf778c0b6add0392cbd4745afb19c694c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.2 MB (273201467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c741a2f6151942eb895503b3364d07b62f044458699b6bc7db6b13aee577dc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ce697b31a0ec3f127d93b7b8a6bdc5d919cbef06753715fbd65ce1d3d5e04`  
		Last Modified: Thu, 02 Oct 2025 04:33:47 GMT  
		Size: 134.7 MB (134724294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f679f9995a93a105b6c7cead0a0813e3b730c6266f4cde0d09c8fcf45a855f`  
		Last Modified: Thu, 02 Oct 2025 04:40:09 GMT  
		Size: 89.1 MB (89124690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633875ba4dfe964874685ee36a207a9680018b27b99c8dc37adf06b8f460e064`  
		Last Modified: Thu, 02 Oct 2025 04:40:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a62b6dd9ced4916ff99d0ac6b3300fdb59b905b9d13c3f738464b2cf9a4cba1`  
		Last Modified: Thu, 02 Oct 2025 04:40:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4536991d99a204e6b859e0faf7956ddaeab20c33a92257a8db9831f7c8c45471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af414c0d15879c85ddbd2ec73ad91a964e795483f30f3656790e6d5652cf178b`

```dockerfile
```

-	Layers:
	-	`sha256:d937eb9864072ec44a28a55fa97062c7a9d24fb8ac2281ec2ee8f9c223c64ef2`  
		Last Modified: Thu, 02 Oct 2025 06:42:05 GMT  
		Size: 7.5 MB (7462821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc967c416676c1a986570e44a223bb6b2608a4085c8fef9cabed9a6179f91a51`  
		Last Modified: Thu, 02 Oct 2025 06:42:06 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json
