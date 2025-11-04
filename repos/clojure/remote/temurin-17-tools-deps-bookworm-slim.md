## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:c9689516a01accc41b9008529ceafe6f263d59495a3433f69027533109a17c20
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:21e8955fa5bc069205230802b6ec6601d5a875344e54e2d21bc151cb92146238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242601959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e31678db168b4f96d945d53544357beea4f61e14f800875ba4b2752eb7a056`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:55:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:10 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:55:10 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:55:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:55:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:55:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:55:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e7c2dfcabbd60f415566180582d4149abbfa5580d10a03e55ca5459561e286`  
		Last Modified: Tue, 04 Nov 2025 14:42:24 GMT  
		Size: 144.7 MB (144693306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb0c0cef8fe095702970310d94cc4004c2f0b4fdaaa16459745cfd5873b90e`  
		Last Modified: Tue, 04 Nov 2025 00:55:58 GMT  
		Size: 69.7 MB (69679046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf8c4e4ca2405d8e5303fcc42dc32eec0bd96d4e45c009750d86ad74e6cee47`  
		Last Modified: Tue, 04 Nov 2025 00:55:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d179c685d392c8a1657034755e8f506d1641efd42eaf63bd5942b30f9839d97`  
		Last Modified: Tue, 04 Nov 2025 00:55:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ed04a02c4796fe4e8d2f48af49f1ce992c5d33b9e63c167521ace4c0e59330c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c240b96448895b7ca67b9187ecac68b25b71a545c5326628bab67619a13f79f3`

```dockerfile
```

-	Layers:
	-	`sha256:b0e62a476c2af782097fa263b709ddac30a9bac037a06771df76e3cf5821b3ca`  
		Last Modified: Tue, 04 Nov 2025 10:41:05 GMT  
		Size: 5.1 MB (5113388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8995fae572f872f5939939333c23e78ea9e914e2bba0297bb02401d228b118c`  
		Last Modified: Tue, 04 Nov 2025 10:41:06 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:009fc55283b0733bcc1222d119a116fd62259dbc7cbb5a9989132936928bef6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241206000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e3e1c7bc700fcddb3daa5a54b70918c41e96a533f21473974dd41f300f3041`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:55:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:47 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:55:47 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059f72fccf642f21a1673e2f1f2bc6da83b6901745131cde2afdcc0e1654d16c`  
		Last Modified: Tue, 04 Nov 2025 00:56:23 GMT  
		Size: 143.5 MB (143542093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532069fbcdfb36057cc434d0fe46e64801b7808e136e3c7b53f454334b66879`  
		Last Modified: Tue, 04 Nov 2025 00:56:39 GMT  
		Size: 69.6 MB (69560492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1883b526c856efb9ba3f5c27c80018f1c7f0f5ce0dfa756cc16c2f72af37f25`  
		Last Modified: Tue, 04 Nov 2025 00:56:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050f6ff4a6d28a6251eef1b86a517dcb7355d9a3cb06c9b715b05985dd3f937e`  
		Last Modified: Tue, 04 Nov 2025 00:56:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ab8bfe725023b88a556f100dbc44ecb3e667501d8f06570097c71673022e5a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c38f92a5c2b8772ab17c26ab1a84f1bd2422d9d5a0ba1155acbe71e70bbb873`

```dockerfile
```

-	Layers:
	-	`sha256:cab37eb34d7b2e973c019aeb70bd3668b50d9f69bfe95926b809265194ee6047`  
		Last Modified: Tue, 04 Nov 2025 10:41:12 GMT  
		Size: 5.1 MB (5119149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05027fc230de50ddd133b219f530f46496dafadb8a2a5d1721b6590a88e06c46`  
		Last Modified: Tue, 04 Nov 2025 10:41:13 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2b78c165bc06f534fec624290f68d341af294e59066c2f8928524d289f7276fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251955774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983f2fe48a6213e411457bc1836b8792cc91831a1deb54a9128b28b890888288`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
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
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5a5db16a674fc9a4c35f8918a61ded99ed0468162f4b9a963e00465d4a0bc5`  
		Last Modified: Tue, 21 Oct 2025 15:48:58 GMT  
		Size: 144.4 MB (144372855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374b00768159464e61a694016aa05f86e95a51dabf0e0e77cef1ec1240d88f55`  
		Last Modified: Tue, 21 Oct 2025 15:56:30 GMT  
		Size: 75.5 MB (75513098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b400201d3fd57653fd03bfc8cedd82eb21daf420faa4bc2e6c4cea5d7d9a9fa`  
		Last Modified: Tue, 21 Oct 2025 15:56:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674cdf4642a1148a03d190559bab6131f87f14e0773e552a50013b78dd4ecd81`  
		Last Modified: Tue, 21 Oct 2025 15:56:16 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ebcc010e791da4de7b21bac5b93a3f732168b3258b84214d6d0f2b6f058ddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48377cd8e0af254f8114259343d8b31b6ed48cf2780f51ade9349f4e40c18b62`

```dockerfile
```

-	Layers:
	-	`sha256:f0e86c7bd099cfb3aaf01c938e389da1a54d55b6171d78fa3231ce989ec2ca80`  
		Last Modified: Tue, 21 Oct 2025 18:37:14 GMT  
		Size: 5.1 MB (5118546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43f9f098ccee770d72aa2c08d732f9346fed7defe75bfb9b22ec3cca2b263c20`  
		Last Modified: Tue, 21 Oct 2025 18:37:15 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b89571b1cfc7487e77ce8fb0d0836b00d18118a3e7e5ab4579d4ef827cdd1a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230099972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb65957893273cc0a98fc24717d7c084750dde28fb247547043c92ef3962c3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:25:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 06:25:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 06:25:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:25:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 06:25:31 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:28:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 06:28:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 06:28:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 06:28:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 06:28:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68313fcc31f44a191d88f4190e266c8e4565e424c2b4ba1e5c7a0cd4cba3da3`  
		Last Modified: Tue, 04 Nov 2025 06:26:10 GMT  
		Size: 134.7 MB (134723626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f50024d7374b1414f4f0deb4dfa8a1029de2e524f9cd07966a8cb5b742ab95`  
		Last Modified: Tue, 04 Nov 2025 06:29:05 GMT  
		Size: 68.5 MB (68490750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc1451267c4d3978dc596e46a94c2a30551cdd4da9ef908992ff160a28d4aff`  
		Last Modified: Tue, 04 Nov 2025 06:28:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4061067046328cc4e8d87c68241c8f290f60b76336a56ae233514474b4f2cb7`  
		Last Modified: Tue, 04 Nov 2025 06:28:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3faa8c3f8daffd45f4deaaf368a4e827aaf3590c4c7b134fd4e237a12e4cb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5119744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d44d7714f6d11de065718f9b5cee5ef139e80e5e7c0b9de9485572036a01e7`

```dockerfile
```

-	Layers:
	-	`sha256:a0985e06d945326bbbab16014ecf1ee6413c2703016685cd688f128bde9ac56d`  
		Last Modified: Tue, 04 Nov 2025 10:41:22 GMT  
		Size: 5.1 MB (5104709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a1a3f22dd1c65e5b1cdb5071a52f81b8ca19095049a165434af32a0d8debd4`  
		Last Modified: Tue, 04 Nov 2025 10:41:23 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json
