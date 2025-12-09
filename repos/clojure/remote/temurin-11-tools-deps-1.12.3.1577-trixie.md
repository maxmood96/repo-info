## `clojure:temurin-11-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:00cc54f3bca2b3266c3ce3a4ac9f7d40e3d1710828693da9b362946e476f97f2
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:382a0795326956630d6634a961b8b5132f373c9bc0e44fa74d709510c4bfa6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279798557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30004fb616035c4fee71838a517e6d75cf506c7f1da7b744611cc081f09400a9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:08:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:08:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:08:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:08:06 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:08:06 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:08:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:08:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:08:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86203fff44548b43a0801de1dc2018dffdd64d66e6a77a7284c7524e6313a93`  
		Last Modified: Thu, 20 Nov 2025 03:28:14 GMT  
		Size: 145.0 MB (144966605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5243e184b07da489fef38412ed31b74cc871b8a641f1ff88352fbba394e6a3a4`  
		Last Modified: Tue, 18 Nov 2025 06:09:06 GMT  
		Size: 85.5 MB (85541761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf202dabd2ff4dde3eedfc5b9a8b9ca7177d9daf26ddd3ec39f4f8893ad1226a`  
		Last Modified: Tue, 18 Nov 2025 06:08:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f30aa211918702cbbf640c268ad7b4471543c4c18f4156374456a9a2c98c667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a491028ff4a7e7c70075ef390560ddf02e16ad86a79fa7b6a9ba90dd7638df`

```dockerfile
```

-	Layers:
	-	`sha256:bd9b093a0cd651f8a35353800e809405781d03e8a61066eaf9850744310b1856`  
		Last Modified: Tue, 18 Nov 2025 07:39:37 GMT  
		Size: 7.5 MB (7487070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f591143f31e44254c3a2005d3e6211333ca3d18ff512a8fb87bd90efce87c40`  
		Last Modified: Tue, 18 Nov 2025 07:39:38 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:83ac0659f730703a7ec0ec7d531aec56f3facf175472b87f7c28f7101bdfb74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276746449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7154249e1b4b6723a8a6087fa1a777e800723b054ae0e7101b4a7404271cb3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:59:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:59:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:59:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:59:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:59:38 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:59:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:59:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:59:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bd085d59990d890df3d1a28551287c89790e640aaf3a9242ee69639728d7dc`  
		Last Modified: Thu, 20 Nov 2025 21:16:36 GMT  
		Size: 141.7 MB (141731561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ba583ebe68eef279a33698b901b4530a535d602899297f950eed8da294c0cd`  
		Last Modified: Tue, 18 Nov 2025 05:00:52 GMT  
		Size: 85.4 MB (85364012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6620a6f1cd84d04b5f57995dbd577c969baf26939be66ed74bf156f8919e66`  
		Last Modified: Tue, 18 Nov 2025 05:00:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b4e363a58a429e8269f55d9e8b8978d0629345bfc851a1a26ed8f689106b650b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff3e120cd0c3634f730a9e295263dc401c00d6c1515eb98cda5409ef982f785`

```dockerfile
```

-	Layers:
	-	`sha256:15afda2c98004f7f559e9c74333d6017bc49eb1bf09adc1969e5282453cb4f7b`  
		Last Modified: Tue, 18 Nov 2025 07:39:45 GMT  
		Size: 7.5 MB (7494718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd607105710f24482625d0e7fec2ad315ff35073b966b7547b4958611cc9513`  
		Last Modified: Tue, 18 Nov 2025 07:39:45 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:4e8fea3d07d3a25b894d79cb4d86e703807d882bae48ccac4e424f0c54fa3cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276138403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bac21e3cae22f0936a8a5686321f300eee3c5b404746e8d9059fd0beb0b007`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:25:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:25:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:25:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:25:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:25:26 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:26:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:26:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:26:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37d1cc451357decc266df875d9334bbd4504581a335e8cd24c32ce8844bcd57`  
		Last Modified: Mon, 08 Dec 2025 23:26:56 GMT  
		Size: 132.1 MB (132081948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604dcd346da19afb81c32af5f3b9feda81de29c4f03371dc8ef71d9531ade219`  
		Last Modified: Mon, 08 Dec 2025 23:27:19 GMT  
		Size: 90.9 MB (90947332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058fea3ccdb73aaf3a9550fbe04f41703f8156fbdf1dcb8965ab9572129801ef`  
		Last Modified: Mon, 08 Dec 2025 23:27:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:25c954d1212362623235bd7f746568410731d9e08730712893483d3090cf476c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fd1ad5565ca9acc1babd57e0d376c94710306030282db8f103eccfccc5a477`

```dockerfile
```

-	Layers:
	-	`sha256:fc94fb298c13af2b02908ff6f70354efd9d5122b0abc6603ddd70ff4ea70417f`  
		Last Modified: Tue, 09 Dec 2025 01:36:07 GMT  
		Size: 7.5 MB (7490874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ecb5f686385a1f59f6cce1d8448c4b690fad8242aeab3065d799fc63e6e02f1`  
		Last Modified: Tue, 09 Dec 2025 01:36:08 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:0392d8af5afc9415b845f530019cdb46a3d52e1144d0be96231a97a5be614a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261552268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b1870f3922b2c2c105807a9ce6bdf81e38c2dfb6a7c18934920a8fc452cae9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:24:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:24:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:24:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:24:23 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:24:23 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:24:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:24:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:24:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54b6906427e688e4a5fd35349c75fc025a2356109f24048c2267857962f7a2c`  
		Last Modified: Tue, 18 Nov 2025 05:25:25 GMT  
		Size: 125.7 MB (125694398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2870de150c8dda78622fae40653f06e449dd56b28a1cd54ded04f18b3bad084`  
		Last Modified: Tue, 18 Nov 2025 05:25:23 GMT  
		Size: 86.5 MB (86511212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151eb2f40aa8d298d725be507ade6375f028256b4dd39311d1e479ea95e1401a`  
		Last Modified: Tue, 18 Nov 2025 05:25:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b74fccd6a2ee22b9c8b9ff68d18893053b4c80b53fac8d145b43f8da2796cb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dfb3b838a7ff49744fc37c03bbfad28532244a3cba838daa1b5ed666c62f688`

```dockerfile
```

-	Layers:
	-	`sha256:3ef01b1d79b73ce7bef62944e783f3a00ce7548b7a61908c730b9bd8abf17160`  
		Last Modified: Tue, 18 Nov 2025 07:39:58 GMT  
		Size: 7.5 MB (7482996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42942e2bee454f3d7752af9dea667f2d517ee42a06a2945d73751c3335a82a5b`  
		Last Modified: Tue, 18 Nov 2025 07:39:59 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json
