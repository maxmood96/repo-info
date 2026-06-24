## `clojure:temurin-26-tools-deps-1.12.5.1654-trixie`

```console
$ docker pull clojure@sha256:8b4500c0ce71e65a50c9da4fd8b5a2af216623551ddc4f3f2d4b74d33093b176
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

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e5ebb5657fd736c3dd6dbb735d7610b4202f17912025a2450e19eeccb7ee19e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226361568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d639d71f4749fe4f2b850581b1405cfc9973909c934976cfe37a0608d58c36e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:23:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:56 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:23:56 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:24:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:24:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:24:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:24:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:24:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f0c90772fc8a120f9d66aee0b56df6d6042b0d670f90605b2147f30e63d2c4`  
		Last Modified: Wed, 24 Jun 2026 02:24:37 GMT  
		Size: 94.5 MB (94524352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f83693e7d3b5553b00b689ef76a053a3038cd131f88366673e5e83f37f6456f`  
		Last Modified: Wed, 24 Jun 2026 02:24:37 GMT  
		Size: 82.5 MB (82518920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e7b6af958107990944622ab9b0c105574267eb8dca8c3ba48402199083be5a`  
		Last Modified: Wed, 24 Jun 2026 02:24:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d580b91bea4a3b425e9e2bb0999fe4be5ef87d05ed0f731b44a543befa8c98`  
		Last Modified: Wed, 24 Jun 2026 02:24:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fabf2e7ba6e90e2d5a21c13468ebc04afb2ad9a3b085b3c0693a2f8c2e4cfa0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7449563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6b1b6699e196d9888001e0e1e4d5d8925ba9dd2fbaedac9d2f6d90a4de6bef`

```dockerfile
```

-	Layers:
	-	`sha256:05b392355a989fc50327cad563e18249a7f16164a53c714adfb23f3927c5425c`  
		Last Modified: Wed, 24 Jun 2026 02:24:33 GMT  
		Size: 7.4 MB (7433662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d49d2d92530f2eb90b29bfc64a317f326f3744ee2b6e0bca2ec2903c4e17cb`  
		Last Modified: Wed, 24 Jun 2026 02:24:32 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1eb393e164c5c77cbccafa54c14f2244a746bea77930d8991f41fba1e6171542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.5 MB (225522011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c88f0983e480016bb8fd94059b2f96dc17720c5cee91d77c79bd762a9e295d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:30:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:30:16 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:30:16 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:30:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:30:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:30:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:30:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:30:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b95e544d6ee236be6b35d07742ab22e118a15e53f5e6261b6b89a026e00ecc2`  
		Last Modified: Wed, 24 Jun 2026 02:30:58 GMT  
		Size: 93.5 MB (93504362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f88f1404f3de841cc1fce5635b8278eb9572d0b5aa0443c2dc5479abbdfce94`  
		Last Modified: Wed, 24 Jun 2026 02:30:57 GMT  
		Size: 82.3 MB (82338212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bb1d9d33c9e52ea9dcdd3bf4451201cc8420f40714ca8cba64d07bed5b6f8c`  
		Last Modified: Wed, 24 Jun 2026 02:30:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6198643564331cf387dbb62ebed51ed5c2a2d7c9f7a3bb2fd4840e69b4d65f40`  
		Last Modified: Wed, 24 Jun 2026 02:30:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:62a8399d2a68ab1a3e2e7cc9832f4667d151fc1ff8ea7eb3d16c9f7f72b29b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7456071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19e643188f92f1d2a5d39dd3811f46f92f87ba581ee866a82e2000585264076`

```dockerfile
```

-	Layers:
	-	`sha256:b12c566f1100178a5456759da1cc4899b81cdb2b1d9d2081541ddc59005e4b8c`  
		Last Modified: Wed, 24 Jun 2026 02:30:54 GMT  
		Size: 7.4 MB (7440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a8030e41b42885197ef5adc73f4170279fded3ec86adece9954750817fe540`  
		Last Modified: Wed, 24 Jun 2026 02:30:54 GMT  
		Size: 16.0 KB (16019 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:4165177b4b9432cebf80e3fc23bf6eb899f90f72a6eaeecb9d577a399480ba3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234979782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef69df2e4741c901abadf6e76243d64268aae22db77e7608c2b64181c86e5d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 08:34:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:34:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:34:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:34:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 08:34:41 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:40:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:40:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:40:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:40:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:40:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99b7058514c1f9221ac3b0625d731341802c32d464fd604a099ae71d3765bbfd`  
		Last Modified: Wed, 24 Jun 2026 00:30:31 GMT  
		Size: 53.1 MB (53138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb8abfa12b6427363309b1547420d955191530c07a3fd257bfff14f6647ed36`  
		Last Modified: Wed, 24 Jun 2026 08:38:02 GMT  
		Size: 93.9 MB (93902053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7649c5f662b0636b872b8353458f164d9af1a3e88fd50d1645a572e2eb2391`  
		Last Modified: Wed, 24 Jun 2026 08:40:52 GMT  
		Size: 87.9 MB (87938620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500ef46ba50e8ecb701915eaf83ff6df36e0363ad14c9acc0eeb3d644ad94344`  
		Last Modified: Wed, 24 Jun 2026 08:40:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9af633f871e3e2f4f6f285c9072473a3121f885aa7f3df130bad43ae702a73`  
		Last Modified: Wed, 24 Jun 2026 08:40:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:39b50496e6238cbce77a845a327bb389c64a3f9192629214ac607d1e258b2462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7437968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7639f28c9750a112cf4a8a9b57df8f484c404d338ee54400ba696587e4c7d5b2`

```dockerfile
```

-	Layers:
	-	`sha256:fa809a9676a1276a410c686101ac272510d75ee1b1ffb9198f168d0bf9af0622`  
		Last Modified: Wed, 24 Jun 2026 08:40:50 GMT  
		Size: 7.4 MB (7422019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a7229c3cc07c95114cf62f28207327aeb8a177c6c15541030026d004a61b415`  
		Last Modified: Wed, 24 Jun 2026 08:40:49 GMT  
		Size: 15.9 KB (15949 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8898b38bd1bf340718ac550a6021a86b704740edcb7f841494e6ca3645f03036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223425942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57432c0c93e6779128ba514dd1fa06f2d77096a8f71d758aa8d3aa7e97a72c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:22:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:22:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:22:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:22:18 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:22:18 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:22:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:22:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:22:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:22:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:22:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f7c77ea537ab464d328802f9350b8031424fb3ba62e536df0444f1d67b82e0`  
		Last Modified: Wed, 24 Jun 2026 04:23:04 GMT  
		Size: 90.5 MB (90536980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13f972f5b579bba0a580dd8c6f5c4f2f321ff3fbb37e60ff1912a267e1b3ae5`  
		Last Modified: Wed, 24 Jun 2026 04:23:04 GMT  
		Size: 83.5 MB (83501864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e773753bc43b0402f522aeefbe730594d49565ba22a6d99a9abef510a7a58e`  
		Last Modified: Wed, 24 Jun 2026 04:23:01 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee24c7db7e7bee384c84845a76849a06a7e5d998704d7d26083d9042324ff65`  
		Last Modified: Wed, 24 Jun 2026 04:23:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:11599873de7348315db893c9ebb72f77b5808c93790ab86cbc278d9e3e908f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90f2530ee7866519c1178ed2db56499fecd7ab85ed29a36b0df1256ee8be48e`

```dockerfile
```

-	Layers:
	-	`sha256:38be285cb9b5c60d1aeb4b524a6aa46e7863a9a47748b301f602cbfb93f6f50d`  
		Last Modified: Wed, 24 Jun 2026 04:23:01 GMT  
		Size: 7.4 MB (7414770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1a352f3698360df5a67904cd3dc454c07746f644807c0fdec9a537b3c187cea`  
		Last Modified: Wed, 24 Jun 2026 04:23:00 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
