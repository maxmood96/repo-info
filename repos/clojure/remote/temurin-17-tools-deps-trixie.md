## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:8c84de7a17c2071bdf74796d893074bc98eccc7d4c37550a7847f8d67b5ee274
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
$ docker pull clojure@sha256:652f0137ec630626a2eb3eca9278b0f1556632c21923264cde8dbca297bfe195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279677461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5718f82e6f075c8739728414bffa0622c3ea8f175bc55853f312ef6d25ba39b0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:32:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:32:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:32:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:32:38 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:32:38 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:32:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:32:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:32:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:32:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:32:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514876d6a631decfe85237bb374fb5d72aa26d41ebddcda4582f140abedc7e2d`  
		Last Modified: Tue, 13 Jan 2026 08:10:50 GMT  
		Size: 144.8 MB (144847951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd81988039969bfa81ff131c753fbc588cbb1135ac044cd2367d3d014a99e39`  
		Last Modified: Tue, 13 Jan 2026 03:33:32 GMT  
		Size: 85.5 MB (85542850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba976665cabcf603bbf95f994fa4be0bc7c25b7fa643b8022976b43ea033f400`  
		Last Modified: Tue, 13 Jan 2026 03:33:27 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83165c7d7f2611d90d08aab4d70ad71d117d972505bdbf7bbbc850c4f03c4c76`  
		Last Modified: Tue, 13 Jan 2026 03:33:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a6bf464bab8c0e6f567bf796625cfbd98daba8725b18d090d849375b8de9e48c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb04ac83cd023257adfc42b64458f73e56d99c4d151655a51d353abfe1e0edf`

```dockerfile
```

-	Layers:
	-	`sha256:9a4e901319e1a1622b09b1f47726991dab9d45cada973ae9a127fad66db1b20d`  
		Last Modified: Tue, 13 Jan 2026 07:41:35 GMT  
		Size: 7.5 MB (7467826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:080045340c697a1f04e0f9bb30beda4e18e6d9cc85c182b69f37f162ba481ea3`  
		Last Modified: Tue, 13 Jan 2026 07:41:36 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:af2c97a9f3f5eb728d6452f432eb9c619bc6a5bf91c829c1a4316d1b5c06c519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278690283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930b022147a4bfa66673c5c5d9bb1de9c6f9733d65e4106d85784df2ec77b30e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:36:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:36:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:36:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:36:17 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:36:17 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:36:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:36:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:36:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:36:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:36:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc73cab3585a3b2f7ae74c39d0333d73aa602f2b47cae3426866af98773d2dca`  
		Last Modified: Tue, 13 Jan 2026 03:36:59 GMT  
		Size: 143.7 MB (143679912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a249bd6a0e98adc5d2fe1674e6f73c5d1fb52b91ab906e8f8bdc9c72a9d3f26`  
		Last Modified: Tue, 13 Jan 2026 03:37:12 GMT  
		Size: 85.4 MB (85361247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e9981fe4d1c61f8edb62d680538f3088109b3788297042cf1c403a85b22585`  
		Last Modified: Tue, 13 Jan 2026 03:37:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9ac9dd30f0d171b15d6a18511c041c931224f6a555ce907bce3d750eefa5a9`  
		Last Modified: Tue, 13 Jan 2026 03:37:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:78950fd3d950d9599fed1a2620f9c878dc91d9a68ff9e690124a40b3cc88d5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7da853289f91d890b3bf885aacf31d2a55105c88c00ae965d74d602504ab24`

```dockerfile
```

-	Layers:
	-	`sha256:687333a0c80fa3cc74895f049012804c779cb98cad59094e2bcc7ca41a0f7b79`  
		Last Modified: Tue, 13 Jan 2026 07:41:43 GMT  
		Size: 7.5 MB (7474856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20cc366e4a41e32f9c50dedb4f052cebf283d7f284290147a48fde6564800a29`  
		Last Modified: Tue, 13 Jan 2026 07:41:44 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ce0f3bf452011b6b2c54b0535d4df4194b060982db6e50608688b9f1b8b3a249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288581444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa3bce68444958f4cb501f480158e5df6568fbe3f285b97b42c5d92aa875e87`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 12:18:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 12:18:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 12:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 12:18:47 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 12:18:49 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 12:21:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 12:21:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 12:21:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 12:21:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 12:21:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7ecea75ca7920b32939fa84de920d3f21637572fc1bdb268cfef22060c6fa0`  
		Last Modified: Tue, 13 Jan 2026 12:20:23 GMT  
		Size: 144.5 MB (144525214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04713be71b20936459b99d07a2873b73b8297d9f29de5932a51d14137cba9da`  
		Last Modified: Tue, 13 Jan 2026 12:22:30 GMT  
		Size: 90.9 MB (90948226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c1df28fc32ff07e64090a8c2b61219ae616acbb1d3e76ebccc01af42f4b328`  
		Last Modified: Tue, 13 Jan 2026 12:22:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d986bb02991651bb54b07b0fd2367183d994c4f23e7dec2b30e8e2d05a33ee76`  
		Last Modified: Tue, 13 Jan 2026 12:22:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:493992f51c21a5dbdcf4af1fab386a2a284f2eddd2fc525a0432e15ae2541dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaf16bad423f3ae7a85158c8bd9eec7e2a74e4e81335e95077fcfbb41d9772a`

```dockerfile
```

-	Layers:
	-	`sha256:680265e8ce4f0e5024274f6fc97b54adb04e9422c91c27bc9fc0063fa452e0da`  
		Last Modified: Tue, 13 Jan 2026 13:36:04 GMT  
		Size: 7.5 MB (7472247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9287379ed7205c34b7aa6cf0f46b17fb551d78056e41f8f055fe0025849ee9d4`  
		Last Modified: Tue, 13 Jan 2026 13:36:04 GMT  
		Size: 15.0 KB (15000 bytes)  
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
		Last Modified: Thu, 01 Jan 2026 07:09:39 GMT  
		Size: 141.9 MB (141889568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2608f484a88cf2b41c5ac45bcdf6d3677bfddbcb2c786c407abb3c6da4ccc1a4`  
		Last Modified: Thu, 01 Jan 2026 06:48:38 GMT  
		Size: 84.4 MB (84423985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2330be42cc0e1c84411574e5559c5ee864268f7c2803ed41a11e074c5724cc23`  
		Last Modified: Thu, 01 Jan 2026 06:48:32 GMT  
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
		Last Modified: Thu, 01 Jan 2026 07:36:02 GMT  
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
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c7e0bb012d5611126d0ae0863e25d8af4cf42e92c2f82fc883577d908e18fd`  
		Last Modified: Thu, 15 Jan 2026 23:18:34 GMT  
		Size: 86.5 MB (86509180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b322e2b33b4e061a0898b556f39068155c74ef71fa3d90b59bd71adeee98718`  
		Last Modified: Thu, 15 Jan 2026 23:18:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeeb695e0a8b1f09bac38fb0ec4671d1d81ab329f9c20856d38001a53d17caa`  
		Last Modified: Thu, 15 Jan 2026 23:18:25 GMT  
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
		Last Modified: Fri, 16 Jan 2026 01:40:49 GMT  
		Size: 7.5 MB (7463748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8ccee7ecec99111558eff1c1f1f651d0455beb8b8e5ecad8102cf35a90434f`  
		Last Modified: Fri, 16 Jan 2026 01:40:50 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
