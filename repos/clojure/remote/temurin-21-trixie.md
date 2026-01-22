## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:5d4de25febae9ebc725c0c0649a7e38a5dcb8e004d85966224af3344a3b551c2
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3480fc16a8afbda6516379ec11767237f8ab3f86b3ab49e26dbf7ed652a3b112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292655824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec058e5f21a0937d343501d334a0f1841f3b33d78acc755ba323e4c6f7c68749`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:01:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:01:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:01:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:01:56 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:01:56 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:02:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:02:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:02:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:02:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:02:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d4d89e4d4f32fe683aaa3364e61b63b819ae1f73bd0bd2c0fc4fc3953ce50c`  
		Last Modified: Fri, 16 Jan 2026 02:02:43 GMT  
		Size: 157.8 MB (157826001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b895a0be70e64b424134b2cc1953669b90e2da451db1a88d55fbcab127d53c`  
		Last Modified: Fri, 16 Jan 2026 02:02:42 GMT  
		Size: 85.5 MB (85543161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b754c808e0e87aa15fcbc1f47368812bb35fba277650b323fb44eabbcdf86816`  
		Last Modified: Fri, 16 Jan 2026 02:02:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ba3031f96490845f4e6f5d79507b59457cd1f274c1541c91b05c891404ea7d`  
		Last Modified: Fri, 16 Jan 2026 02:02:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b40d06665db53006403d73bb3fb36bdf59c9d6804a0a36b2034a6d6ba2c2ce4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cee2b25222030b2a50c2ffd65f8df0b0caa023d1e99aafb7dff663fe5020d34`

```dockerfile
```

-	Layers:
	-	`sha256:a617d5b6e015ea31d658a06518dc328016134dc4d0ec00f3a27702ef60667619`  
		Last Modified: Fri, 16 Jan 2026 02:02:39 GMT  
		Size: 7.5 MB (7470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44802287f0fd4c10b6736e69b7aa95cc561b1b141cdb945a17c69f1a64783a3c`  
		Last Modified: Fri, 16 Jan 2026 02:02:38 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20c0d99f4a5820edb390d8ece71d0d91939ef5c77fa025ca3ae8897ad9944a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291117892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0739eb14f493787031e6c54419caa25ad58243f46362b05276b6618aafd0a9fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:06:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:06:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:06:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:06:51 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:06:51 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:07:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:07:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:07:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:07:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:07:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e7a785535577f6ee62505d8623e620571a2d091cdd9704e665e550ec4abe75`  
		Last Modified: Sat, 17 Jan 2026 13:23:22 GMT  
		Size: 156.1 MB (156107636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620f5fdef7da32e9efe300eaaf48b6c57cb94601c739bf332f50c7148df23a0e`  
		Last Modified: Fri, 16 Jan 2026 02:07:34 GMT  
		Size: 85.4 MB (85361131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01af44b5b0043e6f78481d9a50af1df8fdf8fb4f469078c3e9c7dab65d05bac`  
		Last Modified: Fri, 16 Jan 2026 02:07:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f012fbde90e6ae9c5eb48a87d3b3cefe93f0eb53654c356ac14a9c903c12449`  
		Last Modified: Fri, 16 Jan 2026 02:07:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:26a5b6a92e1ec6dfd515ff2fe9131bc76d654b0417305fef122621d034c9a103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6927e6fe6528f8ad493428d2f14f7153c5bfa1ecad5504354d1ef8804e5c6262`

```dockerfile
```

-	Layers:
	-	`sha256:218424e44550922b2d67fbf136db29bc53e49d3aa8ba4960e9b4f8c4491745e7`  
		Last Modified: Fri, 16 Jan 2026 02:07:30 GMT  
		Size: 7.5 MB (7477958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36954cb7301e542b95f652fac07b6eae98ff9e4561ac3f1fb47612acb67a7497`  
		Last Modified: Fri, 16 Jan 2026 02:07:29 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:710783dff4f3b6a1e3dee075e29ef12ba213b28d3d243f58e0ebc13717163de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301999276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f94fded8fe4aa51c645fddf38d0237f501a0f6fb1e61831bf1035378da99abf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:32:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:32:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:32:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:32:36 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:32:37 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:40:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:40:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:40:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:40:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:40:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb8419d04d870182d92f9dd23172b44a59edb435e25623743b58a1807e6008`  
		Last Modified: Fri, 16 Jan 2026 03:34:25 GMT  
		Size: 157.9 MB (157942967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae10255eddbedef2aacc01c4d059b0977686bc75bc275b07e8e3278e54650604`  
		Last Modified: Fri, 16 Jan 2026 03:42:05 GMT  
		Size: 90.9 MB (90948304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11779f3d2d64dc7f22e6b9494770961d26033d6edfcbbd6ad898e6ce9affcf82`  
		Last Modified: Fri, 16 Jan 2026 03:42:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3014515d582dd07781d0ed67e19e8aa27146d9efb097a8cf3195f3a06da070c`  
		Last Modified: Fri, 16 Jan 2026 03:42:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f798000ae3d4b5d9f340b3035eb91a753718b27651aef36ab897f3e982a63c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581c132ef4cc4c8b44ae5e0dc81965b9cd2507a55ce83c822b69b4e05867d8ac`

```dockerfile
```

-	Layers:
	-	`sha256:52de38276c78b0eb7f03a109775e618ac4dd92e1e4c6e8c09f33c56ed6220293`  
		Last Modified: Fri, 16 Jan 2026 04:48:57 GMT  
		Size: 7.5 MB (7475349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e2cd3cab3f739608a4a042a1e32a1957eec0afd1e94acc3a4ea57cb0e9e0e2`  
		Last Modified: Fri, 16 Jan 2026 04:48:58 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:b20302266a24bd1d322e1163913cbb61394f97fb29d74821f050b19847940705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289390162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabe4a8ae3196f83ae5776053eb20bad676ee5a9dbfbd932e2cd95e35af1cb4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 03:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 03:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 03:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 03:51:04 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 22 Jan 2026 03:51:04 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 04:13:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 22 Jan 2026 04:13:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 22 Jan 2026 04:13:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 04:13:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 04:13:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ed654d72f1583479eae71ff4bca91d394293fa06b9e1bd650a8ac986e87dd2`  
		Last Modified: Thu, 22 Jan 2026 03:57:33 GMT  
		Size: 157.2 MB (157194267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0b8789669bfb079125ce0cfd40cb5fd2db09e819a9b432424db92baa4eb284`  
		Last Modified: Thu, 22 Jan 2026 04:18:30 GMT  
		Size: 84.4 MB (84424010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1644670c2a95fd4dee2151d45b57d1d201fedc283eb9ce270cf308b0af0992d1`  
		Last Modified: Thu, 22 Jan 2026 04:18:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830671b3afc0e3187c461545c74ac6d032188299215aae9b704b84a1819a1c6a`  
		Last Modified: Thu, 22 Jan 2026 04:18:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0be28f07b981b0fddc31beffdd5faedf33452648ce75727239ebcb58f5d10003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c971f987634a5d2c188a1e5d5a1cdafa5088bedd4de92b03c63465275312fc`

```dockerfile
```

-	Layers:
	-	`sha256:4c6f80093c8b750f2c98f6f90799b5b93a0913529fb8aee37b2b92de100c78c0`  
		Last Modified: Thu, 22 Jan 2026 07:36:45 GMT  
		Size: 7.5 MB (7458843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64523b217105fcac2580e39a97f02e62236330611f6935e5ed6930096f793c96`  
		Last Modified: Thu, 22 Jan 2026 04:18:04 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:01d78ac2ea2e0c6336b77497a2c14dcb7d25f49ec14952fb5f15b4c12504d603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282928622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1d777e7ef450d026e0d92602060034a782dba2c1d9552ef197ce8f59656ae7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:21:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:21:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:21:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:21:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:21:27 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:21:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:21:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:21:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:21:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:21:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae6c4a7756d1c3787b30ecc0274649afb3785298dee1ec697d3187c89c66010`  
		Last Modified: Thu, 15 Jan 2026 23:22:15 GMT  
		Size: 147.1 MB (147069873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51def410c3f01bbc3042540299ad2c0da1198686392a329e41c8d9dca6ef3f1`  
		Last Modified: Thu, 15 Jan 2026 23:22:33 GMT  
		Size: 86.5 MB (86509003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c209c73aa27f9d0a756beb789f6dca65b0b87fc3ca272b417332db2623bded8`  
		Last Modified: Thu, 15 Jan 2026 23:22:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce4a04d4f539baa76bc8db9696c66e999e75668ce4278e00c5908c731b6ac08`  
		Last Modified: Thu, 15 Jan 2026 23:22:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ae5948ae66b4095d2690430b00d1dc7112493615c5391a12efc67994cba1cab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0cd898e40ea7b24e1e1a9c208ab66828df4605a069b377c9a2852677668286`

```dockerfile
```

-	Layers:
	-	`sha256:8e1b18a905dd3ecaedc7bfa2a3c255ecff847a751d74d4052b3eba24644f8866`  
		Last Modified: Fri, 16 Jan 2026 01:43:16 GMT  
		Size: 7.5 MB (7466850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87014ac8bb6f12a1e080cb563f1377b596d2679d063eefc8193c7d74325afac9`  
		Last Modified: Thu, 15 Jan 2026 23:22:12 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
