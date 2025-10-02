## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:c5210ac9432726e53c6c1d3a4a6605c7f8f3d10def68a0212a574f5fbbffce0b
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c372b8984f9d84362227c3bba658121931720603916e868b6e64df634d08f099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280484150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e70e2077193c94115a8408927a3afbd2a5d2760f9f1700005786e60e00c122b`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4e0be23e579f67249688ecfe2e8c2e5cd8418cb7567471aade1f5319f9dbec`  
		Last Modified: Thu, 02 Oct 2025 02:28:11 GMT  
		Size: 145.7 MB (145658246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb6c0b87415040f770ca91541f3e9859ab90e5f53a518a3697169fdfb612239`  
		Last Modified: Tue, 30 Sep 2025 00:53:31 GMT  
		Size: 85.5 MB (85540634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ba1815ad00e73bcfb1290c55771432e5eb80b72675f259ea8041921c273bb5`  
		Last Modified: Tue, 30 Sep 2025 00:53:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:642c1f2bf2462769b2237209d02d7d9dcf8797abc0293ab3d4d6ef8def0b41fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709e889ca667213f44decd5a4c296cefb1ff847871825b9a3749bbbad8ad1098`

```dockerfile
```

-	Layers:
	-	`sha256:bc546778f03f4cb3eff57d6fc75bc774eb805a8a52996283214dd71f22aabf51`  
		Last Modified: Wed, 01 Oct 2025 15:36:48 GMT  
		Size: 7.5 MB (7486986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd2bb17d8da21aa6277ee7d8b3aec6f156c2ce7678568015f268aae58a6068e7`  
		Last Modified: Wed, 01 Oct 2025 15:36:49 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e6fb7f15c99ad602506a6d41090f0573f89c158c577300d16e4084942985f0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277471604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83388002cda4343469d40e1fbfd8539509a39d4acd5e4dab2878fb782e107ef8`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53234e573f4c060a914ed580e8d28372a66f19b46cd5aa088fe65ed12492475f`  
		Last Modified: Tue, 30 Sep 2025 00:52:07 GMT  
		Size: 142.5 MB (142458757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c30f680de8893b3ee981118c0c7b33d382b1075959e159765745bbfefa6291`  
		Last Modified: Tue, 30 Sep 2025 00:52:49 GMT  
		Size: 85.4 MB (85363509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09b83951010b0e1416d7d69bfaa114a93fb3e84a35b444e9e90b9c67eee8823`  
		Last Modified: Tue, 30 Sep 2025 00:52:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:12ddf93f64a8f5cc6e529e26c32192676aab5b2f4e6817d800faf7cd042b6ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32178a667d14640f2fe9f75850b55e86fb4d464655189a23afe8d209e54abe96`

```dockerfile
```

-	Layers:
	-	`sha256:c4378d72da83c06aad640f7701bf694962f39073cd737f95141bde8acddf2f9b`  
		Last Modified: Wed, 01 Oct 2025 21:37:54 GMT  
		Size: 7.5 MB (7494634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b15a6eef8aede73c217ab8be91875960c1065fa6c0dd0f42e74771c62313dc`  
		Last Modified: Wed, 01 Oct 2025 21:37:55 GMT  
		Size: 14.3 KB (14345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7f3c24350ae3be636c996295cd5fcacc30b2910bb4b44a303c0c760d9e7b43f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276910849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6678595b176e5371c8a9687e6e805cef395b70eb5bd2f87c5c99f89dfc64e492`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7cc59d27b9842992dd2c96a03ca98e1b99b3821103e576265114b0db84a9f2`  
		Last Modified: Tue, 30 Sep 2025 13:40:32 GMT  
		Size: 132.9 MB (132852830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61da3fae24066199672a472c5bb473b82e84b28745dc9bfe3bcd8225615c7173`  
		Last Modified: Tue, 30 Sep 2025 13:45:22 GMT  
		Size: 90.9 MB (90948158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9247624a191eacdc55384e4b809a12ac5230163a681ba44fc1698262d82424f`  
		Last Modified: Tue, 30 Sep 2025 14:37:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7add706f31caf9bae804bc94c732d356cf0aee13124ed3c1fdb9b5675381baf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96216fc4d9a0b61108c2df4282ff999ae34b58a6d9572a0aed94ff51a3fea3f`

```dockerfile
```

-	Layers:
	-	`sha256:e4a5a42f77d760c570a7fddbea84337b8dd751a61f030da82ce2e939258ed924`  
		Last Modified: Wed, 01 Oct 2025 21:38:01 GMT  
		Size: 7.5 MB (7490790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84fe536573763fc2ad12f2bae323cebb36011bd408a58a793a0a3cb3d8030e9c`  
		Last Modified: Wed, 01 Oct 2025 21:38:02 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:7ffb61a9be354287ff358405684c625ef518037994ceaa8ebc0d5f628076e726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261480358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5a11055f6e5070974594c0b175d2b849b4e794a056e8a4aeb9ad16d60c0044`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9c408a5d908cfca96c82731492c6174b6a579f754dd7b87c31dcd9101a9658`  
		Last Modified: Tue, 30 Sep 2025 13:14:38 GMT  
		Size: 125.6 MB (125622227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e14bca93808130b2ee8eff4dcd9808db04d9ccf98f9f49baeff1abbda2f181`  
		Last Modified: Tue, 30 Sep 2025 13:19:13 GMT  
		Size: 86.5 MB (86506046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68aeae78dd266f21bf389dacd8cc06fe84e993131fa3ac8ac4d446cbfc000aca`  
		Last Modified: Tue, 30 Sep 2025 13:19:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:947dc462529bcbba2af043084eca51eb426b74885e8a6dbec8eb3968946a4622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebab41528ae4fc5e1736c49508a0d7cc123b573a61abb9454a1b95a804599a7`

```dockerfile
```

-	Layers:
	-	`sha256:74365a4a4b40e5c38d2b4b61807711c724abdc2f96198584f70140352839fa8e`  
		Last Modified: Wed, 01 Oct 2025 21:38:08 GMT  
		Size: 7.5 MB (7482912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a754fd146f77f3a8704537027bb3f7c18f99fe6a79f390c7636e3b697d0b7b`  
		Last Modified: Wed, 01 Oct 2025 21:38:09 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
