## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:80914050edb3779285233881bd5679b4d37ada93a62d00900ab98a18404cf39f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7064103f122ebb616699a85f29df45519a133a5f67f4368bf42675b285776dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184361115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c805716ec473f5bf6ec0a1235e37d3cb0c9ea4d38070d6e2dc45e932d8e9380`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:05:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:05:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:05:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:05:39 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:05:39 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:05:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:05:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:05:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc9ef5662e891717a29abf5b8042546158f651e5e41d92d5f29767bd993e830`  
		Last Modified: Tue, 18 Nov 2025 06:06:26 GMT  
		Size: 54.7 MB (54733389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb343c94c40cf83d9377914baba39cfae641e6ade378eddcc1716a8a7b135d2`  
		Last Modified: Tue, 18 Nov 2025 06:06:45 GMT  
		Size: 81.1 MB (81146320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d06efc91f4361a7f3a489466d7cfbe01eba6d469cbef3f71e859ee23ec84500`  
		Last Modified: Tue, 18 Nov 2025 06:06:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5c0b6838ad7c39c6576cf14792c445542326d0e8c3f1fdbdb555c41cfb4ab513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba02cb4b5486d72293b59f738e23582fe477270c66f60faa4179cc4cc403f5f`

```dockerfile
```

-	Layers:
	-	`sha256:a05fb770d46378c3b0da6d4d878e15509a3dc91184d0ca95d1daabc2dbd4d654`  
		Last Modified: Tue, 18 Nov 2025 07:49:18 GMT  
		Size: 7.5 MB (7496500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e313d5e7e9ce672b1688a3417278a60004dfcf799a1d3da60a01b01cf47f5a13`  
		Last Modified: Tue, 18 Nov 2025 07:49:19 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d7d3a33a693cffccb53287b85ce0a0af1c75a98342a9b59d451f0834ecedc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183206035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0499450c1614598bb212f957166f05969a7b6e63f6ff959053dd195c2377f41a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:52:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:52:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:52:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:52:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:52:38 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:52:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:52:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:52:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e39f1b7d6e00ded15e3e4713226cd523482a0a218c100ea243bbefb96f7b9a`  
		Last Modified: Tue, 18 Nov 2025 04:53:28 GMT  
		Size: 53.8 MB (53815013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d0d73c53b94e76a1225538784ef53c121c8e13c240416602e8f23ca87392fa`  
		Last Modified: Tue, 18 Nov 2025 04:53:28 GMT  
		Size: 81.0 MB (81031239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c288d5699ae89ccbe55862c6b1887b0c248d216c572729ee9256b513277827`  
		Last Modified: Tue, 18 Nov 2025 04:53:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1877d2ebaced9a35843b1e5e8717ce81d8c9480432f49820246e49e342120e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9075d4d40cc45e2821fb676778dd2e1a1823d246e054ca37e66b6dc66c60c25`

```dockerfile
```

-	Layers:
	-	`sha256:64ed46b317b2323fa22b54ee4a84515b66b334ced55abd747633d6ee8d2c3f71`  
		Last Modified: Tue, 18 Nov 2025 07:49:25 GMT  
		Size: 7.5 MB (7502961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183328b3e8d477fdb7d444ce3395244087b6acf40ff47f8c3178f912da541f31`  
		Last Modified: Tue, 18 Nov 2025 07:49:26 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:e760d17996ab222aa5e10713913b86801e91229511fd00c12f65ad94dab5f769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191488788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c10608c0f6d501b10e5ae2a7f36d6dd344db454e063aea6b833de201a2aaef6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:37:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:37:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:37:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:37:07 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 22:37:08 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:39:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 22:39:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 22:39:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a51c77f8794a7a48d981ba475763915c444e47af96f90a51cb42c060ef190d`  
		Last Modified: Mon, 08 Dec 2025 22:38:19 GMT  
		Size: 52.2 MB (52175143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83649973de83f9b021d509874d98d033fdc171884f41e1c06efe6d6739e736`  
		Last Modified: Mon, 08 Dec 2025 22:39:53 GMT  
		Size: 87.0 MB (86986024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac1d3794d4bc0de1ea1c3e6b3ed7fa48539c6db503563d326d34289a36dad86`  
		Last Modified: Mon, 08 Dec 2025 22:39:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bc510da5afd7ec5a50b651c2e23672e242ab781e16ff5794d8c67c7de679e847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872d8eacc7b17aa3ce26b673b7c19873e526aa1cf577e8e0fc25c253fdb1d91a`

```dockerfile
```

-	Layers:
	-	`sha256:71b9ee0b69cf729863b02881b3473a020a98d91ccc43bb88221448bb6d47ee05`  
		Last Modified: Tue, 09 Dec 2025 01:40:36 GMT  
		Size: 7.5 MB (7502307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdff75e5ccd8f6a414501b4d5f506874c5dc95e1fb68f4c7a4be70e7138b1424`  
		Last Modified: Tue, 09 Dec 2025 01:40:37 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
