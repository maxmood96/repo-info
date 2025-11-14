## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:ee0e0f3369a05ba7b57aa68499758986a7722f13780e6af6dcf9376f6746cf59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:edb2846b5a91ef32e5ea697fbd4e76df7439d9b46f6eb85b521689f04497fbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156506883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0444146dc56f5b0a579a9f1e1ddfb248dccdbf7d0f5ce7d91c5ed3d4991a16d5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:50:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:50:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:50:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:50:24 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:50:24 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:50:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:50:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:50:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b599f58c9d7b63ce0340b16da47f1d3681b7414891a6a4bb67f380a3468113`  
		Last Modified: Fri, 14 Nov 2025 00:51:15 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae6973f8cdf0388fe90c9588e0bceab59f5a2dc2e3c8ae46675651bcbd1d2d8`  
		Last Modified: Fri, 14 Nov 2025 00:51:18 GMT  
		Size: 72.0 MB (71994762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1180bfe909a6e767eb5642223b3bcdfe1bf554dbebf81c2e7b4121c204d2d758`  
		Last Modified: Fri, 14 Nov 2025 00:51:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:61b94f1f0e1615c649ace105cac98c418f855d8ea2ceb3bb4fee02a8ebe46dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c956a2214ad64500fe45d6737cfc7b8af279acfc8d5f1ed92b2867f2e8def68`

```dockerfile
```

-	Layers:
	-	`sha256:877180d6c90dc3ed78ac18a78f1ba7e30b0a6f87f4fcaf7d35d7e4e761142921`  
		Last Modified: Fri, 14 Nov 2025 01:51:46 GMT  
		Size: 5.4 MB (5377777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd146ed929ff327767f662ba95ffea665eb81d9aeca9458eb91535f9d8605a9`  
		Last Modified: Fri, 14 Nov 2025 01:51:46 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ab73ded19238e5b8e23b2069cbf6c3853376be6e0e2ec600788957c1dd583e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155766537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f12957a33d2f02f204b4bd47564340636f65ecc07e0975a9faa170825e6de18`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:51:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:51:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:51:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:51:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:18 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:52:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:52:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:52:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b85b9b1a0b8938b79f275e12b34be8f0558c34dd0bf62e130debbd7f81fba9a`  
		Last Modified: Fri, 14 Nov 2025 00:52:03 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a200c646e73a1844ac0d65b98056e49a3d875d6461fde292472efa5cb691066`  
		Last Modified: Fri, 14 Nov 2025 00:52:47 GMT  
		Size: 71.8 MB (71808597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed7715c6c81d944e5e8602f25e8c8d4ea2fcb8719a6e4403325ce15216f023b`  
		Last Modified: Fri, 14 Nov 2025 00:52:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6129f75b591fba182c25e021bf2b1d32f98eff2b8efc2d6c22e0196b666798bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd49900c1c3e2318fa7e465c7de24d7e85c9883b08c402a7c69a6af8647520cf`

```dockerfile
```

-	Layers:
	-	`sha256:13896a6c3b661d4e4aacac40264e335773e9aba93dd16b0643a3f3a937722a03`  
		Last Modified: Fri, 14 Nov 2025 01:51:51 GMT  
		Size: 5.4 MB (5384244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a46ccdab1625f7fd2e35dd0b4c73d88584f629ffa437cab272db737cb16c55`  
		Last Modified: Fri, 14 Nov 2025 01:51:52 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c7970f791055c4fa87b43b761bce8ae0afb8d53e110fabce0b41f164a786d4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163171474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efe3857a21a00c1dde09e0ca573eb81e911f6638bfac4bd39874256be36ce6c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:13:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:13:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:13:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:13:08 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:13:08 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:23:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:23:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:23:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0facc06cc8e166d71727a4983c45c13f2011e076102fa7c0cdfb760611832d`  
		Last Modified: Sat, 08 Nov 2025 19:15:06 GMT  
		Size: 52.2 MB (52175085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76ccd3f21b4e6a8e67cf763980967bfdf356a4771ad8c1b7cde391f465cda25`  
		Last Modified: Sat, 08 Nov 2025 19:23:53 GMT  
		Size: 77.4 MB (77397095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b14000c41b80ca275ce544b1b46588bf90aa393a1ceca3dff26673a8acdab26`  
		Last Modified: Sat, 08 Nov 2025 19:23:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f0b3507f5ccb713420d9fc4a4247d5873a69ec86d116c0449a885ff44e1cca75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bbfff60e59b4b3969961c42accbda894a6262ad0d4b30e537b10ad784d0bcc`

```dockerfile
```

-	Layers:
	-	`sha256:506c6899243756115b6de94c03114073006a40f976915f7a6144979b7a5b628a`  
		Last Modified: Sat, 08 Nov 2025 22:55:44 GMT  
		Size: 5.4 MB (5382741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c9b244f1df6259b697c628ee41b49fdfdd5f61c86687bb4f220d7ab4c10a13`  
		Last Modified: Sat, 08 Nov 2025 22:55:45 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
