## `clojure:temurin-21-tools-deps-1.12.2.1565`

```console
$ docker pull clojure@sha256:ac22987484d70f81571d4e6ea3cc6df3c7d5b60058dbc7ad638ba32004b0162c
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

### `clojure:temurin-21-tools-deps-1.12.2.1565` - linux; amd64

```console
$ docker pull clojure@sha256:8814d4583a174a6942a842cc36cb1a0dd802a34e6439d5d13fb73083c303176c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287424215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87c7507e709e45b4507c7ccc6034fa07ea689feb76ef5541d8bbf327a0f590e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c9701605d9a3ad1faa4337faa315e0a434668779166df96b14eb60bc66c372`  
		Last Modified: Tue, 16 Sep 2025 01:07:45 GMT  
		Size: 157.8 MB (157804768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4deef49f82b45831984c5725b4bc3193352a437505ac8dcad2b02c07994431`  
		Last Modified: Tue, 16 Sep 2025 00:33:52 GMT  
		Size: 81.1 MB (81137792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5cc19ba01d651f3acaa170c56f3b1889ed875a9537f09e6b8908577b9ba515`  
		Last Modified: Tue, 16 Sep 2025 00:33:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4920b506be413e22fda36066d6cf66f88c1096f7019d9ee7c91782caf95e95a`  
		Last Modified: Tue, 16 Sep 2025 00:33:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565` - unknown; unknown

```console
$ docker pull clojure@sha256:71b31bd5300f2adfdea4c78a717d9f44746646d633ce30df11cb4aed6c408c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279ca8567fc669d756c8ebe92f091349c81816b88b10bf3b92972257f4dbd1f`

```dockerfile
```

-	Layers:
	-	`sha256:d8cf41dee77df193e90f0a2521fb9bf2c9ffbc83f67743b1c54fa1f32bf953e4`  
		Last Modified: Tue, 16 Sep 2025 00:41:48 GMT  
		Size: 7.4 MB (7379992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:735fc5e6548f00aecf6b6f1f1a2809e7b1d1f6b294eb0d9f79e19ba1f545745c`  
		Last Modified: Tue, 16 Sep 2025 00:41:49 GMT  
		Size: 17.8 KB (17820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9aba700c18a720c2276e4472839393d40c3795420a62309e9b02d51f831acc04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285466911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff49d35a21d7ccbb5648f7a9fa0f6934f2148fdbcfc6738062595b55dfe78ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c04143641a1317696daa1d0cfe8dd755f376701fbb2b0ba8a476d3943d8b725`  
		Last Modified: Tue, 16 Sep 2025 02:02:11 GMT  
		Size: 156.1 MB (156081177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8075dba3462502e2da4e490150b0eab04afb3616f9abea6b1d253337833b308e`  
		Last Modified: Tue, 16 Sep 2025 00:34:48 GMT  
		Size: 81.0 MB (81025673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce918f079fc22c51ae2a632a785592dd00fac4a2e0652de2a51edb9e04fa2ea8`  
		Last Modified: Tue, 16 Sep 2025 00:17:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03281699952b8b25078a6190ee1338d5e5d9298ed32f88e4b676029a0ae51342`  
		Last Modified: Tue, 16 Sep 2025 00:17:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565` - unknown; unknown

```console
$ docker pull clojure@sha256:cc20be01497612caa65c17b1c7300d7d5a6461e6fa05ed55641c42c0dfaf8c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f5ee29f3732e567abe3167882b90a3f6e1339048ee6ed1262d7e4ff3f119d5`

```dockerfile
```

-	Layers:
	-	`sha256:d33deb58fe980a28a0df50cba4ab39040973e4a23b266a2cace2df9bd42dcb95`  
		Last Modified: Tue, 16 Sep 2025 00:41:55 GMT  
		Size: 7.4 MB (7385827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a34500aba0abaa4c83ff1e41f6a5bbc12f6de06ad703f3938b4fbbc30af68b`  
		Last Modified: Tue, 16 Sep 2025 00:41:56 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565` - linux; ppc64le

```console
$ docker pull clojure@sha256:bf197ef82c780179c101ef4cd5c4584bf5d28e72b8a0b7f40a34b4aa58bd3d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297269991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fc6c6ca042e810232a770ab5732e4f17503057e28f4d04f5ced4d71402ceba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b2ca9ff1a3fccb012f6c51a9f097c6995575e5e55d69deb7d54ac91943ca62`  
		Last Modified: Tue, 09 Sep 2025 09:35:24 GMT  
		Size: 158.0 MB (157963479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7c06ab10268aa1b3a5b8bf2361a696eab5af497e9f07984499aa47c75051a`  
		Last Modified: Tue, 09 Sep 2025 12:47:15 GMT  
		Size: 87.0 MB (86978647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72562ecbedd2159dab4f3a7fb2e042d9b0371816114d7d11f802fb5f2b2061aa`  
		Last Modified: Tue, 09 Sep 2025 12:46:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3bea5687d96efa572766e2b400297890d013020145d00dcfa8057ea981b16c`  
		Last Modified: Tue, 09 Sep 2025 12:46:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565` - unknown; unknown

```console
$ docker pull clojure@sha256:c77b2a7eccdf24b927e77008998c3b3b5be4f2a8d2d509ac216839e00d72c576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41b4517a074ab3dbd411ca442453c0e1b898552821543e4bc578eb6112fb418`

```dockerfile
```

-	Layers:
	-	`sha256:6bfc6ef18d380480945e61752acfebb3d38e5112be3c984a2a21996c45257900`  
		Last Modified: Tue, 09 Sep 2025 15:37:53 GMT  
		Size: 7.4 MB (7385242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa58a8bea5ffd35098afce9ba32a53eca385b8ec034de3aed5bfcfe61728199f`  
		Last Modified: Tue, 09 Sep 2025 15:37:54 GMT  
		Size: 17.9 KB (17904 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565` - linux; s390x

```console
$ docker pull clojure@sha256:d2a05f41f0a126adc2683e08262fb577a9bea7dde20d593037ef416efc23ed48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274116628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c44803c4ca511e23ffcc3d92075995d9e2f6c9c0711321cfdf8668875f85458`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84772536e34edd89b294c09dbe86293a053e24f7d3644f8bc0e4612df16f4795`  
		Last Modified: Tue, 09 Sep 2025 07:01:48 GMT  
		Size: 147.0 MB (147027040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29133b04619850b73aaf96e5c487efa0101ef16ad9027c451a7eb55edb17ef5a`  
		Last Modified: Tue, 09 Sep 2025 07:01:56 GMT  
		Size: 80.0 MB (79951012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff869e9132e80d33c1702964ab61924520ba2ab04a92be0f4e514cc80156ab5c`  
		Last Modified: Tue, 09 Sep 2025 06:15:32 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57847003d583d69303f6961da0ef43ae141156d9713375deeb503c450f7de786`  
		Last Modified: Tue, 09 Sep 2025 06:15:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565` - unknown; unknown

```console
$ docker pull clojure@sha256:8474c4a9e45dab4c50daeab0fb9374b4c67b314b2eed6e1fca15eb843a2b9a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61a9f71d0f1f15d49fcb9055415bef994dfb61802a7acf6b3f4aa6e9f2a1b2`

```dockerfile
```

-	Layers:
	-	`sha256:7887b5bc0d9ea87ab1c4226f861a7119be9e3794c042b395313f6969ccc21437`  
		Last Modified: Tue, 09 Sep 2025 06:38:18 GMT  
		Size: 7.4 MB (7371311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e3caf7def50115fb23a08cefcb8ae296dc1d6f2f480226cba0d3a094816527`  
		Last Modified: Tue, 09 Sep 2025 06:38:19 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
