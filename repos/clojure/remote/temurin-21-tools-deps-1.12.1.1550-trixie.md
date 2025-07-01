## `clojure:temurin-21-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:1ed6a5ca08d34c09cc5efa31fe61d78cbfb8e038547ef1d56465cce79ffd6f2c
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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:4dea52fc17027b45f07d486eab5c0a11b6cfcc16c667023d48694f01cf51f7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.3 MB (292254790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280e34a4f2a9c3db87c8a4364a0dfab2e48c5f80ea8308f0dbb391bd70504ae4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30da68c6fb306cb3e238934143f1c7c176c7fe4962b9cbf17140faa0634548a7`  
		Last Modified: Tue, 01 Jul 2025 10:45:50 GMT  
		Size: 157.6 MB (157634504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af51922cc4077783da368004edb19969577607103263d96889829579e2297be`  
		Last Modified: Tue, 01 Jul 2025 10:45:45 GMT  
		Size: 85.4 MB (85355367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4b456f3baca76ab45b81e3e117daf3719271f3740b89f316eff5f8d93f7e13`  
		Last Modified: Tue, 01 Jul 2025 02:45:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b11aa724eb2005ccf896857882a47559cd0eeab5ae7032f797a21b701006f95`  
		Last Modified: Tue, 01 Jul 2025 02:45:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e7525a21fb71e52de2d2d8a3d0ed9b4de9c539c0126f3760aacbf50605fe90eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c2b6f235e9351e19cf8c892104f82ceb8c2d8d586e15304e3361e7e0a64978`

```dockerfile
```

-	Layers:
	-	`sha256:b80bedf434b4225f19142dc8106757b91b11611a56d074cf3ba91df0fb3e0625`  
		Last Modified: Tue, 01 Jul 2025 06:39:44 GMT  
		Size: 7.5 MB (7462923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:232e1b2c9d5ec0e889e1725d30c3e6a847096079da59963e1c8a2c6922f512f5`  
		Last Modified: Tue, 01 Jul 2025 06:39:45 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5e6a6066c1f77e659e6761b7846d40a6db629314fdf724750fc90965531acdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290747835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7094b00cc923a048e7cdfeab49727b3d443f383701bc9b3f3763e9df80d303`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f493c9eb5d7d0c57063d3b4b7cd398e6356bd42fc292d11031058a2292faaaa`  
		Last Modified: Sat, 14 Jun 2025 08:02:21 GMT  
		Size: 155.9 MB (155928809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc37d1dca9b9f9022fec494cec1fffda1d026ec5fa76c48818021170aed25e3f`  
		Last Modified: Wed, 11 Jun 2025 08:41:05 GMT  
		Size: 85.2 MB (85196460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacdea44607f72b9d7677e52c7d4fe32715d631932526d9949a1f8b1f4bcdce6`  
		Last Modified: Wed, 11 Jun 2025 08:40:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225285a282fc4cdf0cf499dd549e300df2a6ceb8360cced052f2b23976840073`  
		Last Modified: Wed, 11 Jun 2025 08:40:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b39f58d66cbe297b6bdbf3a46cf191321518e4a62aa733d4a35a57bc2da93177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284a20c2a01168089953224abde17f65aec84ba118cf4f80795951296dfc34de`

```dockerfile
```

-	Layers:
	-	`sha256:b8ff63e6eac5643aaa0c97b3b1d92fdc4d3b1a12b9ebe5b901f83f2dac1a38e7`  
		Last Modified: Wed, 11 Jun 2025 09:40:16 GMT  
		Size: 7.5 MB (7469973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f40de7ef0c7fa1f57b2b29c0af3d3a946fd2c860b3324a2aa113beb5536bf2d`  
		Last Modified: Wed, 11 Jun 2025 09:40:17 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:a2a73c7f7dd255ce3be312e56d515367b89b433b16ec9886781ec35fde2d2f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301672850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70c3acd59663cc0c10b668a311a944ae2b5513faf56c8fa73fc0a96aeddb66e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc7c6d506806bd280e9e75eeb1542eb6e3a8fda98921026f2d537f223a0edc2`  
		Last Modified: Tue, 01 Jul 2025 08:58:39 GMT  
		Size: 157.8 MB (157804905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4390532b3d9f3bc96819007ad3745d4065a78300330804ca7b70e72f917ffa86`  
		Last Modified: Tue, 01 Jul 2025 09:06:05 GMT  
		Size: 90.8 MB (90769667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2045fc3fa20e99f4277b33e6b0207a8894648aac1c0eda97310982379eb9573`  
		Last Modified: Tue, 01 Jul 2025 09:05:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ed406f0756a9147c3ebb875a4365e918ed440eeb11429df92ce3c008bbe0eb`  
		Last Modified: Tue, 01 Jul 2025 09:05:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6310b795ed82954d8501157084a229589551c94ccccda9a9c2bb65521bf8d6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61ec7b97b0edb49c8cba405eae8734c10a6d68baeb9ec183a3d6369f21e6a46`

```dockerfile
```

-	Layers:
	-	`sha256:040d6fe88f2965aa4e7373b4522aacd158837937ea32526d39b1cfee8c725c04`  
		Last Modified: Tue, 01 Jul 2025 09:40:05 GMT  
		Size: 7.5 MB (7467352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62da221bef854b2e17dc50df19d27e1987d583ea421e8c75f9de8edeb83c0a8`  
		Last Modified: Tue, 01 Jul 2025 09:40:05 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:edbfbe480a6c11882439ca32a7f60686a773ba89889eda67a016dd185b74be02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285438590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df578a73611493bf49c405551fbdf4246ec8a8709deb7069cb5c32f9570a873`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e076e085e4924513404df674a4b5cdd11b691d0a99549b6d4e3c46e86877f1`  
		Last Modified: Tue, 01 Jul 2025 03:02:40 GMT  
		Size: 153.4 MB (153449649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e031c8c36ce5ae72ae17b82b20d3b8c893dc9818b08e07cb8c2e96db91429a25`  
		Last Modified: Tue, 01 Jul 2025 03:17:44 GMT  
		Size: 84.2 MB (84237742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf65a88e6e3882ea20858b7f9d17cad52ba6c9f3bd3503b4bf5b856d18461a6`  
		Last Modified: Tue, 01 Jul 2025 03:17:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042b7ed731889731e7aa56a333f66c9fe6e72ea1828bc0b30e11494733eb0c4f`  
		Last Modified: Tue, 01 Jul 2025 03:17:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:25d2145882f33706e67664766ad6a5534a60114fcee0b94d37cc664ddcbd7286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7467371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7178316ac0c5fcac869f0c11c0215b99cb2af7db9d6815777e6962545c7f1f18`

```dockerfile
```

-	Layers:
	-	`sha256:54d37d07439520109b19f8db8be1b96997b5650edd58b5872bca5e88a884cac8`  
		Last Modified: Tue, 01 Jul 2025 06:40:07 GMT  
		Size: 7.5 MB (7450846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a67b8c6fe460fbad870953717a68066f568a27120b570ba7fd850e78f89d9cd`  
		Last Modified: Tue, 01 Jul 2025 06:40:08 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:5bd194b2b874f3f4ec4713a4bd2d77a96038ca7c9b39d45626e3211ec826eed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282590280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d299498979cd9d01548740b8ae53a50db59386c1690e918604b025e0ebd52442`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e01cf6c04a398e587786425ca5ff74d6a15f413fa4bc6373eda72ad291890c5`  
		Last Modified: Tue, 01 Jul 2025 13:21:29 GMT  
		Size: 146.9 MB (146911003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d928867c32cb9223ba2f618687502bce61c08442813a470e611fa1da2aad2da9`  
		Last Modified: Tue, 01 Jul 2025 08:22:59 GMT  
		Size: 86.3 MB (86334576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed1b2d49beb9cec7f05b4383c5e9ae8c917f8829e62f238d63dc674c05eea9f`  
		Last Modified: Tue, 01 Jul 2025 08:22:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d55e0f90af53aaf26fcaf9670b0f51b0876faf4e55265167620b47bf6782e49`  
		Last Modified: Tue, 01 Jul 2025 08:22:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c2073c15abc6b02a95ed30ffc283f48108b7d263ffe0121cad7cdfca5c6b6a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7475310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4f53e21e6fac1dfb7c28edc26c3e86cf8b7c10ec94c94f31ac7ea93c0bea9d`

```dockerfile
```

-	Layers:
	-	`sha256:effdde05a839ea039c43c83c072078ef890671d896fb48647367625529b07fc5`  
		Last Modified: Tue, 01 Jul 2025 09:40:17 GMT  
		Size: 7.5 MB (7458845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12b5b2a04f798d980b9b9a19d867161e21c8f9601861a1263d79209f9326c08`  
		Last Modified: Tue, 01 Jul 2025 09:40:18 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
